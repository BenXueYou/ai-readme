针对不同场景有三个方案

方案一：针对单个工程项目，配置husky插件，可以配置在工程模板中

方案二：安装全局插件，自动写入脚本，只需要两步操作，拦截所有git commit 命令

方案三：手动配置脚本，拦截所有git commit 命令，针对个别插件安装失败的情况使用 



## 单个项目

配置git commit 命令拦截hook, 校验 commit-msg 格式规范

前面默认git >= 2.27.0, node >=14

### 1、安装huskey@4.3.8

```bash
npm install --save-dev husky@4.3.8
```

### 2、初始化配置文件

- 在package.json scripts 属性中添加命令并保存：

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

### 3、配置自定义的git commit-msg格式规范

- commitlint 提交校验安装配置

  ```bash
  npm install --save-dev @commitlint/cli@16.3.0 @commitlint/config-conventional@16.2.4
  ```

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
>   若是不生效， 请检查根目录下.git/config 文件中是否含有高版本husky的字段配置， 若有则注释掉husky的配置
>    ```
>    
>    



## 安装脚本插件

### 安装chusky

```bash
npm install chusky --save-dev
```

### 配置启动脚本

在package.json

```json
"scripts": {
    "postinstall": "node ./node_modules/chusky/bin/index.js",
},
```

### 测试脚本

```bash
npm install

git add .

git commit "your message"
```



## 配置全局检查的脚本

说明： `~/.git` 通常指的是用户主目录下的`.git`目录

### 创建 ~/.gitconfig 文件

```bash
[user]
 	name = pengxueyou # 配置git username
 	email = pengxueyou@hikvision.com.cn # 配置 git 邮箱
[core]
	autocrlf = false
	hooksPath = ~/.git/hooks # 指定脚本位置
[credential]
	helper = store
[http]
	sslVerify = true
	sslBackend = schannel

```

### 创建 ~/.git/hooks/commit-msg

```bash
#!/bin/sh

# Created by Husky v4.3.8 (https://github.com/typicode/husky#readme)
#   At: 2024/8/8 下午8:51:41
#   From: undefined (undefined)
echo "---------开始执行检查脚本----------"
# 获取提交信息文件的路径
commit_msg_file=$1

# 读取提交信息
commit_msg=$(cat "$commit_msg_file")

# 打印提交信息（可选）
echo "Commit message: $commit_msg"

keywords="feat:|fix:|perf:|impr:|ci:|docs:|style:|refactor:|test:|chore:|jvm:|pom:|apm:|conf:|typo:|wip:"
# 定义关键词列表
EXCLUDED_KEYWORDS=("【" "】" "[]" "【】")

# 在这里可以添加您需要的逻辑来处理提交信息
# 例如，检查提交信息是否符合某种格式
if ! echo "$commit_msg" | grep -qE "^($keywords)" ; then
  echo "Error: Commit message must start with one of the following keywords:[ 'feat', 'fix', 'docs', 'style', 'refactor', 'perf', 'test', 'chore', 'revert', 'build', 'impr','ci','jvm','pom','apm','conf','typo', 'wip']"
  exit 1
fi

# 检查提交信息长度是否超过50字符
if [ ${#commit_msg} -gt 50 ]; then
    echo "Error: Commit message length exceeds 50 characters."
    exit 1
fi

# 遍历关键词列表，检查提交信息中是否不包含任何关键词
for keyword in "${EXCLUDED_KEYWORDS[@]}"; do
    if echo "$commit_msg" | grep -qE "$keyword"; then
        echo "Error: Commit message contains an excluded keyword '$keyword'."
        exit 1
    fi
done

exit 0
```

