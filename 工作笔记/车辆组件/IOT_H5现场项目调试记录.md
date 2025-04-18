## IOT_H5现场项目调试记录

- 总部本地调试手机：
  型号： 华为 ATU-AL0

  开机密码： 124341

### Iot本地调试信息

调试服务地址：10.41.4.66   账号密码：admin/Abc12345

地图经纬度中心点设置：115.86603  28.4487341    地图区域范围经纬度：111.86603    27.525687    117.931525    29.550017

hgis-web后端管理地址： https://10.41.4.66/hgis-services/conf/index.html#/     （hgis-web）

地图调试参数：

http://111.75.227.156:19010/arcgis/rest/services/JXMAP_NEW/MapServer

http://111.75.227.156:19010/arcgis/rest/services/JXMAP_NEW/MapServer/tile/3/176/838

// let imgStr = "https://10.41.4.66/ngx/proxy?i=" + base64.encode(`${mapIp}/tile/{z}/{x}/{y}.png`);

// let mapIp = "http://111.75.227.156:19010/arcgis/rest/services/JXMAP_NEW/MapServer";

```json
{
    center: "115.86603,28.4487341",
    enableVtMap: false,
    extent: "111.86603,27.525687,117.931525,29.550017",
    factor: 0,
    imageFormat: "png",
    imgUrl: "http://111.75.227.156:19010/arcgis/rest/services/JXMAP_NEW/MapServer",
    imgUrl_w: "",
    imgUrl_ww: "",
    initLevel: 4,
    mapType: "ArcGISMap_on",
    maxLevel: 9,
    minLevel: 0,
    mixedUrl: "",
    offMap: false,
    resolutions: [0.010986328383069278, 0.005493164191534639, 0.0027465820957673194, 0.0013732910478836597,…],
    srid: 4326,
    tfwUrl: "",
    tileOrigin: "-180.0,90.0",
    tileSize: 256,
    vecUrl: "http://111.75.227.156:19010/arcgis/rest/services/JXMAP_NEW/MapServer",
    vecUrl_w: "",
    vecUrl_ww: "",
    vtMatrixStatus: "none"
}
```



### 江西交通集团Iot调试信息

项目技术支持： 万振辉

管理系统后端地址：[https://59.63.158.26:446/portal/](https://moa.hikvision.com/pcim/1.2.14/conversation?rnd=1611218985347#)

服务调试IP地址：59.63.158.26.446

账号密码：admin    Gtjt@12328

地图经纬度中心点：118.10415153979261    27.321992355276784     

地图区域经纬度范围：109.76098430945025    24.071172729111456    122.44731868913497   30.57281198144211

调试参数记录：

http://111.75.227.156:19010/arcgis/rest/services/JXMAP_NEW/MapServer/tile/14/365493/1730161

http://111.75.227.156:19010/arcgis/rest/services/JXMAP_NEW/MapServer/tile/9/11223/54149
http://111.75.227.156:19010/arcgis/rest/services/JXMAP_NEW/MapServer/tile/10/22448/108302



### 乌克兰项目地图翻译：

项目经理： 刘伟21   APP原生端：董业军

中英文字段你翻译平台：http://highway.hikvision.com/#/multilingual-management/StringManage

总部185测试环境 平台： https://10.19.166.185/portal/ hikadmin/Abc123++ 

运管： http://10.19.166.185:8001/center/ hikadmin/Abc123++ 

平台服务器： 服务器1/16核/64G: 10.19.166.185 55555 root/HCM123++

调试账号二： 

IP：10.19.166.183
hikadmin/Abc12345



### 青海西宁项目车辆布控

项目现场支持：祁万龙

问题反馈：

1、手机要有报警功能，对已布控的人和车；（客户端整改）

2、车辆布控时，要实现将报警推给布控人员；（客户端整改）

3、车辆布控时，选择布控人员时需要有搜索栏或者手动输入功能，目前没有，市局3000+多用户，翻起来比较困难；（H5端添加分页）

4、车辆查询是，将所属地改成“青”，现在默认“浙” （H5端修改默认参数）

采用本地调试服务地址：10.41.4.66   账号密码：admin/Abc12345



### iot_2.0_组件调试信息

- 接口地址： https://10.17.70.103   admin/Abc12345    

  运营： https://10.17.70.103:8001/center  sysadmin/Abc12345+  

  平台： https://10.17.70.103/portal/ admin/12345

  金仓：10.19.177.109:54321 kingbase/kingbase

  大数据：10.17.70.117/115/113

  后台ssh端口22， root/ga@hik123

- 接口地址：https://10.19.177.56    admin/Abc12345





### ifar 架构调试信息 

 1.6版本测试演示环境：10.19.189.38

账号密码: ys /Abc12345

2.0版本测试演示环境 https://10.19.189.124/  账号密码: ys /Abc12345



阿联酋Ajman警局平安城市

10.66.163.143 admin/shajia@123++



### iSee构架调试信息：

测试环境：10.4.67.200
账号密码：admin/Abc123+++

 **10.19.223.31**    ys/Abc123++



#### 通用调试网络

无线网名称：HIK-Office

密码：HIKhik@2017

#### 小程序调试环境

hikyun@aliyun.com/Hikyun~!@345

hikyunplayer@163.com/Abc12345



#### 2021年Q4升级的调试环境

iFar调试环境：10.41.6.163 admin@Abc12345

2.0 调试环境 10.19.189.124 ys/Abc12345

2.1 调试环境：https://10.33.65.205  admin/Abc123++

3.0 调试环境   10.19.177.77   admin   Abc12345

- 1.6版本测试演示环境：https://10.19.189.38  账号密码: ys /Abc12345

- 2.0版本测试演示环境 https://10.19.189.124/  账号密码: ys /Abc12345



车辆详情接口数据解析错误

10.196.1.62   admin/Hik12345    1. 6-jsBridge

ys_pvia/Abc12345 10.19.189.135

10.196.1.62  admin Hik12345

10.17.70.105

移动应用开发平台 管理员账号：hiksa hiksa-12345



如果你们那边能规避掉合规那边的需求，可以找移动端这边取消掉这个限制的
