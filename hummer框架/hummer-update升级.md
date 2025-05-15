### 升级脚手架

#### 安装脚手架工具

```bash 
# 先卸载掉原来的版本， 去掉安装外网的安装
npm uninstall -g @hummer/cli

# 切换公司内网的npm 代理源
npm config set registry http://af.hikvision.com.cn/artifactory/api/npm/npm-pbg/

# 全局安装 内网的版本
npm install -g @hummer/cli   

# 检查是否安装成功
hummer --version   

# 返回版本 11.1.1

```

#### 初始化工程模板

```bash
# 通过内网的hatom2-cli 脚手架 初始化模板工程
npm install hatom2-cli@2.4.3 -g

# 检查版本hatom2-cli 的版本号
hatom --version 
# 返回版本 > 2.4.x

# 初始化模板工程
hatom init hummer-vue-tpl <项目名称>
```



#### 打包命令

```bash
npm run build
```



#### 文件的配置

#### 

在 hm.config.js 文件中， 配置打包编码压缩配置

```javascript
webpack: {
      ...
      optimization: {
        minimize: argv.command === "dev" ? false : true, // 压缩配置
      }    
}
```



### 升级的要点

> 确保升级后插件的版本如下

```bash
@hummer/tenon-vue : 11.0.0
@hummer/cli: 11.1.1
# 如项目中出现hatom-ui框架，请确保hatom-ui 升级为0.0.2
hatom-ui: 0.0.2
```



### 升级后打包测试

脚手架工具的版本号以及时间打印，确保升级成功

![202312-8659cfee573d4d625acdffe43cf4647c](C:\Users\pengxueyou\Documents\HikLink_Files\pengxueyou\received\202312-8659cfee573d4d625acdffe43cf4647c.png)