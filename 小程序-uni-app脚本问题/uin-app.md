

### uni-app 自定义基座

- 1、uni-app 转 原生 小程序  预览  H5 页面
- 2、uni-app 框架 解析  小程序 页面 结构

```json
keyAlias: 'android.keystore' 
keyPassword: 'hik_mobile' 
```

 [android.keystore](C:\Users\pengxueyou\Documents\HikLink_Files\pengxueyou\received\android.keystore) 



### 云帆小程序：

##### 嗨通行（访客预约小程序）

```bash
dev："wx46197efdf65d1f93"    平台：http://10.42.1.126/login   cloud_ma Abc123++
prod: "wxeb6ca133a00eedc6"   平台： https://acsc.hikyun.com/login   pt-ma Abc123++
```



##### 嗨通行（访客审批小程序）: appid

```bash
dev："wx46197efdf65d1f93"    平台：http://10.42.1.126/login   cloud_ma Abc123++
prod: "wxeb6ca133a00eedc6"   平台： https://acsc.hikyun.com/login   pt-ma Abc123++
```



##### 模块菜单：

**食堂消费： （H5）**  https://10.17.80.37:3036/mobile-h5/wechat/menu
	1、食堂消费的H5放进海康云帆微信小程序
	2、账户充值、账户记录、分享码、付款码、订餐、送餐、报餐

<img src="C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20231107195313414.png" alt="image-20231107195313414" style="zoom:50%;" />

嵌入h5资源有uni-app 的 web-view组件 配置  [[uni.webview.1.5.5.js](https://gitcode.net/dcloud/hello-uni-app-x/-/blob/alpha/hybrid/html/uni.webview.1.5.5.js)](https://gitcode.net/dcloud/hello-uni-app-x/-/blob/alpha/hybrid/html/uni.webview.1.5.5.js)

```html
    <div class="con-menu">
      <div @click="gotoPage('/wechat/accountPrepaid')">
        <div class="img-box"><img src="@/assets/images/btn_cz.png" srcset="../../assets/images/btn_cz@2x.png 2x,
              ../../assets/images/btn_cz@3x.png 3x" alt="prepaid.png" />
        </div>
        <div>账户充值</div>
      </div>
      <div @click="gotoPage('/wechat/accountRecord')">
        <div class="img-box"><img src="@/assets/images/btn_jl.png" srcset="../../assets/images/btn_jl@2x.png 2x,
              ../../assets/images/btn_jl@3x.png 3x" alt="record.ong" />
        </div>
        <div>账户记录</div>
      </div>
      <div @click="handleQrCode">
        <div class="img-box"><img src="@/assets/images/btn_fx.png" srcset="../../assets/images/btn_fx@2x.png 2x,
              ../../assets/images/btn_fx@3x.png 3x" alt="qrcode.png" />
        </div>
        <div>分享码</div>
      </div>
      <div @click="gotoPage('/qrcode')">
        <div class="img-box"><img src="@/assets/images/icon_fkm_wx.png" srcset="../../assets/images/icon_fkm_wx@2x.png 2x,
              ../../assets/images/icon_fkm_wx@3x.png 3x" alt="付款码icon" />
        </div>
        <div>付款码</div>
      </div>
      <div v-show="basicData.hasComcsAuth" @click="gotoPage('/order/home')">
        <div class="img-box"><img src="@/assets/images/icon_order.png" srcset="../../assets/images/icon_order@2x.png 2x,
              ../../assets/images/icon_order@3x.png 3x" alt="订餐icon" />
        </div>
        <div>订餐</div>
      </div>
      <div v-show="basicData.hasComcsAuth && basicData.isDeliver" @click="gotoPage('/delivery/home')">
        <div class="img-box"><img src="@/assets/images/icon_delivery.png" srcset="../../assets/images/icon_delivery@2x.png 2x,      ../../assets/images/icon_delivery@3x.png 3x" alt="送餐icon" />
        </div>
        <div>送餐</div>
      </div>
      <div v-show="showBcOrder" @click="gotoPage('/reserve/reportmeal')">
        <div class="img-box"><img :src="bcOrder" alt="报餐icon" /></div>
        <div>报餐</div>
      </div>
      <div v-show="showAdminBcOrder" @click="gotoPage('/reserve/adreportmeal')">
        <div class="img-box"><img :src="adminBcOrder" alt="管理员报餐icon" /></div>
        <div>管理员报餐</div>
      </div>
    </div>
```



**门禁：** 
	1、门禁通行二维码：可复用“嗨通行”中已实现的“通行二维码”

<img src="C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20231107194811814.png" alt="image-20231107194811814" style="zoom:50%;" /><img src="C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20231107194840947.png" alt="image-20231107194840947" style="zoom:50%;" />

此处有一个H5连接， 实现url中点击页面的弹窗动作

​	2、远程开门：可复用“嗨通行”中已实现的“云门禁”

```js
// 云门禁
if (type === 'cloudAccess') {
    this.tui.webView.navigateTo({
       url: `/pages/staff/cloud-access/index?sessionId=${localStorage.getItem('staffSessionId')}`
    })
    return
}
```

​	反向加载到H5连接	

**考勤：**
	1、考勤统计：可复用“嗨通行”中已实现的“出勤统计”

```js
 // 出勤统计
  if (type === 'attendanceStatistics') {
    this.tui.webView.navigateTo({
      url: `/pages/attendance/checkIn?tab=statics&sessionId=${localStorage.getItem('staffSessionId')}`
    })
    return
  }
```

​	反向加载到H5连接	

2、考勤打卡：可复用“嗨通行”中已实现的“考勤打卡”

```js
 // 考勤打卡
  if (type === 'attendanceCard') {
    this.tui.webView.navigateTo({
      url: `/pages/attendance/checkIn?tab=checkIn&sessionId=${localStorage.getItem('staffSessionId')}`
    })
    return
  }
```
​	反向加载到H5连接	

**对讲：**
	1、半屏跳转云对讲小程序
	2、https://help.hikyun.com/document/1691979475200717/1691979488027625/0

```javascript
// 半屏跳转的API
wx.openEmbeddedMiniProgram({
      appId: "wxc1d1be0f868d5c6c", // appId
      path: "/pages/live-player/live-player",  // 页面路由
      envVersion: "trial",
      verify: "unionProduct",
      success(res){
        console.log(res);
      },
      fail(err){
        console.log(err)
      }
    })

```



**视频：**
	1.监控点列表（注：c端用户接口、参考嗨通行）

```
H5 未找到监控点列表  可能需要原生开发
```

​	2.预览回放：第一个版本使用萤石小程序半屏跳转方式实现

```bash
wx.openEmbeddedMiniProgram({
      appId: "wxc1d1be0f868d5c6c", // appId
      path: "/pages/live-player/live-player",  // 页面路由
      envVersion: "trial",
      verify: "unionProduct",
      success(res){
        console.log(res);
      },
      fail(err){
        console.log(err)
      }
    })
```



1、uni-tpl 脚手架  在 vue/cli 中

2、手动合并脚手架tpl

3、打包插件 @dcloudio/uni-mp-weixin

4、webpack 源码分析

5、分包插件 SplitChunksPlugin

6、webpack-bundle-analyzer

```
webpack-bundle-analyzer
```















蜀 黔 秦 台 陇 滇 新 港  澳

浙AAM1234 浙AF82804 浙A98AM2

```javascript



```



