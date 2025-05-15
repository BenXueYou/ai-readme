



旧综合安防平台的仓库

https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vacsc-portal
https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vacsc-miniprogram
https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vacsc-official-accounts
https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vacsc-person
https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vacsc-smart-campus
https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vacsc-abchina
https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vacsc-k8s
https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vacsc-value-added
https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vacsc-lghp-web
https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vacsc-attendance
https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vacsc-visitor

新综合安防平台的仓库——云曜组件

https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vtenant-cems // 消费

https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vtenant-acscperson // 人员管理

https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vtenant-res // 设备管理

https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vtenant-attendance // 考勤

https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vtenant-acscevent // 门禁事件

https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vtenant-org // 区域管理

https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vtenant-acscaccess // 门禁权限

https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vtenant-log // 日志

https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vtenant-cpark // 停车

https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vtenant-facemgr // 人脸库

https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vtenant-visitor // 访客

https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vtenant-alarm // 告警

https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vtenant-video // 视频

https://sys-gitlab.hikvision.com.cn/PBG/pre-research/hikkan/frontend/vtenant-trusteeship // 托管























https://pb.hik-cloud.com/safe-center/index.html#/authLoginPage/minerva?fromType=webOuath&response_type=code&state=STATE&client_id=yunyaostageClient&menu_uri=minerva&redirect_uri=https%3A%2F%2Fisccems-stage.hikyun.com

https://pb.hik-cloud.com/safe-center/index.html#/authLoginPage/minerva?fromType=webOuath&response_type=code&state=STATE&menu_uri=minerva&redirect_uri=https%3A%2F%2Fisccems-stage.hikyun.com

https://pb.hik-cloud.com/safe-center/index.html#/authLoginPage/minerva?fromType=webOuath&response_type=code&state=STATE&client_id=yunyaostageClient&menu_uri=minerva&redirect_uri=https%3A%2F%2Fisccems-stage.hikyun.com

```Mermaid
graph TD
    A[开始] --> B{record.orderStatus}
    B -- "未支付(unpaid)" --> C{"!record.payStatus"}
    C -- "是(yes)" --> D{"status === 'cancel'"}
    D -- "是(yes)" --> E["startLoading('取消中')"]
    E --> F["cancelOrder({orderId: record.orderId, personId: getItem('personIndexCode')})"]
    F --> G["successToast('取消成功')"]
    G --> H[手动修改状态]
    H --> I[结束]
    C -- "否(no)" --> J["path = `/order/pay/${record.merchantId}/${Number(record.totalPrice.price) * 100}?orderIds=${record.orderNo}&orderId=${record.orderId}`"]
    J --> K["router.push(path)"]
    B -- "已下单(ordered)" --> L{"!record.payStatus"}
    L -- "是(yes)" --> M{"status === 'cancel'"}
    M -- "是(yes)" --> N["startLoading('取消中')"]
    N --> O["cancelOrder({orderId: record.orderId, personId: getItem('personIndexCode')})"]
    O --> P["successToast('取消成功')"]
    P --> Q[手动修改状态]
    Q --> R[结束]
    L -- "否(no)" --> S["path = `/order/pay/${record.merchantId}/${Number(record.totalPrice.price) * 100}?orderIds=${record.orderNo}&orderId=${record.orderId}`"]
    S --> T["router.push(path)"]
    B -- "已发货(delivered)" --> U["path = `/order/record/comment/${record.orderNo}`"]
    U --> V["router.push(path)"]
    V --> W[结束]
```

食堂消费分两次提测 2号晚上提测

提测内容包括

```json
1.数据同步 包括学生老师和其组织 
2.web端单点登录 
3.app端单点登录到送餐页面 
4.小程序端单点登录到充值页面并能充值
```

域名地址：
生产环境地址： https://cemsc.hikyun.com
测试环境地址： https://cemsc-stage-h5.hikyun.com

首页地址：/mobile-h5/wechat/home
充值地址：/mobile-h5/wechat/accountPrepaid
送餐页地址：/mobile-h5/delivery/home

参数地址：?state=minervaXcx&token=XXXXXXXXX

state：来源 ，枚举值 minervaApp    --  APP
minervaXcx     --  微信小程序
minervaClass    --  班牌
token:   用户token

https://cemsc.hikyun.com/mobile-h5/wechat/home?state=minervaXcx&token=XXXXXXXXX

```javascript
// 小程序
http://localhost:3000/mobile-h5/wechat/home?state=minervaXcx&token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE3NDU0ODk4MTMsImlhdCI6MTc0NTQ4MjYxMywidG9rZW4iOiJ7XCJwcm9qZWN0SWRcIjpcIjExMjcxNzQ0Nzc2OTE0MTZcIixcInBlcnNvbklkXCI6XCIxMTI3MDUyMzMxODEzMTQ0XCJ9In0.Kz-m1MBwsPdbuineTHuC_oafWxFJx0JoYmcT0OsCt-4

http://10.11.65.23:3000/mobile-h5/order/home?state=minervaApp&token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE3NDM2MDUxNDYsImlhdCI6MTc0MzU5Nzk0NiwidG9rZW4iOiJ7XCJwcm9qZWN0SWRcIjpcIjExMjcxNzQ0Nzc2OTE0MTZcIixcInBlcnNvbklkXCI6XCIxMTI2MjQzMzAwOTAzMTkyXCJ9In0.VHI-iMzCUZgPqCZZRBgE48r9d9m0L3XbfxG1iZQzcSg

// app
http://10.11.65.23:3000/mobile-h5/delivery/home?state=minervaApp&token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE3NDM2MDU5NTAsImlhdCI6MTc0MzU5ODc1MCwidG9rZW4iOiJ7XCJwcm9qZWN0SWRcIjpcIjExMjcxNzQ0Nzc2OTE0MTZcIixcInBlcnNvbklkXCI6XCIxMTI3MDUyMzMxODEzMTQ0XCJ9In0.-XPlmxNu7QMc7JtV-yC5zr5jMRYgV70hsQKRrJib3zY

// 班牌
http://10.11.65.23:8080/cems-classbrand-h5/#/home?state=minervaClass&token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE3NDQ3NzcyNDAsImlhdCI6MTc0NDc3MDA0MCwidG9rZW4iOiJ7XCJwcm9qZWN0SWRcIjpcIjExMjcxNzQ0Nzc2OTE0MTZcIixcInBlcnNvbklkXCI6XCIxMTI3MDUyMzMxODEzMTQ0XCJ9In0.q6HjCDVvOuAwZ-ZKgBXCtmXGIDX2RgltrcngsKVHtIc
```

https://cemsc.hikyun.com/mobile-h5/delivery/home

朋学友：4b649c2cf6334e7f9afd23cb48fbbb45

李四：f4f0daf62d2049e5809a3dc26701006d

webapi/comcs/ui/app/merchant/v1/getMealAndDishCategory

webapi/comcs/ui/app/merchant/v1/mealAndDishCategory

https://10.11.65.23:3001/mobile-h5/wechat/home?state=minervaClass&token=

http://localhost:8080/cems-classbrand-h5/#/home?state=minervaClass&token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE3NDI4NzcwOTYsImlhdCI6MTc0Mjg2OTg5NiwidG9rZW4iOiJ7XCJwcm9qZWN0SWRcIjpcIjExMjcxNzQ0Nzc2OTE0MTZcIixcInBlcnNvbklkXCI6XCIxMTI3NTYxMzY0NzYyMTM2XCJ9In0.3L2H9K3cyJZUJlxsdcDndrRjqnTreBkjhMgymF6Ishk

https://cemsc-stage-h5.hikyun.com/mobile-h5/wechat/home?state=minervaXvc&token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE3NDM0MTI1NTIsImlhdCI6MTc0MzQwNTM1MiwidG9rZW4iOiJ7XCJwcm9qZWN0SWRcIjpcIjExMjcxNzQ0Nzc2OTE0MTZcIixcInBlcnNvbklkXCI6XCIxMTI2MjQzMzAwOTAzMTkyXCJ9In0.ABDnB7hlwJXABmUCh9L1qPuyl7plEBuW05M86Jjys70

https://cemsc-**sta**ge-h5.hikyun.com/mobile-h5/wechat/home?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE3NDI4ODc4NjYsImlhdCI6MTc0Mjg4MDY2NiwidG9rZW4iOiJ7XCJwcm9qZWN0SWRcIjpcIjExMjcxNzQ0Nzc2OTE0MTZcIixcInBlcnNvbklkXCI6XCIxMTI3NTYxMzY0NzYyMTM2XCJ9In0.frzEm31GhS-TQUEzP2crV5hakEy2Vbsfr6SwNV04GgA

https://cemsc.hikyun.com/mobile-h5/wechat/accountPrepaid

wechat/accountPrepaid

```javascript
        window.location.href = `https://www.abchina.com/luascript/mobilePayLua/{"return":{"tokenID":"${tokenId}","backURL":"${window.location.origin}/mobile/result?from=abchina&billNo=${billNo}"}}`


```

```py
import bpy

# 删除默认立方体
bpy.ops.object.select_all(action='SELECT')
bpy.ops.object.delete(use_global=False)

# 创建一个球体作为大脑模型
bpy.ops.mesh.primitive_uv_sphere_add(radius=1, location=(0, 0, 0))
brain = bpy.context.object
brain.name = "Brain"

# 细分球体使其更光滑
bpy.ops.object.modifier_add(type='SUBSURF')
brain.modifiers["Subdivision"].levels = 3
bpy.ops.object.shade_smooth()

# 创建材质并应用到大脑模型
material = bpy.data.materials.new(name="BrainMaterial")
material.use_nodes = True
brain.data.materials.append(material)

# 获取材质节点
nodes = material.node_tree.nodes
links = material.node_tree.links

# 清空默认节点
for node in nodes:
    nodes.remove(node)

# 添加 Principled BSDF 节点
bsdf = nodes.new(type='ShaderNodeBsdfPrincipled')
bsdf.location = (0, 0)

# 添加 Glass BSDF 节点
glass = nodes.new(type='ShaderNodeBsdfGlass')
glass.location = (-200, 0)

# 添加 Mix Shader 节点
mix_shader = nodes.new(type='ShaderNodeMixShader')
mix_shader.location = (200, 0)

# 添加输出节点
output = nodes.new(type='ShaderNodeOutputMaterial')
output.location = (400, 0)

# 连接节点
links.new(bsdf.outputs['BSDF'], mix_shader.inputs[1])
links.new(glass.outputs['BSDF'], mix_shader.inputs[2])
links.new(mix_shader.outputs['Shader'], output.inputs['Surface'])

# 设置毛玻璃效果
glass.inputs['IOR'].default_value = 1.45  # 折射率
mix_shader.inputs['Fac'].default_value = 0.7  # 混合系数

# 设置蓝色渐变背景
world = bpy.data.worlds.new(name="World")
bpy.context.scene.world = world
world.use_nodes = True

# 获取世界节点
world_nodes = world.node_tree.nodes
world_links = world.node_tree.links

# 清空默认节点
for node in world_nodes:
    world_nodes.remove(node)

# 添加背景节点
background = world_nodes.new(type='ShaderNodeBackground')
background.location = (0, 0)

# 添加渐变纹理节点
gradient = world_nodes.new(type='ShaderNodeValToRGB')
gradient.location = (-200, 0)

# 添加纹理坐标节点
tex_coord = world_nodes.new(type='ShaderNodeTexCoord')
tex_coord.location = (-400, 0)

# 添加映射节点
mapping = world_nodes.new(type='ShaderNodeMapping')
mapping.location = (-300, 0)

# 添加输出节点
output = nodes.new(type='ShaderNodeOutputMaterial')
output.location = (400, 0)

# 连接节点
links.new(bsdf.outputs['BSDF'], mix_shader.inputs[1])
links.new(glass.outputs['BSDF'], mix_shader.inputs[2])
links.new(mix_shader.outputs['Shader'], output.inputs['Surface'])

# 设置毛玻璃效果
glass.inputs['IOR'].default_value = 1.45  # 折射率
mix_shader.inputs['Fac'].default_value = 0.7  # 混合系数

# 设置蓝色渐变背景
world = bpy.data.worlds.new(name="World")
bpy.context.scene.world = world
world.use_nodes = True

# 获取世界节点
world_nodes = world.node_tree.nodes
world_links = world.node_tree.links

# 清空默认节点
for node in world_nodes:
    world_nodes.remove(node)

# 添加背景节点
background = world_nodes.new(type='ShaderNodeBackground')
background.location = (0, 0)

# 添加渐变纹理节点
gradient = world_nodes.new(type='ShaderNodeValToRGB')
gradient.location = (-200, 0)

# 添加纹理坐标节点
tex_coord = world_nodes.new(type='ShaderNodeTexCoord')
tex_coord.location = (-400, 0)

# 添加映射节点
mapping = world_nodes.new(type='ShaderNodeMapping')
mapping.location = (-300, 0)

# 添加输出节点
world_output = world_nodes.new(type='ShaderNodeOutputWorld')
world_output.location = (200, 0)

# 连接节点
world_links.new(tex_coord.outputs['Generated'], mapping.inputs['Vector'])
world_links.new(mapping.outputs['Vector'], gradient.inputs['Fac'])
world_links.new(gradient.outputs['Color'], background.inputs['Color'])
world_links.new(background.outputs['Background'], world_output.inputs['Surface'])

# 设置渐变颜色
gradient.color_ramp.elements[0].color = (0, 0.2, 0.8, 1)  # 深蓝
gradient.color_ramp.elements[1].color = (0, 0.5, 1, 1)    # 浅蓝

# 设置摄像机位置
bpy.ops.object.camera_add(location=(0, -5, 3))
camera = bpy.context.object
camera.rotation_euler = (1.2, 0, 0)
bpy.context.scene.camera = camera

# 设置灯光
bpy.ops.object.light_add(type='SUN', location=(5, 5, 5))
sun = bpy.context.object
sun.data.energy = 5

# 设置渲染引擎为 Cycles
bpy.context.scene.render.engine = 'CYCLES'

# 设置渲染分辨率
bpy.context.scene.render.resolution_x = 1920
bpy.context.scene.render.resolution_y = 1080

# 渲染图像
bpy.ops.render.render(write_still=True)
```

人员信息---组织管理模块：  开发进度100%，自测进度80%
人员信息---人员管理模块：  开发进度100%，自测进度70%
人员分组---分组管理模块：  开发进度100%，自测进度80%
待审核人员---人员审核模块：  开发进度100%，自测进度60%
待审核人员---人员H5录入模块：  开发进度80%，自测进度0%
参数配置模块：开发进度60%，自测进度0%

人脸库管理---人脸比对计划模块： 开发进度100%，自测进度50%
人脸库管理---人脸比对设备点模块： 开发进度100%，自测进度50%
人脸库管理---人脸分组管理模块： 开发进度100%，自测进度50%
人脸库管理---人脸对比结果模块： 开发进度100%，自测进度50%

停车服务管理模块：开发进度100%，自测进度100%

云眸&云曜业务融合

1、根据业务云眸企业人员管理整合综合安防云需求，完成人员管理公共组件开发，并集成到云眸企业平台中

2、根据云眸企业人脸库整合综合安防云业务需求，完成人脸库应用对接，新增人脸比对应用销售项的支持

3、结合访客业务对接云停车业务业务需求，完成访客访问区域配置项新增云停车主机、智慧云停车场点

4、支撑云眸企业门禁业务改造，新增门禁点计划模板功能模块，支持门禁权限配置权限组，配置人员分组以及计划模板功能

云帆业务平台组件支撑

1、支持云帆访客业务组件日常维护， 完善嗨通行小程序应邀流程优化，应邀链接自动定向到预约详情
2、完善云帆访客业务嗨访客小程序预约表单流程，兼容了iOS输入框交互与鸿蒙系统的样式渲染
3、支撑云帆消费组件基线日常维护工作，完善消费统计报表交互、订单排序等，修复历史遗留缺陷修复

租户平台yres组件建设

1、支撑基础服务设备资源管理业务功能迭代工作，根据需求完成评审工作以及开发方案与工作量评估
2、支持平台对接国标V3设备，支持设备添加、删除、查询以及通道管理
3、修复并优化测试提出的应用易用性专项走查提出的缺陷建议

1、结合业务需求，梳理消费组件、人员管理组件等菜单管理以及结构关系；
2、协助消费组件对接云眸单点登录，以及消费组件菜单页面集成工作；
2.1、完成消费组件、人员组件以及系统配置菜单权限码、代码路由与uri路径映射表；
2.2、完成代码工程目录结构与路由关系结构新增；
2.3、整理菜单图标样式将svg图标转为icon font文件样式；
3、支撑云曜视频业务组件功能与云眸融合开发工作；
3.1、梳理云曜视频监控、视频轮巡业务中使用C++插件场景
3.2、对接云眸C++视频播放插件，评估开发工作量
3.3、完成物联网平台视频监控、视频播放C++插件替换
3.4、替换租户平台-视频监控、视频轮巡组件、告警组件视频播放web-control插件
3.5、替换运营平台电子地图组件视频播放web-control插件
4、支撑云眸AI增值业务对接云市场线上支付开票功能开发
5、支撑小程序访客业务功能迁移到云眸小程序开发工作
5.1、梳理小程序访客业务模块相关页面，评估开发工作量，制定开发计划
5.2、完成小程序访客端预约业务模块开发
5.3、完成小程序员工端邀约业务模块开发
5.4、完成小程序员工端审批业务模块开发
5.5、结合平台web端动态表单等配置功能，调试访客业务多场景下的正常流程

1、云眸企业1.7.2版本对接自定义表单功能 12月30日发布

2、Hitom移动应用开发平台3.4.3版本， 12月31日发布

3、访客小程序补丁版本发布，12月31日完成缺陷修复，发布日期（陈绍鹏 答复 暂定1月3日发布 ）

4、云眸企业V1.7.3版本人员管理功能，排期未定  (前端工作量12月30日给出精确评估， 后端孙涛确认31日前给出排期)

5、云眸企业V1.7.4-AR车间、生产报工、设备运维 https://hikke.hikvision.com.cn/#/projects/70393/iterations/6761200294821d1674d6fdef?share=true （12月30日启动需求评审）

6、企微指纹考勤机接入（2.10 联调；3.18 测试；4.30 发布）

7、消费对账定制功能需求 （需求整理中）

8、现场反馈的鸿蒙系统兼容问题  （市场上纯鸿蒙next 系统 的 手机不是很多，刘一驰答复现场，当前暂缓，后续逐步修复兼容问题）

http://defect.hikvision.com.cn/approve/document?flowInstId=355718170---必填的校验没有拦住，访客预约和邀约

http://defect.hikvision.com.cn/approve/document?flowInstId=356322454----IOS：体验有问题，需要解决这周  （已解决）

http://defect.hikvision.com.cn/approve/document?flowInstId=356035962--我再想一想表单刷新 （已解决）

http://defect.hikvision.com.cn/approve/document?flowInstId=356322286 --安卓 （已解决）

http://defect.hikvision.com.cn/approve/document?flowInstId=356322118--时间显示具体单位

http://defect.hikvision.com.cn/approve/document?flowInstId=356321872--上传图片首次会刷新表单，（已解决）

http://defect.hikvision.com.cn/approve/document?flowInstId=355985527---[云眸企业小程序] 游客打开短信邀约链接，确认协议后登录，直接跳转到访客首页，而没有打开接受邀请页面，-----预约一样，就是首次使用，注册登录后没办法跳转到预约或者应邀界面，需要二次操作

http://defect.hikvision.com.cn/approve/document?flowInstId=356242420--没有上传图片，有图片字段，给个默认图片

http://defect.hikvision.com.cn/approve/document?flowInstId=354636807--交互体验

http://defect.hikvision.com.cn/approve/document?flowInstId=355901126--填写的优化

http://defect.hikvision.com.cn/approve/document?flowInstId=356030410 自定义字段没有显示的问题

http://defect.hikvision.com.cn/approve/document?flowInstId=355955215 ---智能门禁] 配置入园承诺后访客在小程序预约，页面展示不合理，出现大量空白 （已解决）

http://defect.hikvision.com.cn/approve/document?flowInstId=356030470--证件号码根据内置规则校验

http://defect.hikvision.com.cn/approve/document?flowInstId=356283027--web 最大天数控制问题

http://defect.hikvision.com.cn/approve/document?flowInstId=355516183--下拉框的默认选中项

人员管理  （10号给出接口文档， 人脸库13号给出接口文档）

移动端管理：

待审核人员

人员记录

门禁权限控制

1、由于访客业务理解不到位，评估工作量偏差较大
2、提测过程中缺陷总数超过30个以上，未达到预期
3、云眸云曜融合访客业务版本开发勉强发布，质量不高
4、无法推动计划中视频插件开发任务按期完成
5、因为工作量评估不准确，导致后期工作中压力较大，出现心态崩溃，导致计划安排出现混乱，且有质量问题，需要自省

1、与后端配合较好，快速完成中信银行三个定制需求版本开发，单版本缺陷总数不超过10个缺陷且均是2小时内修复
2、完成农行消费业务需求定制开发，较快好完成自测发布，未出现质量问题
3、快速完成云帆人员通行/门禁业务现场问题修复，2小时解决

1、租户yres组件前端工作中规中矩，配合后端完成功能优化，缺陷修复
2、提交测试包均未出现中级缺陷，单版本低级缺陷不超过3个
3、尽管发布版本较多，由于单版本需求小而碎，质量均达到预期

1、移动端应用业务支撑中发布了4个版本，开发平台两个版本，分发平台两个版本
2、开发平台与分发平台的业务需求中均包括了对鸿蒙应用的支持
3、其它均为功能优化已知缺陷修复
4、移动端脚手架没有发布新的版本
5、新增了帮助文档内容，设计文档未输出

1、工作任务已经完成海客平台录入
2、未有新的组件输出

1. "https://pbpic.hik-cloud.com/siot/uploads/permanent/enterpriseProduction/2024/12/28/be2d93e82f8d4453b252eb1000619aae/f3d05490-c4eb-11ef-adcc-ad283cdfde71.pdf"
2. "https://pbpic.hik-cloud.com/siot/uploads/permanent/enterpriseProduction/2024/12/28/be2d93e82f8d4453b252eb1000619aae/11da9b80-c4ec-11ef-adcc-ad283cdfde71.jpg"
3.

https://10.11.65.14:7777/h5/order/submit/index?statusBarHeight=28.363636&token=eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJhY2Nlc3NfdG9rZW4iLCJwYXlsb2FkIjoie1wiYWNjZXNzS2V5XCI6XCIxNjk3MDc1NDE2OTIwMDY2MVwiLFwiZXhwaXJlZFwiOjQzMjAwLFwicHJvZHVjdENvZGVcIjpcImlvdGlfMzYxMzM0OTcxNTcyMjRcIn0iLCJleHAiOjE3MzEwMDg3MDl9.d6bo5tGHs08-ox91pnajdcMjCZY_VnIAxG4pMP08vdm1X_6vW-_NffViJZTHUXE5-i5ydQ7xz5FafrjALbYFnw&AppRouterinterceptor=1&ApplicationSource=3&firstPage=0&version=2.38.11&eruda=false&env=pb&taxNo=91110108774061536M&billNo=202411060873979696&userId=1234567890&tenantId=126791064111999&salerType=0&billDateTime=2024-10-31 23:23:23&access_token=eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJhY2Nlc3NfdG9rZW4iLCJwYXlsb2FkIjoie1wiYWNjZXNzS2V5XCI6XCIxNjk3MDc1NDE2OTIwMDY2MVwiLFwiZXhwaXJlZFwiOjQzMjAwLFwicHJvZHVjdENvZGVcIjpcImlvdGlfMzYxMzM0OTcxNTcyMjRcIn0iLCJleHAiOjE3MzA5MTc4NzB9.1i6Rsc0S9YnzTqoUR6jBGC19JG1gCaMoznv1Pw4dOLIz-vgTzbVHVpyM4_W2ezs-59rJ4lGxEElipUfza_PPwA&invoiceDetail=01&titleType=1&buyerTaxNo=342201198903296716&buyerName=张毛磊&remarks=海康威视测试&pushEmail=1910797487@qq.com&pushPhone=17799813018&invoiceDetailsList=[{"goodsName":"zmlaaa","goodsQuantity":"1","goodsTotalPriceTax":"2","goodsSpecification":"测试","goodsUnit":"个"}]

com.hikvision.clhymobile

https://10.11.65.14:7777/?taxNo=91110108774061536M&billNo=202411060873979696&userId=1234567890&tenantId=126791064111999&salerType=0&billDateTime=2024-10-31 23:23:23&access_token=eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJhY2Nlc3NfdG9rZW4iLCJwYXlsb2FkIjoie1wiYWNjZXNzS2V5XCI6XCIxNjk3MDc1NDE2OTIwMDY2MVwiLFwiZXhwaXJlZFwiOjQzMjAwLFwicHJvZHVjdENvZGVcIjpcImlvdGlfMzYxMzM0OTcxNTcyMjRcIn0iLCJleHAiOjE3MzA5MTc4NzB9.1i6Rsc0S9YnzTqoUR6jBGC19JG1gCaMoznv1Pw4dOLIz-vgTzbVHVpyM4_W2ezs-59rJ4lGxEElipUfza_PPwA&invoiceDetail=01&titleType=1&buyerTaxNo=342201198903296716&buyerName=张毛磊&remarks=海康威视测试&pushEmail=1910797487@qq.com&pushPhone=17799813018&invoiceDetailsList='[{"goodsName":"zmlaaa","goodsQuantity":"1","goodsTotalPriceTax":"2","goodsSpecification":"测试","goodsUnit":"个"}]'#/index

```json
{
	"code": 0,
	"message": null,
	"data": {
		"menuId": "2",
		"menuCode": "invitation",
		"menuName": "访客邀约",
		"showOrder": 2,
		"moduleList": [{
			"moduleId": "b60575fb471e421ca0dcf9712c5cc2a7",
			"moduleName": "访客信息",
			"moduleCode": "visitorInfo_invitation",
			"moduleType": 0,
			"isSystem": true,
			"isEnableConfig": false,
			"isOpen": true,
			"isEnableIsOpen": false,
			"showOrder": 1,
			"fieldList": [{
				"fieldId": "3ef2d573ef0546dfac7eeb0badcf7f4c",
				"fieldName": "访客照片",
				"fieldCode": "visitorPhoto_visitorInfo_invitation",
				"inputItemId": "IMAGE",
				"inputItemName": "图片上传",
				"isSystem": true,
				"isEnableConfig": false,
				"isOpen": true,
				"isEnableIsOpen": true,
				"isRequired": true,
				"isEnableIsRequired": true,
				"isTableDisplay": false,
				"isEnableIsTableDisplay": false,
				"showOrder": 11,
				"configValue": "{}"
			}, {
				"fieldId": "a7057a647ff24ef982a4fe427ad1e172",
				"fieldName": "访客姓名",
				"fieldCode": "visitorName_visitorInfo_invitation",
				"inputItemId": "INPUT",
				"inputItemName": "输入框",
				"isSystem": true,
				"isEnableConfig": false,
				"isOpen": true,
				"isEnableIsOpen": false,
				"isRequired": true,
				"isEnableIsRequired": false,
				"isTableDisplay": false,
				"isEnableIsTableDisplay": false,
				"showOrder": 24,
				"configValue": "{\r\n \"hint\": \"1~32个字符；不能包含 '' / \\\\\\\\ : * ? \\\" < > | 这些特殊字符\",\r\n \"regular\": \"^[^\\\\''\\\\/\\\\:\\\\*\\\\?\\\"<>\\\\\\\\|]{1,32}$\"\r\n}"
			}, {
				"fieldId": "d154c0958a4d4b7785bc89aeb6cc683c",
				"fieldName": "手机号码",
				"fieldCode": "visitorPhoneNum_visitorInfo_invitation",
				"inputItemId": "INPUT",
				"inputItemName": "输入框",
				"isSystem": true,
				"isEnableConfig": false,
				"isOpen": true,
				"isEnableIsOpen": false,
				"isRequired": true,
				"isEnableIsRequired": false,
				"isTableDisplay": false,
				"isEnableIsTableDisplay": false,
				"showOrder": 25,
				"configValue": "{\r\n \"hint\": \"1-20个数字\",\r\n \"regular\": \"^[0-9]{1,20}$\"\r\n}"
			}, {
				"fieldId": "f3a25968ca804af793564d10278be9c1",
				"fieldName": "性别",
				"fieldCode": "visitorSex_visitorInfo_invitation",
				"inputItemId": "SELECT",
				"inputItemName": "下拉选择",
				"isSystem": true,
				"isEnableConfig": false,
				"isOpen": true,
				"isEnableIsOpen": false,
				"isRequired": true,
				"isEnableIsRequired": false,
				"isTableDisplay": false,
				"isEnableIsTableDisplay": false,
				"showOrder": 26,
				"configValue": "{\r\n \"hint\": \"男性请填1，女性请填2\",\r\n \"isMultiple\": false,\r\n \"selectList\": \"[{\\\"id\\\":\\\"1\\\",\\\"value\\\":\\\"男\\\",\\\"checked\\\":false},{\\\"id\\\":\\\"2\\\",\\\"value\\\":\\\"女\\\",\\\"checked\\\":false}]\"\r\n}"
			}, {
				"fieldId": "a43083202b89482d83081285fbe48c00",
				"fieldName": "车牌号码",
				"fieldCode": "visitorCarNumber_visitorInfo_invitation",
				"inputItemId": "INPUT",
				"inputItemName": "输入框",
				"isSystem": true,
				"isEnableConfig": false,
				"isOpen": false,
				"isEnableIsOpen": true,
				"isRequired": false,
				"isEnableIsRequired": true,
				"isTableDisplay": false,
				"isEnableIsTableDisplay": false,
				"showOrder": 27,
				"configValue": "{\r\n \"hint\": \"1-16个字符；不能包含 '' / \\\\\\\\ : * ? \\\" < > | 这些特殊字符\",\r\n \"regular\": \"^[^\\\\''\\\\/\\\\:\\\\*\\\\?\\\"<>\\\\\\\\|]{1,16}$\"\r\n}"
			}, {
				"fieldId": "946c0107d7c64e539c4da70f02a24a9b",
				"fieldName": "来访单位",
				"fieldCode": "visitorWorkUnit_visitorInfo_invitation",
				"inputItemId": "INPUT",
				"inputItemName": "输入框",
				"isSystem": true,
				"isEnableConfig": false,
				"isOpen": false,
				"isEnableIsOpen": true,
				"isRequired": false,
				"isEnableIsRequired": true,
				"isTableDisplay": false,
				"isEnableIsTableDisplay": false,
				"showOrder": 28,
				"configValue": "{\r\n \"hint\": \"1-32个字符；不能包含 '' / \\\\\\\\ : * ? \\\" < > | 这些特殊字符\",\r\n \"regular\": null\r\n}"
			}, {
				"fieldId": "b21c8d975536451ba981996a0bd777b0",
				"fieldName": "证件号码",
				"fieldCode": "visitorIdentityNum_visitorInfo_invitation",
				"inputItemId": "INPUT",
				"inputItemName": "输入框",
				"isSystem": true,
				"isEnableConfig": false,
				"isOpen": false,
				"isEnableIsOpen": true,
				"isRequired": false,
				"isEnableIsRequired": true,
				"isTableDisplay": false,
				"isEnableIsTableDisplay": false,
				"showOrder": 29,
				"configValue": "{\r\n \"hint\": \"身份证号码需符合18位字符，格式为[省代码][市代码][县代码][年月日][0～9/X]；其他证件号码需符合1～20位数字、字母\",\r\n \"regular\": \"^[0-9A-Za-z]{1,20}\"\r\n}"
			}, {
				"fieldId": "6b076f7deb3b49e1858d0ac9f85e2814",
				"fieldName": "访客住址",
				"fieldCode": "visitorAddress_visitorInfo_invitation",
				"inputItemId": "INPUT",
				"inputItemName": "输入框",
				"isSystem": true,
				"isEnableConfig": false,
				"isOpen": false,
				"isEnableIsOpen": true,
				"isRequired": false,
				"isEnableIsRequired": true,
				"isTableDisplay": false,
				"isEnableIsTableDisplay": false,
				"showOrder": 32,
				"configValue": "{\r\n \"hint\": \"1～128个字符；不能包含 '' / \\\\ : * ? \\\" < > | 这些特殊字符\",\r\n \"regular\": \"^[^\\\\''\\\\/\\\\:\\\\*\\\\?\\\"<>\\\\\\\\|]{0,128}$\"\r\n}"
			}, {
				"fieldId": "d383ea5ec3bc446db248da8a62040566",
				"fieldName": "asdffffffffffasdfffffffffffffffs",
				"fieldCode": "9ccdac10d98a45c6868e706325ea2f55",
				"inputItemId": "INPUT",
				"inputItemName": "输入框",
				"isSystem": false,
				"isEnableConfig": true,
				"isOpen": true,
				"isEnableIsOpen": true,
				"isRequired": true,
				"isEnableIsRequired": true,
				"isTableDisplay": true,
				"isEnableIsTableDisplay": true,
				"showOrder": 41,
				"configValue": "{\"defaultName\":\"\",\"inputValidType\":\"9\",\"regular\":\"/^[^'\\\\/\\\\:\\\\*\\\\?\\\\\\\"<>\\\\|\\\\\\\\]{1,20}$/\",\"hint\":\"长度1-20位，不支持特殊字符'/:*?\\\\\\\"<>|\\\\\"}"
			}, {
				"fieldId": "b8d5f78e6e3b4c9b9be13ceecb86f383",
				"fieldName": "asdfasdfsadfadfadfadfadfadfadfad",
				"fieldCode": "f7791bbcc44d485996f0e440d437c991",
				"inputItemId": "SELECT",
				"inputItemName": "下拉选择",
				"isSystem": false,
				"isEnableConfig": true,
				"isOpen": true,
				"isEnableIsOpen": true,
				"isRequired": true,
				"isEnableIsRequired": true,
				"isTableDisplay": true,
				"isEnableIsTableDisplay": true,
				"showOrder": 42,
				"configValue": "{\"isMultiple\":false,\"selectList\":[{\"value\":\"asdfsafdsfad\",\"checked\":true,\"checkDisabled\":false},{\"value\":\"asdffffffffffffffffffffffffffffffffffffffff\",\"checked\":false,\"checkDisabled\":false}]}"
			}, {
				"fieldId": "8b10a7ef88674d27aa29b0d4b30d9a45",
				"fieldName": "asdfsdfaaaaaaaaaaaaaaaaaaaaaaaaa",
				"fieldCode": "3b87e44925f54f9c9bd3297ded8edda1",
				"inputItemId": "IMAGE",
				"inputItemName": "图片上传",
				"isSystem": false,
				"isEnableConfig": true,
				"isOpen": true,
				"isEnableIsOpen": true,
				"isRequired": true,
				"isEnableIsRequired": true,
				"isTableDisplay": true,
				"isEnableIsTableDisplay": true,
				"showOrder": 43,
				"configValue": "{}"
			}]
		}, {
			"moduleId": "de16b22d7de040a79ee0e038cb0581f8",
			"moduleName": "访问信息",
			"moduleCode": "visitInfo_invitation",
			"moduleType": 0,
			"isSystem": true,
			"isEnableConfig": false,
			"isOpen": true,
			"isEnableIsOpen": false,
			"showOrder": 2,
			"fieldList": [{
				"fieldId": "8d47f75381b84135897db2477af55413",
				"fieldName": "访问时间",
				"fieldCode": "visitTme_visitInfo_invitation",
				"inputItemId": "TIME",
				"inputItemName": "时间选择",
				"isSystem": true,
				"isEnableConfig": true,
				"isOpen": true,
				"isEnableIsOpen": false,
				"isRequired": true,
				"isEnableIsRequired": false,
				"isTableDisplay": false,
				"isEnableIsTableDisplay": false,
				"showOrder": 33,
				"configValue": "{\r\n \"mustFlag\": true,\r\n \"dateFormat\": \"yyyy-MM-dd HH:mm\",\r\n \"nowDayRange\": 7,\r\n \"daysFlag\": true,\r\n \"maxDay\": 7,\r\n \"timeRange\": \"HH:mm-HH:mm\",\r\n \"length\": \"1HH\",\r\n \"granularity\": \"30mm\"\r\n}"
			}, {
				"fieldId": "1195c32b72fb4ea68f0f9e9b8145ec21",
				"fieldName": "访问区域",
				"fieldCode": "visitRegion_visitInfo_invitation",
				"inputItemId": "SELECT",
				"inputItemName": "下拉选择",
				"isSystem": true,
				"isEnableConfig": true,
				"isOpen": true,
				"isEnableIsOpen": false,
				"isRequired": true,
				"isEnableIsRequired": false,
				"isTableDisplay": false,
				"isEnableIsTableDisplay": false,
				"showOrder": 34,
					"configValue": "{\"isMultiple\":false,\"selectList\":[{\"value\":\"其它\",\"checked\":true,\"checkDisabled\":false},{\"value\":\"考察\",\"checked\":false,\"checkDisabled\":false}]}"
			}, {
				"fieldId": "8170995ac92049808c9f1da9e22fe16b",
				"fieldName": "邀请事由",
				"fieldCode": "visitorPurpose_visitInfo_invitation",
				"inputItemId": "SELECT",
				"inputItemName": "下拉选择",
				"isSystem": true,
				"isEnableConfig": true,
				"isOpen": true,
				"isEnableIsOpen": false,
				"isRequired": true,
				"isEnableIsRequired": false,
				"isTableDisplay": false,
				"isEnableIsTableDisplay": false,
				"showOrder": 35,
				"configValue": "{\"isMultiple\":false,\"selectList\":[{\"value\":\"其它\",\"checked\":true,\"checkDisabled\":false},{\"value\":\"考察\",\"checked\":false,\"checkDisabled\":false}]}"
			}, {
				"fieldId": "c22a1f7037a14629b90c32f911982eee",
				"fieldName": "啊啊啊啊啊啊啊萨达萨达飒飒的撒是阿斯蒂撒但阿斯蒂撒但",
				"fieldCode": "c86738ebb0254215a3cfc9f2b6c3b8c0",
				"inputItemId": "INPUT",
				"inputItemName": "输入框",
				"isSystem": false,
				"isEnableConfig": true,
				"isOpen": true,
				"isEnableIsOpen": true,
				"isRequired": true,
				"isEnableIsRequired": true,
				"isTableDisplay": true,
				"isEnableIsTableDisplay": true,
				"showOrder": 36,
				"configValue": "{\"defaultName\":\"\",\"inputValidType\":\"9\",\"regular\":\"/^[^'\\\\/\\\\:\\\\*\\\\?\\\\\\\"<>\\\\|\\\\\\\\]{1,20}$/\",\"hint\":\"长度1-20位，不支持特殊字符'/:*?\\\\\\\"<>|\\\\\"}"
			}, {
				"fieldId": "740f96fd1c57426f96248ad10ff3ac8f",
				"fieldName": "撒旦发",
				"fieldCode": "dd2beb0e8cb24dc2aa9c7bd8a3862997",
				"inputItemId": "IMAGE",
				"inputItemName": "图片上传",
				"isSystem": false,
				"isEnableConfig": true,
				"isOpen": true,
				"isEnableIsOpen": true,
				"isRequired": true,
				"isEnableIsRequired": true,
				"isTableDisplay": true,
				"isEnableIsTableDisplay": true,
				"showOrder": 37,
				"configValue": "{}"
			}, {
				"fieldId": "e276171e752841fc90fbccf215342841",
				"fieldName": "asdfffffffffffffffffffffffffffff",
				"fieldCode": "31b1dcb72bdb4f66b8fd969b97f03dd6",
				"inputItemId": "SELECT",
				"inputItemName": "下拉选择",
				"isSystem": false,
				"isEnableConfig": true,
				"isOpen": true,
				"isEnableIsOpen": true,
				"isRequired": true,
				"isEnableIsRequired": true,
				"isTableDisplay": true,
				"isEnableIsTableDisplay": true,
				"showOrder": 38,
				"configValue": "{\"isMultiple\":false,\"selectList\":[{\"value\":\"qwerqwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwww\",\"checked\":true,\"checkDisabled\":false},{\"value\":\"qwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwww\",\"checked\":false,\"checkDisabled\":false}]}"
			}, {
				"fieldId": "a5257ae998b24e9ba99cdfb856cde751",
				"fieldName": "asdddddddddddddddddddddddddddddd",
				"fieldCode": "b642c4f0d30d428aa25c55568dcd298a",
				"inputItemId": "INPUT",
				"inputItemName": "输入框",
				"isSystem": false,
				"isEnableConfig": true,
				"isOpen": true,
				"isEnableIsOpen": true,
				"isRequired": true,
				"isEnableIsRequired": true,
				"isTableDisplay": true,
				"isEnableIsTableDisplay": true,
				"showOrder": 39,
				"configValue": "{\"defaultName\":\"\",\"inputValidType\":\"9\",\"regular\":\"/^[^'\\\\/\\\\:\\\\*\\\\?\\\\\\\"<>\\\\|\\\\\\\\]{1,20}$/\",\"hint\":\"长度1-20位，不支持特殊字符'/:*?\\\\\\\"<>|\\\\\"}"
			}, {
				"fieldId": "5da7e991650d4de08b89572d90e8db4d",
				"fieldName": "asdddddddddd1ddddddddddddddddddd",
				"fieldCode": "3f43538bbc534f13ac6bcd75506bf22e",
				"inputItemId": "IMAGE",
				"inputItemName": "图片上传",
				"isSystem": false,
				"isEnableConfig": true,
				"isOpen": true,
				"isEnableIsOpen": true,
				"isRequired": true,
				"isEnableIsRequired": true,
				"isTableDisplay": true,
				"isEnableIsTableDisplay": true,
				"showOrder": 40,
				"configValue": "{}"
			}]
		}]
	},
	"success": true
}
```

https://pb.hik-cloud.com/safe-center/index.html#/login/retail?response_type=code&state=STATE&client_id=yunyaodevClient&redirect_uri=https%3A%2F%2Fisccems-dev2.hikyun.com%2F%3Fcode%3Dbabac6f8e08f46fc9288cf9446d3e7f2

https://pb.hik-cloud.com/safe-center/index.html#/login/single?response_type=code&state=STATE&client_id=yunyaodevClient&redirect_uri=https%3A%2F%2Fisccems-dev2.hikyun.com

babac6f8e08f46fc9288cf9446d3e7f2

https://acsc-pre.hikyun.com/mpvisitor/visitor/staff/pages/staff/backlog/backlog?sessionId=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE3Mjk3Mzk0NjAsImlhdCI6MTcyOTY1MzA2MCwidG9rZW4iOiJ7XCJwcm9qZWN0SWRcIjpcIjE3NDg4MDU4MzcyMFwiLFwicHJvZHVjdENvZGVcIjpcIjE3MDM2NjQ2MjA3NDkxNjlcIixcIm9wZW5JZFwiOlwib2hNTDI0cV96bXZmSzNMUU1mSUNzanhlcjQxd1wiLFwicGVyc29uSWRcIjpcIjcwMTM1NTgwMjg1NlwiLFwicmVnaXN0ZXJUeXBlXCI6XCJ3eGFwcFwiLFwic2Vzc2lvbktleVwiOlwiQVZheld3cW9tZHBNSVB0b3hqemNWUT09XCJ9In0.edUzHzRvk2UWnfx6b5QTMcSrLyAGiF_Lj-jw1cKvH8s

https://acsc-pre.hikyun.com/webapi/yacswxmp/api/v1/wechat/miniapp/wcma-bevisitor/login?code=0b1DoLFa1UrzoI0cIJIa1AIbX31DoLFV

https://acscss-pre.hikyun.com/webapi/yacswxmp/api/v1/wechat/miniapp/wcma-visitor/login?code=0e1arF0w3ABsJ33eBN1w3hPYJz1arF0i

acsc-frontend-prod:1.2.5-isc-2024102301

http://10.11.65.14:8080/mpvisitor/visitor/visitor/reserve?sessionId=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE3MzA5NDYyMDYsImlhdCI6MTczMDg1OTgwNiwidG9rZW4iOiJ7XCJwcm9qZWN0SWRcIjpcIjE2NDMyNDUxODcxMTJcIixcInByb2R1Y3RDb2RlXCI6XCIxNzAzNjY0NjIwNzQ5MTY5XCIsXCJvcGVuSWRcIjpcIm9rNmJQNUxFZmpZaHFENVc5Q05xRWVuemdoMGtcIixcInJlZ2lzdGVyVHlwZVwiOlwid3hhcHBcIixcInNlc3Npb25LZXlcIjpcIlEwSXhhbnQ4Qk0vZWxtRmpxQW5TckE9PVwifSJ9.-Iyj33asK4aldmLoYqUKLIL5M4o-be2QoT4JzlptyxQ&projectId=174880583720&enterpriseName=1111&reserveType=goMiniReserve&inDetails=null&type=accept-invite

http://ygw/gateway/

%Java_Home%\bin;

%Java_Home%\jre\bin;

C:\Program Files\Common Files\Oracle\Java\javapath;

%SystemRoot%\system32;

%SystemRoot%;

%SystemRoot%\System32\Wbem;

%SYSTEMROOT%\System32\WindowsPowerShell\v1.0\;

%SYSTEMROOT%\System32\OpenSSH\;

C:\Program Files\TortoiseSVN\bin;

D:\Yarn\bin\;%NVM_HOME%;

%NVM_SYMLINK%;

D:\nodejs\node_global;

E:\nvm\v17.6.0:\Tool\AdbTool\;

D:\wxTool\;

D:\Git\cmd;

D:\Subversion\bin;

D:\wxTool\dll;

D:\Python;

D:\Tool\adb;

C:\Program Files\Docker\Docker\resources\bin
