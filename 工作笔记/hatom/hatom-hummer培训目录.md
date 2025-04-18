

## Hatom-Hummer使用手册



### 简介

​		本文档主要讲述的是海康移动应用开发平台使用说明，以及使用hatom脚手架+hummer框架开发流程。包含开发环境搭建、开发工具安装、工程模板下载、平台使用。

### 开发环境

开发环境包含node环境安装、@hummer/cli、hatom2-cli等工具。node版本建议node14 [下载](https://nodejs.org/en/download/)，[安装教程](https://blog.csdn.net/qq_42006801/article/details/124830995) ，检查node是否安装成功

```
node --verion
npm --version
```

有版本号返回，即为安装成功，接下来可以安装@hummer/cli、hatom2-cli, 安装命令如下：

```bash
npm install -g @hummer/cli
npm install -g hatom2-cli
```

通过命令行检查是否安装成功

```bash
hummer --version
hatom --version
```

有版本号版本，即为安装成功。接下来推荐coding工具[vscode](https://code.visualstudio.com/Download)，初始化工程模板。



### 开发流程

初始化工程模板，在控制终端输入命令，如下：

```bash
hatom init hummer-vue-tpl hello
```

完成项目工程初始化，当前根目录下会生成目录 hello(初始化的项目名称)。通过vscode打开hello，输入目录下终端， 输入项目运行命令，如下：

```
npm run dev
```

会默认打开浏览器加载 本地IP:8000端口，即应用运行成功, 在dist目录下会生成成果物hm_hello。 打包命令为：

```
npm run build
```

在dist目录下生成zip包hm_hell_时间戳.zip

### 开说说明

#### 目录结构

```shell
├── dist  ·························································· 构建成果物
│   ├── hm_${webappJson.h5packCode}  ······························· 开发环境构建
│   └── hm_${webappJson.h5packCode}_${new Date().getTime()}.zip ···· 生产环境构建zip包
│
│
├── src  ··························································· 业务代码
│   │
│   ├── api  ······················································· 网络API
│   │   ├── api.js  ················································ api 接口url
│   │   └── http.js  ··············································· http 请求方法
│   │
│   ├── assets  ···················································· 资源文件目录
│   │   ├── icons  ················································· 图标
│   │   ├── images  ················································ 图片
│   │   │   └── bg.png  ·····································....··· 背景图
│   │   └── styles  ················································ 样式
│   │       ├── animation.css  ····································· 动画样式
│   │       └── reset.css  ········································· 重置样式表
│   │
│   ├── components  ················································ 公共组件
│   │   ├── i-nav  ················································· nav组件
│   │   │   ├── src
│   │   │   │   └── i-nav.vue
│   │   │   └── index.js
│   │   ├── i-tabbar  ·············································· tabbar组件
│   │   │   ├── src
│   │   │   │   └── i-tabbar.vue
│   │   │   └── index.js
│   │   └── index.js  ·············································· 封装
│   │
│   ├── common  ···················································· 业务配置
│   │   ├── utils    
│   │   │   ├── reg.js  ············································ 公共正则
│   │   │   └── util.js  ··········································· 公共方法
│   │   └── index.js  ·············································· 封装
│   │
│   │
│   ├──  mixins  ··················································· 全局过滤器
│   │   └── index.js
│   │
│   │
│   ├── pages  ····················································· 应用页面
│   │   ├── page1  ················································· 页面一
│   │   │   ├── App.vue ............................................ 根组件
│   │   │   └── entry.js  .......................................... 入口文件 
│   │   │   
│   │   ├── page2  ················································· 页面二
│   │   │   ├── App.vue ............................................ 根组件
│   │   │   └── entry.js  .......................................... 入口文件
│   │   │   
│   │   └── page3  ················································· 页面三iSee
│   │       ├── App.vue ............................................ 根组件
│   │       └── entry.js  .......................................... 入口文件
│   │
│   │
│   └── store  ····················································· tenon-store 插件
│       ├── actions.js
│       ├── getters.js
│       ├── index.js
│       ├── mutations.js
│       └── state.js
│
├── webApp.json  ··················································· hatom 框架配置文件
│
├── hm.config.js  ·················································· hummer + webpack 配置
│
├── package-lock.json  ············································· package-lock.json
│
└── package.json  ·················································· package.json
```



#### UI组件库

UI组件库[hummer-front](https://github.com/OrangeLab/hummer-front), 使用[教程](https://hummer.didi.cn/doc-tenon#/zh-CN/component_view)

- **View** 基本视图
- **Text** 文本
- **Image **图片
- **Button **按钮
- **Input** 输入框
- **TextArea** 文本输入框
- **Scroller **滚动容器
- **HorizontalScroller **横向滚动容器
- **List** 复用列表
- **ViewPager** 轮播
- **Navigator** 路由模块
- **Animation** 动画模块
- **Toast** Toast 提示
- **DialogDialog**  弹窗

#### 图片加载

无效加载方式

直接加载相对路径是无效的 如下：

```html
 <image src="../assets/images/logo.png"></image>
```

有效加载方式

1、使用 require()函数进行图片加载

```html
 <image :src="require('../assets/images/logo.png')"></image>
```

2、使用require()函数之后的地址

首先在代码中执行require()函数

```javascript
created() {
  require('../assets/images/logo.png')
}
```

之后会在dist文件下images下有图片路径， 直接填写dist下的文件路径， 如下

```html
 <image src="../images/logo.png)"></image>
```

#### 动态class

这种是无效的写法，无法动态加载样式，如下：

```html
 <view :class="active? 'acive-class':''"></view>
```

使用 :style="{ width: currentImage === v ? 50: 56, height: currentImage === v ? 50: 56 }"

#### 背景图片

css中无效的写法， 如下：

background-color: url("../assets/images/logo.png")

#### style样式

不建议使用 scss/sass/less

```css
<style>

.active-class {
  // css 属性
}
</style>
```

#### 网路请求

axios/ajax 无效

采用hummer封装的网络请求对象 request

```javascript
var request = new Request();
request.url = "http://xxx.xxx.xxx.xxx:8000/test";
request.method = "GET";
request.send((response) => {
    /**
     * status	 number	状态码	{ status: 200 }
	* header	 Object	请求头信息	
	* data	     Object	响应数据	{ data: { aa: 11, bb: 22} }
	* error	     Object	请求错误	{ error: { code: 404, msg: 'not found' } }
    */
});
```

#### API调用

Hummer 原生的API，使用[教程文档](https://hummer.didi.cn/doc#/zh-CN/hummer)

##### Hummer.env

内置环境变量。

| 属性名          | 类型   | 说明                                             | 示例       |
| :-------------- | :----- | :----------------------------------------------- | :--------- |
| platform        | string | 平台类型                                         | `'iOS'     |
| osVersion       | string | 平台系统版本号                                   | `'14.0'    |
| appVersion      | string | App版本号                                        | `'1.0'`    |
| appName         | string | App名字                                          | `'Hummer'` |
| statusBarHeight | number | 状态栏高度（单位：dp或pt）                       | `44`       |
| safeAreaBottom  | number | iOS安全区域高度（单位：dp或pt）（Android可忽略） | `34`       |
| deviceWidth     | number | 设备宽度（单位：dp或pt）                         | `414`      |
| deviceHeight    | number | 设备高度（单位：dp或pt）                         | `896`      |
| availableWidth  | number | 可用范围宽度（单位：dp或pt）                     | `414`      |
| availableHeight | number | 可用范围高度（单位：dp或pt）                     | `852`      |
| scale           | number | 像素缩放比例                                     | `3`        |

##### Hummer.notifyCenter

全局消息通知类。

```js
/**
 * 设置消息监听事件
 * 
 * @param event 事件名称
 * @param callback 接收消息回调，value为消息内容
 */
 addEventListener(event: String, callback: (value: Object) => void)
/**
 * 取消消息监听事件
 * 
 * @param event 事件名称
 * @param callback 接收消息回调，addEventListener时的callback对象
 */
 removeEventListener(event: String, callback: (value: Object) => void)
/**
 * 发送消息
 * 
 * @param event 事件名称
 * @param value 消息内容
 */
 triggerEvent(event: String, value: Object)

```

##### demo示例代码

```javascript
// 渲染Hummer页面
Hummer.render(new View());
// 获取平台类型
let platform = Hummer.env.platform;

// 全局消息中心
let callback = (value) => {};
// 设置消息监听
Hummer.notifyCenter.addEventListener("event", callback);
// 取消消息监听
Hummer.notifyCenter.removeEventListener("event", callback);
// 发送消息
Hummer.notifyCenter.triggerEvent("event", {test: 1234});
```

##### 进阶API

[数据传递](https://hummer.didi.cn/doc#/zh-CN/android_doc_advanced#liu-shu-ju-chuan-di)、[页面跳转](https://hummer.didi.cn/doc#/zh-CN/android_doc_advanced#wu-ye-mian-tiao-zhuan)、自定义API[Bridge 用法](https://hummer.didi.cn/doc#/zh-CN/android_doc_advanced#si-bridge-yong-fa) 、[教程](https://hummer.didi.cn/doc#/zh-CN/android_doc_advanced)，调用自定义API方法

Test 原生java静态类

```js
Test.nativeFunc(111, 222);
```

自定义导出类 TestModel,  onTest 为 java实例方法

```
const test = new TestModel();
test.onTest()
```



### 平台使用

登录[移动应用开发平台](https://hatom2.hikyun.com/)，进入我的应用， 创建硬件应用：

#### 创建应用

<div align="left"><img width="720px" style="border:3px solid #eaecef" src="./images/mp/image_9.png" /></div>

<div align="left"><img width="720px" style="border:3px solid #eaecef" src="./images/mp/image_10.png" /></div>



#### 配置应用

<div align="left"><img width="720px" style="border:3px solid #eaecef" src="./images/mp/image_11.png" /></div>

#### 配置模板

<div align="left"><img width="720px" style="border:3px solid #eaecef" src="./images/mp/image_12.png" /></div>

#### 配置组件

<div align="left"><img width="720px" style="border:3px solid #eaecef" src="./images/mp/image_13.png" /></div>

#### 上传成果物

<div align="left"><img width="720px" style="border:3px solid #eaecef" src="./images/mp/image_14.png" /></div>

<div align="left"><img width="720px" style="border:3px solid #eaecef" src="./images/mp/image_15.png" /></div>



#### 配置证书

<div align="left"><img width="720px" style="border:3px solid #eaecef" src="./images/mp/image_16.png" /></div>

#### 编译配置

<div align="left"><img width="720px" style="border:3px solid #eaecef" src="./images/mp/image_17.png" /></div>

#### 编译日志

<div align="left"><img width="720px" style="border:3px solid #eaecef" src="./images/mp/image_7.png" /></div>



#### 配置开发人员

点击右上角人员配置

<div align="left"><img width="720px" style="border:3px solid #eaecef" src="./images/mp/image_8.png" /></div>

#### 生成编译记录

<div align="left"><img width="720px" style="border:3px solid #eaecef" src="./images/mp/image_18.png" /></div>
