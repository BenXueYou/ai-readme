eslint 规范问题的收集：

目前收集到反馈是：

1、jsx 语法支持， 目前的插件不太支持

```json
"parser": "vue-eslint-parser",
"parserOptions": {
    "sourceType": "module",
    "ecmaVersion": 2020,
    "ecmaFeatures": {
      "globalReturn": false,
      "impliedStrict": false,
      "jsx": true // 是否支持jsx
    }
 },
```

2、路由问题

```json
  /** 类命名: 首字母大写 */
  "vue/component-definition-name-casing": ["error", "PascalCase"],
```

3、逗号的间隔

```json
/** 控制逗号前后的空格 */ 
    "comma-spacing": [
      2,
      {
        before: false,
        after: true
      }
    ],
    /** 强制在 function的左括号之前使用一致的空格 */
    "space-before-function-paren": [2, "always"],
    /** 强制在圆括号内使用一致的空格 */
    "space-in-parens": [2, "never"],
    /** 要求操作符周围有空格 */
    "space-infix-ops": 2,
    /** 强制在一元操作符前后使用一致的空格 */
    "space-unary-ops": [
      2,
      {
        words: true,
        nonwords: false
      }
    ],
```

4、单标签闭合问题

```json
    /** 标签闭合问题 */ 
    "vue/html-self-closing": ["error", {
      "html": {
        "void": "never",
        "normal": "never",
        "component": "always"
      },
      "svg": "always",
      "math": "always"
    }],
```

5、单行长度换行

```json
 "vue/max-len": ["error", {
        "code": 80,
        "template": 80,
        "tabWidth": 2,
        "comments": 80,
        "ignorePattern": "",
        "ignoreComments": false,
        "ignoreTrailingComments": false,
        "ignoreUrls": false,
        "ignoreStrings": false,
        "ignoreTemplateLiterals": false,
        "ignoreRegExpLiterals": false,
        "ignoreHTMLAttributeValues": false,
        "ignoreHTMLTextContents": false,
    }]
```





在构建命令前增加一句这个export PATH=/data1/cdToolkits/tools/thirdpart/node/node_14/bin:$PATH
