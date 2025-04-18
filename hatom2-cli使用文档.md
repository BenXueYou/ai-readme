<div align="center">
    <a href="https://static.hikyun.com/hatom-static/logo.png">
      <img width="200" height="200" src="https://hatom.gitee.io/hatom-assets/hatom2-cli/logo.png">
    </a>
</div>

<h1 align="center">hatom2-cli</h1>

<p align="center">
  hatom官方前端脚手架
</p>
<br>

![npm][npm-shield]
![Dependencies][deps-shield]
![Install Size][size-shield]


├── [hatom2是什么](#1) <br>
├── [hatom2-cli有什么功能](#2)<br>
├── [安装](#3)<br>
├── [使用](#4)<br>
├── [模板](#5)<br>
│   ├── [spa-tpl模板](#5-1)<br>
│   │    ├── [开始](#5-1-1)<br>
│   │    ├── [选配](#5-1-2)<br>
│   │    ├── [运行](#5-1-3)<br>
│   │    └── [目录结构](#5-1-4)<br>
│   ├── [spa-demo模板](#5-2)<br>
│   ├── [mpa-tpl模板](#5-3)<br>
│   │    ├── [开始](#5-3-1)<br>
│   │    ├── [选配](#5-3-2)<br>
│   │    ├── [运行](#5-3-3)<br>
│   │    └── [目录结构](#5-3-4)<br>
│   └── [mpa-demo模板](#5-4) 

├── [调试](#6)<br>
│   ├── [pc端](#6-1)<br>
│   └── [设备端](#6-2)<br>
├── [应用开发与工程组织](#7)<br>
│   ├── [页面缓存](#7-1)<br>
│   ├── [路由动画](#7-2)<br>
│   ├── [公共组件](#7-3)<br>
│   ├── [全局方法、全局正则](#7-4)<br>
│   ├── [全局过滤器](#7-5)<br>
│   ├── [布局](#7-6)<br>
│   ├── [业务配置](#7-7)<br>
│   │    ├── [基础配置](#7-7-1)<br>
│   │    ├── [多页面配置](#7-7-2)<br>
│   ├── [雪碧图](#7-8)<br>
│   └── [其他注意事项](#7-9)<br>
├── [基础插件使用](#8)<br>
└── [高级插件使用](#9)<br>

<span id="1"></span>
## hatom2-cli是什么

hatom2-cli脚手架工具提供了一组灵活的交互命令，可以通过命令快速生成项目工程，从而避免babel、loader等繁琐的配置，使前端开发人员可以直接进行应用开发。其次，脚手架封装了hatom原生插件，不用进行额外的配置，就可以直接调用硬件设备（手机、pad等）的原生能力。同时，脚手架集成了目前比较流行的移动端UI框架，cube-ui、Vant，可以通过交互命令进行UI框架的选择，也可以选择其他的UI框架。最后，脚手架集成了eslint、stylelint，这样可以更好地规范你的代码。

<span id="2"></span>
## hatom2-cli有什么功能
* 快速生成前端工程，直接进行业务开发
* 封装硬件原生能力，方便调用
* 实现沉浸式布局
* 选配UI组件，当前提供cube-ui、Vant、自定义三种选配项
  * [cube-ui](https://didi.github.io/cube-ui/#/zh-CN/docs/introduction): 由滴滴开源的基于 Vue.js 实现的移动端组件库 
  * [Vant](https://vant-contrib.gitee.io/vant/#/zh-CN/): 轻量、可靠的移动端 Vue 组件库
  * 自定义
* 可选择的eslint、stylelint，更好的规范代码

<span id="3"></span>
## 安装
需要：[Node.js](https://nodejs.org/en/)(>=10.12.0), and npm version 6.4.1+.

全局安装：

``` bash
npm install -g hatom2-cli

$ hatom -V 
2.1.0
```

非全局安装：

```ssh
npx install hatom2-cli

$ npx hatom -V
2.1.0

```

<span id="4"></span>
## 使用

``` bash
# 查看版本
hatom -V/--version

# 帮助信息
hatom -help

# 查看所有模板
hatom list

# 工程初始化
hatom init <template> <project>

# 脚手架配置更新 hatom.js
hatom upd hatom

# 脚手架配置更新 webpack
hatom upd build

# 脚手架配置更新 hatom corejs
hatom upd core
```

<span id="5"></span>
## 模板
当前提供六种工程模板：

* [spa-tpl](https://gitee.com/hatom/hatom-spa-tpl) —— 基于webapck5+vue2的hatom单页应用模板
* [spa-demo](https://gitee.com/hatom/hatom-spa-demo) —— 基于spa-tpl模板搭建的单页应用demo
* [mpa-tpl](https://gitee.com/hatom/hatom-mpa-tpl) —— 基于webapck5+vue2搭建的多页应用模板
* [mpa-demo](https://gitee.com/hatom/hatom-mpa-demo) —— 基于mpa-tpl模板搭建的多页应用demo
* [uni-tpl](https://gitee.com/hatom/hatom-uni-tpl) —— 基于uni-app+uni-hatom插件搭建的应用模板 ( v2.3.0+)
* [uni-demo](https://gitee.com/hatom/hatom-uni-demo) —— 基于uni-tpl模板搭建的uni-app应用demo ( v2.3.0+)

<span id="5-1"></span>
### spa-tpl模板

<span id="5-1-1"></span>
#### 开始
全局模式：

``` bash
hatom init spa-tpl hello
```

非全局模式：

``` bash
npx hatom init spa-tpl hello
```

<span id="5-1-2"></span>
#### 选配

``` bash
# ? 项目名称（hello）
<enter>

# ? 项目描述（A hatom project）
hello project

# ? 版本（1.0.0）
<enter>

# 作者 (support.hikyun@hikvision.com.cn)
<enter>

# app远程地址（）
<enter>

# ？安装vuex（Y/n）
<enter>

# ? UI组件（Use arrow.keys）
  > Vant Weapp (轻量、可靠的小程序 UI 组件库)
    Cube-ui (基于 Vue.js 实现的精致移动端组件库) 
    None (add by yourself)
<enter>

# ? 是否使用ESLint规范代码行为（Y/n）
<enter>

# ? 选择一种ESLint规范（Use arrow keys）
  > Standard
    hatom
    none
<enter>
```

<span id="5-1-3"></span>
#### 运行

``` bash
cd hello
npm run dev
```
#### 调试

``` bash
npm run debug
```

<span id="5-1-4"></span>
#### 目录结构
``` bash
├── build  ······································· 构建配置
│   ├── webpack.dev.conf.js  ····················· 开发环境构建配置
│   └── webpack.prod.conf.js  ···················· 生产环境构建配置
│
│
├── src  ········································· 业务代码
│   │
│   ├── assets  ·································· 资源文件目录
│   │   ├── icons  ······························· 图标、可自动生成雪碧图
│   │   ├── images  ······························ 图片
│   │   │   └── sprite.png  ······················ 雪碧图
│   │   └── styles  ······························ 样式
│   │       ├── animation.css  ··················· 动画样式
│   │       ├── reset.css  ······················· 重置样式表
│   │       └── sprite.css  ······················ 雪碧图样式
│   │
│   ├── components  ······························ 公共组件
│   │   ├── i-nav  ······························· nav组件
│   │   │   ├── src
│   │   │   │   └── i-nav.vue
│   │   │   └── index.js
│   │   ├── i-tabbar  ···························· tabbar组件
│   │   │   ├── src
│   │   │   │   └── i-tabbar.vue
│   │   │   └── index.js
│   │   ├── utils    
│   │   │   ├── reg.js  ·························· 公共正则
│   │   │   └── util.js  ························· 公共方法
│   │   └── index.js  ···························· 封装
│   │
│   ├── config  ·································· 业务配置
│   │   ├── api.js  ······························ 接口地址
│   │   ├── constant.js  ························· 全局常量
│   │   ├── http.js  ····························· axios封装
│   │   ├── index.js  ···························· 封装
│   │   └── webApp.json  ························· app配置
│   │
│   ├── corejs  ·································· hatom封装
│   │   ├── WebViewJavascriptBridge.js
│   │   ├── hatom.js
│   │   └── pageRouter.json
│   │
│   ├── filters  ································· 全局过滤器
│   │   ├── filter.js
│   │   └── index.js
│   │
│   ├── layouts  ································· 布局
│   │   ├── layout1.vue  ························· 布局一
│   │   └── layout2.vue  ························· 布局二
│   │
│   ├── pages  ··································· 应用页面
│   │   ├── index  ······························· 首页
│   │   │   └── index.vue
│   │   ├── page1  ······························· 页面一
│   │   │   ├── detail.vue
│   │   │   └── index.vue
│   │   ├── page2  ······························· 页面二
│   │   │   └── index.vue
│   │   ├── page3  ······························· 页面三
│   │   │   └── index.vue
│   │   ├── page4  ······························· 页面四
│   │   │   └── index.vue
│   │   └── plugins-example  ····················· 插件页面
│   │       └── index.vue
│   │
│   ├── router  ·································· 路由配置
│   │   └── index.js
│   │
│   ├── store  ··································· vuex配置
│   │   ├── actions.js
│   │   ├── getters.js
│   │   ├── index.js
│   │   ├── mutations.js
│   │   └── state.js
│   │
│   ├── App.vue  ································· 根组件
│   │
│   ├── html.tmpl  ······························· html模板
│   │
│   ├── logo.ico  ································ logo.ico
│   │
│   └── main.js  ································· 入口
│
│
├── .editorconfig  ······························· 编辑器配置    
│
├── .eslintignore  ······························· eslint白名单配置
│
├── .eslintrc.js  ································ eslint配置
│
├── .gitignore  ·································· git白名单
│
├── .postcssrc.js  ······························· postCss配置
│
├── .stylelintignore  ···························· stylelint白名单配置
│
├── .stylelintrc.json  ··························· stylelint配置
│
├── babel.config.js  ····························· babel配置
│
├── package-lock.json  ··························· package-lock.json
│
└── package.json  ································ package.json
```

<span id="5-2"></span>
### spa-demo模板

<a href="https://static.hikyun.com/hatom-static/logo.png">
  <img width="200" height="200" src="https://hatom.gitee.io/hatom-assets/hatom2-cli/hatom-spa-demo.png">
</a>

<span id="5-3"></span>
### mpa-tpl 模板

<span id="5-3-1"></span>
#### 开始
全局模式：

``` bash
hatom init mpa-tpl mpa-demo
```

非全局模式：

``` bash
npx hatom init mpa-tpl mpa-demo
```

<span id="5-3-2"></span>
#### 选配

同 spa-tpl

<span id="5-3-3"></span>
#### 运行

同 spa-tpl

<span id="5-3-4"></span>
#### 目录结构
``` bash
├── build  ······································· 构建配置
│   ├── webpack.dev.conf.js  ····················· 开发环境构建配置
│   └── webpack.prod.conf.js  ···················· 生产环境构建配置
│
│
├── src  ········································· 业务代码
│   │
│   ├── assets  ·································· 资源文件目录
│   │   ├── icons  ······························· 图标、可自动生成雪碧图
│   │   ├── images  ······························ 图片
│   │   │   └── sprite.png  ······················ 雪碧图
│   │   └── styles  ······························ 样式
│   │       ├── animation.css  ··················· 动画样式
│   │       ├── reset.css  ······················· 重置样式表
│   │       └── sprite.css  ······················ 雪碧图样式
│   │
│   ├── components  ······························ 公共组件
│   │   ├── i-nav  ······························· nav组件
│   │   │   ├── src
│   │   │   │   └── i-nav.vue
│   │   │   └── index.js
│   │   ├── i-tabbar  ···························· tabbar组件
│   │   │   ├── src
│   │   │   │   └── i-tabbar.vue
│   │   │   └── index.js
│   │   ├── utils    
│   │   │   ├── reg.js  ·························· 公共正则
│   │   │   └── util.js  ························· 公共方法
│   │   └── index.js  ···························· 封装
│   │
│   ├── config  ·································· 业务配置
│   │   ├── api.js  ······························ 接口地址
│   │   ├── constant.js  ························· 全局常量
│   │   ├── http.js  ····························· axios封装
│   │   ├── index.js  ···························· 封装
│   │   └── webApp.json  ························· app配置
│   │
│   ├── corejs  ·································· hatom封装
│   │   ├── WebViewJavascriptBridge.js
│   │   ├── hatom.js
│   │   └── pageRouter.json
│   │
│   ├── filters  ································· 全局过滤器
│   │   ├── filter.js
│   │   └── index.js
│   │
│   ├── layouts  ································· 布局
│   │   ├── layout1.vue  ························· 布局一
│   │   └── layout2.vue  ························· 布局二
│   │
│   ├── pages  ··································· 应用页面
│   │   ├── page1  ······························· 页面一
│   │   │   ├── views                              业务组件
|   │   │   │   ├── hello-world
|   │   │   │   └── index.vue
│   │   │   ├── App.vue .......................... 根组件
│   │   │   ├── main.js .......................... 入口文件
│   │   │   ├── router.js ........................ 路由文件
│   │   │   └── store.js  ........................ vuex文件 
│   │   │   
│   │   ├── page2  ······························· 页面二iFar
│   │   │   ├── views                              业务组件
|   │   │   │   └── ifar.vue
│   │   │   ├── App.vue .......................... 根组件
│   │   │   ├── main.js .......................... 入口文件
│   │   │   ├── router.js ........................ 路由文件
│   │   │   └── store.js  ........................ vuex文件
│   │   │   
│   │   └── page3  ······························· 页面三iSee
│   │       ├── views                              业务组件
|   │       │   └── isee.vue
│   │       ├── App.vue .......................... 根组件
│   │       ├── main.js .......................... 入口文件
│   │       ├── router.js ........................ 路由文件
│   │       └── store.js  ........................ vuex文件
│   │
│   │
│   ├── html.tmpl  ······························· html模板
│   │
│   ├── logo.ico  ································ logo.ico
│   │
│   └── main.js  ································· 入口
│
│
├── .editorconfig  ······························· 编辑器配置    
│
├── .eslintignore  ······························· eslint白名单配置
│
├── .eslintrc.js  ································ eslint配置
│
├── .gitignore  ·································· git白名单
│
├── .postcssrc.js  ······························· postCss配置
│
├── .stylelintignore  ···························· stylelint白名单配置
│
├── .stylelintrc.json  ··························· stylelint配置
│
├── babel.config.js  ····························· babel配置
│
├── package-lock.json  ··························· package-lock.json
│
└── package.json  ································ package.json
```

<span id="5-4"></span>

### mpa-demo模板

<a href="https://static.hikyun.com/hatom-static/logo.png">
  <img width="200" height="200" src="https://hatom.gitee.io/hatom-assets/hatom2-cli/hatom-mpa-demo.png">
</a>

<span id="6"></span>
## 调试

<span id="6-1"></span>
### pc端：

1. 运行工程，在浏览器地址栏中输入地址
2. 打开浏览器控制台，并切换至device toolbar模式
<img width="730" src="https://hatom.gitee.io/hatom-assets/hatom2-cli/device-toolbar.png">


<span id="6-2"></span>
### 设备端：

1. 登录[移动应用开发平台](https://hatom2.hikyun.com/tooldownload),在工具下载模块中下载 无架构调试工具

<img width="730" src="https://hatom.gitee.io/hatom-assets/hatom2-cli/tool-download.png">

2. 在设备上安装调试工具，与pc连接至同一网域，并代开调试工具

3. 在入口文件main.js中执行去掉vconsole的相关注释

4. 在地址栏中输入工程运行地址，点击确定

<img width=320 src="https://hatom.gitee.io/hatom-assets/hatom2-cli/dev-1.png">

5. 点击屏幕右下角vConsole按钮，即可在设备端打开控制台进行调试
<div>
  <img width=320 src="https://hatom.gitee.io/hatom-assets/hatom2-cli/dev-2.png">  
  <img width=320 src="https://hatom.gitee.io/hatom-assets/hatom2-cli/dev-3.png">
</div>

<span id="7"></span>
## 应用开发与工程组织

<span id="7-1"></span>
### 页面缓存
PC端的分页是采用页码的形式，而移动端多采用上拉加载、下拉刷新的形式，在点击列表进入详情页面再返回的时候，如果不进行页面缓存，不仅需要重新请求资源（在需要流量付费的场景下简直无法容忍），而且列表页面也回到了最开始的第一条的位置，这时如果还想紧接上次查看的地方继续往下，就需要不断滑动，直到滑动到上次的位置，当数据量多的时候可能再也回不到上一次查看的位置了。试想一下你们刷今日头条的场景吧。
因此，在移动端开发的时候，需要对页面进行缓存。我们这里采用vue的内置组件[keep-alive](https://cn.vuejs.org/v2/api/#keep-alive)，提供了一种通用的实现页面缓存的方案，当然，也有很多其他的方案，比如[vue-page-stack](https://github.com/hezhongfeng/vue-page-stack/blob/HEAD/README.zh-cn.md), 请开发者根据实际场景自行评估，这里不再赘述。下面将介绍hatom如何用keep-alive组件实现页面缓存:

src/layouts/layout1.vue:

```html
<template>
  <keep-alive :include="whiteList" :exclue="blackList">
    <router-view></router-view>
  </keep-alive>
<template>
<script>
export default {
  data () {
    return {
      whiteList: [],
      blackList: []
    }
  },
  watch: {
     $route: {
        immediate: true,
        handler (newRoute, oldRoute) {
          if (newRoute.meta.cache) {
            this.whiteList = Array.from(new Set([newRoute.name, ...this.whiteList]))
            this.blackList = this.blackList.filter((name) => name !== newRoute.name)
          } else {
            this.whiteList = this.whiteList.filter((name) => name !== newRoute.name)
            this.blackList = Array.from(new Set([newRoute.name, ...this.blackList]))
          }
        }
     }
  }
}
</script>
```

src/router/index.js:

``` javascript
router.beforeEach((to, from, next) => {
  to.meta.cache = to.query.cache || true
  next()
})
```

记录页面位置,src/pages/page1/index.vue:

```html
<template>
  <div class="page1"></div>
</template>
<script>
export default {
  name: 'page1',
  data () {
    return {
      scrollTop: 0
    }  
  },
  beforeRouteLeave (to, from, next) {
    this.scrollTop = document.querySelector('.page1').scrollTop
    next()
  },
  activated () {
    document.querySelector('.page1').scrollTop = this.scrollTop;
  }
}

</script>
```

使用:

``` javascript
this.$router.push({ path: '/page1', query: { cache: true } })

```

<span id="7-2"></span>
### 路由动画
如果想提升用户体验，最好在页面切换的过程中加上过渡动画。同样，我们也提供了一种实现路由动画的的方案，你要做的只是一些简单的配置。在我们的方案中，由浅层级的页面过渡到深层级的页面，采用从右至左的过渡方式，相反，采用从左至右的过渡方案，具体配置如下：

src/router/index.js

``` javascript
// 在meta标签中配置页面层级，如：
{
  path: '/index',
  name: 'index',
  component: Index,
  meta: { deep: 0 }
},
{
  path: '/page1',
  name: 'page1',
  component: Page1,
  meta: { deep: 1 }
}

// 在全局路由守卫中，根据deep,动态设置全局变量$directon
router.before((to, from, next) => {
  Vue.prototype.$direction = to.meta >= from.meta.deep ? 'left' : 'right'
})
```
在使用<router-view>的地方，添加<transition>动画，如在src/App.vue中：

``` html
<template>
  <div id="app">
    <transition :name="$direction"><router-view></router-view></transition>
  </div>
</template>

```

设置动画样式，在src/assets/styles/animation.css中：

``` css
/** 左飞入 */
.left-enter {
  transform: translateX(100%);
}

.left-enter-to {
  transform: translateX(0);
}

.left-enter-active {
  transition: 0.3s;
}

/** 右飞入 */
.right-enter {
  transform: translateX(-100%);
}

.right-enter-to {
  transform: translateX(0);
}

.right-enter-active {
  transition: 0.3s;
}

```

<span id="7-3"></span>
### 公共组件
全局新增公共组件请放置于src/components/下，采用kebab-case（短横线命名），组件结构采用统一的形式，并在src/components/index.js文件中进行注册。eg:

tabbar组件

组件结构:

``` bash
├── i-tabbar ························ tabbar组件文件夹 
│   ├── index.js ···················· install方法
│   └── src ························· 组件业务逻辑文件夹
│       └── i-tabbar.vue ············ 组件业务逻辑
```
i-tabbar.vue:

``` html
<template>
  <div class="i-tabbar">
    ...
  </div>
</template>
<script>
export default {
  name: 'ITabbar',
  data () {
     return {}
  },
  ...
}
</script>
<style lang="scss" scoped>
.i-tabbar {
  /* ... */
}
</style>
```
index.vue:

``` javascript
import ITabbar from './src/i-tabbar.vue'
ITabbar.install = (Vue) => {
  Vue.component(ITabbar.name, ITabbar)
}
export default ITabbar
```

最后在src/components/index.js文件中进行注册:

``` javascript
import ITabbar from './i-tabbar/index.js'
const components = [  
  ITabbar
]
```
使用:

``` html
<i-tabbar></itabbar>

```

<span id="7-4"></span>
### 全局方法、全局正则
全局方法、全局正则可以分别添加于src/components/utils/util.js文件和src/components/utils/reg文件中，这样，在任意vue文件中即可通过this.$+方法名/正则名直接调用。eg:

使用:

``` javascript
mounted () {
  this.$isMobile()
  this.$EMAIL_TEST('support.hikyun@hikvision.com')
}

```

<span id="7-5"></span>
### 全局过滤器 
在src/filters/filter.js中可以注册vue全局过滤器，spa-tpl模板中，使用[dayjs(2KB)](https://www.npmjs.com/package/dayjs)默认添加了timeFormat时间格式转换，将时间格式转换为YYYY-MM-DD HH:mm:ss形式。eg:

使用:

``` html 
<template>
  <div class="time">{{ new Date() | timeFormat }}</div>
</template>

```

<span id="7-6"></span>
### 布局
应用中通用布局可以放置于src/layouts文件夹中，再在src/router.js路由配置中通过子路由的形式使用添加好的布局，从而提高代码的复用，spa-tpl模板提供了两种布局，layout1常用的导航栏+内容+tabbar布局，layout2为导航栏+内容布局。eg:


src/router/index.js:

``` javascript
import Layout1 from '@/src/layouts/layout1'
import Page1 from '@/src/page/page1/index'

staticRoutes = [
  {
    path: '/page1',
    name: 'layout1',
    component: Layout1,
    redirect: '/page1',
    children: [
      {
        path: 'page1',
        name: 'page1',
        component: Page1
      }
    ]
  }
]

```

<span id="7-7"></span>
<span id="7-7-1"></span>
### 业务配置
在src/config目录中，可以进行一些全局变量的配置：

* api.js 配置接口地址，如在api.js配置 BAIDU:'https://www.baidu.com', 可以在任意vue文件中通过`this.$BAIDU`引用

* constant.js 配置全局常量,如配置SHEIGHT:screen.height，通过`this.SHEIGHT`引用，建议常量使用大写字母命名

* http.js axios全局拦截器，可以在`request.interceptors.request`和`request.interceptors.response`进行相关业务的配置，如鉴权方面的操作等

* webApp.json 是app的相关设置，一般在脚手架生成项目时与package.json保持一致，但也可以手动进行设置，相关参数如下：

|  参数   | 说明  | 类型  | 默认配置  |
|  ----  | ----  | ----  | ----  |
| h5packCode | 包名，在同一个APP中要保持唯一性，不然会影响当前 H5应用和其他相同code的H5应用 | String | - |
| versionName  | 版本号 | String | 1.0.0 |
| author  | 作者 | String | support.hikyun@hikvision.com |
| description  | 描述 | String | A hatom project |
| updateTime  | 单元格 | String  | 项目创建时间 |
| androidMinNativeVersion  | 当前 H5包支持的当前 App 的最低版本号，如在社区APP中使用的H5包配置为2.0.0,则表示当前 H5只兼容2.0.0版本以上的 APP，低于2.0.0的不兼容 | Sting | 1.0.0 |
| iOSMinNativeVersion  | 同上 | String | 1.0.0 |
| whiteList  | H5资源白名单, hatom框架对H5资源包加载的网络请求拦截的白名单，也可不做配置 | Array | ["file:///*","*://127.0.0.1","*.hikyun.com",] |
| url  | 应用远程地址，""为本地加载 | String |   |
| componentId  | H5接收消息推送的类型集合，如配置为 [alarm, device]则表示在接收到类型表示为 alarm 和 device 的消息后，APP 会将消息转发给 当前 H5应用 | Array | ["componentId1", "componentId2"] |
| menuList | 门户组件菜单配置 | Array | [] |
| ext  | 拓展字段 | Object | {} |

<br />
<span id="7-7-2"></span>
### 多页面说明
在src/core.js目录中，多页面的配置：
* pageRouter.json 是app多页面的相关配置，app打包编译H5资源包时，会解析该文件注册多个webview。
同时工程运行时，也会解析该文件，生成多页面入口。
 相关参数如下：

|  参数   | 说明  | 类型  | 默认配置  |
|  ----  | ----  | ----  | ----  |
| routes | 路由列表| Array | [ { ...options } ] |

<br />

options说明, 每一个options对应一个入口页面，相关参数如下：

|  参数   | 说明  | 类型  | 默认配置  |
|  ----  | ----  | ----  | ----  |
| type | 页面类型分为三种：普通类型(standard)、顶部标题栏(topbar)、底部导航栏(bottomNavigation$$portal$$0)| String | standard  |
| name | 页面名| String | - |
| path | 页面入口相对路径| String | - |
| data | 页面配置数据（普通类型不需要进行配置）| Array | { ...opts } |

<br />

opts说明, 每一个type类型对应一个opts页面配置，可根据当前页面嵌入的场景进行配置，相关参数如下：
|  参数   | 说明  | 类型  | 默认配置  |
|  ----  | ----  | ----  | ----  |
| topbar | 页面类型为顶部标题栏(topbar) 配置| Object  |  -  |
| bottomNavigation | 页面类型为底部导航栏(bottomNavigation$$portal$$0)底部菜单配置| Object | - |

topbar 配置示例

```
"topbar": {
  /** 顶部左侧按钮 */
  "leftButton": {
    "type": "text", 
    "textColor": "#FFFFFFFF",
    "text": "返回"
  },
  /** 顶部右侧按钮 */
  "rightButton": {
    "type": "img",
    "img": "icon.png"
  },
  /** 配置顶部标题，只支持文本类型 */
  "title": {
    "type": "text",
    "textColor": "#FFFFFFFF",
    "text": "Page1 Title"
  },
  /** 配置顶部背景色，目前只支持颜色类型 */
  "background": {
    "type": "color",
    "color": "#FFFF0000"
  }
}
```
bottomNavigation$$portal$$0 字段分为三部分，bottomNavigation、portal、0 ，
第一部分固定不变，第二部分表示分组，第三部分表示底部菜单排列位置（从0开始），
根据分组字段，将同一分组根据排列次序在底部进行排布。配置示例：
```
"bottomNavigation": {
  /** 配置菜单文字以及选中/未选中颜色 */
  "title": {
    "textColorSelected": "#FFFFFFFF",
    "textColorUnselected": "#FFFFFFFF",
    "text": "检测"
  },
  /** 配置菜单图标，含选中/未选中状态 */
  "icon": {
    "imgUnselected": "icons/1-实时监测-normol.png",
    "imgSelected": "icons/1-实时监测-hover.png"
  },
  /** 配置菜单背景色 */
  "background": {
    "color": "#FFFF0000"
  }
}
```

<br />
完整实例：

```
{
  "routes": [
    {
      "type": "standard",
      "name": "index",
      "path": "index.html",
      "data": {}
    },
    {
      "type": "topbar",
      "name": "page1",
      "path": "page1.html",
      "data": {
        "topbar": {
          /** 顶部左侧按钮 */
          "leftButton": {
            "type": "text", 
            "textColor": "#FFFFFFFF",
            "text": "返回"
          },
          /** 顶部右侧按钮 */
          "rightButton": {
            "type": "img",
            "img": "icon.png"
          },
          /** 配置顶部标题，只支持文本类型 */
          "title": {
            "type": "text",
            "textColor": "#FFFFFFFF",
            "text": "Page1 Title"
          },
          /** 配置顶部背景色，目前只支持颜色类型 */
          "background": {
            "type": "color",
            "color": "#FFFF0000"
          }
        }
      }
    }
    {
      "type": "bottomNavigation$$portal$$0",
      "name": "page2",
      "path": "page2.html",
      "data": {
        "bottomNavigation": {
          "title": {
            "textColorSelected": "#FFFFFFFF",
            "textColorUnselected": "#FFFFFFFF",
            "text": "检测"
          },
          /** 配置菜单图标，含选中/未选中状态 */
          "icon": {
            "imgUnselected": "icons/1-实时监测-normol.png",
            "imgSelected": "icons/1-实时监测-hover.png"
          },
          /** 配置菜单背景色 */
            "background": {
              "color": "#FFFF0000"
            }
          }
        }
      }
    },
    {
      "type": "bottomNavigation$$portal$$1",
      "name": "page5",
      "path": "page5.html",
      "data": {
        ...
      }
    },
    {
      "type": "bottomNavigation$$portal$$2",
      "name": "page6",
      "path": "page6.html",
        "data": {
          ...
        }
    },
  ]
}
```

<span id="7-8"></span>
### 雪碧图
将一些小图标制作成一张雪碧图，是一个比较好的主意。多亏了[webpack-spritesmith](https://www.npmjs.com/package/webpack-spritesmith)插件，我们在此基础上进行了一些封装和配置，使雪碧图制作和使用非常方便。你需要做的就是：

1、将图标文件例如arrow-left.png拖动到/src/assets/icons文件件内

2、在需要使用的地方引入`<i class="icon-arrow-left></i>`

确实只需要如此简单的两步。hatom会将/src/assets/icons文件夹内的所有文件，制作成雪碧图sprite.png并放置于src/assets/images文件夹内，同事生成相关的定位样式sprite.css放置于src/assets/styles中。

<span id="7-9"></span>
###其他注意事项

#### 路由模式
vue支持hash和history两种模式的路由配置，但基于某些原因，hatom只能支持hash模式的路由配置，否则会达不到预期的结果。

#### 成果物
成果物目录结构:

``` bash
├── index.html ··································· index.html
├── logo.ico ····································· logo.ico
├── pageRouter.json ······························ hatom相关配置
├── static
│   ├── css
│   │   └── main_792f30f7dda223670a32.css ········ css资源
│   └── js
│       ├── main_3161817b.bundle.js ·············· js资源
└── webApp.json ·································· app配置
```

hatom默认将成果物生成名为webapp_ + webApp.h5packCode的zip文件，帮面后续再平台上上传编译，其中webapp_为保留关键字，在编译过程中会使用到，切勿修改。实际上，如果不使用hatom官方脚手架，只需要保持相关的目录结构和配置文件一致也可以正常运行。 


<span id="8"></span>
## 基础插件使用

[相机](#plugin-1)

[二维码扫描](#plugin-2)

[GPS定位](#plugin-3)

[跳转第三方地图](#plugin-4)

[本地存储](#plugin-5)

[获取网路状态](#plugin-6)

[获取设备屏幕信息](#plugin-7)

[设置顶部状态栏](#plugin-8)

[容器操作：退出、返回、清缓存](#plugin-9)

[拨打电话](#plugin-10)

[分享](#plugin-11)

<span id="plugin-1"></span>
### 1.相机

  使用示例：

  ```javascript
    hatom.camera(res => {
      console.log(res.message)
    }, {
      mQuality: '', 
      destType: '',
      srcType: '',
      targetWidth: '',
      targetHeight: '',
      encodingType: '',
      mediaType: '',
      allowEdit: false,
      correctOrientation: false,
      saveToPhotoAlbum: false
    })

  ```

  参数说明：

  | 参数               | 类型  | 必填 | 描述                                                                           |
  | ------------------ | ------ | -------- | ------------------------------------------------------------------------------ |
  | callback           | 函数  | 是 | 回调函数                                                                       |
  | options           | Object | 否 |  参数对象                                |

  <br>
  options 参数说明：
  
  | 参数               | 类型  | 必填 | 描述                                                                           |
  | ------------------ | ------ | -------- | ------------------------------------------------------------------------------ |
  | mQuality           | String | 否 | 图像质量：图像质量在 0~100 内，默认值为 50                                     |
  | destType           | String | 否  | 照片返回格式：0--base64 编码字符串；1--图片文件 URL；2--图片本机 URL。默认为 1 |
  | srcType            | String | 否 | 照片调用位置：0--打开照片库；1--打开本机相机；2--打开已保存的相册。默认为 1    |
  | targetWidth        | String | 否 | 图片缩放宽度（宽和高只有一个的时候是按照等比例进行缩放）                                                                   |
  | targetHeight       | String | 否 | 图片缩放高度（宽和高只有一个的时候是按照等比例进行缩放）                                                                   |
  | encodingType       | String | 否 | 图片返回格式： 0--JPEG 格式图像；1--PNG 格式图像。默认为 0                     |
  | mediaType          | String | 否 | 选择 media 类型。picture/video/allMedia,分别对应 0，1，2，默认为 0             |
  | allowEdit          | Boolean   | 否 | true--允许编辑 false--不允许编辑。默认 false                                   |
  | correctOrientation | Boolean   | 否 | 如果是横向拍摄的照片，会自动旋转到正确的方向，解决部分机型拍照后照片方向问题。默认 false                      |
  | saveToPhotoAlbum   | Boolean  | 否  | false-不保存到图片库中 true-保存到图片库中。默认 false 

  <br>

  返回说明：

  
  | 参数 | 类型   | 描述                               |
  | ----- | ------ | ---------------------------------- |
  | code  | string | 返回码  0表示成功 |
  | message  | string | 返回值  默认图片地址 |

  <br>

<span id="plugin-2"></span>
### 2. 二维码扫描

  使用示例：

  ```javascript
  hatom.scan(res => {
    const message = JSON.parse(res.message)
    console.log(message);
  });
  ```

  参数说明：

  | 参数     | 类型 | 必填 | 描述     |
  | -------- | ---- | ----- | -------- |
  | callback | 函数 | 是 | 回调函数 |

  <br>

  返回参数：

  | 参数 | 类型   | 描述                               |
  | ----- | ------ | ---------------------------------- |
  | code  | string | 返回码  0表示成功 |
  | message  | string | 返回值  json字符串 |

  <br>

  json字符串通过JSON.parse(message)转为对象

  参数如下所示：

  | 参数      | 类型   | 描述                                |
  | --------- | ------ | ----------------------------------- |
  | text      | String | 扫描所获得的信息（文本/链接         |
  | format    | String | 扫描码格式：AZTEC（高级二维码，无扫描方向的限制）、CODABAR（库德巴码）、CODE_39（早期自检的条码，被更现代的Code 93和Code 128代替）、CODE_93（自由长度的代码，93条形码）、CODE_128（现代条码）、DATA_MATRIX（编码文本和数字数据的矩阵二维码）、EAN_8（欧洲标准条形码）、EAN_13（欧洲标准条形码拓展版）、ITF（交叉二五条码）、MAXICODE（美国资讯条码）、PDF_417（堆叠式二维条形码）、QR_CODE（二维码）、RSS_14（RSS线性条码）、UPC_A（12位数字条形码）、UPC_E（6位数字）、UPC_EAN_EXTENSION（美、加、欧盟拓展码） |
  | cancelled | Boolean   | false-取消扫描 true-没有取消扫描    |

  <br>


<span id="plugin-3"></span>
### 3. GPS定位

* getLocation 获取当前定位信息

  使用示例：
   ```javascript
    hatom.locationInfo.getLocation(res => {
      const message = JSON.parse(res.message)
      console.log(message);
    })
  ```
  参数说明：

  | 参数   | 类型 | 必填 | 描述     |
  | -------- | ---- | ----- | -------- |
  | callback | 函数 | 是 | 回调函数 |

  返回说明：

    | 参数 | 类型   | 描述                               |
    | ----- | ------ | ---------------------------------- |
    | code  | string | 返回码  0表示成功 |
    | message  | string | 返回值  json字符串 |

    <br>
    
  json字符串通过JSON.parse(message)转为对象
  
  参数如下所示：

    | 参数      | 类型   | 描述                                |
    | --------- | ------ | ----------------------------------- |
    | latitude      | number | 纬度        |
    | longitude |   number   | 经度    |

    <br>
* getLocationPermission 跳转手机定位权限设置页面

  使用示例：
  ```javascript
    hatom.locationInfo.getLocationPermission()
  ```
  返回说明：

  无

  <br>


* turnOffLocation 关闭手机定位

  使用getLocation获取定位成功之后，可调用该接口关闭定位

  使用示例：
   ```javascript
    hatom.locationInfo.turnOffLocation();
  ```
  返回说明：

  无

  <br>

<span id="plugin-4"></span>
### 4. 跳转第三方地图

  使用示例：
   ```javascript
    const params = {
      coordType: "WGS84",
      latitude: "31.311381",
      longitude: "121.516675"
    };
    hatom.goMapApp(() => {}, params);
  ```
  参数说明：

  | 参数       | 类型  | 必填 | 描述                                   |
  | ---------- | ------ | ----- | -------------------------------------- |
  | callback   | 函数  | 是 | 回调函数                               |
  | options | String | 是 | 坐标类型：CGCS2000、WGS84、GCJ02、BD09 |

  <br>

  options 参数说明：

  | 参数       | 类型  | 必填 | 描述                                   |
  | ---------- | ------ | ----- | -------------------------------------- |
  | coordType | String | 是 | 坐标类型：CGCS2000、WGS84、GCJ02、BD09 |
  | latitude  | String |  是 |经度                                   |
  | longitude | String |是| 纬度                                    |

  <br>


  返回参数

  无

### 5. 本地存储

* setItem 本地存储

  使用示例：

  ```javascript
  const key = "company";
  const value = "xxx";
  /** 传参均为字符串，value可传json字符串 */
  hatom.storage.setItem(key, value);
  ```
  参数说明：

  | 参数  | 类型          | 必填 |              描述              |
  | ----- | -------------- | ------ | :----------------------------: |
  | key   | String        | 是 |      本地缓存中指定的 key      |
  | value | String | 是 | 需要存储的内容,可传json字符串 |

  <br>

  返回参数

  无

* getItem 获取本地缓存

  使用示例：

  ```javascript
    const key = "company";
    hatom.storage.getItem(key, res => {
      // 通过回调函数获取已存储数据
      console.log(res.message);
    });
  ```
  参数说明：

  | 参数 | 类型  | 必填 |         描述         |
  | ---- | ------ | ----- | :------------------: |
  | key  | String | 是 | 本地缓存中指定的 key |

  <br>

  返回参数：

  | 参数 | 类型   | 描述                               |
  | ----- | ------ | ---------------------------------- |
  | code  | String | 返回码  0表示成功 |
  | message  | String | 返回值  |

  <br>

<span id="plugin-6"></span>
### 6. 网络状态
  使用示例：
   ```javascript
  hatom.networkManager(res => {
    /** 根据返回信息message判断当前网络状态 */
    console.log(res.message);
  });
  ```
  参数说明：

  | 参数   | 类型 | 必填 | 描述     |
  | -------- | ---- | ----- | -------- |
  | callback | 函数 | 是 | 回调函数 |

  <br>


  返回说明：

  | 参数 | 类型   | 描述                               |
  | ----- | ------ | ---------------------------------- |
  | code  | string | 返回码  0表示成功 |
  | message  | string | 返回值 枚举值 |

  <br>

  message的枚举值说明：

  | 参数   | 类型   | 描述         |
  | -------- | ------ | ------------ |
  | unknown  | String | 未知连接     |
  | ethernet | String | 以太网连接   |
  | wifi     | String | WiFi 连接    |
  | 2g       | String | 2G 网络      |
  | 3g       | String | 3G 网络      |
  | 4g       | String | 4G 网络      |
  | none     | String | 没有网络连接 |

  <br>

<span id="plugin-7"></span>
### 7. 获取设备屏幕信息
* 异步获取设备屏幕信息

  使用示例：
  ```javascript
  hatom.getScreenInfo(res => {
      const message = JSON.parse(res.message)
      console.log(message);
  })

  ```
  参数说明：

  | 参数   | 类型 | 必填 | 描述     |
  | -------- | ---- | ----- | -------- |
  | callback | 函数 | 是 | 回调函数 |

  <br>


  | 参数 | 类型   | 描述                               |
  | ----- | ------ | ---------------------------------- |
  | code  | String | 返回码  0表示成功 |
  | message  | String | 返回值 json 字符串|

  <br>
  json字符串通过JSON.parse(message)转为对象

  参数说明如下：

  | 参数   | 类型   | 描述         |
  | ---------- | -------- | --------------- |
  | screenDensityDpi  | String | 设备屏幕Dpi，像素密度     |
  | statusBarHeight     | String | 设备状态栏高度    |
  | screenScreenRotation       | String | 设备屏幕是否旋转      |
  | screenDensity       | String | 设备屏幕密度 dpi/px=density      |
  | screenWidth | String | 设备屏幕宽度   |
  | screenHeight       | String | 设备屏幕高度      |
  | appScreenWidth       | String | 应用屏幕宽度      |
  | appScreenHeight       | String | 应用屏幕高度 appScreenHeight=screenHeight-statusBarHeight    |

  <br>

* 同步获取设备屏幕信息，返回promise对象

  使用示例一
  ```javascript
  async getSyncScreenInfo () {
    const res = await hatom.getSyncScreenInfo();
    const screenInfo = JSON.parse(res.message);
    console.log(screenInfo);
  }
  ```
  使用示例二

  ```javascript
  hatom.getSyncScreenInfo().then(res=>{
    const screenInfo = JSON.parse(res.message);
    console.log(screenInfo);
  });
  ```
  参数说明：无

  返回参数： 同上

<span id="plugin-8"></span>
### 8.设置顶部状态栏

  使用示例：
  ```javascript
  hatom.statusBar.setStatusBarMode({
    iconMode: 'dark'
  },
  (res) => {
    console.log(res)
  })
  ```
  参数说明：

  | 参数   | 类型 | 必填 | 描述     |
  | -------- | ---- | ----- | -------- |
  | iconMode | string | 是 | 状态栏模式， dark模式， light模式  |

  <br>

  返回说明：

  无

<span id="plugin-9"></span>
 ### 9. 容器操作说明

* 退出容器 单页面应用中，即为退出应用， 多页面则为退出该webview 容器

  使用示例：
  ```javascript
  hatom.page.exit();
  ```
  参数说明：

  | 参数   | 类型 | 必填 | 描述     |
  | -------- | ---- | ----- | -------- |
  | callback | 函数 | 否 | 回调函数 |

  <br>


  返回说明：

  无

* 返回上一步

  使用示例：
  ```javascript
  hatom.page.back();
  ```
  参数说明：

  | 参数   | 类型 | 必填 | 描述     |
  | -------- | ---- | ----- | -------- |
  | callback | 函数 | 否 | 回调函数 |

  <br>
  返回说明：

  无


* 清除缓存 清除该容器的缓存

  使用示例：
  ```javascript
  hatom.page.cleanCache();
  ```
  参数说明：

  | 参数   | 类型 | 必填 | 描述     |
  | -------- | ---- | ----- | -------- |
  | callback | 函数 | 否 | 回调函数 |

  <br>

  返回说明：

  无

<span id="plugin-10"></span>
 ### 10. 拨打电话

  使用示例：
  ```javascript
  hatom.phoneCall(res => {
    // 通话情况
  }, {
    phoneNumber: "XXX"
  });

  ```
  参数说明

  | 参数   | 类型 | 必填 | 描述     |
  | -------- | ---- | ----- | -------- |
  | callback | 函数 | 否 | 回调函数 |
  | options | Object | 是 | 传入的参数 |

  <br>

  options 说明：

  | 参数   | 类型 | 必填 | 描述     |
  | -------- | ---- | ----- | -------- |
  | phoneNumber | String | 是 | 电话号码 |

  <br>

  返回说明:

  | 参数 | 类型   | 描述                               |
  | ----- | ------ | ---------------------------------- |
  | code  | String | 返回码  0表示成功 |
  | message  | String | 返回的信息文本说明， "success" 表示成功  |

  <br>

<span id="plugin-11"></span>
  ### 11.分享

  * 分享文本
    使用示例:
    ```javascript
      hatom.shareText((res) => {
        // 分享结果
      },
      {
        text： "分享的文本"
      })
    ```
    参数说明：
  
    | 参数   | 类型 | 必填 | 描述     |
    | -------- | ---- | ----- | -------- |
    | callback | 函数 | 否 | 回调函数 |
    | options | Object | 是 | 传入的参数 |

    <br>


    options 说明：
  
    | 参数   | 类型 | 必填 | 描述     |
    | -------- | ---- | ----- | -------- |
    | text： | String | 是 | 分享的文本 |

    <br>

    返回说明：

    | 参数 | 类型   | 描述                               |
    | ----- | ------ | ---------------------------------- |
    | code  | String | 返回码  0表示成功 |
    | message  | String | 返回的信息文本说明， "success" 表示成功  |

    <br>


  * 分享图片
    使用示例:
    ```javascript
      hatom.sharePic((res) => {
        // 分享结果
      },
      {
        pic "分享的base64图片"
      })
    ```
    参数说明：
  
    | 参数   | 类型 | 必填 | 描述     |
    | -------- | ---- | ----- | -------- |
    | callback | 函数 | 否 | 回调函数 |
    | options | Object | 是 | 传入的参数 |

    <br>


    options 说明：
  
    | 参数   | 类型 | 必填 | 描述     |
    | -------- | ---- | ----- | -------- |
    | pic | String | 是 | 图片base64字符串 |

    <br>


    返回说明：

    | 参数 | 类型   | 描述                               |
    | ----- | ------ | ---------------------------------- |
    | code  | String | 返回码  0表示成功 |
    | message  | String | 返回的信息文本说明， "success" 表示成功  |

    <br>

<span id="9"></span>
## 高级插件使用

[登录](#h-plugin-1)

[多页面跳转](#h-plugin-2)

[生命周期](#h-plugin-3)

[原生消息](#h-plugin-4)

[顶部标题栏](#h-plugin-5)

[底部标题栏](#h-plugin-6)



<span id="h-plugin-1"></span>
### 1.登录

* 获取登录信息

  对接云曜、ifar构架，与登录组件配合使用，用于登录之后获取登录相关信息，包括服务器地址、用户名、token 等信息。

  使用示例：

  ```javascript
  hatom.rootInfo.getRootInfo(res => {
    const data = JSON.parse(res.message);
    console.log(data);
  });
  ```

  参数说明：

    | 参数               | 类型  | 必填 | 描述                                                                           |
    | ------------------ | ------ | -------- | ------------------------------------------------------------------------------ |
    | callback           | 函数  | 是 | 回调函数                                                                       |

    <br>

  返回说明：

    | 参数 | 类型   | 描述                               |
    | ----- | ------ | ---------------------------------- |
    | code  | string | 返回码  0表示成功 |
    | message  | string | 返回值  json字符串 |

  <br />
  json字符串通过JSON.parse(message)转为对象，转化后的对象参数如下所示：

  | 参数          | 类型   | 描述                                |
  | ------------- | ------ | ----------------------------------- |
  | address       | String | 平台地址，例如：https://10.2.145.82 |
  | routeData     | String | 路由参数，内部路由跳转传参，具体值可自定                  |
  | routeType     | int | 路由形式，根据这个值来做内部路由的跳转，具体值可自定                  |
  | token         | String | token                               |

  <br />

> 注意事项： 其余字段可扩展。

* 跳转到登录页

  使用示例:

  ```javascript
  hatom.rootInfo.redirectLogin();
  ```
  返回说明：

  无

<span id="h-plugin-2"></span>

### 2.多页面跳转

* 跳转到新的页面

  使用示例：
  ```javascript
  /** pageName为跳转页面名称 */
  const pageName = 'page1.html'
  const data = {
  params: {
      'page': pageName
  },
  target: `html:hatom://${pageName}`
  };
  /** 跳转到page1.html */
  hatom.page.pushPage(data);
  ```
  参数说明：

  | 参数   | 类型 | 必填 | 描述     |
  | -------- | ---- | ----- | -------- |
  | params | Object | 是 | 跳转页面参数， 包含页面名称 |
  | target | String | 是 | 这个字段中的 hatom 要与 webApp.json 文件中的 h5packCode 保持一致 |

  <br />

  params参数说明：
  | 参数   | 类型 | 必填 | 描述     |
  | -------- | ---- | ----- | -------- |
  | page | Object | 是 | 页面名称 |

  <br />

  > 注意事项： 其余字段可扩展。

  <br />

* 跳转回已经打开过的页面 

   使用示例：
   ```javascript
  /** pageName为跳转页面名称 */
  const pageName = 'page2.html'
  const data = {
  params: {
      'page': pageName
  },
  target: `html:hatom://${pageName}`
  };
  /** 跳转回到page2.html */
  hatom.page.popPage(data);
   ```
  参数说明：

    同 pushPage 

<br />

<span id="h-plugin-3"></span>

### 3.页面生命周期

<br />

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;原生打开前端页面会有一个生命周期：onStart、onStop、onDestroyView

<br />

* onStart
  主要用于刚进入页面需要执行的操作，由于首次进入页面的时候，页面刚打开的时候 onStart 事件还未注册，因此调用不到，但可以用 Vue 的生命周期函数进行规避。举例应用场景：A 页面注册 onStart 事件--->跳转到 B 页面---->在 B 页面进行操作(对 A 页面有影响)---->返回 A 页面---->(此时 A 页面需要执行一些操作)可在 onStart 事件进行处理。
  <br />
  使用示例：
  ```javascript
  hatom.setBridge("onStart", res => {
    // 执行onStart回调
  });
  ```
  参数说明：
  | 参数   | 类型 | 必填 | 描述     |
  | -------- | ---- | ----- | -------- |
  | onStart | String | 是 | 事件名称，固定值：onStart |
  | callback | Function | 是 | 回调函数 |

<br />

* onStop
  页面隐藏不可见时会触发该生命周期函数。举例应用场景：A 页面注册 onStop 事件---->(即将跳转 B 页面)执行 onStop 事件----->跳转到 B 页面。
  使用示例：
  ```javascript
  hatom.setBridge("onStop", () => {
    // 执行onStop回调
  });
  ```
  参数说明：
  | 参数   | 类型 | 必填 | 描述     |
  | -------- | ---- | ----- | -------- |
  | onStop | String | 是 | 事件名称，固定值：onStop |
  | callback | Function | 是 | 回调函数 |

<br />

* onDestroyView
  页面销毁时，页面销毁时需要进行资源的回收，类似消息推送等。

  使用示例：
  ```javascript
  hatom.setBridge("onDestroyView", () => {
    // 执行onDestroyView回调，进行资源释放
  });
  ```
  参数说明：
  | 参数   | 类型 | 必填 | 描述     |
  | -------- | ---- | ----- | -------- |
  | onDestroyView | String | 是 | 事件名称，固定值：onDestroyView |
  | callback | Function | 是 | 回调函数 |

<span id="h-plugin-4"></span>

### 4.消息通知

* setBridge 注册原生消息

  使用实例：
  ```javascript
  /** 
   * 向原生端注册一个方法，供原生消息调用
   * 以onBackPressed为例子，注册一个onBackPressed方法用于监听安卓虚拟返回键
   */
  hatom.setBridge("onBackPressed", res => {
    // 在此处处理消息通知
    hatom.page.back()
  });
  ```
  参数说明：
  | 参数   | 类型 | 必填 | 描述     |
  | -------- | ---- | ----- | -------- |
  | funcName | String | 是 | 事件名称，作为消息通道，名称唯一，重复则会覆盖原有的消息通道 |
  | callback | Function | 是 | 回调函数 |

<br />

* startMessage 开启消息通知

  使用示例：
  ```javascript
  /**
   * 注册消息通道
   * 在开启消息通知之前提需注册一个方法作为消息通道，供原生消息调用
   * 以getMessage为例子，注册一个getMessage方法用于处理接收消息
   * 为保证消息通道唯一 可以传参为 随机数 + '.' + 前端注册方法名
   */
  const timestmap = +new Date();
  hatom.setBridge(`${timestamp}.getMessage`, res => {
    // 在此处处理消息通知
    console.log("----getMessage方法回调-----");
  });
  /** 开启消息通知
   *  将参数传给原生端，然后原生接受到消息就会调用getMessage方法，
   *  前端通过getMessage处理消息就可以 
   */
  const data = {
      message: `${timestamp}.getMessage`
  };
  hatom.message.startMessage(
    res => {
        console.log(res.message);
    },
    data
  );
  ```
  参数说明:
  | 参数   | 类型 | 必填 | 描述     |
  | -------- | ---- | ------ | -------- |
  | callback | 函数  | 是 | 回调函数 |
  | data | Object  | 是 | 注册的消息通道 |  

  <br />
  data说明：

  | 参数   | 类型 | 必填 | 描述     |
  | -------- | ---- | ------ | -------- |
  | message | String  | 是 | 与之前setBridge注册的事件名称保持一致 |


* stopMessage 停止接收消息

  使用示例：
  ```javascript
  const data = {
    message: `${timestamp}.getMessage`
  };
  //关闭消息通知
  hatom.message.stopMessage(res => {
    console.log(res.message);
  }, data);
  ```

  参数说明:
  | 参数   | 类型 | 必填 | 描述     |
  | -------- | ---- | ------ | -------- |
  | callback | 函数  | 是 | 回调函数 |
  | data | Object  | 是 | 注册的消息通道 |

  <br />
  data说明：

  | 参数   | 类型 | 必填 | 描述     |
  | -------- | ---- | ------ | -------- |
  | message | String  | 是 | 与之前setBridge注册的事件名称保持一致 |

<span id="h-plugin-5"></span>

### 5.顶部标题栏

顶部标题栏除了在 pageRouter.json 进行初始化配置外，在前端页面，也能通过调用插件的方式进行修改调整。

| 接口                 | 描述                       |
| -------------------- | -------------------------- |
| setTopBarLeftButton  | 配置顶部标题栏左侧按钮     |
| setTopBarRightButton | 配置顶部标题栏右侧按钮     |
| setTopBarTitle       | 设置顶部 title             |
| setTopBarBackground  | 设置背景颜色               |
| leftButtonOnClick    | 顶部标题栏左侧按钮点击事件 |
| rightButtonOnClick   | 顶部标题栏右侧按钮点击事件 |

* setTopBarLeftButton

  使用示例：

  ```javascript
  const params1 = {
    type: "img",
    img: "icons/arrow_left.png" // 相对根目录位置
  };
  hatom.topBar.setTopBarLeftButton(res => {}, params1);
  ```
* setTopBarRightButton

  使用示例：
  ```javascript
  const params2 = {
    type: "img",
    img: "icons/logo.png" // 相对根目录位置
  };
  hatom.topBar.setTopBarRightButton(res => {}, params2);
  ```
* setTopBarTitle

  使用示例：
  ```javascript
  const params3 = {
    type: "text",
    textColor: "#00ffd5",
    text: "重新设置的TITLE"
  };
  hatom.topBar.setTopBarTitle(res => {}, params3);
  ```
* setTopBarBackground

  使用示例：
  ```javascript
  const params4 = {
    type: "color",
    color: "#cccccc"
  };
  hatom.topBar.setTopBarBackground(res => {}, params4);
  ```
* leftButtonOnClick

  使用示例：
  ```javascript
  /** 注册顶部标题栏左侧事件 */
  hatom.setBridge("leftButtonOnClick", res => {
    hatom.page.back();
  });
  ```
* rightButtonOnClick

  使用示例：

  ```javascript
  /** 注册顶部标题栏右侧事件 */
  hatom.setBridge("rightButtonOnClick", res => {
    alert("点击Home页面右侧按钮");
    console.log("rightButton");
  });
  ```

<span id="h-plugin-6"></span>

### 6.底部菜单栏

底部导航栏与顶部标题栏一样，需要在 pageRouter.json 进行初始化配置，在前端页面也可以对底部导航栏进行修改配置。

| 接口               | 描  述                                                                         |
| ------------- | ---------------------------------------------------------------------------- |
| setItemConfig | 配置底部导航栏：包括背景色、文字（选中/未选中颜色配置）、图标（选中/未选中） |
| selectItem    | 切换底部菜单 tab                                                             |
| selectItem    | 切换底部菜单 tab                                                             |
| setBadge      | 设置badge 数字                                                              |

<br />

* 配置底部导航栏

  使用示例：
  ```javascript
  const params = {
    position: 0,
    bottomNavigation: {
      title: {
        textColorSelected: "#FFFFFFFF",
        textColorUnselected: "#FFFFFFFF",
        text: "PAGE2"
      },
      icon: {
        imgUnselected: "icons/logo.png",
        imgSelected: "icons/logo.png"
      },
      background: {
        color: "#FFFF0000"
      }
    }
  };
  hatom.bottomBar.setItemConfig(res => {}, params);
  ```

* 切换底部菜单 tab

  使用示例：
  ```javascript
  // 传入要切换的菜单tab在底部栏的序号，例如：1
  const params = {
    position: 1
  };
  hatom.bottomBar.selectItem(res => {}, params);
  ```

* 设置 badge 数字

  使用示例：
  ```javascript
  // 传参position为要设置菜单tab的序号，number为要设置badge数字
  const params = {
    position: 0,
    number: 10
  };
  hatom.bottomBar.setBadge(res => {
    // alert(res);
  }, params);
  ```

### 7.其他插件

更多业务插件见[hatom 平台组件市场](https://hatom2.hikyun.com)，组件详情使用说明文档，可根据业务定制不同的专有组件

[npm-shield]: https://img.shields.io/badge/npm-10.12.0-brightgreen
[deps-shield]: https://img.shields.io/badge/dependencies-up%20to%20date-orange
[size-shield]: https://img.shields.io/badge/unpacked%20size-43.6KB-blue