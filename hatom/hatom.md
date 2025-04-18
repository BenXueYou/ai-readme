hatom移动端仓库说明

### htiom平台

仓库地址：https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vhatom.git

### 帮助文档

仓库地址：https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vhatom-doc.git

### 脚手架hatom2-cli

仓库地址：http://iris.hikvision.com.cn/pengxueyou/hatom2-cli.git

### 模板工程

仓库地址：

```javascript
{
    "spa-tpl": "http://iris.hikvision.com.cn/liuhao17/hatom-spa-tpl.git",
	"spa-demo":  "http://iris.hikvision.com.cn/liuhao17/hatom-spa-demo.git",
	"mpa-tpl":  "http://iris.hikvision.com.cn/liuhao17/hatom-mpa-tpl.git",
	"mpa-demo": "http://iris.hikvision.com.cn/liuhao17/hatom-mpa-demo.git",
	"uni-tpl": "http://iris.hikvision.com.cn/pengxueyou/hatom-uni-tpl.git",
	"uni-demo": "http://iris.hikvision.com.cn/pengxueyou/hatom-uni-demo.git",
	"hummer-vue-tpl": "http://iris.hikvision.com.cn/pengxueyou/hummer-vue-tpl.git"
}
```

### 插件hatom-js

仓库地址：http://iris.hikvision.com.cn/pengxueyou/hatom-js.git

### hatom-hummer

仓库地址： http://iris.hikvision.com.cn/pengxueyou/hatom-hummer.git

### hatom-ui 组件

仓库地址： http://iris.hikvision.com.cn/pengxueyou/hatom-ui.git

### hatom-h5-demo

仓库地址：http://iris.hikvision.com.cn/pengxueyou/hatom-h5-demo.git

### 插件发布流程

```bash
# 切换源码代理仓库
npm config set registry http://af.hikvision.com.cn/artifactory/api/npm/npm-pbg/

# 用户登录
npm login

# 输入用户名密码
npm-pbg/helloworld

# 输入邮箱
oa@hikvision.com.cn

# 设置发布的版本
npm version <update_type>

# 发布命令
npm publish

```

### 插件仓库站点

浏览地址：http://af.hikvision.com.cn/ui/packages



H5组件：

云曜视频中心APP_H5： https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/app-h5

云远bmobile_h5: https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/bmobile-h5

