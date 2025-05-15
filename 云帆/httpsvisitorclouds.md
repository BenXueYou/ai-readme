```json
  {
                "orderId": "fd1b3ef030f83d0052acd600c10004f2",,
                "visitorBatch": "eaf9920a612033b0b076d609233dee00",,
                "status": "拜访中",
                "visitorPurpose": "其他",
                "beVisitorPersonName": "朋学友",
                "beVisitorEnterpriseName": null,
                "startTime": 1733821260000,
                "endTime": 1734451140000,
                "visitorLeader": "1",
                "buttonList": [
                    {
                        "buttonKey": "visitorViewDetail",
                        "buttonName": "查看详情"
                    }
                ],
                "tenantId": "be2d93e82f8d4453b252eb1000619aae",
                "backlogId": null
            },
```









http://10.11.65.14:8080/mpvisitor/visitor/staff/interviewRecords

http://10.11.65.14:8080/#/visitor/reserve-again?reserveType=goMiniReserve&type=again&orderId=91682c5df7a3e90bab025e426689c321&visitorBatch=fb09e74148f9198be6fb303950a11442&status=%E5%B7%B2%E5%8F%96%E6%B6%88&visitorPurpose=%E5%85%B6%E4%BB%96&beVisitorPersonName=%E5%86%AF%E6%B4%8B%E9%98%B3123&beVisitorEnterpriseName&startTime=1733986260000&endTime=1734245460000&visitorLeader=1&tenantId=be2d93e82f8d4453b252eb1000619aae&backlogId&projectId=be2d93e82f8d4453b252eb1000619aae

```

访问记录： http://10.11.65.14:8080/#/visitor 
受访记录： http://10.11.65.14:8080/#/staff/interviewRecords
访客邀约： /pages/visitor/invite/index
访客预约： /pages/visitor/reserve/index


员工角色下，待审批详情 路由：http://10.11.65.14:8080/#/staff/visitorDetail  入参 visitorBatch、projectId（租户ID）

访客角色下，重新预约/修改预约 路由： /pages/visitor/reserve/reserve-form， 入参参考 buttonKey.js 文件

提交预约，取消预约、取消同行，都是二次弹窗加刷新页面
查看凭证/待访详情  跳转路由： /pages/visitor/reserve/reserve-detail ， 入参如下：
if (type !== 'again') {
        data = {
          personName: item.beVisitPersonName,
          phoneNo: item.beVisitPhoneNum,
          reason: item.purpose,
          visitStartTime: moment(item.startTime).format('YYYY/MM/DD HH:mm'),
          visitEndTime: moment(item.endTime).format('YYYY/MM/DD HH:mm'),
          orderId: item.orderId,
          visitorBatch: item.visitorBatch,
          projectId: item.projectId,
          reserveType: 'goMiniReserve',
          type: type
        }
      } else {
        data = {
          personName: '',
          phoneNo: '',
          reason: '',
          visitStartTime: moment(new Date())
            .add(new Date().getHours() < 23 ? 1 : 0, 'H')
            .minutes(0)
            .second(0)
            .format('YYYY/MM/DD HH:mm'),
          visitEndTime: moment(new Date()).format('YYYY/MM/DD 23:59'),
          orderId: item.orderId,
          visitorBatch: item.visitorBatch,
          projectId: item.projectId,
          reserveType: 'goMiniReserve',
          type: type
        }
      }
      console.log('=====', stringfy('/pages/visitor/reserve/reserve-detail', data))
      mpx.navigateTo({
        // 小程序
        url: stringfy('/pages/visitor/reserve/reserve-detail', data)
      })

```



http://10.11.65.14:8080/#/visitor/reserve?sessionId=9ace5778-1d1e-4c40-90f7-3f8ed3a01024&projectId=b69af485a2b34135bb4b031f3a8dd61e&enterpriseName=%E4%BA%91%E7%9C%B8%E4%BC%81%E4%B8%9A%E7%94%9F%E4%BA%A7%E7%AE%A1%E7%90%862&reserveType=goMiniReserve&inDetails=undefined

https://pb.hik-cloud.com/mp-visitor-h5/index.html#/visitor/reserve-update?sessionId=2bdaaf2b-0f0e-4b71-8d1a-262b875d5a76&orderId=ecb25b53662a5f26a2b004f8eeabfa28&projectId=be2d93e82f8d4453b252eb1000619aae&visitorBatch=SO20241210170207367ho8s3_7UrPQ&reserveType=goMiniReserve&orderModel=

https://pb.hik-cloud.com/mp-visitor-h5/index.html#/visitor/reserve?type=update&reserveType=goMiniReserve&orderId=ecb25b53662a5f26a2b004f8eeabfa28&visitorBatch=SO20241210170207367ho8s3_7UrPQ&status=%E5%BE%85%E6%8B%9C%E8%AE%BF&visitorPurpose=%E5%85%B6%E4%BB%96&beVisitorPersonName=%E6%9C%8B%E5%AD%A6%E5%8F%8B&beVisitorEnterpriseName&startTime=1733821260000&endTime=1734451140000&visitorLeader=1&tenantId=be2d93e82f8d4453b252eb1000619aae&backlogId



审批逾期记录：http://10.11.65.14:8080/mpvisitor/visitor/staff/approvaHistory

受访历史记录：http://10.11.65.14:8080/mpvisitor/visitor/staff/inviteHistory

预约历史记录： http://10.11.65.14:8080/mpvisitor/visitor/visitor/history







staff/approvaHistory

visitor/history

invitation/log/doing













1、【vtenant-res】V1.14.33版本（8人天）

a>设备基本能力同步（包括在线状态、撤防、设备升级状态等）批量同步刷新，与详情页单个设备同步功能

b>添加设备管理的详情返回列表的翻页缓存功能

c>优化区域管理模糊搜索功能的交互，以及自定义表头功能重置

d>修复其他已知缺陷4个，地图组件展示设备批量导出路由返回功能等

2、【vhitom】支撑发布组件下架以及组件版本下架的功能发布 （1.5人天）

3、【云帆访客】访客1.2.5版本提测以及融合云功能联调，以及访客预约小程序、审批小程序、公众号/H5页面之前遗留缺陷评估（2.5人天）

4、【云帆消费】支撑云帆消费对接云眸单点登录功能（2.5人天）

5、【vtenant-res】支撑设备托管需求开发，后端已经列入到Q4计划中，工作量暂未评估







https://pb.hik-cloud.com/safe-center/index.html#/login/single?response_type=code&state=STATE&client_id=yunyaodevClient&redirect_uri=https%3A%2F%2F10.11.65.14%3A7777%2Flog

https://pb.hik-cloud.com/safe-center/index.html#/login/single?response_type=code&state=STATE&client_id=yunyaodevClient&redirect_uri=https%3A%2F%2Fisccems-dev2.hikyun.com

























https://visitorclouds.hikvision-secu.com:1443/mpvisitor/visitor/visitor/reserve?sessionId=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE3Mjc0NDA1ODIsImlhdCI6MTcyNzM1NDE4MiwidG9rZW4iOiJ7XCJwcm9qZWN0SWRcIjpcIjIwMDI2NTk4MjQ1NzM5MlwiLFwicHJvZHVjdENvZGVcIjpcIjE2MjMyOTM1ODk0NTkzMjBcIixcIm9wZW5JZFwiOlwib2s2YlA1TEVmallocUQ1VzlDTnFFZW56Z2gwa1wiLFwicmVnaXN0ZXJUeXBlXCI6XCJ3eGFwcFwiLFwic2Vzc2lvbktleVwiOlwieWlSc3BPL2FNTTBlQXFwK3N4ak8xQT09XCJ9In0.3gflB5V_irzVHx_u8XUcOI3BwKKrTFAuvRTG2uwEqXE&projectId=129348984536200&enterpriseName=山西通源高科贸易有限公司&reserveType=goMiniReserve&inDetails=null



?sessionId=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE3Mjc0ODcwNjQsImlhdCI6MTcyNzQwMDY2NCwidG9rZW4iOiJ7XCJwcm9qZWN0SWRcIjpcIjIwMDI2NTk4MjQ1NzM5MlwiLFwicHJvZHVjdENvZGVcIjpcIjE2MjMyOTM1ODk0NTkzMjBcIixcIm9wZW5JZFwiOlwib2s2YlA1TEVmallocUQ1VzlDTnFFZW56Z2gwa1wiLFwicmVnaXN0ZXJUeXBlXCI6XCJ3eGFwcFwiLFwic2Vzc2lvbktleVwiOlwiZmNMK01Fb0d5c1FFM1FzTjMvTnd1QT09XCJ9In0.SWuA9115QCWdwsjx4JCS3aDp_fIo36pxU8ZnqEMzeJo&projectId=129658899561608&enterpriseName=陕西蓝方电子科技有限公司&reserveType=goMiniReserve&inDetails=null



http://10.11.65.14:8080/mpvisitor/visitor/visitor/reserve?sessionId=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE3Mjc0ODcwNjQsImlhdCI6MTcyNzQwMDY2NCwidG9rZW4iOiJ7XCJwcm9qZWN0SWRcIjpcIjIwMDI2NTk4MjQ1NzM5MlwiLFwicHJvZHVjdENvZGVcIjpcIjE2MjMyOTM1ODk0NTkzMjBcIixcIm9wZW5JZFwiOlwib2s2YlA1TEVmallocUQ1VzlDTnFFZW56Z2gwa1wiLFwicmVnaXN0ZXJUeXBlXCI6XCJ3eGFwcFwiLFwic2Vzc2lvbktleVwiOlwiZmNMK01Fb0d5c1FFM1FzTjMvTnd1QT09XCJ9In0.SWuA9115QCWdwsjx4JCS3aDp_fIo36pxU8ZnqEMzeJo&projectId=129658899561608&enterpriseName=%E9%99%95%E8%A5%BF%E8%93%9D%E6%96%B9%E7%94%B5%E5%AD%90%E7%A7%91%E6%8A%80%E6%9C%89%E9%99%90%E5%85%AC%E5%8F%B8&reserveType=goMiniReserve&inDetails=null



http://10.11.65.14:8080/mpvisitor/visitor/visitor/reserve?sessionId=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE3Mjc0ODcwNjQsImlhdCI6MTcyNzQwMDY2NCwidG9rZW4iOiJ7XCJwcm9qZWN0SWRcIjpcIjIwMDI2NTk4MjQ1NzM5MlwiLFwicHJvZHVjdENvZGVcIjpcIjE2MjMyOTM1ODk0NTkzMjBcIixcIm9wZW5JZFwiOlwib2s2YlA1TEVmallocUQ1VzlDTnFFZW56Z2gwa1wiLFwicmVnaXN0ZXJUeXBlXCI6XCJ3eGFwcFwiLFwic2Vzc2lvbktleVwiOlwiZmNMK01Fb0d5c1FFM1FzTjMvTnd1QT09XCJ9In0.SWuA9115QCWdwsjx4JCS3aDp_fIo36pxU8ZnqEMzeJo&projectId=129658899561608&enterpriseName=%E9%99%95%E8%A5%BF%E8%93%9D%E6%96%B9%E7%94%B5%E5%AD%90%E7%A7%91%E6%8A%80%E6%9C%89%E9%99%90%E5%85%AC%E5%8F%B8&reserveType=goMiniReserve&inDetails=null

https://visitorclouds.hikvision-secu.com:1443/mpvisitor/visitor/visitor?sessionId=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE3Mjc1MTUwNDgsImlhdCI6MTcyNzQyODY0OCwidG9rZW4iOiJ7XCJwcm9qZWN0SWRcIjpcIjIwMDI2NTk4MjQ1NzM5MlwiLFwicHJvZHVjdENvZGVcIjpcIjE2MjMyOTM1ODk0NTkzMjBcIixcIm9wZW5JZFwiOlwib2s2YlA1TEVmallocUQ1VzlDTnFFZW56Z2gwa1wiLFwicmVnaXN0ZXJUeXBlXCI6XCJ3eGFwcFwiLFwic2Vzc2lvbktleVwiOlwiazcyZkNRQkJWU00rNjhZTzdRcDludz09XCJ9In0.E0049Q9Fxz6yeFkqdP12q8h-CfvioObAKiD3sneLcGY



https://10.11.65.14:7778/#/home?code=123&projectId=985489775071528