
```javascript
/**
 * path是node的默认库我们在启动项目的时候使用的是node的环境所以path库就可以直接使用了，而不需要在安装了，
 * 这就是为什么package.json中没有path的原因
 */
import path from 'path'

/** 带有typescript编译器错误的的rollup插件,它可以打印出typescript语法和语义诊断消息*/
import ts from 'rollup-plugin-typescript2'

/** 替换文件中的目标字符串 */
import replace from '@rollup/plugin-replace'

/**
 * 允许 Rollup 从 JSON 文件中导入数据
 * 例如：import {version} from '../package.json';
 */
import json from '@rollup/plugin-json'

// 环境变量中目标模块为设置异常处理，由于命令行中输入的模块名跟 packages 目录项模块不匹配导致
if (!process.env.TARGET) {
  throw new Error('TARGET package must be specified via --environment flag.')
}

// 根目录下 package.json 中定义的版本号
const masterVersion = require('./package.json').version
// 根目录下 packages 路径
const packagesDir = path.resolve(__dirname, 'packages')
// 命令行中输入的模块名称在 packages 目录中所匹配的模块路径
const packageDir = path.resolve(packagesDir, process.env.TARGET)
// packages 目录下某模块名称
const name = path.basename(packageDir)
const resolve = p => path.resolve(packageDir, p)
// 引入当前模块下的 package.json 文件
const pkg = require(resolve(`package.json`))
// 引入当前模块下的 package.json 文件 中设定的 buildOptions 属性
const packageOptions = pkg.buildOptions || {}

// ensure TS checks only once for each build
// 全局记录TS检测状态，完成一次检测后记录状态，防止多次检测，出现错误。
let hasTSChecked = false

/**
 * 一、全局打包: vue(.runtime).global(.prod).js：【使用 CDN 或没有构建工具】
 *
 * 1、全局打包不是 UMD 构建的，它们被打包成 IIFEs，并且仅用于通过 <script src="..."> 直接使用。
 *    format: `iife`
 *    https://developer.mozilla.org/en-US/docs/Glossary/IIFE
 *    iife 的全称是 Immediately Invoked Function Expression ，即"立即调用的函数表达式"，
 *    可以很容易的用 JS 来表达：(function () {}())
 *    用于通过 <script src="..."> 直接使用。
 * 2、若要通过浏览器中的 <script src="..."> 直接使用，则暴露 Vue 全局。
 * 3、vue.global.js 是包含编译器和运行时的“完整”构建版本，因此它支持动态编译模板。
 * 4、vue.runtime.global.js 只包含运行时，并且需要在构建步骤期间预编译模板。
 *
 * 二、vue(.runtime).esm-browser(.prod).js：【使用 CDN 或没有构建工具】
 *
 * 1、用于通过原生 ES 模块导入使用 (在浏览器中通过 <script type="module"> 来使用)。
 * 2、与全局构建版本共享相同的运行时编译、依赖内联和硬编码的 prod/dev 行为。
 *
 * 三、vue(.runtime).esm-bundler.js：【使用构建工具】
 *
 * 1、vue.runtime.esm-bundler.js (默认) 仅运行时，并要求所有模板都要预先编译。
 *    这是构建工具的默认入口 (通过 package.json 中的 module 字段)，
 *    因为在使用构建工具时，模板通常是预先编译的 (例如：在 *.vue 文件中)。
 * 2、vue.esm-bundler.js 包含运行时编译器。
 *    如果你使用了一个构建工具，但仍然想要运行时的模板编译 (例如，DOM 内 模板或通过内联 JavaScript 字符串的模板)，
 *    请使用这个文件。你需要配置你的构建工具，将 vue 设置为这个文件
 *
 * 四、vue.cjs(.prod).js：【服务端渲染】
 *
 * 1、通过 require() 在 Node.js 服务器端渲染使用。
 * 2、如果你将应用程序与带有 target: 'node' 的 webpack 打包在一起，并正确地将 vue 外部化，则将加载此文件。
 * 3、dev/prod 文件是预构建的，但是会根据 process.env.NODE_ENV 自动加载相应的文件。
 */
const outputConfigs = {
  'esm-bundler': {
    file: resolve(`dist/${name}.esm-bundler.js`),
    format: `es`
  },
  'esm-browser': {
    file: resolve(`dist/${name}.esm-browser.js`),
    format: `es`
  },
  cjs: {
    file: resolve(`dist/${name}.cjs.js`),
    format: `cjs`
  },
  global: {
    file: resolve(`dist/${name}.global.js`),
    format: `iife`
  },

  // runtime-only builds, for main "vue" package only
  'esm-bundler-runtime': {
    file: resolve(`dist/${name}.runtime.esm-bundler.js`),
    format: `es`
  },
  'esm-browser-runtime': {
    file: resolve(`dist/${name}.runtime.esm-browser.js`),
    format: 'es'
  },
  'global-runtime': {
    file: resolve(`dist/${name}.runtime.global.js`),
    format: 'iife'
  }
}

// 模块默认打包方式
const defaultFormats = ['esm-bundler', 'cjs']
/**
 * 命令行中输入的 -f | --formats 信息会在 scripts/dev.js 中赋值给环境变量 env.FORMATS。
 * 如 'esm-bundler,cjs' 多个值时中间可用逗号分隔.
 * process.env.FORMATS 默认值：'global'
 */

const inlineFormats = process.env.FORMATS && process.env.FORMATS.split(',')

/**
 * 模块打包类型优先级：
 * 第1优先级: inlineFormats 即命令行输入的 格式类型
 * 第2优先级: packageOptions.formats 即命/packages目录下子模块 package.json 中 buildOptions 属性定义的formats
 * 第2优先级: defaultFormats 即默认打包方式 ['esm-bundler', 'cjs']
 */
const packageFormats = inlineFormats || packageOptions.formats || defaultFormats

/**
 * 正式环境打包时(非dev开发环境)，需要添加 --prodOnly | -p 参数，
 * -- 在 scripts/build.js 中，会检查命令行参数设置，参数正确时会设置 env.PROD_ONLY 环境变量。
 * 1、正式环境 打包配置信息为 [];
 * 2、其他非正式环境 通过函数 createConfig 创建配置信息；
 */
const packageConfigs = process.env.PROD_ONLY
  ? []
  : packageFormats.map(format => createConfig(format, outputConfigs[format]))

if (process.env.NODE_ENV === 'production') {
  packageFormats.forEach(format => {
    if (packageOptions.prod === false) {
      return
    }
    if (format === 'cjs') {
      packageConfigs.push(createProductionConfig(format))
    }
    if (/^(global|esm-browser)(-runtime)?/.test(format)) {
      packageConfigs.push(createMinifiedConfig(format))
    }
  })
}

export default packageConfigs

/**
 * 生成非正式环境模块打包配置信息
 * @param {*} format 当前模块 formats 中的一个，如: /packages/vue/package.json buildOptions 属性中 formats 列表元素
 * @param {*} output 定义输出配置信息 类型：{ file: string, format: string } 具体可参考变量: outputConfigs 元素属性值
 * @param {*} plugins
 * @returns
 */
function createConfig(format, output, plugins = []) {
  // 没有定义package输出相关配置信息：打印警告信息 & 线程退出
  if (!output) {
    console.log(require('chalk').yellow(`invalid format: "${format}"`))
    process.exit(1)
  }

  // 根据全局环境变量SOURCE_MAP信息，给 output 变量设置 sourcemap 属性。
  // 受控于命令行参数 --formats | -f 的影响
  output.sourcemap = !!process.env.SOURCE_MAP
  /**
   * 给 output 变量设置 externalLiveBindings 属性，默认值（true）
   * 当设置为false时，Rollup不会生成代码来支持外部导入的模块(假设导出的模块不会随时间而改变的前提下)。
   * 这将允许Rollup生成更优化的代码。请注意，当存在涉及外部依赖项的循环依赖项时，这可能会导致问题。
   * 这将避免大多数情况下Rollup在代码中生成getter，因此在许多情况下可用于使代码IE8兼容。
   */
  output.externalLiveBindings = false

  /**
   * 判断是否是正式环境打包：根据环境变量__DEV__ || 打包文件的输出路径名称是否以 '.prod.js' 结尾
   * __DEV__ 什么时候被赋值的 (大概率跟 process.env.NODE_ENV 相关)
   */
  const isProductionBuild =
    process.env.__DEV__ === 'false' || /\.prod\.js$/.test(output.file)

  /* esm-bundler esm-browser cjs global 类型 详见 38~71 行注释 */
  const isBundlerESMBuild = /esm-bundler/.test(format)
  const isBrowserESMBuild = /esm-browser/.test(format)
  const isNodeBuild = format === 'cjs'
  const isGlobalBuild = /global/.test(format)

  /**
   * 全局打包时，读取模块下 package.json 文件 中设定的 buildOptions 属性中的name属性赋值给output.name
   */
  if (isGlobalBuild) {
    output.name = packageOptions.name
  }

  // 判断是否生成 .d.ts 和 .d.ts.map 文件
  const shouldEmitDeclarations = process.env.TYPES != null && !hasTSChecked

  /** 配置TS 插件 */
  const tsPlugin = ts({
    // check: 设置为false可避免对代码进行任何诊断检查。
    check: process.env.NODE_ENV === 'production' && !hasTSChecked,
    /**
     * tsconfig的路径.json。如果您的tsconfig在项目目录中有其他名称或相对位置，请设置此选项。
     * 默认情况下，将尝试加载/tsconfig.json，但如果文件丢失，则不会失败，除非明确设置该值。
     */
    tsconfig: path.resolve(__dirname, 'tsconfig.json'),
    /* 缓存的路径。默认为node_modules目录下的一个的文件夹 */
    cacheRoot: path.resolve(__dirname, 'node_modules/.rts2_cache'),
    /**
     * 覆盖原有的 tsconfigDefaults 配置信息 = merge tsconfig.json to tsconfigDefaults;
     */
    tsconfigOverride: {
      compilerOptions: {
        sourceMap: output.sourcemap,
        /**
         * 为项目中TypeScript和JavaScript生成.d.ts文件
         */
        declaration: shouldEmitDeclarations,
        /**
         * 开启 --declarationMap ，编译器会同时生成 .d.ts 和 .d.ts.map 文件。
         * 语言服务现在能够正确识别这些映射文件，并且使用它们来映射到源码。
         * 也就是说，在使用“跳到定义之处”功能时，会直接跳转到源码文件，而不是 .d.ts 文件。
         */
        declarationMap: shouldEmitDeclarations
      },
      // 指定解析 include 属性配置信息时，应该跳过的文件名称
      exclude: ['**/__tests__', 'test-dts']
    }
  })
  // we only need to check TS and generate declarations once for each build.
  // it also seems to run into weird issues when checking multiple times
  // during a single build.

  // 防止出现问题，每次构建只做一次 TS 检测
  hasTSChecked = true

  // 定义模块入口文件
  const entryFile = /runtime$/.test(format) ? `src/runtime.ts` : `src/index.ts`

  // 指出应将哪些模块视为外部模块，不会与你的库打包在一起。
  const external =
    isGlobalBuild || isBrowserESMBuild
      ? packageOptions.enableNonBrowserBranches
        ? // externalize postcss for @vue/compiler-sfc
          // because @rollup/plugin-commonjs cannot bundle it properly
          ['postcss']
        : // normal browser builds - non-browser only imports are tree-shaken,
          // they are only listed here to suppress warnings.
          ['source-map', '@babel/parser', 'estree-walker']
      : // Node / esm-bundler builds. Externalize everything.
        [
          ...Object.keys(pkg.dependencies || {}),
          ...Object.keys(pkg.peerDependencies || {}),
          ...['path', 'url'] // for @vue/compiler-sfc
        ]

  // the browser builds of @vue/compiler-sfc requires postcss to be available
  // as a global (e.g. http://wzrd.in/standalone/postcss)

  /**rollup通过`external` + `output.globals`来标记外部依赖 */
  output.globals = {
    postcss: 'postcss'
  }

  /**
   * node 插件
   * 1. @rollup/plugin-node-resolve插件：使用节点解析算法在 node_modules 中查找第三方模块
   * 2. @rollup/plugin-commonjs插件：将CommonJS模块转换为ES6，以便它们可以包含在Rollup bundle中
   * 3. rollup-plugin-node-builtins插件: 允许 node 内置模块 to be required/imported.
   * 4. rollup-plugin-node-globals插件: 用于嵌入 node 全局信息，包括用于browserify的代码，即使它使用进程或缓冲区，也应该可以工作
   */
  const nodePlugins =
    packageOptions.enableNonBrowserBranches && format !== 'cjs'
      ? [
          require('@rollup/plugin-node-resolve').nodeResolve({
            // 如果'true'，插件将更优先使用内置模块（例如'fs'，'path`）。如果'false'，插件将查找本地安装的同名模块。
            preferBuiltins: true
          }),
          require('@rollup/plugin-commonjs')({
            sourceMap: false
          }),
          require('rollup-plugin-node-builtins')(),
          require('rollup-plugin-node-globals')()
        ]
      : []

  return {
    // 入口文件
    input: resolve(entryFile),
    // Global and Browser ESM builds inlines everything so that they can be
    // used alone.
    // 外部依赖的名称
    external,
    plugins: [
      // 包含 JSON 插件
      json({
        // 为JSON对象的每个属性生成命名导出。默认为true
        namedExports: false
      }),
      tsPlugin,
      // 配置替换插件中需要替换的变量，打包过程中替换文件中的字符串。
      createReplacePlugin(
        isProductionBuild,
        isBundlerESMBuild,
        isBrowserESMBuild,
        // isBrowserBuild?
        (isGlobalBuild || isBrowserESMBuild || isBundlerESMBuild) &&
          !packageOptions.enableNonBrowserBranches,
        isGlobalBuild,
        isNodeBuild
      ),
      ...nodePlugins,
      ...plugins
    ],
    output,
    // 拦截警告消息.如果未配置，警告信息将被去重并打印到控制台。
    onwarn: (msg, warn) => {
      if (!/Circular/.test(msg)) {
        warn(msg)
      }
    },
    treeshake: {
      // code from imported modules will only be retained if at least one exported value is used
      // 如果引入的模块代码想要保留，至少需要有一个该模块元素被使用过。
      moduleSideEffects: false
    }
  }
}

/**
 * 配置 Replace 插件
 */
function createReplacePlugin(
  isProduction,
  isBundlerESMBuild,
  isBrowserESMBuild,
  isBrowserBuild,
  isGlobalBuild,
  isNodeBuild
) {
  // 打包文件时替换文件中的字符串。
  const replacements = {
    __COMMIT__: `"${process.env.COMMIT}"`,
    __VERSION__: `"${masterVersion}"`,
    __DEV__: isBundlerESMBuild
      ? // preserve to be handled by bundlers
        `(process.env.NODE_ENV !== 'production')`
      : // hard coded dev/prod builds
        !isProduction,
    // this is only used during Vue's internal tests
    __TEST__: false,
    // If the build is expected to run directly in the browser (global / esm builds)
    __BROWSER__: isBrowserBuild,
    __GLOBAL__: isGlobalBuild,
    __ESM_BUNDLER__: isBundlerESMBuild,
    __ESM_BROWSER__: isBrowserESMBuild,
    // is targeting Node (SSR)?
    __NODE_JS__: isNodeBuild,

    // feature flags
    __FEATURE_SUSPENSE__: true,
    __FEATURE_OPTIONS_API__: isBundlerESMBuild ? `__VUE_OPTIONS_API__` : true,
    __FEATURE_PROD_DEVTOOLS__: isBundlerESMBuild
      ? `__VUE_PROD_DEVTOOLS__`
      : false,
    ...(isProduction && isBrowserBuild
      ? {
          'context.onError(': `/*#__PURE__*/ context.onError(`,
          'emitError(': `/*#__PURE__*/ emitError(`,
          'createCompilerError(': `/*#__PURE__*/ createCompilerError(`,
          'createDOMCompilerError(': `/*#__PURE__*/ createDOMCompilerError(`
        }
      : {})
  }
  // allow inline overrides like
  //__RUNTIME_COMPILE__=true yarn build runtime-core
  Object.keys(replacements).forEach(key => {
    if (key in process.env) {
      replacements[key] = process.env[key]
    }
  })
  return replace(replacements)
}

/**
 * Prod 正式环境：format === 'cjs' 生成服务端渲染包时 额外配置信息
 * @param {*} format
 * @returns
 */
function createProductionConfig(format) {
  return createConfig(format, {
    file: resolve(`dist/${name}.${format}.prod.js`),
    format: outputConfigs[format].format
  })
}

/**
 * Prod 正式环境: global-runtime|esm-browser-runtime 的额外配置
 * @param {*} format
 * @returns
 */
function createMinifiedConfig(format) {
  // minify generated es bundle 压缩 ES code
  const { terser } = require('rollup-plugin-terser')
  return createConfig(
    format,
    {
      file: outputConfigs[format].file.replace(/\.js$/, '.prod.js'),
      format: outputConfigs[format].format
    },
    [
      terser({
        module: /^esm/.test(format), // true is set when format is esm or es
        compress: {
          // 5 | 2015 | 2016 | 2017 | 2018 | 2019 | 2020;
          ecma: 2015,
          pure_getters: true
        }
      })
    ]
  )
}
```