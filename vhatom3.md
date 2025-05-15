```javascript
vhatom3.0.1补丁需求
1、组件编辑页字段 组件构架字段  与  tag标签 字段  // OK
2、用户管理 域账号审核 total 字段               // OK
3、外部用户，我的组件、我的模板列表的授权
4、横屏启动页的回显逻辑                        
5、总览里面的 跳转 旧平台 跳不了                // OK
6、帮助文档路由链接                            // OK
7、开发者与管理员路由共享
8、启动页的屏幕分辨率                         // OK
   



vhatom3.1版本
1、应用配置页面， 门户模板中的配置项， 实时预览采用iframe



```

```bash
cross-env VUE_APP_ENV=test node inquirer.js && cross-env NODE_ENV=development UNI_PLATFORM=mp-weixin vue-cli-service uni-build --watch --mode test

cross-env VUE_APP_ENV=master node inquirer.js && cross-env NODE_ENV=production UNI_PLATFORM=mp-weixin vue-cli-service uni-build --mode master
```



```json
{
    "code": "0",
    "msg": "successful",
    "data": {
        "pluginId": "webapp-bms",
        "name": "车辆查询",
        "category": 1,
        "describe": "智能应用平台配套手机客户端中集成的H5组件——车辆查询功能",
        "preImage": "http://10.2.145.31:9000/online-static/plugins/webapp-bms_202211300247_4109/1669789401957_89eb41bb-6a17-1283-5645-e588e1c18bbb_1080x1920.png;http://10.2.145.31:9000/online-static/plugins/webapp-bms_202211300247_4109/1669789415154_0a5d5e96-8a89-45af-5950-227c26bfe8a5_1080x1920.png",
        "example": "",
        "tags": "云远(iFar);车辆;过车查询",
        "userId": "669278507233424",
        "versionCode": "3.0.11-SNAPSHOT",
        "readme": "",
        "platformType": 3,
        "dependencyPath": "webapp-bms",
        "requirementsGathering": "",
        "operatingGuide": "",
        "problemFeedback": "",
        "maintainer": "朋学友",
        "pluginType": 0,
        "parentPluginId": "",
        "hardwareAble": 0,
        "pluginFramework": 2,
        "uploadType": 2,
        "applicablePlatform": "1;2;3",
        "configJson": "[]",
        "achievePackage": "",
        "descProfile": "",
        "id": "webapp-bms_202211300247_4109",
        "publisher": "pengxueyou",
        "createTime": "2022-11-30 14:47:36",
        "updateTime": "2023-09-08 16:52:55",
        "publishTime": "",
        "recommendations": 0,
        "like": 0,
        "references": "",
        "isDelete": false,
        "pluginVersionInfoList": [
            {
                "versionCode": "3.0.11-SNAPSHOT",
                "describe": "升级",
                "status": 0,
                "pluginVersionId": 2484,
                "pluginId": "webapp-bms_202211300247_4109",
                "category": 1,
                "configJson": "[]",
                "uploader": "",
                "uploaderName": "",
                "createTime": "2023-09-08 16:52:55",
                "updateTime": "2023-09-08 16:52:55"
            },
            {
                "versionCode": "3.0.0",
                "describe": "更新版本号",
                "status": 1,
                "pluginVersionId": 1738,
                "pluginId": "webapp-bms_202211300247_4109",
                "category": 1,
                "configJson": "[]",
                "uploader": "",
                "uploaderName": "",
                "createTime": "2022-11-30 14:53:01",
                "updateTime": "2023-03-16 16:37:33"
            },
            {
                "versionCode": "1.0.0",
                "describe": "",
                "status": 1,
                "pluginVersionId": 1736,
                "pluginId": "webapp-bms_202211300247_4109",
                "category": 1,
                "configJson": "[]",
                "uploader": "",
                "uploaderName": "",
                "createTime": "2022-11-30 14:47:36",
                "updateTime": "2023-03-16 16:37:19"
            }
        ],
        "parentPluginName": "",
        "hardwareDeviceDTOList": [],
        "appCounts": "",
        "ilike": false
    }
}
```



