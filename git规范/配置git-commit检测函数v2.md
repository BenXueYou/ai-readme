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

以上： 钩子函数已经配置完毕， 执行 git commit 命令之后，会被拦截开始执行./husky/下 commit-msg 配置文件中脚本



### 3、配置自定义的git commit-msg格式规范

- commitlint 提交校验安装配置

  ```bash
  npm install --save-dev @commitlint/cli@17.0.2 @commitlint/config-conventional@17.0.2
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

> 注意： 需要去掉package.json中配置项如下：
>
> ```json
>   "commitlint": {
>     "extends": [
>       "@commitlint/config-conventional"
>     ]
>   }
> ```
>
> 