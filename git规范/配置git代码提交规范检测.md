## 方案一

配置git commit 命令拦截hook, 校验 commit-msg 格式规范，默认git >= 2.27.0, node >=14

### 1、修改配置文件

- 删除package-lock.json文件

- 删除package.json中的冗余配置

  ```json
  {
    "scripts": {
        "commit": "git-cz",
    },  
    "commitlint": {
      "extends": [
        "@commitlint/config-conventional"
      ]
    },
    "config": {
      "commitizen": {
        "path": "node_modules/cz-customizable"
      }
    },
    "devDependencies": {
        "commitizen": "^3.0.5"
    }
  }
  ```

- 在package.json 添加配置：

  ```json
  {
    "husky": {
      "hooks": {
        "pre-commit": "lint-staged",
        "commit-msg": "commitlint -E HUSKY_GIT_PARAMS"
      }
    },
  }
  ```

- 在package.json 修改插件版本号

  ```json
  
  {
    "devDependencies": {
      "@commitlint/cli": "16.3.0",
      "@commitlint/config-conventional": "16.2.4",
      "husky": "4.3.8",
    }
  }
  ```

### 2、添加规范配置文件

在工程根目录创建commitlint.config.js文件

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
        'impr', 
        'ci', 
        'jvm', 
        'pom', 
        'apm', 
        'conf', 
        'typo', 
        'wip' 
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

### 3、 安装更新插件

```bash
npm install
```

> 若是不生效， 请检查根目录下.git/config 文件中是否含有高版本husky的字段配置， 若有则注释掉husky的配置
