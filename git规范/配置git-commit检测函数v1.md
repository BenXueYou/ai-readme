配置git commit 命令拦截hook, 校验 commit-msg 格式规范

前面默认git >= 2.27.0, node >=14

### 1、安装huskey@8.0.1

```bash
npm install --save-dev husky@8.0.1
```

### 2、初始化配置文件

- 在package.json scripts 属性中添加命令并保存：

```json
"scripts": {
	"prepare": "npx husky install"
} 
```

- 在控制台输入：npm run prepare 初始化 husky, 在工程根目录创建.husky目录

![image-20240807173244417](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20240807173244417.png)

- 初始化commit-msg函数配置文件

  ```bash
  npx husky add .husky/commit-msg 'npx --no-install commitlint --edit "$1"'
  ```

  在./husky/commit-msg文件中生成

  ```bash
  #!/usr/bin/env sh
  . "$(dirname -- "$0")/_/husky.sh"
  npx --no-install commitlint --edit $1
  ```

  

- 初始化pre-commit函数配置文件

  ```bash
  npx husky add .husky/pre-commit "npx lint-staged"
  ```

  在./husky/pre-commit文件中生成

  ```bash
  #!/usr/bin/env sh
  . "$(dirname -- "$0")/_/husky.sh"
  npx lint-staged
  ```

以上： 钩子函数已经配置完毕， 执行 git commit 命令之后，会被拦截开始执行./husky/下 pre-commit、commit-msg 配置文件中脚本



### 3、配置自定义的git commit-msg格式规范

- commitlint 提交校验安装配置

  ```bash
  npm install --save-dev @commitlint/cli@17.0.2 @commitlint/config-conventional@17.0.2
  
  npm install -g commitizen@4.2.4 // 建议全局安装 基于Node.js的 git commit 命令行工具，辅助生成标准化规范化的 commit message
  ```

  

- 安装自定义项目提交配置适配器

  ```bash
  npm install --save-dev cz-customizable@6.3.0
  ```

在工程目录创建commitlint.config.js文件

```js
'use strict';
module.exports = {
  extends: ['@commitlint/config-conventional'],
  rules: {
    'type-enum': [
      2,
      'always',
      [
        'feat', 
        'fix', 
        'docs', 
        'style', 
        'refactor', 
        'perf', 
        'test', 
        'chore', 
        'revert', 
        'build', 
        "impr", 
        "ci", 
        "jvm", 
        "pom", 
        "apm", 
        "conf", 
        "typo", 
        "wip", 
      ]
    ],
    'type-case': [0],
    'type-empty': [0],
    'scope-empty': [0],
    'scope-case': [0],
    'subject-full-stop': [0, 'never'],
    'subject-case': [0, 'never'],
    'header-max-length': [0, 'always', 72]
  }
};

```

- 配置脚本关联

  在package.json文件中添加

  ```json
  "config": {
      "commitizen": {
        "path": "./node_modules/cz-customizable"
      }
   }
  ```

  

### 4、配置lint-staged脚本

- 安装lint-staged 用于预提交时要进行代码检查的规范

```bash
npm install --save-dev lint-staged@12.5.0
```

- 在package.json 新增lint-staged 配置

```json
"scripts": {
    "lint": "eslint --ext .js,.vue src",
    "lint:style": "stylelint src/**/*.{vue,scss}"
},
"lint-staged": {
    "src/**/*.{js,vue}": [
      "npm run lint"
    ],
    "src/**/*.{vue,scss}": [
      "npm run lint:style"
    ]
 },
```



### 5、进行代码检查的规范配置

#### 5.1安装插件

      ```bash
       npm install stylelint-config-hikyun eslint-plugin-hikyun --save-dev // 建议安装 版本1.0.0 +
      ```

> 注1：不删除package-lock.json文件下， 删除冗余依赖的过程，需要执行uninstall 插件，才能修改lock文件中的插件， 以eslint-webpack-plugin为例
>
> ```bash
> npm uninstall eslint-webpack-plugin
> ```
>
> 注2：直接删除package.json文件文件中的依赖， 同时删除package-lock.json文件（有风险， 不推荐！！！），删除node_modules文件夹， 重新安装依赖， 此过程会重新构建lock文件依赖结构
>
> 注3：注意锁定vue版本~2.6.14，以及vue-template-compiler版本~2.6.14。因为2.7.x 之后css的deep选择器语法有变更，根据自己的项目谨慎选择，是否升级vue版本
>
> ```bash
> npm install --force  // 其中npm < 7 下 --force参数会失效，不会安装peerDependencies 下依赖，--legacy-peer-deps 这个会忽略同等依赖的
> ```

#### 5.2配置插件

- **配置.eslintrc.js**

  ```js
  module.exports = {
    root: true,
    extends: [
      "plugin:hikyun/recommended"
    ],
    plugins: ["hikyun"],
    rules: {}
  };
  ```

  在build/webpack.dev.conf.js中:

  const ESLintPlugin = require('eslint-webpack-plugin'); //这里是webpack编译加载eslint插件， 不需额外安装，已经在eslint-plugin-hikyun中依赖列表中

  在plugins字段下：
  ```js
  plugins: [
    new ESLintPlugin({
        context: rootPath,
        extensions: ['js', 'vue'],
        files: path.resolve(rootPath, 'src'),
        formatter: require("eslint-friendly-formatter")
    })   
  ]
  ```

  注：const rootPath = path.resolve(__dirname, ".."); // 项目根目录

- **配置stylelintrc.json**

```json
{
"extends": "stylelint-config-hikyun"
}
```

在build/webpack.dev.conf.js中:

const StylelintPlugin = require("stylelint-webpack-plugin"); //这里是webpack编译加载stylelint插件， 不需额外安装，已经在stylelint-config-hikyun中依赖列表中

在plugins字段下添加：

```js
new StylelintPlugin({
   cache: true,
   context: rootPath,
   files: path.resolve(rootPath, 'src'),
   extensions: ['css', 'scss', 'html', 'vue', 'js'],
   configFile: path.resolve(rootPath, ".stylelintrc.json")
})
```

注， 某些工程配置是stylelintrc.js，需要注意 当 stylelintrc.json 在webpack.config.js中 StylelintPlugin 中 configFile 字段配置的路径名称一致，

#### 5.3.测试插件

- **在package.json中添加脚本 （自动修复脚本去掉 --fix）**

  `"scripts": {`
  `  "eslint:lint": "eslint --ext .js,.vue src",`
  `  "stylelint:lint": "stylelint src/**/*.{vue,scss}",`
  `}`

- #### 在终端测试命令

  ```bash
  npm run eslint:lint
  npm run stylelint:lint
  ```

  

  **则可以统计到问题数量， 建议两个命令分开执行**

  ![img](https://rdwiki.hikvision.com.cn/download/attachments/192277113/image-lint.png?version=1&modificationDate=1665394090695&api=v2)

     

  关于 stylinelint 问题总数的统计， 大家在统计的时候，没有eslint总数那么方便， 最简单的方法可以参考 下图：

  在 控制台终端 搜素 “Expected” 可以在右上角看到总数

  ![img](https://rdwiki.hikvision.com.cn/download/attachments/192277113/clip_image002.jpg?version=1&modificationDate=1665394793329&api=v2)

