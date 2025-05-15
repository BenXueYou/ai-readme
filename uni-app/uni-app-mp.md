### 一、uni-app脚手架使用

#### 安装工具

全局安装 vue-cli

```shell
npm install -g @vue/cli
```

#### 创建模板

```bash
vue create -p dcloudio/uni-preset-vue my-project
```

使用Vue3/Vite版

- 创建以 javascript 开发的工程（如命令行创建失败，请直接访问gitee下载模板）

  ```shell
  npx degit dcloudio/uni-preset-vue#vite my-vue3-project
  ```

  ```shell
  npx degit dcloudio/uni-preset-vue#vite-alpha my-vue3-project
  ```

- 创建以 typescript 开发的工程（如命令行创建失败，请直接访问gitee下载模板）

  ```shell
  npx degit dcloudio/uni-preset-vue#vite-ts my-vue3-project
  ```

#### 注意事项

- Vue3/Vite版要求 node 版本`^14.18.0 || >=16.0.0`
- 如果使用 HBuilderX（3.6.7以下版本）运行 Vue3/Vite 创建的最新的 cli 工程，需要在 HBuilderX 运行配置最底部设置 node路径 为自己本机高版本 node 路径（注意需要重启 HBuilderX 才可以生效）
  - HBuilderX Mac 版本菜单栏左上角 HBuilderX->偏好设置->运行配置->node路径
  - HBuilderX Windows 版本菜单栏 工具->设置->运行配置->node路径

#### 运行发布

```shell
npm run dev:%PLATFORM%
npm run build:%PLATFORM%
```

#### [参考文档](https://uniapp.dcloud.net.cn/quickstart-cli.html)



### 二、原生小程序转uni-app工具

支持转换**微信、QQ、头条/抖音、支付宝/钉钉和百度等小程序**转换到 uni-app 项目

输入小程序项目路径，即可输出 uni-app 项目。

工具同时支持 npm 安装 和 HbuilderX 插件(不依赖环境) 两种形式安装，安装方式如下：

#### [npm 安装](https://github.com/zhangdaren/miniprogram-to-uniapp#npm-安装)

```
$ npm install miniprogram-to-uniapp -g
```



#### [使用方法](https://github.com/zhangdaren/miniprogram-to-uniapp#使用方法)

```
Usage: wtu [options]

Options:

  -V, --version          output the version number [版本信息]
  -i, --input <target>   the input path for weixin miniprogram project [输入目录]
  -h, --help             output usage information [帮助信息]
  -c, --cli              the type of output project is vue-cli, which default value is false [是否转换为vue-cli项目，默认false]
  -m, --merge            merge wxss file into vue file, which default value is false [是否合并wxss到vue文件，默认false]
  -t, --template         transform template and include to component, which default value is false [转换template和include为单独组件，默认false]
```



#### [示例:](https://github.com/zhangdaren/miniprogram-to-uniapp#示例)

##### [默认转换:](https://github.com/zhangdaren/miniprogram-to-uniapp#默认转换)

```
$ wtu -i "./miniprogram-project"
```



注："./miniprogram-project" 是要转换的小程序项目目录，如路径中有空格应该用引号引起来。

##### [将 wxss 合并入 vue 文件:](https://github.com/zhangdaren/miniprogram-to-uniapp#将-wxss-合并入-vue-文件)

```
$ wtu -i "./miniprogram-project" -m
```



##### [转换项目为 vue-cli 项目:](https://github.com/zhangdaren/miniprogram-to-uniapp#转换项目为-vue-cli-项目)

```
$ wtu -i "./miniprogram-project" -c
```



##### [将 template 里面的 import/template 和 include 标签转换为单独组件(实验性):](https://github.com/zhangdaren/miniprogram-to-uniapp#将-template-里面的-importtemplate-和-include-标签转换为单独组件实验性)

```
$ wtu -i "./miniprogram-project" -t
```



待命令行运行结束，会在小程序项目的同级目录有以 小程序项目名 + "_uni" 或 小程序目录名 + "_uni-cli" 目录，即是转换好的 uni-app 项目，转换好后，请使用 HBuilderX 导入并运行。

#### [HbuilderX 插件安装](https://github.com/zhangdaren/miniprogram-to-uniapp#hbuilderx-插件安装)

请参考项目：[【HBuilder X 插件】 转换各种小程序为 uni-app 项目](https://ext.dcloud.net.cn/plugin?id=2656) 进行食用。

#### [说明文档](https://github.com/zhangdaren/miniprogram-to-uniapp#说明文档)

关于本工具转换原理及常见问题，请见：[miniprogram-to-uniapp文档](https://l4rz4zwpx7.k.topthink.com/@kmrvzg72lx/)



### 三、使用问题

1、配置文件 default.theme.json 未处理

在 `manifest.json -> mp-weixin` 中配置：

- 配置 `darkmode:true`
- 配置 `themeLocation`，指定变量配置文件 `theme.json` 路径，例如：在根目录下新增 `theme.json`，需要配置 `"themeLocation":"theme.json"`
- 在 `theme.json` 中定义相关变量
- 在 `pages.json` 中以@开头引用变量
- 整体配置

2、全局的自动注入局部组件

- easycom 需要 采用vant 自定义 源码方式
- 将源码放入src目录下wxcomponents文件夹中

3、注意兼容插件版本

安装插件脚本

```bash
npm install --ignore-scripts puppeteer
```



