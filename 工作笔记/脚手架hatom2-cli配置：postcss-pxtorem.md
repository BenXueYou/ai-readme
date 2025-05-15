### 脚手架hatom2-cli配置：postcss-pxtorem

1、安装postcss-loader、postcss-pxtorem

```sh
npm install --save-dev postcss-loader postcss
npm install postcss postcss-pxtorem --save-dev
```

2、配置插件：

项目根目录下创建：.postcssrc.js

```js
module.exports = {
    plugins: [
        require("autoprefixer"),
        ["postcss-pxtorem",
        {
            rootValue: 16,
            unitPrecision: 5,
            propList: ['*'],
            selectorBlackList: [],
            replace: true,
            mediaQuery: false,
            minPixelValue: 0,
            exclude: /node_modules/i
        }]
    ]
}
```

https://www.jianshu.com/p/79eefcc5418f

