# [云曜前端代码规范-插件配置](https://wiki.hikvision.com.cn/pages/viewpage.action?pageId=188650738)

为了代码规范统一性，发布了eslint-plugin-hikyun插件便于管理 [发布地址](https://af.hikvision.com.cn/ui/packages/npm:%2F%2Feslint-plugin-hikyun?name=eslint-plugin-hikyun&type=packages) 

插件依赖：eslint 7+、 vue-eslint-parser 8.0、 eslint-plugin-vue 7.0、 stylelint 13、stylelint-webpack-plugin、stylelint-scss, stylelint-order

在插件中eslint-plugin-hikyun 已经peerDependencies, 无需额外安装，各个项目中已经存在的插件，注意核对版本

```javascript
  "peerDependencies": {
    "@babel/eslint-parser": "^7.18.9",
    "eslint": ">=7",
    "stylelint": "^13.11.0",
    "stylelint-order": "^5.0.0",
    "vue-eslint-parser": "^8.3.0",
    "eslint-plugin-vue": "^7.20.0"
  },
```



### 安装插件

```bash

npm install stylelint-webpack-plugin eslint-plugin-hikyun --save-dev

```

**注意**：安装插件的过程中，遇到版本不兼容， 不建议删除package-lock.json文件, 以eslint-plugin-hikyun插件为例

```bash
npm uninstall eslint-plugin-hikyun
npm install eslint-plugin-hikyun@0.0.3  --save-dev
```



### 配置插件

- #### 配置eslint.js

```javascript
module.exports = {
 root: true,
 extends: [
  "plugin:hikyun/recommended"
 ],
 plugins: ["hikyun"],
 rules: {}
};
```

- #### 配置stylelintrc.json

```json
{
  "extends": ["./node_modules/eslint-plugin-hikyun/lib/stylelint.js"],
  "rules": {}
}
```

这里**注意**， 某些工程配置是stylelintrc.js，需要注意 当 stylelintrc.json 在webpack.config.js中 StylelintPlugin 中 configFile 字段配置的路径名称一致，

```javascript
    new StylelintPlugin({
      configFile: path.resolve(rootPath, ".stylelintrc.json"),
      cache: true,
      files: ["**/*.css", "**/*.scss", "**/*.html", "**/*.js", "**/*.vue"]
    }),
```



### 测试插件

- #### 在package.json中添加脚本 （自动修复脚本去掉 --fix）

```javascript
 "scripts": {
  "eslint:lint": "eslint --ext .js,.vue src",
  "stylelint:lint": "stylelint src/**/*.{vue,scss}",
 }
```

- #### 在终端测试命令

```bash
 npm run eslint:lint
 npm run stylelint:lint
```

则可以统计到问题数量， 建议两个命令分开执行

执行结果如下：

![](D:\Typora\doc\eslint\image-lint.png)



### 其他问题

#### 配置支持 jsx

**vue 支持jsx 语法的前提** ：

babel生态圈插件支持：@babel/core、@babel/eslint-parser、@babel/plugin-transform-runtime、@babel/plugin-proposal-class-properties、@babel/plugin-syntax-dynamic-import

vue 生态圈插件支持：@vue/babel-helper-vue-jsx-merge-props、  @vue/babel-preset-jsx

以上大部分会在脚手架中会自带插件  需要核对 （@babel/eslint-parser、vue-eslint-parser）两个插件

同时支持babel配置文件**babel.config.js**

```javascript
module.exports = {
  "presets": [
    ["@babel/env", { "modules": false, "targets": { "ie": 11 }}],
    "@vue/babel-preset-jsx"
  ],
  "sourceType": 'unambiguous',
  "plugins": ["@babel/plugin-transform-runtime", "@babel/plugin-proposal-class-properties", "@babel/plugin-syntax-dynamic-import"]
};
```



可能会遇到以下问题

![image-20220831102331667](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20220831102331667.png)

报错的原因是这种直接返回dom 标签 属于 jsx 语法

![image-20220831103153072](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20220831103153072.png)

在eslint.js中新增配置

```javascript
module.exports = {
  root: true,
  parser: "vue-eslint-parser",
  parserOptions: {
    "parser": "@babel/eslint-parser",
    ecmaVersion: 2021,
    sourceType: 'module',
    ecmafeatures: {
      // 是否允许在全局作用域下使用 return 语句 
      globalReturn: false,
      // 是否启用全局 strict 模式（严格模式） 
      impliedStrict: false,
      // 是否启用对实验性的objectRest/spreadProperties的支持
      experimentalObjectRestSpread: false,
      jsx: false
    },
    jsx: false
  },
  extends: ["plugin:hikyun/recommended"],
  plugins: ["hikyun"],
  rules: {}
};
```

