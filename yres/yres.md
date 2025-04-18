一、子设备添加

1、接入协议， 萤石协议/MQTT（不调试）  

2、物联接入协议带入到， 区分支不支持字设备 （驱动）

3、 传感器设备下发， 设备厂商字段， （数据字段）固定后缀   common.manufacturer.hikvision  类型

4、关联传感器   添加传感器， deviceTypeCode（主类型）/  channelType(子类型)/ 监测类型



























































web前端开发技能
1、掌握html几种标签类型，CSS基本布局方法，flex弹性布局，居中布局，定位/浮动、盒子模型等，基本CSS动画
2、掌握js基本数据类型，数据类型的区别以及校验方法，数组对象的几种操作方法，排序、去重、查找，删除等
3、掌握http网络请求框架ajax/axios， 理解浏览器跨域问题的原理以及掌握几种解决跨域问题的方案
4、掌握并理解js的原型链，几种常见原型链的继承与拓展方式
5、掌握浏览器的存储的特性，cookie、sessionStorage、localStorage等
6、掌握基本框架Vue/React、   webpack/vite、git/SVN等工具
7、掌控几种http服务的部署nginx、apache等webServer
8、掌握常见的几种编码工具（vsCode、HBuilderX等），调试工具（postman、xshell）



/web/maintenance/business/get    api.js 中         无调用

/web/maintenance/business/page 

/web/maintenance/business/name/unique 

/web/maintenance/business/modules/define/tree

/web/maintenance/business/save





1、鸿蒙模板添加组件，无法选择鸿蒙组件
2、鸿蒙应用的编译日志，status 状态 与 isFinshed 不一致。 isFinished 是 true 是结束状态的情况下， status 还是 1， 没有返回打包执行结果



**应用转让后负责人变更，原负责人成为普通成员**
**正式应用或非正式且未使用默认签名的应用，可以上传应用包到Hido平台，受控签名**



| **子模块编号** | **子模块名称** | **功能描述**                               | **是否关键模块** |
| -------------- | -------------- | ------------------------------------------ | ---------------- |
| PD-004-01      | 模板列表       | 模板列表                                   | 是               |
| PD-004-02      | 模板新建       | 创建一个新模板                             | 是               |
| PD-004-03      | 模板编辑       | 编辑修改一个模板                           | 是               |
| PD-004-04      | 模板发布       | 模板发布并开放给其他开发者使用             | 是               |
| PD-004-05      | 模板删除       | 删除一个已知的模板                         | 是               |
| PD-004-06      | 模板转让       | 模板负责人可以将模板管理权限转让给指定用户 | 是               |
| PD-004-07      | 模板收藏       | 模板收藏后，关联到收藏列表中或是模板广场   | 是               |
| PD-004-08      | 绑定应用       | 在模板列表中，直接反向关联到应用中         | 是               |
| PD-004-09      | 发布审核       | 开发者发布模板后，需要经过管理员审核       | 是               |
| PD-004-10      | 授权管理       | 不开放的模板可以通过授权给指定用户使用     | 是               |







| 模块编号 | 模块名称   | 模块来源 |
| -------- | ---------- | -------- |
| PD-001   | 总览       | 产品需求 |
| PD-002   | 应用管理   | 产品需求 |
| PD-003   | 组件管理   | 产品需求 |
| PD-004   | 模板管理   | 产品需求 |
| PD-005   | 小程序管理 | 产品需求 |
| PD-006   | 资源广场   | 产品需求 |
| PD-007   | 壳工程管理 | 产品需求 |
| PD-008   | 设备管理   | 产品需求 |
| PD-009   | 用户管理   | 产品需求 |
| PD-010   | 组织管理   | 产品需求 |
| PD-011   | 广告管理   | 产品需求 |
| PD-012   | 统计分析   | 产品需求 |
| PD-013   | 应用开发   | 产品需求 |
| PD-014   | 帮助文档   | 产品需求 |





| **子模块编号** | **子模块名称** | **功能描述**                               | **是否关键模块** |
| -------------- | -------------- | ------------------------------------------ | ---------------- |
| PD-003-01      | 组件列表       | 组件的编辑                                 | 是               |
| PD-003-02      | 组件新增       | 创建一个新的组件                           | 是               |
| PD-003-03      | 组件升级       | 组件成果物更新升级                         | 是               |
| PD-003-04      | 组件发布       | 组件成果物升级之后发布新的版本             | 是               |
| PD-003-05      | 组件收藏       | 组件广场中收藏相关业务能力的组件           | 是               |
| PD-003-06      | 组件删除       | 删除组件功能                               | 是               |
| PD-003-07      | 组件编辑       | 组件的编辑、配置功能                       | 是               |
| PD-003-08      | 发布审核       | 开发者发布组件后，需要经过管理员审核       | 是               |
| PD-003-09      | 授权管理       | 不开放的组件可以通过授权给指定用户使用     | 是               |
| PD-003-10      | 组件转让       | 组件负责人可以将组件管理权限转让给指定用户 | 是               |



| **子模块编号** | **子模块名称** | **功能描述**                       | **是否关键模块** |
| -------------- | -------------- | ---------------------------------- | ---------------- |
| PD-002-01      | 应用列表       | 查询应用列表                       | 是               |
| PD-002-02      | 应用创建       | 应用创建流程                       | 是               |
| PD-002-03      | 应用编辑       | 完善一个应用的基本信息配置         | 是               |
| PD-002-04      | 应用配置       | 构成应用功能的组件配置             | 是               |
| PD-002-05      | 应用转让       | 应用转让后负责人变更               | 是               |
| PD-002-06      | 应用调试       | 调试应用的工具                     | 是               |
| PD-002-07      | 应用编译       | 打包编译生成成果物                 | 是               |
| PD-002-08      | 应用删除       | 应用删除后标记为已删除，且数据保存 | 是               |
| PD-002-09      | 应用签名       | 上传应用包到Hido平台，受控签名     | 是               |

```json

测试hitom  com.ceshi.hitpm

测试步骤   com.asfd.qw12qwe


需求文档2份  评审/交互评审 缺陷以及改进建议5条

设计文档2份 评审修改意见5条

代码实现 2个  自测测试报告2份或是3份评审意见   审核缺陷5个

维护2个案例

规划1份

项目管理3项：

组织能力建设 体系建设案例（1个）  知识总结经典案例（2个）  知识分享（2个） 人才培养（2个）人才发展体系建设（1个）


1、有一个年后定制的四维地图没有验收反馈
2、TPC业务基线： 车辆查询地图抓拍地点经纬度 与 web端过车查询的抓拍地点不一致， 偶现车道名称不一致，车道方向不一致，违法行为不一致，车辆品牌的数据结果不一致 （delay缺陷）
3、pvia业务基线：车辆查询地图抓拍地点经纬度 与 web端过车查询的抓拍地点不一致， 偶现车道名称不一致，车道方向不一致，违法行为不一致，车辆品牌的数据结果不一致 （delay缺陷）
4、交管APP项目/高速APP项目： 不定时出现项目测试申请，出现一些服务接口字段变更，或是功能模块集成跳转参数 （出现多次的已解决的缺陷）
5、高速APP项目：不定时出现项目测试申请，出现一些服务接口字段变更，或是功能跳转参数 （出现多次的已解决的缺陷）
6、基线框架1.6.x版本，对接局域网网关总线，拦截所有网络请求，通过新的网络插件进行http请求 （出现多次的已解决的功能版本）
7、基线框架3.x版本，对接局域网网关总线，拦截所有网络请求，通过新的网络插件进行http请求 （出现多次的已解决的功能版本）





各位同事，大家好！
为帮助公司微信小程序（后续简称：小程序）合规发布，规避潜在风险，按照法务/网络安全部推出的安全、隐私合规检测检测规范要求，HiDO推出了微信小程序管理平台（后续简称：管理平台）。
管理平台提供的基本能力可参考相应wiki：
https://wiki.hikvision.com.cn/pages/viewpage.action?pageId=224246683。
微信小程序试用群，邀请部分小程序开发人员尝鲜试用，受邀人员有以下权益：
1、提前熟悉了解管理平台
2、对管理平台提出合理建议和意见，管理平台开发人员将会快速响应、认真考虑、若建议合适则会在管理平台中加入
受邀人员可通过云文档完成必要信息录入，云文档：https://docs.hikvision.com/#/file/nodcn95UNKZb-GfD4coy-81aEvv
```

```bash
"@dcloudio/uni-automator": "^2.0.2-3081220230817001"
```

 terserOptions: { compress: { pure_funcs: [console.log]}} 

 terserOptions: { compress: { pure_funcs: [console.log]}} 

```bash
		   '100': 'Continue',
            '101': 'Switching Protocols',
            '102': 'Processing',
            '103': 'Early Hints',
            '200': 'OK',
            '201': 'Created',
            '202': 'Accepted',
            '203': 'Non-Authoritative Information',
            '204': 'No Content',
            '205': 'Reset Content',
            '206': 'Partial Content',
            '207': 'Multi-Status',
            '208': 'Already Reported',
            '226': 'IM Used',
            '300': 'Multiple Choices',
            '301': 'Moved Permanently',
            '302': 'Found',
            '303': 'See Other',
            '304': 'Not Modified',
            '305': 'Use Proxy',
            '307': 'Temporary Redirect',
            '308': 'Permanent Redirect',
            '400': 'Bad Request',
            '401': 'Unauthorized',
            '402': 'Payment Required',
            '403': 'Forbidden',
            '404': 'Not Found',
            '405': 'Method Not Allowed',
            '406': 'Not Acceptable',
            '407': 'Proxy Authentication Required',
            '408': 'Request Timeout',
            '409': 'Conflict',
            '410': 'Gone',
            '411': 'Length Required',
            '412': 'Precondition Failed',
            '413': 'Payload Too Large',
            '414': 'URI Too Long',
            '415': 'Unsupported Media Type',
            '416': 'Range Not Satisfiable',
            '417': 'Expectation Failed',
            '418': "I'm a Teapot",
            '421': 'Misdirected Request',
            '422': 'Unprocessable Entity',
            '423': 'Locked',
            '424': 'Failed Dependency',
            '425': 'Too Early',
            '426': 'Upgrade Required',
            '428': 'Precondition Required',
            '429': 'Too Many Requests',
            '431': 'Request Header Fields Too Large',
            '451': 'Unavailable For Legal Reasons',
            '500': 'Internal Server Error',
            '501': 'Not Implemented',
            '502': 'Bad Gateway',
            '503': 'Service Unavailable',
            '504': 'Gateway Timeout',
            '505': 'HTTP Version Not Supported',
            '506': 'Variant Also Negotiates',
            '507': 'Insufficient Storage',
            '508': 'Loop Detected',
            '509': 'Bandwidth Limit Exceeded',
            '510': 'Not Extended',
            '511': 'Network Authentication Required'
```

男：15858111316
女：15868174767 339005199503020028 浙A792XB



https://10.15.82.14:8088/webapi/hatom/web/rest/v1/tp/appTemplateCollections

https://10.15.82.14:8088/webapi/hatom/web/rest/v1/tp/appTemplateCollections?tempSourceVal=mine&type=&keyword=&limit=6&start=0&platformType=1

```json
{
    tempSourceVal: 'mine',
    type: "",
    keyword: "",
    limit:6,
    start:0,
    category: 0,
    platformType:1,
}
```



```json
{
    "tag":null,
    "limit":15,
    "start":0,
    "name":"",
    "sort":6,
    "category":0
}
```



选择一个提供短信转发功能的服务，这些服务通常会提供API用于接收短信并将其转发到指定的目标

mp-hikyun 这个仓库的代码权限我这边没有





在Web/H5端使用JavaScript解码PS格式视频文件可能需要结合使用第三方库、转码工具来实现。以下是一些常用的第三方库和转码工具，可以帮助您实现PS格式视频文件的解码和转换：

1. **FFmpeg.js**：FFmpeg.js 是基于 FFmpeg 的 JavaScript 版本，可以在浏览器中运行。您可以使用 FFmpeg.js 将 PS 格式视频文件转换为其他格式，例如 MP4、WebM 等。它提供了丰富的功能和命令行工具，可以帮助您进行视频格式转换。
2. **MediaInfo.js**：MediaInfo.js 是一个 JavaScript 版本的 MediaInfo 库，可以用于获取视频文件的元数据信息，包括视频编解码格式、分辨率、帧率等。通过分析 PS 格式视频文件的元数据信息，您可以更好地了解视频文件的属性，为后续的处理提供依据。
3. **Video.js**：Video.js 是一个流行的 HTML5 视频播放器库，它提供了丰富的 API 和插件，可以用于在 Web 页面中播放视频。您可以结合 Video.js 和其他库来实现 PS 格式视频文件的播放和转换。
4. **Hls.js**：Hls.js 是一个 JavaScript 实现的 HTTP Live Streaming (HLS) 客户端，可以用于在浏览器中播放 HLS 格式的视频流。如果您的 PS 格式视频文件可以转换为 HLS 格式，您可以使用 Hls.js 在 Web 页面中播放这些视频文件。

需要注意的是，这些工具和库可能需要一定的学习成本，并且在使用过程中可能会遇到一些限制和兼容性问题。在选择工具和库时，建议根据您的具体需求和项目情况进行评估和选择。同时，由于 PS 格式视频文件相对较少在 Web 端使用，可能会增加实现的难度，您可能需要进行更多的测试和调试来确保功能的正常运行。







hitom内迁工作有两块

1、现有外网云曜版本的改造
	a> 修改鉴权的逻辑，校验用户登录信息，外部用户以及管理员账号保留原有的逻辑，内部开发者账号做内网地址的重定向

2、内迁新版本分支的功能点开发

​	a> 去掉与云曜控制台头部的关联，将头部组件的逻辑代码去掉，同时去掉客服评价组件， 去掉百度统计SDK
​    b> 修改登录鉴权的逻辑，将云曜用户注册域账号的逻辑去掉
​    c> 添加http接口鉴权逻辑，配置http对象初始化参数，将未通过接口鉴权的操作，重定向到OA登录页面
​    d> 将http接口请求头参数的token 替换为 OA 鉴权参数 cookie 中的 JESSIONID
​    e> 去掉阿里云OSS服务的对接，替换minio SDK对接， 新增OSS鉴权接口
​    f>  检查所有文件上传逻辑，包括图片，zip包，md文件 以及 iOS/Android 成果物包 文件名以及大小校验,  配置新的分片上传逻辑



