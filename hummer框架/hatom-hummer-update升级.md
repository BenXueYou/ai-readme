### 升级脚手架

#### 安装脚手架

```bash 
# 全局安装
npm install -g hatom-hummer-cli

# 检查是否安装成功
hatom-hummer --version

```

#### 初始化工程模板

```bash
hatom init hummer-vue-tpl <项目名称>
```

#### 打包命令

```bash
npm run build
# 或
hatom-hummer build
```



#### 静态提升配置

在 hm.config.js 文件中

```javascript
buildOptions: {
    tenonLoaderOptions: {
        compilerOptions: {
          hoistStatic: false
        }
    }
},
```



#### 文件压缩配置

在 hm.config.js 文件中

```javascript
webpack: {
      ...
      optimization: {
        minimize: argv.command !== "dev" ? false : true,
      }    
}
```



#### 打包命令的配置

在 package.json 文件中

```javascript
"scripts": {
    "build": "hatom-hummer build",
    "dev": "hatom-hummer dev",
    "debug": "npm run dev & hatom-hummer debug"
  }
```

