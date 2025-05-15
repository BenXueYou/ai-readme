# Api Documentation


**简介**:Api Documentation


**HOST**:http://10.11.64.114:8089


**联系人**:


**Version**:1.0


**接口路径**:/v3/api-docs


[TOC]






# 01_访客信息查询


## 05_待办结果回调


**接口地址**:`/webapi/visitorcs/api/v1/visitor/backlog/callBack`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.待办结果回调
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "backlogId": "",
  "backlogStatus": "",
  "backlogStatusExtraData": "",
  "backlogStatusResult": "",
  "backlogType": "",
  "backlogTypeBusinessId": "",
  "operatePersonId": "",
  "operatePersonName": "",
  "operateTime": "",
  "operateUserId": "",
  "operateUserName": "",
  "productCode": "",
  "projectId": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|backlogOperateCallbackDto|BacklogOperateCallbackDto|body|true|BacklogOperateCallbackDto|BacklogOperateCallbackDto|
|&emsp;&emsp;backlogId|||false|string||
|&emsp;&emsp;backlogStatus|||false|string||
|&emsp;&emsp;backlogStatusExtraData|||false|string||
|&emsp;&emsp;backlogStatusResult|||false|string||
|&emsp;&emsp;backlogType|||false|string||
|&emsp;&emsp;backlogTypeBusinessId|||false|string||
|&emsp;&emsp;operatePersonId|||false|string||
|&emsp;&emsp;operatePersonName|||false|string||
|&emsp;&emsp;operateTime|||false|string||
|&emsp;&emsp;operateUserId|||false|string||
|&emsp;&emsp;operateUserName|||false|string||
|&emsp;&emsp;productCode|||false|string||
|&emsp;&emsp;projectId|||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created|ActionErrorResult|
|401|Unauthorized|ActionErrorResult|
|403|Forbidden|ActionErrorResult|
|404|Not Found|ActionErrorResult|


**响应状态码-200**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


**响应状态码-201**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-401**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-403**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-404**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


## 08_查询数据库中已登录客户端数量


**接口地址**:`/webapi/visitorcs/rpc/v1/client/login/info/num`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.查询数据库中已登录客户端数量
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "productId": "bbb",
  "projectId": "aaa"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|visitorBaseRequest|VisitorBaseRequest|body|true|VisitorBaseRequest|VisitorBaseRequest|
|&emsp;&emsp;productId|产品编号||false|string||
|&emsp;&emsp;projectId|项目编号||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«int»|
|201|Created|ActionErrorResult|
|401|Unauthorized|ActionErrorResult|
|403|Forbidden|ActionErrorResult|
|404|Not Found|ActionErrorResult|


**响应状态码-200**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|integer(int32)|integer(int32)|
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": 0,
	"msg": "success"
}
```


**响应状态码-201**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-401**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-403**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-404**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


## 04_获取移动端人员的访客记录


**接口地址**:`/webapi/visitorcs/rpc/v1/mobile/visitor/info`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.获取移动端人员的访客记录
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "earlyEndTimeISO": "2018-10-29T15:33:07+08:00",
  "earlyRealEndTimeISO": "2018-10-29T15:50:07+08:00",
  "earlyRegisterTimeISO": "2018-10-29T15:33:07+08:00",
  "earlyStartTimeISO": "2018-10-29T15:33:07+08:00",
  "isDel": "1",
  "lateEndTimeISO": "2018-10-29T15:55:07+08:00",
  "lateRealEndTimeISO": "2018-10-29T15:55:07+08:00",
  "lateRegisterTimeISO": "2018-10-29T15:55:07+08:00",
  "lateStartTimeISO": "2018-10-29T15:55:07+08:00",
  "noticeRemark": "",
  "productId": "bbb",
  "projectId": "aaa",
  "retinueNum": 0,
  "updateBatch": "",
  "updateOrderId": "",
  "visitorOpenId": "1253566554"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|visitorRequest|VisitorRequest|body|true|VisitorRequest|VisitorRequest|
|&emsp;&emsp;earlyEndTimeISO|最早预计离开时间||false|object||
|&emsp;&emsp;earlyRealEndTimeISO|最早离开时间||false|object||
|&emsp;&emsp;earlyRegisterTimeISO|最早来访时间||false|object||
|&emsp;&emsp;earlyStartTimeISO|最早预计来访时间||false|object||
|&emsp;&emsp;isDel|是否删除：0删除，其他或没有值：不删除,访客注销时需要删除||true|object||
|&emsp;&emsp;lateEndTimeISO|最晚预计离开时间||false|object||
|&emsp;&emsp;lateRealEndTimeISO|最晚离开时间||false|object||
|&emsp;&emsp;lateRegisterTimeISO|最晚来访时间||false|object||
|&emsp;&emsp;lateStartTimeISO|最晚预计来访时间||false|object||
|&emsp;&emsp;noticeRemark|||false|string||
|&emsp;&emsp;productId|产品编号||false|string||
|&emsp;&emsp;projectId|项目编号||true|string||
|&emsp;&emsp;retinueNum|||false|integer(int32)||
|&emsp;&emsp;updateBatch|||false|string||
|&emsp;&emsp;updateOrderId|||false|string||
|&emsp;&emsp;visitorOpenId|访客openId||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«List«VisitorResponse»»|
|201|Created|ActionErrorResult|
|401|Unauthorized|ActionErrorResult|
|403|Forbidden|ActionErrorResult|
|404|Not Found|ActionErrorResult|


**响应状态码-200**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|array|VisitorResponse|
|&emsp;&emsp;productId|产品编号|string||
|&emsp;&emsp;projectId|项目编号|string||
|&emsp;&emsp;visitorOpenId||string||
|&emsp;&emsp;visitorUserId||string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": [
		{
			"productId": "bbb",
			"projectId": "aaa",
			"visitorOpenId": "",
			"visitorUserId": ""
		}
	],
	"msg": "success"
}
```


**响应状态码-201**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-401**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-403**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-404**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


## 01_查询今日预计来访记录


**接口地址**:`/webapi/visitorcs/rpc/v1/visitor/expected/count`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.支持根据条件查询今日预计来访记录
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "productId": "bbb",
  "projectId": "aaa"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|visitorBaseRequest|VisitorBaseRequest|body|true|VisitorBaseRequest|VisitorBaseRequest|
|&emsp;&emsp;productId|产品编号||false|string||
|&emsp;&emsp;projectId|项目编号||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«int»|
|201|Created|ActionErrorResult|
|401|Unauthorized|ActionErrorResult|
|403|Forbidden|ActionErrorResult|
|404|Not Found|ActionErrorResult|


**响应状态码-200**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|integer(int32)|integer(int32)|
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": 0,
	"msg": "success"
}
```


**响应状态码-201**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-401**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-403**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-404**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


## 03_查询访客记录-同时根据参数决定是否删除所有查询出的记录


**接口地址**:`/webapi/visitorcs/rpc/v1/visitor/info`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.支持根据条件查询访客记录
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "earlyEndTimeISO": "2018-10-29T15:33:07+08:00",
  "earlyRealEndTimeISO": "2018-10-29T15:50:07+08:00",
  "earlyRegisterTimeISO": "2018-10-29T15:33:07+08:00",
  "earlyStartTimeISO": "2018-10-29T15:33:07+08:00",
  "isDel": "1",
  "lateEndTimeISO": "2018-10-29T15:55:07+08:00",
  "lateRealEndTimeISO": "2018-10-29T15:55:07+08:00",
  "lateRegisterTimeISO": "2018-10-29T15:55:07+08:00",
  "lateStartTimeISO": "2018-10-29T15:55:07+08:00",
  "noticeRemark": "",
  "productId": "bbb",
  "projectId": "aaa",
  "retinueNum": 0,
  "updateBatch": "",
  "updateOrderId": "",
  "visitorOpenId": "1253566554"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|visitorRequest|VisitorRequest|body|true|VisitorRequest|VisitorRequest|
|&emsp;&emsp;earlyEndTimeISO|最早预计离开时间||false|object||
|&emsp;&emsp;earlyRealEndTimeISO|最早离开时间||false|object||
|&emsp;&emsp;earlyRegisterTimeISO|最早来访时间||false|object||
|&emsp;&emsp;earlyStartTimeISO|最早预计来访时间||false|object||
|&emsp;&emsp;isDel|是否删除：0删除，其他或没有值：不删除,访客注销时需要删除||true|object||
|&emsp;&emsp;lateEndTimeISO|最晚预计离开时间||false|object||
|&emsp;&emsp;lateRealEndTimeISO|最晚离开时间||false|object||
|&emsp;&emsp;lateRegisterTimeISO|最晚来访时间||false|object||
|&emsp;&emsp;lateStartTimeISO|最晚预计来访时间||false|object||
|&emsp;&emsp;noticeRemark|||false|string||
|&emsp;&emsp;productId|产品编号||false|string||
|&emsp;&emsp;projectId|项目编号||true|string||
|&emsp;&emsp;retinueNum|||false|integer(int32)||
|&emsp;&emsp;updateBatch|||false|string||
|&emsp;&emsp;updateOrderId|||false|string||
|&emsp;&emsp;visitorOpenId|访客openId||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«List«VisitorResponse»»|
|201|Created|ActionErrorResult|
|401|Unauthorized|ActionErrorResult|
|403|Forbidden|ActionErrorResult|
|404|Not Found|ActionErrorResult|


**响应状态码-200**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|array|VisitorResponse|
|&emsp;&emsp;productId|产品编号|string||
|&emsp;&emsp;projectId|项目编号|string||
|&emsp;&emsp;visitorOpenId||string||
|&emsp;&emsp;visitorUserId||string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": [
		{
			"productId": "bbb",
			"projectId": "aaa",
			"visitorOpenId": "",
			"visitorUserId": ""
		}
	],
	"msg": "success"
}
```


**响应状态码-201**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-401**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-403**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-404**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


## 06_回填预约记录访客openId及userId


**接口地址**:`/webapi/visitorcs/rpc/v1/visitor/order/update`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.回填预约记录访客openId及userId
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "productId": "bbb",
  "projectId": "aaa",
  "visitorOpenId": "1253566554",
  "visitorPhone": "1253566554",
  "visitorUserId": "1253566554"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|visitorUpdate|VisitorUpdate|body|true|VisitorUpdate|VisitorUpdate|
|&emsp;&emsp;productId|产品编号||false|string||
|&emsp;&emsp;projectId|项目编号||true|string||
|&emsp;&emsp;visitorOpenId|访客openId||false|object||
|&emsp;&emsp;visitorPhone|访客手机号||false|object||
|&emsp;&emsp;visitorUserId|访客userId||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created|ActionErrorResult|
|401|Unauthorized|ActionErrorResult|
|403|Forbidden|ActionErrorResult|
|404|Not Found|ActionErrorResult|


**响应状态码-200**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


**响应状态码-201**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-401**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-403**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-404**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


## 02_查询到访记录


**接口地址**:`/webapi/visitorcs/rpc/v1/visitor/register/count`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.支持根据条件查询到访记录
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "earlyEndTimeISO": "2018-10-29T15:33:07+08:00",
  "earlyRealEndTimeISO": "2018-10-29T15:50:07+08:00",
  "earlyRegisterTimeISO": "2018-10-29T15:33:07+08:00",
  "earlyStartTimeISO": "2018-10-29T15:33:07+08:00",
  "isDel": "1",
  "lateEndTimeISO": "2018-10-29T15:55:07+08:00",
  "lateRealEndTimeISO": "2018-10-29T15:55:07+08:00",
  "lateRegisterTimeISO": "2018-10-29T15:55:07+08:00",
  "lateStartTimeISO": "2018-10-29T15:55:07+08:00",
  "noticeRemark": "",
  "productId": "bbb",
  "projectId": "aaa",
  "retinueNum": 0,
  "updateBatch": "",
  "updateOrderId": "",
  "visitorOpenId": "1253566554"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|visitorRequest|VisitorRequest|body|true|VisitorRequest|VisitorRequest|
|&emsp;&emsp;earlyEndTimeISO|最早预计离开时间||false|object||
|&emsp;&emsp;earlyRealEndTimeISO|最早离开时间||false|object||
|&emsp;&emsp;earlyRegisterTimeISO|最早来访时间||false|object||
|&emsp;&emsp;earlyStartTimeISO|最早预计来访时间||false|object||
|&emsp;&emsp;isDel|是否删除：0删除，其他或没有值：不删除,访客注销时需要删除||true|object||
|&emsp;&emsp;lateEndTimeISO|最晚预计离开时间||false|object||
|&emsp;&emsp;lateRealEndTimeISO|最晚离开时间||false|object||
|&emsp;&emsp;lateRegisterTimeISO|最晚来访时间||false|object||
|&emsp;&emsp;lateStartTimeISO|最晚预计来访时间||false|object||
|&emsp;&emsp;noticeRemark|||false|string||
|&emsp;&emsp;productId|产品编号||false|string||
|&emsp;&emsp;projectId|项目编号||true|string||
|&emsp;&emsp;retinueNum|||false|integer(int32)||
|&emsp;&emsp;updateBatch|||false|string||
|&emsp;&emsp;updateOrderId|||false|string||
|&emsp;&emsp;visitorOpenId|访客openId||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«int»|
|201|Created|ActionErrorResult|
|401|Unauthorized|ActionErrorResult|
|403|Forbidden|ActionErrorResult|
|404|Not Found|ActionErrorResult|


**响应状态码-200**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|integer(int32)|integer(int32)|
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": 0,
	"msg": "success"
}
```


**响应状态码-201**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-401**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-403**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-404**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


## 07_回填二级审批记录openId


**接口地址**:`/webapi/visitorcs/rpc/v1/visitor/second/order/update`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.回填二级审批记录openId
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "beVisitorOpenId": "aa",
  "personId": "aa",
  "phone": "12221122",
  "productId": "12221122",
  "projectId": "12221122"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|bindOpenIdRequest|根据personId增加二级审批记录中的被访人的openId数据|body|true|BindOpenIdRequest|BindOpenIdRequest|
|&emsp;&emsp;beVisitorOpenId|beVisitorOpenId||false|string||
|&emsp;&emsp;personId|personId||false|string||
|&emsp;&emsp;phone|phone||false|string||
|&emsp;&emsp;productId|产品编号(<=32)||true|string||
|&emsp;&emsp;projectId|项目编号(<=32)||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created|ActionErrorResult|
|401|Unauthorized|ActionErrorResult|
|403|Forbidden|ActionErrorResult|
|404|Not Found|ActionErrorResult|


**响应状态码-200**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


**响应状态码-201**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-401**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-403**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-404**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


# 04_权限组管理


## 02_获取访客权限组信息


**接口地址**:`/webapi/visitorcs/ui/v1/privilege/info`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>获取访客权限组信息，用于配置自动审批的默认权限组。
 发布版本：V1.0.0</p>



**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«List«PrivilegeResponse»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|array|PrivilegeResponse|
|&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;disorder|更新序号|integer(int32)||
|&emsp;&emsp;groupId|权限组ID|string||
|&emsp;&emsp;groupName|权限组名称|string||
|&emsp;&emsp;isDefault|是否默认权限组|string||
|&emsp;&emsp;productId|产品编号|string||
|&emsp;&emsp;projectId|项目编号|string||
|&emsp;&emsp;remark|备注说明|string||
|&emsp;&emsp;select||boolean||
|&emsp;&emsp;status|状态：0正常 -1已删除|integer(int32)||
|&emsp;&emsp;updateTime|更新时间|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": [
		{
			"createTime": "2021-07-01 12:00:00",
			"disorder": 123,
			"groupId": "ccc",
			"groupName": "园区北门",
			"isDefault": "0",
			"productId": "bbb",
			"projectId": "aaa",
			"remark": "拜访",
			"select": true,
			"status": 0,
			"updateTime": "2021-07-11 12:00:00"
		}
	],
	"msg": "success"
}
```


# 09_微信公众号管理_被访人


## 04_审批通过


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/beVisitor/approval/order`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>微信公众号审批通过接口。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "beVisitorOpenId": "1253566554",
  "orderId": "asdghasdgasd",
  "productId": "",
  "projectId": "1112220",
  "remark": "asdghasdgasd",
  "visitorPrivilegeGroupIds": "123232323,2222222,33333333"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|completeParamDto|审批接口入参|body|true|CompleteParamDto|CompleteParamDto|
|&emsp;&emsp;beVisitorOpenId|微信H5使用时为必填字段，用户页面授权唯一编码：openId||true|object||
|&emsp;&emsp;orderId|访客id||true|object||
|&emsp;&emsp;productId|||false|string||
|&emsp;&emsp;projectId|项目编号||true|object||
|&emsp;&emsp;remark|备注||false|object||
|&emsp;&emsp;visitorPrivilegeGroupIds|访客权限组ids,以英文逗号分割权限组id||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 13_员工批量审批


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/beVisitor/batch/approval/order`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>微信公众号审批退回接口。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "orderIds": "[\"0a869b06f4ff4da29949acf006405c39\"]",
  "remark": "asdghasdgasd",
  "type": "approval",
  "visitorPrivilegeGroupIds": "123232323,2222222,33333333"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|batchCompleteParamDto|批量审批接口入参|body|true|BatchCompleteParamDto|BatchCompleteParamDto|
|&emsp;&emsp;orderIds|访客id||true|array|string|
|&emsp;&emsp;remark|备注||false|object||
|&emsp;&emsp;type|批量审批类型：approval(审批通过);reject(审批退回)||true|string||
|&emsp;&emsp;visitorPrivilegeGroupIds|访客权限组ids,以英文逗号分割权限组id||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 11_接受邀约


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/beVisitor/invitation/accepting`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.访客点击邀约请求，接受邀约
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "openId": "12221122",
  "orderId": "6546sdafs56adf",
  "visitorAddress": "中南海",
  "visitorBirthplace": "安徽",
  "visitorCarNumber": "浙A12321",
  "visitorCustoma": "123232323",
  "visitorCustomb": "123232323",
  "visitorCustomc": "123232323",
  "visitorCustomd": "123232323",
  "visitorCustome": "123232323",
  "visitorCustomf": "123232323",
  "visitorCustomg": "123232323",
  "visitorCustomh": "123232323",
  "visitorCustomi": "123232323",
  "visitorCustomj": "123232323",
  "visitorIdentityAddr": "安徽芜湖",
  "visitorIdentityIssuer": "芜湖公安",
  "visitorIdentityNum": "123232323",
  "visitorIdentityType": 111,
  "visitorName": "小红",
  "visitorPersonNum": 10,
  "visitorWorkUnit": "海康"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|invitationAcceptRequest|访客接受邀约请求参数|body|true|InvitationAcceptRequest|InvitationAcceptRequest|
|&emsp;&emsp;openId|访客公众号编号(<=32,可为空,微信公众号号操作时赋值,短信链接,h5不用)||false|string||
|&emsp;&emsp;orderId|预约单Id||true|string||
|&emsp;&emsp;visitorAddress|访客住址||false|string||
|&emsp;&emsp;visitorBirthplace|籍贯||false|string||
|&emsp;&emsp;visitorCarNumber|车牌号||false|string||
|&emsp;&emsp;visitorCustoma|自定义字段a||false|string||
|&emsp;&emsp;visitorCustomb|自定义字段b||false|string||
|&emsp;&emsp;visitorCustomc|自定义字段c||false|string||
|&emsp;&emsp;visitorCustomd|自定义字段d||false|string||
|&emsp;&emsp;visitorCustome|自定义字段e||false|string||
|&emsp;&emsp;visitorCustomf|自定义字段f||false|string||
|&emsp;&emsp;visitorCustomg|自定义字段g||false|string||
|&emsp;&emsp;visitorCustomh|自定义字段h||false|string||
|&emsp;&emsp;visitorCustomi|自定义字段i||false|string||
|&emsp;&emsp;visitorCustomj|自定义字段j||false|string||
|&emsp;&emsp;visitorIdentityAddr|证件地址||false|string||
|&emsp;&emsp;visitorIdentityIssuer|发证机关||false|string||
|&emsp;&emsp;visitorIdentityNum|证件号码||false|string||
|&emsp;&emsp;visitorIdentityType|证件类型||false|integer(int32)||
|&emsp;&emsp;visitorName|访客姓名||true|string||
|&emsp;&emsp;visitorPersonNum|访客人数：默认1||true|integer(int32)||
|&emsp;&emsp;visitorWorkUnit|访客所属单位||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 12_员工取消邀约


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/beVisitor/invitation/cancel`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.员工点击邀约中状态的信息，可以取消邀约
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "openId": "12221122",
  "orderId": "6546sdafs56adf"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|invitationCancelRequest|员工取消邀约请求参数|body|true|InvitationCancelRequest|InvitationCancelRequest|
|&emsp;&emsp;openId|员工公众号编号(<=32,可为空,微信公众号号操作时赋值,短信链接,h5不用)||true|string||
|&emsp;&emsp;orderId|预约单Id||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 09_发起邀约


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/beVisitor/invitation/founding`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.员工发起邀约请求
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "defaultOrderId": "12211111111111x",
  "openId": "12221122",
  "visitorEndTime": "2021-05-03T17:30:08+08:00",
  "visitorName": "小红",
  "visitorPhoneNum": "123",
  "visitorPrivilegeGroupIds": "123,1231",
  "visitorPurpose": "参观",
  "visitorStartTime": "2004-05-03T17:30:08+08:00",
  "visitorTypeId": "1"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|invitationStartRequest|员工发起邀约请求参数|body|true|InvitationStartRequest|InvitationStartRequest|
|&emsp;&emsp;defaultOrderId|默认邀约编号(供分享前生成邀约记录)||false|string||
|&emsp;&emsp;openId|用户公众号编号(<=32)||true|string||
|&emsp;&emsp;visitorEndTime|离开时间(ISO)||false|string||
|&emsp;&emsp;visitorName|访客姓名||true|string||
|&emsp;&emsp;visitorPhoneNum|访客手机号码||true|string||
|&emsp;&emsp;visitorPrivilegeGroupIds|访客拜访区域编号集合||true|string||
|&emsp;&emsp;visitorPurpose|邀请事由||false|string||
|&emsp;&emsp;visitorStartTime|来访时间(ISO)||false|string||
|&emsp;&emsp;visitorTypeId|访客类型||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«InvitationStartResponse»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|InvitationStartResponse|InvitationStartResponse|
|&emsp;&emsp;orderId|邀约编号|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"orderId": "12211111111111x"
	},
	"msg": "success"
}
```


## 10_邀约预览


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/beVisitor/invitation/wechat/{orderId}/preview`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.访客邀约信息预览
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "sceneshow": "sms"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|orderId|orderId|path|true|string||
|invitationPreviewRequest|邀约预览请求参数|body|true|InvitationPreviewRequest|InvitationPreviewRequest|
|&emsp;&emsp;sceneshow|链接打开场景(sms短信 mp_notice 微信公众号通知 mp_share 微信公众号分享 ma_share 微信小程序分享 log 记录)||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«InvitationPreviewResponse»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|InvitationPreviewResponse|InvitationPreviewResponse|
|&emsp;&emsp;approvalResult||string||
|&emsp;&emsp;authBarCode|访客二维码|string||
|&emsp;&emsp;beVisitorGroupName||string||
|&emsp;&emsp;beVisitorOpenId|被访人微信公众号openid|string||
|&emsp;&emsp;beVisitorPersonName|被访人姓名|string||
|&emsp;&emsp;beVisitorPhoneNum|被访人手机号码|string||
|&emsp;&emsp;endTime||string||
|&emsp;&emsp;startTime||string||
|&emsp;&emsp;status|记录状态。0：待审核；1：正常；2：迟到；3：失效；4：审核退回；5：超期自动签离；6：已签离；7：超期未签离；8：已到达；9：审核失效；10：邀约中；11：邀约失效|integer(int32)||
|&emsp;&emsp;visitorAddress|访客住址|string||
|&emsp;&emsp;visitorBirthplace|籍贯|string||
|&emsp;&emsp;visitorCarNumber|车牌号|string||
|&emsp;&emsp;visitorCustoma|自定义字段a|string||
|&emsp;&emsp;visitorCustomb|自定义字段b|string||
|&emsp;&emsp;visitorCustomc|自定义字段c|string||
|&emsp;&emsp;visitorCustomd|自定义字段d|string||
|&emsp;&emsp;visitorCustome|自定义字段e|string||
|&emsp;&emsp;visitorCustomf|自定义字段f|string||
|&emsp;&emsp;visitorCustomg|自定义字段g|string||
|&emsp;&emsp;visitorCustomh|自定义字段h|string||
|&emsp;&emsp;visitorCustomi|自定义字段i|string||
|&emsp;&emsp;visitorCustomj|自定义字段j|string||
|&emsp;&emsp;visitorEndTime|预计离开时间,必须晚于当前时间和预计来访时间|string||
|&emsp;&emsp;visitorIdentityAddr|证件地址|string||
|&emsp;&emsp;visitorIdentityIssuer|发证机关|string||
|&emsp;&emsp;visitorIdentityNum|证件号码|string||
|&emsp;&emsp;visitorIdentityType|证件类型|integer(int32)||
|&emsp;&emsp;visitorName|访客姓名|string||
|&emsp;&emsp;visitorPersonNum|访客人数：默认1|integer(int32)||
|&emsp;&emsp;visitorPhoneNum||string||
|&emsp;&emsp;visitorPhoto||string||
|&emsp;&emsp;visitorPurpose|来访事由,长度为1～128个字符|string||
|&emsp;&emsp;visitorStartTime|预计来访时间|string||
|&emsp;&emsp;visitorTypeId|访客类型|string||
|&emsp;&emsp;visitorWorkUnit|访客所属单位|string||
|&emsp;&emsp;weChatMpName|公众号名称|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"approvalResult": "",
		"authBarCode": "123",
		"beVisitorGroupName": "",
		"beVisitorOpenId": "12221xsssa",
		"beVisitorPersonName": "小红",
		"beVisitorPhoneNum": "18235642566",
		"endTime": "",
		"startTime": "",
		"status": 123,
		"visitorAddress": "中南海",
		"visitorBirthplace": "安徽",
		"visitorCarNumber": "浙A12321",
		"visitorCustoma": "123232323",
		"visitorCustomb": "123232323",
		"visitorCustomc": "123232323",
		"visitorCustomd": "123232323",
		"visitorCustome": "123232323",
		"visitorCustomf": "123",
		"visitorCustomg": "123",
		"visitorCustomh": "123",
		"visitorCustomi": "123",
		"visitorCustomj": "123",
		"visitorEndTime": "2004-05-03T18:30:08+08:00",
		"visitorIdentityAddr": "安徽芜湖",
		"visitorIdentityIssuer": "芜湖公安",
		"visitorIdentityNum": "123232323",
		"visitorIdentityType": 111,
		"visitorName": "小红",
		"visitorPersonNum": 10,
		"visitorPhoneNum": "",
		"visitorPhoto": "",
		"visitorPurpose": "参观",
		"visitorStartTime": "2004-05-03T17:30:08+08:00",
		"visitorTypeId": "1",
		"visitorWorkUnit": "海康",
		"weChatMpName": "10"
	},
	"msg": "success"
}
```


## 06_被访人微信预约取消接口


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/beVisitor/order/cancel`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>被访人微信预约取消接口。
 发布版本：V1.0.0</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|orderId|orderId|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 02_查询预约记录详情


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/beVisitor/record/detail`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>微信公众号查询被访记录详情接口。
 发布版本：V1.0.0</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|orderId|orderId|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«OrderResponse»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|OrderResponse|OrderResponse|
|&emsp;&emsp;approvalResult||string||
|&emsp;&emsp;authBarCode|访客二维码|string||
|&emsp;&emsp;authIdentityPid|身份证序列号|string||
|&emsp;&emsp;authTempCard|访客卡号|string||
|&emsp;&emsp;authVisitorCode|访客验证码|string||
|&emsp;&emsp;backlogId||string||
|&emsp;&emsp;beVisitorGroupId|被访人部门ID|string||
|&emsp;&emsp;beVisitorGroupName|被访人部门名称|string||
|&emsp;&emsp;beVisitorOpenId|被访人openid|string||
|&emsp;&emsp;beVisitorPersonId|被访人ID|string||
|&emsp;&emsp;beVisitorPersonName|被访人名称|string||
|&emsp;&emsp;beVisitorPhoneNum|被访人手机号|string||
|&emsp;&emsp;beVisitorUserId||string||
|&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;createUserType|创建者身份类型：1-平台用户，2-内部人员，3-来访人员|integer(int32)||
|&emsp;&emsp;disorder|添加序号|integer(int32)||
|&emsp;&emsp;endTime|预计离开时间|string||
|&emsp;&emsp;endTimeDifference|预计离开时间时差|string||
|&emsp;&emsp;endTimeUTC|预计离开时间UTC|integer(int64)||
|&emsp;&emsp;orderId|预约单号|string||
|&emsp;&emsp;orderModel|预约模式 person:指定人员预约 space:场地预约|string||
|&emsp;&emsp;processId|审批规则id|string||
|&emsp;&emsp;processItemId|审批规则实例id|string||
|&emsp;&emsp;processRemark|备注|string||
|&emsp;&emsp;productId|产品编号|string||
|&emsp;&emsp;projectId|项目编号|string||
|&emsp;&emsp;realEndTime|签离时间|string||
|&emsp;&emsp;realEndTimeDifference|签离时间时差|string||
|&emsp;&emsp;realEndTimeUTC|签离时间UTC|integer(int64)||
|&emsp;&emsp;registerPlace|访客登记地点|string||
|&emsp;&emsp;registerTime|登记时间|string||
|&emsp;&emsp;registerTimeDifference|登记时间时差|string||
|&emsp;&emsp;registerTimeUTC|登记时间UTC|integer(int64)||
|&emsp;&emsp;startTime|预计来访时间|string||
|&emsp;&emsp;startTimeDifference|预计来访时间时差|string||
|&emsp;&emsp;startTimeUTC|预计来访时间UTC|integer(int64)||
|&emsp;&emsp;status|记录状态。0：待审批；1：正常；2：迟到；3：预约逾期；4：审批退回；5：超期自动签离；6：访客签离；7：超期未签离；8：已到达；9：审批逾期；10：邀约中；11：邀约逾期；12：邀约失效(员工取消)；13：邀约失效(访客取消)；14：预约失效(员工取消)；15：预约失效(访客取消)|integer(int32)||
|&emsp;&emsp;svrCodeIdentity|证件照对应图片服务器serviceNodes|string||
|&emsp;&emsp;svrCodeScanning|证件扫描照对应图片服务器serviceNodes|string||
|&emsp;&emsp;svrCodeVisitor|访客头像对应图片服务器serviceNodes|string||
|&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;visitBatch|访客批次|string||
|&emsp;&emsp;visitorAddress|访客住址|string||
|&emsp;&emsp;visitorAllowTimes|访客进入次数|integer(int32)||
|&emsp;&emsp;visitorBirthplace|籍贯|string||
|&emsp;&emsp;visitorCarNumber|车牌号|string||
|&emsp;&emsp;visitorCustoma|自定义字段a：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomb|自定义字段b：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomc|自定义字段c：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomd|自定义字段d：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustome|自定义字段e：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomf|自定义字段f：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomg|自定义字段g：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomh|自定义字段h：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomi|自定义字段i：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomj|自定义字段j：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorGroupId|访客名单分组ID|string||
|&emsp;&emsp;visitorIdentityAddr|证件地址|string||
|&emsp;&emsp;visitorIdentityIssuer|发证机关|string||
|&emsp;&emsp;visitorIdentityNum|证件号码|string||
|&emsp;&emsp;visitorIdentityPhoto|证件照片|string||
|&emsp;&emsp;visitorIdentityType|证件类型：111、身份证|integer(int32)||
|&emsp;&emsp;visitorName|姓名|string||
|&emsp;&emsp;visitorOpenId|访客微信公众号唯一标识|string||
|&emsp;&emsp;visitorPersonNum|来访人数|integer(int32)||
|&emsp;&emsp;visitorPhoneNum|手机号|string||
|&emsp;&emsp;visitorPhoto|访客头像|string||
|&emsp;&emsp;visitorPhotoFlag|人脸质量合格标识。0：合格；1：不合格|string||
|&emsp;&emsp;visitorPinyin|访客名首字母缩写|string||
|&emsp;&emsp;visitorPrivilegeGroupIds|访客权限组ids|string||
|&emsp;&emsp;visitorPurpose|来访事由|string||
|&emsp;&emsp;visitorScanningPhoto|证件扫描照片|string||
|&emsp;&emsp;visitorSex|性别：1、男；2、女|integer(int32)||
|&emsp;&emsp;visitorTemperature|访客体温|string||
|&emsp;&emsp;visitorTemperatureStatus|访客体温状态|integer(int32)||
|&emsp;&emsp;visitorTypeId|访客类型id|string||
|&emsp;&emsp;visitorUserId||string||
|&emsp;&emsp;visitorWorkUnit|访客来访单位|string||
|&emsp;&emsp;webLabel|记录状态描述-web端|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"approvalResult": "",
		"authBarCode": "123",
		"authIdentityPid": "123",
		"authTempCard": "123",
		"authVisitorCode": "123",
		"backlogId": "",
		"beVisitorGroupId": "123",
		"beVisitorGroupName": "123",
		"beVisitorOpenId": "123",
		"beVisitorPersonId": "123",
		"beVisitorPersonName": "123",
		"beVisitorPhoneNum": "123",
		"beVisitorUserId": "",
		"createTime": "123",
		"createUserType": 123,
		"disorder": 123,
		"endTime": "123",
		"endTimeDifference": "123",
		"endTimeUTC": 123,
		"orderId": "123",
		"orderModel": "person",
		"processId": "123",
		"processItemId": "123",
		"processRemark": "123",
		"productId": "123",
		"projectId": "123",
		"realEndTime": "123",
		"realEndTimeDifference": "123",
		"realEndTimeUTC": 123,
		"registerPlace": "123",
		"registerTime": "123",
		"registerTimeDifference": "123",
		"registerTimeUTC": 123,
		"startTime": "123",
		"startTimeDifference": "123",
		"startTimeUTC": 123,
		"status": 123,
		"svrCodeIdentity": "123",
		"svrCodeScanning": "123",
		"svrCodeVisitor": "123",
		"updateTime": "123",
		"visitBatch": "123",
		"visitorAddress": "123",
		"visitorAllowTimes": 123,
		"visitorBirthplace": "123",
		"visitorCarNumber": "123",
		"visitorCustoma": "123",
		"visitorCustomb": "123",
		"visitorCustomc": "123",
		"visitorCustomd": "123",
		"visitorCustome": "123",
		"visitorCustomf": "123",
		"visitorCustomg": "123",
		"visitorCustomh": "123",
		"visitorCustomi": "123",
		"visitorCustomj": "123",
		"visitorGroupId": "123",
		"visitorIdentityAddr": "123",
		"visitorIdentityIssuer": "123",
		"visitorIdentityNum": "123",
		"visitorIdentityPhoto": "123",
		"visitorIdentityType": 123,
		"visitorName": "123",
		"visitorOpenId": "123",
		"visitorPersonNum": 123,
		"visitorPhoneNum": "123",
		"visitorPhoto": "123",
		"visitorPhotoFlag": "123",
		"visitorPinyin": "123",
		"visitorPrivilegeGroupIds": "123",
		"visitorPurpose": "123",
		"visitorScanningPhoto": "123",
		"visitorSex": 123,
		"visitorTemperature": "123",
		"visitorTemperatureStatus": 123,
		"visitorTypeId": "123",
		"visitorUserId": "",
		"visitorWorkUnit": "123",
		"webLabel": "123"
	},
	"msg": "success"
}
```


## 03_查询有访问记录的日期


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/beVisitor/record/orderDay`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>微信公众号查询有访问记录的日期接口。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "beVisitorOpenId": "1253566554",
  "earlyStartTimeISO": "2018-10-29T15:33:07+08:00",
  "lateStartTimeISO": "2018-10-29T15:55:07+08:00",
  "projectId": "1112220",
  "statusList": "653232"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|orderDayDto|访客微信预约查询信息对象|body|true|OrderDayDto|OrderDayDto|
|&emsp;&emsp;beVisitorOpenId|微信H5使用时为必填字段，用户页面授权唯一编码：openId||true|object||
|&emsp;&emsp;earlyStartTimeISO|最早预计来访时间||false|object||
|&emsp;&emsp;lateStartTimeISO|最晚预计来访时间||false|object||
|&emsp;&emsp;projectId|项目编号||true|object||
|&emsp;&emsp;statusList|预约单状态状态||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«Set«string»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|array||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": [],
	"msg": "success"
}
```


## 01_查询预约记录：支持查询被访记录，审批记录


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/beVisitor/record/page`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>微信公众号预约记录查询接口：支持查询被访记录，审批记录。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "backlogId": "bbb",
  "beVisitorOpenId": "1253566554",
  "beVisitorPersonId": "6546sdafs56adf",
  "beVisitorPersonName": "小东",
  "cardNo": "1234567890",
  "disorder": 123,
  "earlyEndTimeISO": "2018-10-29T15:33:07+08:00",
  "earlyRealEndTimeISO": "2018-10-29T15:50:07+08:00",
  "earlyRegisterTimeISO": "2018-10-29T15:33:07+08:00",
  "earlyStartTimeISO": "2018-10-29T15:33:07+08:00",
  "identityId": "111",
  "lateEndTimeISO": "2018-10-29T15:55:07+08:00",
  "lateRealEndTimeISO": "2018-10-29T15:55:07+08:00",
  "lateRegisterTimeISO": "2018-10-29T15:55:07+08:00",
  "lateStartTimeISO": "2018-10-29T15:55:07+08:00",
  "maxTemperature": "42",
  "minTemperature": "38",
  "orderId": "1253566554",
  "pageNo": "3",
  "pageSize": "50",
  "productId": "bbb",
  "projectId": "aaa",
  "projectIdList": "[\"0a869b06f4ff4da29949acf006405c39\"]",
  "qrCode": "1234567890",
  "registerPlace": "aaa1112ssfddd",
  "sort": "desc",
  "statusList": "0",
  "temperatureStatus": 0,
  "type": "1",
  "visitorAddress": "访客住址",
  "visitorBirthplace": "籍贯",
  "visitorCarNumber": "浙A32216",
  "visitorCode": "1234",
  "visitorCustoma": "1253566554",
  "visitorCustomb": "1253566554",
  "visitorCustomc": "1253566554",
  "visitorCustomd": "1253566554",
  "visitorCustome": "1253566554",
  "visitorCustomf": "1253566554",
  "visitorCustomg": "1253566554",
  "visitorCustomh": "1253566554",
  "visitorCustomi": "1253566554",
  "visitorCustomj": "1253566554",
  "visitorIdentityAddr": "证件地址",
  "visitorIdentityIssuer": "发证机关",
  "visitorIdentityNum": "32165165165161",
  "visitorName": "小红",
  "visitorOpenId": "1253566554",
  "visitorPhoneNum": "1253566554",
  "visitorPurpose": "参观",
  "visitorSex": "1",
  "visitorSexs": "[1,0]",
  "visitorTypeId": "1",
  "visitorWorkUnit": "访客所在公司"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|orderRequest|OrderRequest|body|true|OrderRequest|OrderRequest|
|&emsp;&emsp;backlogId|待办编号||false|string||
|&emsp;&emsp;beVisitorOpenId|被访人openId||false|object||
|&emsp;&emsp;beVisitorPersonId|被访人ID||false|object||
|&emsp;&emsp;beVisitorPersonName|被访人姓名||false|object||
|&emsp;&emsp;cardNo|卡号||false|object||
|&emsp;&emsp;disorder|更新顺序||false|integer(int32)||
|&emsp;&emsp;earlyEndTimeISO|最早预计离开时间||false|object||
|&emsp;&emsp;earlyRealEndTimeISO|最早离开时间||false|object||
|&emsp;&emsp;earlyRegisterTimeISO|最早来访时间||false|object||
|&emsp;&emsp;earlyStartTimeISO|最早预计来访时间||false|object||
|&emsp;&emsp;identityId|证件类型：111身份证，335驾驶证，131工作证，133学生证，114军官证，414护照，990其他||false|object||
|&emsp;&emsp;lateEndTimeISO|最晚预计离开时间||false|object||
|&emsp;&emsp;lateRealEndTimeISO|最晚离开时间||false|object||
|&emsp;&emsp;lateRegisterTimeISO|最晚来访时间||false|object||
|&emsp;&emsp;lateStartTimeISO|最晚预计来访时间||false|object||
|&emsp;&emsp;maxTemperature|最高体温||false|string||
|&emsp;&emsp;minTemperature|最低体温||false|string||
|&emsp;&emsp;orderId|orderId||false|object||
|&emsp;&emsp;pageNo|查询时第几页||true|object||
|&emsp;&emsp;pageSize|查询时单页条数,限定大小不能超过1000||true|object||
|&emsp;&emsp;productId|产品编号||false|string||
|&emsp;&emsp;projectId|项目编号||false|string||
|&emsp;&emsp;projectIdList|项目编号集合||false|array|string|
|&emsp;&emsp;qrCode|二维码内容||false|object||
|&emsp;&emsp;registerPlace|访客登记地点||false|object||
|&emsp;&emsp;sort|排序方式：desc:按预计来访时间倒序，asc:按预计来访时间正序：||false|string||
|&emsp;&emsp;statusList|预约状态的集合:0：待审批；1：正常；2：迟到；3：预约逾期；4：审批退回；5：超期自动签离；6：访客签离；7：超期未签离；8：已到达；9：审批逾期；10：邀约中；11：邀约逾期；12：邀约失效(员工取消)；13：邀约失效(访客取消)；14：预约失效(员工取消)；15：预约失效(访客取消)||false|object||
|&emsp;&emsp;temperatureStatus|体温状态(0正常，1异常)||false|integer(int32)||
|&emsp;&emsp;type|查询类型:(0：被访记录，1：审批记录，2：邀约记录---微信端使用）,（3:预约记录，4：来访记录----web端使用)||false|string||
|&emsp;&emsp;visitorAddress|访客住址||false|object||
|&emsp;&emsp;visitorBirthplace|籍贯||false|object||
|&emsp;&emsp;visitorCarNumber|车牌号||false|object||
|&emsp;&emsp;visitorCode|访客验证码||false|object||
|&emsp;&emsp;visitorCustoma|自定义字段a||false|object||
|&emsp;&emsp;visitorCustomb|自定义字段b||false|object||
|&emsp;&emsp;visitorCustomc|自定义字段c||false|object||
|&emsp;&emsp;visitorCustomd|自定义字段d||false|object||
|&emsp;&emsp;visitorCustome|自定义字段e||false|object||
|&emsp;&emsp;visitorCustomf|自定义字段f||false|object||
|&emsp;&emsp;visitorCustomg|自定义字段g||false|object||
|&emsp;&emsp;visitorCustomh|自定义字段h||false|object||
|&emsp;&emsp;visitorCustomi|自定义字段i||false|object||
|&emsp;&emsp;visitorCustomj|自定义字段j||false|object||
|&emsp;&emsp;visitorIdentityAddr|证件地址||false|object||
|&emsp;&emsp;visitorIdentityIssuer|发证机关||false|object||
|&emsp;&emsp;visitorIdentityNum|证件号码||false|object||
|&emsp;&emsp;visitorName|访客姓名||false|object||
|&emsp;&emsp;visitorOpenId|访客openId||false|object||
|&emsp;&emsp;visitorPhoneNum|手机号||false|object||
|&emsp;&emsp;visitorPurpose|来访事由||false|object||
|&emsp;&emsp;visitorSex|性别,1男,2女||false|object||
|&emsp;&emsp;visitorSexs|访客性别集合||false|object||
|&emsp;&emsp;visitorTypeId|访客类型||false|object||
|&emsp;&emsp;visitorWorkUnit|访客来访单位||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PageResult«OrderResponse»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PageResult«OrderResponse»|PageResult«OrderResponse»|
|&emsp;&emsp;list|数据信息|array|OrderResponse|
|&emsp;&emsp;&emsp;&emsp;approvalResult||string||
|&emsp;&emsp;&emsp;&emsp;authBarCode|访客二维码|string||
|&emsp;&emsp;&emsp;&emsp;authIdentityPid|身份证序列号|string||
|&emsp;&emsp;&emsp;&emsp;authTempCard|访客卡号|string||
|&emsp;&emsp;&emsp;&emsp;authVisitorCode|访客验证码|string||
|&emsp;&emsp;&emsp;&emsp;backlogId||string||
|&emsp;&emsp;&emsp;&emsp;beVisitorGroupId|被访人部门ID|string||
|&emsp;&emsp;&emsp;&emsp;beVisitorGroupName|被访人部门名称|string||
|&emsp;&emsp;&emsp;&emsp;beVisitorOpenId|被访人openid|string||
|&emsp;&emsp;&emsp;&emsp;beVisitorPersonId|被访人ID|string||
|&emsp;&emsp;&emsp;&emsp;beVisitorPersonName|被访人名称|string||
|&emsp;&emsp;&emsp;&emsp;beVisitorPhoneNum|被访人手机号|string||
|&emsp;&emsp;&emsp;&emsp;beVisitorUserId||string||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;createUserType|创建者身份类型：1-平台用户，2-内部人员，3-来访人员|integer||
|&emsp;&emsp;&emsp;&emsp;disorder|添加序号|integer||
|&emsp;&emsp;&emsp;&emsp;endTime|预计离开时间|string||
|&emsp;&emsp;&emsp;&emsp;endTimeDifference|预计离开时间时差|string||
|&emsp;&emsp;&emsp;&emsp;endTimeUTC|预计离开时间UTC|integer||
|&emsp;&emsp;&emsp;&emsp;orderId|预约单号|string||
|&emsp;&emsp;&emsp;&emsp;orderModel|预约模式 person:指定人员预约 space:场地预约|string||
|&emsp;&emsp;&emsp;&emsp;processId|审批规则id|string||
|&emsp;&emsp;&emsp;&emsp;processItemId|审批规则实例id|string||
|&emsp;&emsp;&emsp;&emsp;processRemark|备注|string||
|&emsp;&emsp;&emsp;&emsp;productId|产品编号|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目编号|string||
|&emsp;&emsp;&emsp;&emsp;realEndTime|签离时间|string||
|&emsp;&emsp;&emsp;&emsp;realEndTimeDifference|签离时间时差|string||
|&emsp;&emsp;&emsp;&emsp;realEndTimeUTC|签离时间UTC|integer||
|&emsp;&emsp;&emsp;&emsp;registerPlace|访客登记地点|string||
|&emsp;&emsp;&emsp;&emsp;registerTime|登记时间|string||
|&emsp;&emsp;&emsp;&emsp;registerTimeDifference|登记时间时差|string||
|&emsp;&emsp;&emsp;&emsp;registerTimeUTC|登记时间UTC|integer||
|&emsp;&emsp;&emsp;&emsp;startTime|预计来访时间|string||
|&emsp;&emsp;&emsp;&emsp;startTimeDifference|预计来访时间时差|string||
|&emsp;&emsp;&emsp;&emsp;startTimeUTC|预计来访时间UTC|integer||
|&emsp;&emsp;&emsp;&emsp;status|记录状态。0：待审批；1：正常；2：迟到；3：预约逾期；4：审批退回；5：超期自动签离；6：访客签离；7：超期未签离；8：已到达；9：审批逾期；10：邀约中；11：邀约逾期；12：邀约失效(员工取消)；13：邀约失效(访客取消)；14：预约失效(员工取消)；15：预约失效(访客取消)|integer||
|&emsp;&emsp;&emsp;&emsp;svrCodeIdentity|证件照对应图片服务器serviceNodes|string||
|&emsp;&emsp;&emsp;&emsp;svrCodeScanning|证件扫描照对应图片服务器serviceNodes|string||
|&emsp;&emsp;&emsp;&emsp;svrCodeVisitor|访客头像对应图片服务器serviceNodes|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;&emsp;&emsp;visitBatch|访客批次|string||
|&emsp;&emsp;&emsp;&emsp;visitorAddress|访客住址|string||
|&emsp;&emsp;&emsp;&emsp;visitorAllowTimes|访客进入次数|integer||
|&emsp;&emsp;&emsp;&emsp;visitorBirthplace|籍贯|string||
|&emsp;&emsp;&emsp;&emsp;visitorCarNumber|车牌号|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustoma|自定义字段a：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomb|自定义字段b：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomc|自定义字段c：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomd|自定义字段d：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustome|自定义字段e：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomf|自定义字段f：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomg|自定义字段g：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomh|自定义字段h：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomi|自定义字段i：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomj|自定义字段j：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorGroupId|访客名单分组ID|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityAddr|证件地址|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityIssuer|发证机关|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityNum|证件号码|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityPhoto|证件照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityType|证件类型：111、身份证|integer||
|&emsp;&emsp;&emsp;&emsp;visitorName|姓名|string||
|&emsp;&emsp;&emsp;&emsp;visitorOpenId|访客微信公众号唯一标识|string||
|&emsp;&emsp;&emsp;&emsp;visitorPersonNum|来访人数|integer||
|&emsp;&emsp;&emsp;&emsp;visitorPhoneNum|手机号|string||
|&emsp;&emsp;&emsp;&emsp;visitorPhoto|访客头像|string||
|&emsp;&emsp;&emsp;&emsp;visitorPhotoFlag|人脸质量合格标识。0：合格；1：不合格|string||
|&emsp;&emsp;&emsp;&emsp;visitorPinyin|访客名首字母缩写|string||
|&emsp;&emsp;&emsp;&emsp;visitorPrivilegeGroupIds|访客权限组ids|string||
|&emsp;&emsp;&emsp;&emsp;visitorPurpose|来访事由|string||
|&emsp;&emsp;&emsp;&emsp;visitorScanningPhoto|证件扫描照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorSex|性别：1、男；2、女|integer||
|&emsp;&emsp;&emsp;&emsp;visitorTemperature|访客体温|string||
|&emsp;&emsp;&emsp;&emsp;visitorTemperatureStatus|访客体温状态|integer||
|&emsp;&emsp;&emsp;&emsp;visitorTypeId|访客类型id|string||
|&emsp;&emsp;&emsp;&emsp;visitorUserId||string||
|&emsp;&emsp;&emsp;&emsp;visitorWorkUnit|访客来访单位|string||
|&emsp;&emsp;&emsp;&emsp;webLabel|记录状态描述-web端|string||
|&emsp;&emsp;pageNo|页码|integer(int32)||
|&emsp;&emsp;pageSize|页大小|integer(int32)||
|&emsp;&emsp;total|总条数|integer(int64)||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"list": [
			{
				"approvalResult": "",
				"authBarCode": "123",
				"authIdentityPid": "123",
				"authTempCard": "123",
				"authVisitorCode": "123",
				"backlogId": "",
				"beVisitorGroupId": "123",
				"beVisitorGroupName": "123",
				"beVisitorOpenId": "123",
				"beVisitorPersonId": "123",
				"beVisitorPersonName": "123",
				"beVisitorPhoneNum": "123",
				"beVisitorUserId": "",
				"createTime": "123",
				"createUserType": 123,
				"disorder": 123,
				"endTime": "123",
				"endTimeDifference": "123",
				"endTimeUTC": 123,
				"orderId": "123",
				"orderModel": "person",
				"processId": "123",
				"processItemId": "123",
				"processRemark": "123",
				"productId": "123",
				"projectId": "123",
				"realEndTime": "123",
				"realEndTimeDifference": "123",
				"realEndTimeUTC": 123,
				"registerPlace": "123",
				"registerTime": "123",
				"registerTimeDifference": "123",
				"registerTimeUTC": 123,
				"startTime": "123",
				"startTimeDifference": "123",
				"startTimeUTC": 123,
				"status": 123,
				"svrCodeIdentity": "123",
				"svrCodeScanning": "123",
				"svrCodeVisitor": "123",
				"updateTime": "123",
				"visitBatch": "123",
				"visitorAddress": "123",
				"visitorAllowTimes": 123,
				"visitorBirthplace": "123",
				"visitorCarNumber": "123",
				"visitorCustoma": "123",
				"visitorCustomb": "123",
				"visitorCustomc": "123",
				"visitorCustomd": "123",
				"visitorCustome": "123",
				"visitorCustomf": "123",
				"visitorCustomg": "123",
				"visitorCustomh": "123",
				"visitorCustomi": "123",
				"visitorCustomj": "123",
				"visitorGroupId": "123",
				"visitorIdentityAddr": "123",
				"visitorIdentityIssuer": "123",
				"visitorIdentityNum": "123",
				"visitorIdentityPhoto": "123",
				"visitorIdentityType": 123,
				"visitorName": "123",
				"visitorOpenId": "123",
				"visitorPersonNum": 123,
				"visitorPhoneNum": "123",
				"visitorPhoto": "123",
				"visitorPhotoFlag": "123",
				"visitorPinyin": "123",
				"visitorPrivilegeGroupIds": "123",
				"visitorPurpose": "123",
				"visitorScanningPhoto": "123",
				"visitorSex": 123,
				"visitorTemperature": "123",
				"visitorTemperatureStatus": 123,
				"visitorTypeId": "123",
				"visitorUserId": "",
				"visitorWorkUnit": "123",
				"webLabel": "123"
			}
		],
		"pageNo": 1,
		"pageSize": 20,
		"total": 5
	},
	"msg": "success"
}
```


## 05_审批退回


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/beVisitor/reject/order`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>微信公众号审批退回接口。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "beVisitorOpenId": "1253566554",
  "orderId": "asdghasdgasd",
  "productId": "",
  "projectId": "1112220",
  "remark": "asdghasdgasd",
  "visitorPrivilegeGroupIds": "123232323,2222222,33333333"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|completeParamDto|审批接口入参|body|true|CompleteParamDto|CompleteParamDto|
|&emsp;&emsp;beVisitorOpenId|微信H5使用时为必填字段，用户页面授权唯一编码：openId||true|object||
|&emsp;&emsp;orderId|访客id||true|object||
|&emsp;&emsp;productId|||false|string||
|&emsp;&emsp;projectId|项目编号||true|object||
|&emsp;&emsp;remark|备注||false|object||
|&emsp;&emsp;visitorPrivilegeGroupIds|访客权限组ids,以英文逗号分割权限组id||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


# 10_微信公众号管理_访客


## 08_校验被访人信息并返回被访人名称


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/visitor/check/beVisitor`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>校验被访人信息并返回被访人名称。
 发布版本：V1.0.0</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|openId|访客微信openId|query|true|string||
|phoneNo|被访人手机号|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«string»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": "",
	"msg": "success"
}
```


## 06_查询访客信息字段


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/visitor/field/info`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>查询访客信息字段(基础字段，自定义字段，来访事由，访客类型)。
 发布版本：V1.0.0</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|appId|微信appId|query|true|string||
|type|操作类型：0：访客，1：被访人|query|true|string||
|orderModel|orderModel|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«List«FieldResponse»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|array|FieldResponse|
|&emsp;&emsp;dataList||array|DataDictionarySingleDto|
|&emsp;&emsp;&emsp;&emsp;selected||boolean||
|&emsp;&emsp;&emsp;&emsp;text||string||
|&emsp;&emsp;&emsp;&emsp;value||object||
|&emsp;&emsp;fieldInfoDto||FieldInfoDto|FieldInfoDto|
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;customOption|自定义选择框的枚举值|object||
|&emsp;&emsp;&emsp;&emsp;dataValue|关联的枚举值|string||
|&emsp;&emsp;&emsp;&emsp;defaultValue|默认字段|string||
|&emsp;&emsp;&emsp;&emsp;disorder|更新顺序|integer||
|&emsp;&emsp;&emsp;&emsp;display|是否可见，0表示可见，1表示不可见|string||
|&emsp;&emsp;&emsp;&emsp;fieldProperties|字段属性：0：访客信息字段，1：被访人信息字段|string||
|&emsp;&emsp;&emsp;&emsp;fieldType|参数类型|string||
|&emsp;&emsp;&emsp;&emsp;hint|表单项的提示信息|string||
|&emsp;&emsp;&emsp;&emsp;maxLength|最大字段长度|integer||
|&emsp;&emsp;&emsp;&emsp;overseas|是否支持海外|string||
|&emsp;&emsp;&emsp;&emsp;paraId|paraId|string||
|&emsp;&emsp;&emsp;&emsp;paraKey|表单项名称key|string||
|&emsp;&emsp;&emsp;&emsp;paraName|表单项名称|string||
|&emsp;&emsp;&emsp;&emsp;placeholder|表单项的placeholder，vue-i18n多语言的key，比如人员民族中的请选择提示|string||
|&emsp;&emsp;&emsp;&emsp;productId|产品编号|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目编号|string||
|&emsp;&emsp;&emsp;&emsp;readOnly|是否可修改，0表示不可修改,1表示可修改|string||
|&emsp;&emsp;&emsp;&emsp;regular|表单的正则表达式|string||
|&emsp;&emsp;&emsp;&emsp;required|是否必填，0表示必填，1表示非必填|string||
|&emsp;&emsp;&emsp;&emsp;showType|表单项类型。1：input；2：select；3：data-picker；6：pic|string||
|&emsp;&emsp;&emsp;&emsp;status|访客字段状态：0正常 -1已删除|integer||
|&emsp;&emsp;&emsp;&emsp;tips|提示信息|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;subHint||string||
|&emsp;&emsp;subParaKey||string||
|&emsp;&emsp;subParaName||string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": [
		{
			"dataList": [
				{
					"selected": true,
					"text": "",
					"value": {}
				}
			],
			"fieldInfoDto": {
				"createTime": "2021-07-01 12:00:00",
				"customOption": "123",
				"dataValue": "123",
				"defaultValue": "其他",
				"disorder": 1,
				"display": "1",
				"fieldProperties": "0",
				"fieldType": "1",
				"hint": "123",
				"maxLength": 11,
				"overseas": "1",
				"paraId": "ccc",
				"paraKey": "123",
				"paraName": "aaa",
				"placeholder": "123",
				"productId": "bbb",
				"projectId": "aaa",
				"readOnly": "1",
				"regular": "123",
				"required": "1",
				"showType": "1",
				"status": 0,
				"tips": "输入车牌号码信息可作为您去拜访时的停车凭证",
				"updateTime": "2021-07-11 12:00:00"
			},
			"subHint": "",
			"subParaKey": "",
			"subParaName": ""
		}
	],
	"msg": "success"
}
```


## 13_公众号上传预约表单中的图片


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/visitor/image/upload`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.上传图片
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "imageData": "dgfrgrttr",
  "productId": "bbb",
  "projectId": "aaa",
  "type": "passback"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|pictureRequest|PictureRequest|body|true|PictureRequest|PictureRequest|
|&emsp;&emsp;imageData|图片数据，base64编码(不含data:image/jpg;base64)||true|object||
|&emsp;&emsp;productId|产品编号||false|string||
|&emsp;&emsp;projectId|项目编号||false|string||
|&emsp;&emsp;type|visitor/diy：预约字段||true|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«AcscImageUploadResponse»|
|201|Created|ActionErrorResult|
|204|No Content||
|401|Unauthorized|ActionErrorResult|
|403|Forbidden|ActionErrorResult|
|404|Not Found|ActionErrorResult|


**响应状态码-200**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|AcscImageUploadResponse|AcscImageUploadResponse|
|&emsp;&emsp;faceId|人脸专用：人脸图片编号|string||
|&emsp;&emsp;faceLevel|人脸专用：人脸质量级别(高>=80分，中>=70分 低>=60分 不合格<60)|string||
|&emsp;&emsp;faceScore|人脸专用：人脸评分值|integer(int32)||
|&emsp;&emsp;imageUrl|图片地址|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"faceId": "1179524873320912",
		"faceLevel": "中",
		"faceScore": 20,
		"imageUrl": "http://aliyun.com/image/122ssss.jpg"
	},
	"msg": "success"
}
```


**响应状态码-201**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-401**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-403**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-404**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


## 01_访客微信公众号预约


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/visitor/order`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>访客微信公众号访客预约接口。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "beVisitorOpenId": "1253566554",
  "beVisitorPersonId": "6546sdafs56adf",
  "beVisitorPersonName": "aaaa",
  "beVisitorPhoneNum": "123232323",
  "orderId": "6546sdafs56adf",
  "orderModel": "person",
  "projectId": "1112220",
  "visitEndTime": "2004-05-03T18:30:08+08:00",
  "visitStartTime": "2004-05-03T17:30:08+08:00",
  "visitorAddress": "123232323",
  "visitorBirthplace": "123232323",
  "visitorCarNumber": "123",
  "visitorCustoma": "123232323",
  "visitorCustomb": "123232323",
  "visitorCustomc": "123232323",
  "visitorCustomd": "123232323",
  "visitorCustome": "123232323",
  "visitorCustomf": "123",
  "visitorCustomg": "123",
  "visitorCustomh": "123",
  "visitorCustomi": "123",
  "visitorCustomj": "123",
  "visitorIdentityAddr": "123232323",
  "visitorIdentityIssuer": "123232323",
  "visitorIdentityNum": "123232323",
  "visitorIdentityType": "111",
  "visitorOpenId": "1253566554",
  "visitorPersonNum": "10",
  "visitorPrivilegeGroupIds": "123232323,2222222,33333333",
  "visitorPurpose": "参观",
  "visitorUserId": "",
  "visitorWorkUnit": "123232323"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|visitorInfoDto|访客微信预约信息对象|body|true|VisitorInfoDto|VisitorInfoDto|
|&emsp;&emsp;beVisitorOpenId|被访人微信openId||false|object||
|&emsp;&emsp;beVisitorPersonId|被访人唯一标识(该字段必填)||false|object||
|&emsp;&emsp;beVisitorPersonName|被访人姓名||false|object||
|&emsp;&emsp;beVisitorPhoneNum|被访人手机号||false|object||
|&emsp;&emsp;orderId|预约单Id||false|object||
|&emsp;&emsp;orderModel|预约模式 person:指定人员预约 space:场地预约||false|string||
|&emsp;&emsp;projectId|项目编号||false|object||
|&emsp;&emsp;visitEndTime|预计离开时间,必须晚于当前时间和预计来访时间||false|object||
|&emsp;&emsp;visitStartTime|预计来访时间||false|object||
|&emsp;&emsp;visitorAddress|访客住址||false|object||
|&emsp;&emsp;visitorBirthplace|籍贯||false|object||
|&emsp;&emsp;visitorCarNumber|车牌号||false|string||
|&emsp;&emsp;visitorCustoma|自定义字段a：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|object||
|&emsp;&emsp;visitorCustomb|自定义字段b：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|object||
|&emsp;&emsp;visitorCustomc|自定义字段c：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|object||
|&emsp;&emsp;visitorCustomd|自定义字段d：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|object||
|&emsp;&emsp;visitorCustome|自定义字段e：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|object||
|&emsp;&emsp;visitorCustomf|自定义字段f：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|string||
|&emsp;&emsp;visitorCustomg|自定义字段g：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|string||
|&emsp;&emsp;visitorCustomh|自定义字段h：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|string||
|&emsp;&emsp;visitorCustomi|自定义字段i：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|string||
|&emsp;&emsp;visitorCustomj|自定义字段j：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|string||
|&emsp;&emsp;visitorIdentityAddr|证件地址||false|object||
|&emsp;&emsp;visitorIdentityIssuer|发证机关||false|object||
|&emsp;&emsp;visitorIdentityNum|证件号码||false|object||
|&emsp;&emsp;visitorIdentityType|证件类型||false|object||
|&emsp;&emsp;visitorOpenId|访客微信openId||false|object||
|&emsp;&emsp;visitorPersonNum|访客人数：默认1||false|object||
|&emsp;&emsp;visitorPrivilegeGroupIds|访客权限组ids，以,分割权限组id||false|object||
|&emsp;&emsp;visitorPurpose|来访事由,长度为1～128个字符||false|object||
|&emsp;&emsp;visitorUserId|||false|string||
|&emsp;&emsp;visitorWorkUnit|访客来访单位||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 02_访客微信预约取消接口


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/visitor/order/cancel`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>访客微信预约取消接口。
 发布版本：V1.0.0</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|orderId|orderId|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 05_查询预约详情


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/visitor/order/detail`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>查询预约详情接口。
 发布版本：V1.0.0</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|orderId|orderId|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«OrderResponse»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|OrderResponse|OrderResponse|
|&emsp;&emsp;approvalResult||string||
|&emsp;&emsp;authBarCode|访客二维码|string||
|&emsp;&emsp;authIdentityPid|身份证序列号|string||
|&emsp;&emsp;authTempCard|访客卡号|string||
|&emsp;&emsp;authVisitorCode|访客验证码|string||
|&emsp;&emsp;backlogId||string||
|&emsp;&emsp;beVisitorGroupId|被访人部门ID|string||
|&emsp;&emsp;beVisitorGroupName|被访人部门名称|string||
|&emsp;&emsp;beVisitorOpenId|被访人openid|string||
|&emsp;&emsp;beVisitorPersonId|被访人ID|string||
|&emsp;&emsp;beVisitorPersonName|被访人名称|string||
|&emsp;&emsp;beVisitorPhoneNum|被访人手机号|string||
|&emsp;&emsp;beVisitorUserId||string||
|&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;createUserType|创建者身份类型：1-平台用户，2-内部人员，3-来访人员|integer(int32)||
|&emsp;&emsp;disorder|添加序号|integer(int32)||
|&emsp;&emsp;endTime|预计离开时间|string||
|&emsp;&emsp;endTimeDifference|预计离开时间时差|string||
|&emsp;&emsp;endTimeUTC|预计离开时间UTC|integer(int64)||
|&emsp;&emsp;orderId|预约单号|string||
|&emsp;&emsp;orderModel|预约模式 person:指定人员预约 space:场地预约|string||
|&emsp;&emsp;processId|审批规则id|string||
|&emsp;&emsp;processItemId|审批规则实例id|string||
|&emsp;&emsp;processRemark|备注|string||
|&emsp;&emsp;productId|产品编号|string||
|&emsp;&emsp;projectId|项目编号|string||
|&emsp;&emsp;realEndTime|签离时间|string||
|&emsp;&emsp;realEndTimeDifference|签离时间时差|string||
|&emsp;&emsp;realEndTimeUTC|签离时间UTC|integer(int64)||
|&emsp;&emsp;registerPlace|访客登记地点|string||
|&emsp;&emsp;registerTime|登记时间|string||
|&emsp;&emsp;registerTimeDifference|登记时间时差|string||
|&emsp;&emsp;registerTimeUTC|登记时间UTC|integer(int64)||
|&emsp;&emsp;startTime|预计来访时间|string||
|&emsp;&emsp;startTimeDifference|预计来访时间时差|string||
|&emsp;&emsp;startTimeUTC|预计来访时间UTC|integer(int64)||
|&emsp;&emsp;status|记录状态。0：待审批；1：正常；2：迟到；3：预约逾期；4：审批退回；5：超期自动签离；6：访客签离；7：超期未签离；8：已到达；9：审批逾期；10：邀约中；11：邀约逾期；12：邀约失效(员工取消)；13：邀约失效(访客取消)；14：预约失效(员工取消)；15：预约失效(访客取消)|integer(int32)||
|&emsp;&emsp;svrCodeIdentity|证件照对应图片服务器serviceNodes|string||
|&emsp;&emsp;svrCodeScanning|证件扫描照对应图片服务器serviceNodes|string||
|&emsp;&emsp;svrCodeVisitor|访客头像对应图片服务器serviceNodes|string||
|&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;visitBatch|访客批次|string||
|&emsp;&emsp;visitorAddress|访客住址|string||
|&emsp;&emsp;visitorAllowTimes|访客进入次数|integer(int32)||
|&emsp;&emsp;visitorBirthplace|籍贯|string||
|&emsp;&emsp;visitorCarNumber|车牌号|string||
|&emsp;&emsp;visitorCustoma|自定义字段a：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomb|自定义字段b：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomc|自定义字段c：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomd|自定义字段d：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustome|自定义字段e：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomf|自定义字段f：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomg|自定义字段g：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomh|自定义字段h：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomi|自定义字段i：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomj|自定义字段j：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorGroupId|访客名单分组ID|string||
|&emsp;&emsp;visitorIdentityAddr|证件地址|string||
|&emsp;&emsp;visitorIdentityIssuer|发证机关|string||
|&emsp;&emsp;visitorIdentityNum|证件号码|string||
|&emsp;&emsp;visitorIdentityPhoto|证件照片|string||
|&emsp;&emsp;visitorIdentityType|证件类型：111、身份证|integer(int32)||
|&emsp;&emsp;visitorName|姓名|string||
|&emsp;&emsp;visitorOpenId|访客微信公众号唯一标识|string||
|&emsp;&emsp;visitorPersonNum|来访人数|integer(int32)||
|&emsp;&emsp;visitorPhoneNum|手机号|string||
|&emsp;&emsp;visitorPhoto|访客头像|string||
|&emsp;&emsp;visitorPhotoFlag|人脸质量合格标识。0：合格；1：不合格|string||
|&emsp;&emsp;visitorPinyin|访客名首字母缩写|string||
|&emsp;&emsp;visitorPrivilegeGroupIds|访客权限组ids|string||
|&emsp;&emsp;visitorPurpose|来访事由|string||
|&emsp;&emsp;visitorScanningPhoto|证件扫描照片|string||
|&emsp;&emsp;visitorSex|性别：1、男；2、女|integer(int32)||
|&emsp;&emsp;visitorTemperature|访客体温|string||
|&emsp;&emsp;visitorTemperatureStatus|访客体温状态|integer(int32)||
|&emsp;&emsp;visitorTypeId|访客类型id|string||
|&emsp;&emsp;visitorUserId||string||
|&emsp;&emsp;visitorWorkUnit|访客来访单位|string||
|&emsp;&emsp;webLabel|记录状态描述-web端|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"approvalResult": "",
		"authBarCode": "123",
		"authIdentityPid": "123",
		"authTempCard": "123",
		"authVisitorCode": "123",
		"backlogId": "",
		"beVisitorGroupId": "123",
		"beVisitorGroupName": "123",
		"beVisitorOpenId": "123",
		"beVisitorPersonId": "123",
		"beVisitorPersonName": "123",
		"beVisitorPhoneNum": "123",
		"beVisitorUserId": "",
		"createTime": "123",
		"createUserType": 123,
		"disorder": 123,
		"endTime": "123",
		"endTimeDifference": "123",
		"endTimeUTC": 123,
		"orderId": "123",
		"orderModel": "person",
		"processId": "123",
		"processItemId": "123",
		"processRemark": "123",
		"productId": "123",
		"projectId": "123",
		"realEndTime": "123",
		"realEndTimeDifference": "123",
		"realEndTimeUTC": 123,
		"registerPlace": "123",
		"registerTime": "123",
		"registerTimeDifference": "123",
		"registerTimeUTC": 123,
		"startTime": "123",
		"startTimeDifference": "123",
		"startTimeUTC": 123,
		"status": 123,
		"svrCodeIdentity": "123",
		"svrCodeScanning": "123",
		"svrCodeVisitor": "123",
		"updateTime": "123",
		"visitBatch": "123",
		"visitorAddress": "123",
		"visitorAllowTimes": 123,
		"visitorBirthplace": "123",
		"visitorCarNumber": "123",
		"visitorCustoma": "123",
		"visitorCustomb": "123",
		"visitorCustomc": "123",
		"visitorCustomd": "123",
		"visitorCustome": "123",
		"visitorCustomf": "123",
		"visitorCustomg": "123",
		"visitorCustomh": "123",
		"visitorCustomi": "123",
		"visitorCustomj": "123",
		"visitorGroupId": "123",
		"visitorIdentityAddr": "123",
		"visitorIdentityIssuer": "123",
		"visitorIdentityNum": "123",
		"visitorIdentityPhoto": "123",
		"visitorIdentityType": 123,
		"visitorName": "123",
		"visitorOpenId": "123",
		"visitorPersonNum": 123,
		"visitorPhoneNum": "123",
		"visitorPhoto": "123",
		"visitorPhotoFlag": "123",
		"visitorPinyin": "123",
		"visitorPrivilegeGroupIds": "123",
		"visitorPurpose": "123",
		"visitorScanningPhoto": "123",
		"visitorSex": 123,
		"visitorTemperature": "123",
		"visitorTemperatureStatus": 123,
		"visitorTypeId": "123",
		"visitorUserId": "",
		"visitorWorkUnit": "123",
		"webLabel": "123"
	},
	"msg": "success"
}
```


## 04_访客预约记录查询接口


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/visitor/order/page`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>访客预约记录查询接口。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "backlogId": "bbb",
  "beVisitorOpenId": "1253566554",
  "beVisitorPersonId": "6546sdafs56adf",
  "beVisitorPersonName": "小东",
  "cardNo": "1234567890",
  "disorder": 123,
  "earlyEndTimeISO": "2018-10-29T15:33:07+08:00",
  "earlyRealEndTimeISO": "2018-10-29T15:50:07+08:00",
  "earlyRegisterTimeISO": "2018-10-29T15:33:07+08:00",
  "earlyStartTimeISO": "2018-10-29T15:33:07+08:00",
  "identityId": "111",
  "lateEndTimeISO": "2018-10-29T15:55:07+08:00",
  "lateRealEndTimeISO": "2018-10-29T15:55:07+08:00",
  "lateRegisterTimeISO": "2018-10-29T15:55:07+08:00",
  "lateStartTimeISO": "2018-10-29T15:55:07+08:00",
  "maxTemperature": "42",
  "minTemperature": "38",
  "orderId": "1253566554",
  "pageNo": "3",
  "pageSize": "50",
  "productId": "bbb",
  "projectId": "aaa",
  "projectIdList": "[\"0a869b06f4ff4da29949acf006405c39\"]",
  "qrCode": "1234567890",
  "registerPlace": "aaa1112ssfddd",
  "sort": "desc",
  "statusList": "0",
  "temperatureStatus": 0,
  "type": "1",
  "visitorAddress": "访客住址",
  "visitorBirthplace": "籍贯",
  "visitorCarNumber": "浙A32216",
  "visitorCode": "1234",
  "visitorCustoma": "1253566554",
  "visitorCustomb": "1253566554",
  "visitorCustomc": "1253566554",
  "visitorCustomd": "1253566554",
  "visitorCustome": "1253566554",
  "visitorCustomf": "1253566554",
  "visitorCustomg": "1253566554",
  "visitorCustomh": "1253566554",
  "visitorCustomi": "1253566554",
  "visitorCustomj": "1253566554",
  "visitorIdentityAddr": "证件地址",
  "visitorIdentityIssuer": "发证机关",
  "visitorIdentityNum": "32165165165161",
  "visitorName": "小红",
  "visitorOpenId": "1253566554",
  "visitorPhoneNum": "1253566554",
  "visitorPurpose": "参观",
  "visitorSex": "1",
  "visitorSexs": "[1,0]",
  "visitorTypeId": "1",
  "visitorWorkUnit": "访客所在公司"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|orderRequest|OrderRequest|body|true|OrderRequest|OrderRequest|
|&emsp;&emsp;backlogId|待办编号||false|string||
|&emsp;&emsp;beVisitorOpenId|被访人openId||false|object||
|&emsp;&emsp;beVisitorPersonId|被访人ID||false|object||
|&emsp;&emsp;beVisitorPersonName|被访人姓名||false|object||
|&emsp;&emsp;cardNo|卡号||false|object||
|&emsp;&emsp;disorder|更新顺序||false|integer(int32)||
|&emsp;&emsp;earlyEndTimeISO|最早预计离开时间||false|object||
|&emsp;&emsp;earlyRealEndTimeISO|最早离开时间||false|object||
|&emsp;&emsp;earlyRegisterTimeISO|最早来访时间||false|object||
|&emsp;&emsp;earlyStartTimeISO|最早预计来访时间||false|object||
|&emsp;&emsp;identityId|证件类型：111身份证，335驾驶证，131工作证，133学生证，114军官证，414护照，990其他||false|object||
|&emsp;&emsp;lateEndTimeISO|最晚预计离开时间||false|object||
|&emsp;&emsp;lateRealEndTimeISO|最晚离开时间||false|object||
|&emsp;&emsp;lateRegisterTimeISO|最晚来访时间||false|object||
|&emsp;&emsp;lateStartTimeISO|最晚预计来访时间||false|object||
|&emsp;&emsp;maxTemperature|最高体温||false|string||
|&emsp;&emsp;minTemperature|最低体温||false|string||
|&emsp;&emsp;orderId|orderId||false|object||
|&emsp;&emsp;pageNo|查询时第几页||true|object||
|&emsp;&emsp;pageSize|查询时单页条数,限定大小不能超过1000||true|object||
|&emsp;&emsp;productId|产品编号||false|string||
|&emsp;&emsp;projectId|项目编号||false|string||
|&emsp;&emsp;projectIdList|项目编号集合||false|array|string|
|&emsp;&emsp;qrCode|二维码内容||false|object||
|&emsp;&emsp;registerPlace|访客登记地点||false|object||
|&emsp;&emsp;sort|排序方式：desc:按预计来访时间倒序，asc:按预计来访时间正序：||false|string||
|&emsp;&emsp;statusList|预约状态的集合:0：待审批；1：正常；2：迟到；3：预约逾期；4：审批退回；5：超期自动签离；6：访客签离；7：超期未签离；8：已到达；9：审批逾期；10：邀约中；11：邀约逾期；12：邀约失效(员工取消)；13：邀约失效(访客取消)；14：预约失效(员工取消)；15：预约失效(访客取消)||false|object||
|&emsp;&emsp;temperatureStatus|体温状态(0正常，1异常)||false|integer(int32)||
|&emsp;&emsp;type|查询类型:(0：被访记录，1：审批记录，2：邀约记录---微信端使用）,（3:预约记录，4：来访记录----web端使用)||false|string||
|&emsp;&emsp;visitorAddress|访客住址||false|object||
|&emsp;&emsp;visitorBirthplace|籍贯||false|object||
|&emsp;&emsp;visitorCarNumber|车牌号||false|object||
|&emsp;&emsp;visitorCode|访客验证码||false|object||
|&emsp;&emsp;visitorCustoma|自定义字段a||false|object||
|&emsp;&emsp;visitorCustomb|自定义字段b||false|object||
|&emsp;&emsp;visitorCustomc|自定义字段c||false|object||
|&emsp;&emsp;visitorCustomd|自定义字段d||false|object||
|&emsp;&emsp;visitorCustome|自定义字段e||false|object||
|&emsp;&emsp;visitorCustomf|自定义字段f||false|object||
|&emsp;&emsp;visitorCustomg|自定义字段g||false|object||
|&emsp;&emsp;visitorCustomh|自定义字段h||false|object||
|&emsp;&emsp;visitorCustomi|自定义字段i||false|object||
|&emsp;&emsp;visitorCustomj|自定义字段j||false|object||
|&emsp;&emsp;visitorIdentityAddr|证件地址||false|object||
|&emsp;&emsp;visitorIdentityIssuer|发证机关||false|object||
|&emsp;&emsp;visitorIdentityNum|证件号码||false|object||
|&emsp;&emsp;visitorName|访客姓名||false|object||
|&emsp;&emsp;visitorOpenId|访客openId||false|object||
|&emsp;&emsp;visitorPhoneNum|手机号||false|object||
|&emsp;&emsp;visitorPurpose|来访事由||false|object||
|&emsp;&emsp;visitorSex|性别,1男,2女||false|object||
|&emsp;&emsp;visitorSexs|访客性别集合||false|object||
|&emsp;&emsp;visitorTypeId|访客类型||false|object||
|&emsp;&emsp;visitorWorkUnit|访客来访单位||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PageResult«OrderResponse»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PageResult«OrderResponse»|PageResult«OrderResponse»|
|&emsp;&emsp;list|数据信息|array|OrderResponse|
|&emsp;&emsp;&emsp;&emsp;approvalResult||string||
|&emsp;&emsp;&emsp;&emsp;authBarCode|访客二维码|string||
|&emsp;&emsp;&emsp;&emsp;authIdentityPid|身份证序列号|string||
|&emsp;&emsp;&emsp;&emsp;authTempCard|访客卡号|string||
|&emsp;&emsp;&emsp;&emsp;authVisitorCode|访客验证码|string||
|&emsp;&emsp;&emsp;&emsp;backlogId||string||
|&emsp;&emsp;&emsp;&emsp;beVisitorGroupId|被访人部门ID|string||
|&emsp;&emsp;&emsp;&emsp;beVisitorGroupName|被访人部门名称|string||
|&emsp;&emsp;&emsp;&emsp;beVisitorOpenId|被访人openid|string||
|&emsp;&emsp;&emsp;&emsp;beVisitorPersonId|被访人ID|string||
|&emsp;&emsp;&emsp;&emsp;beVisitorPersonName|被访人名称|string||
|&emsp;&emsp;&emsp;&emsp;beVisitorPhoneNum|被访人手机号|string||
|&emsp;&emsp;&emsp;&emsp;beVisitorUserId||string||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;createUserType|创建者身份类型：1-平台用户，2-内部人员，3-来访人员|integer||
|&emsp;&emsp;&emsp;&emsp;disorder|添加序号|integer||
|&emsp;&emsp;&emsp;&emsp;endTime|预计离开时间|string||
|&emsp;&emsp;&emsp;&emsp;endTimeDifference|预计离开时间时差|string||
|&emsp;&emsp;&emsp;&emsp;endTimeUTC|预计离开时间UTC|integer||
|&emsp;&emsp;&emsp;&emsp;orderId|预约单号|string||
|&emsp;&emsp;&emsp;&emsp;orderModel|预约模式 person:指定人员预约 space:场地预约|string||
|&emsp;&emsp;&emsp;&emsp;processId|审批规则id|string||
|&emsp;&emsp;&emsp;&emsp;processItemId|审批规则实例id|string||
|&emsp;&emsp;&emsp;&emsp;processRemark|备注|string||
|&emsp;&emsp;&emsp;&emsp;productId|产品编号|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目编号|string||
|&emsp;&emsp;&emsp;&emsp;realEndTime|签离时间|string||
|&emsp;&emsp;&emsp;&emsp;realEndTimeDifference|签离时间时差|string||
|&emsp;&emsp;&emsp;&emsp;realEndTimeUTC|签离时间UTC|integer||
|&emsp;&emsp;&emsp;&emsp;registerPlace|访客登记地点|string||
|&emsp;&emsp;&emsp;&emsp;registerTime|登记时间|string||
|&emsp;&emsp;&emsp;&emsp;registerTimeDifference|登记时间时差|string||
|&emsp;&emsp;&emsp;&emsp;registerTimeUTC|登记时间UTC|integer||
|&emsp;&emsp;&emsp;&emsp;startTime|预计来访时间|string||
|&emsp;&emsp;&emsp;&emsp;startTimeDifference|预计来访时间时差|string||
|&emsp;&emsp;&emsp;&emsp;startTimeUTC|预计来访时间UTC|integer||
|&emsp;&emsp;&emsp;&emsp;status|记录状态。0：待审批；1：正常；2：迟到；3：预约逾期；4：审批退回；5：超期自动签离；6：访客签离；7：超期未签离；8：已到达；9：审批逾期；10：邀约中；11：邀约逾期；12：邀约失效(员工取消)；13：邀约失效(访客取消)；14：预约失效(员工取消)；15：预约失效(访客取消)|integer||
|&emsp;&emsp;&emsp;&emsp;svrCodeIdentity|证件照对应图片服务器serviceNodes|string||
|&emsp;&emsp;&emsp;&emsp;svrCodeScanning|证件扫描照对应图片服务器serviceNodes|string||
|&emsp;&emsp;&emsp;&emsp;svrCodeVisitor|访客头像对应图片服务器serviceNodes|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;&emsp;&emsp;visitBatch|访客批次|string||
|&emsp;&emsp;&emsp;&emsp;visitorAddress|访客住址|string||
|&emsp;&emsp;&emsp;&emsp;visitorAllowTimes|访客进入次数|integer||
|&emsp;&emsp;&emsp;&emsp;visitorBirthplace|籍贯|string||
|&emsp;&emsp;&emsp;&emsp;visitorCarNumber|车牌号|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustoma|自定义字段a：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomb|自定义字段b：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomc|自定义字段c：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomd|自定义字段d：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustome|自定义字段e：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomf|自定义字段f：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomg|自定义字段g：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomh|自定义字段h：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomi|自定义字段i：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomj|自定义字段j：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorGroupId|访客名单分组ID|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityAddr|证件地址|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityIssuer|发证机关|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityNum|证件号码|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityPhoto|证件照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityType|证件类型：111、身份证|integer||
|&emsp;&emsp;&emsp;&emsp;visitorName|姓名|string||
|&emsp;&emsp;&emsp;&emsp;visitorOpenId|访客微信公众号唯一标识|string||
|&emsp;&emsp;&emsp;&emsp;visitorPersonNum|来访人数|integer||
|&emsp;&emsp;&emsp;&emsp;visitorPhoneNum|手机号|string||
|&emsp;&emsp;&emsp;&emsp;visitorPhoto|访客头像|string||
|&emsp;&emsp;&emsp;&emsp;visitorPhotoFlag|人脸质量合格标识。0：合格；1：不合格|string||
|&emsp;&emsp;&emsp;&emsp;visitorPinyin|访客名首字母缩写|string||
|&emsp;&emsp;&emsp;&emsp;visitorPrivilegeGroupIds|访客权限组ids|string||
|&emsp;&emsp;&emsp;&emsp;visitorPurpose|来访事由|string||
|&emsp;&emsp;&emsp;&emsp;visitorScanningPhoto|证件扫描照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorSex|性别：1、男；2、女|integer||
|&emsp;&emsp;&emsp;&emsp;visitorTemperature|访客体温|string||
|&emsp;&emsp;&emsp;&emsp;visitorTemperatureStatus|访客体温状态|integer||
|&emsp;&emsp;&emsp;&emsp;visitorTypeId|访客类型id|string||
|&emsp;&emsp;&emsp;&emsp;visitorUserId||string||
|&emsp;&emsp;&emsp;&emsp;visitorWorkUnit|访客来访单位|string||
|&emsp;&emsp;&emsp;&emsp;webLabel|记录状态描述-web端|string||
|&emsp;&emsp;pageNo|页码|integer(int32)||
|&emsp;&emsp;pageSize|页大小|integer(int32)||
|&emsp;&emsp;total|总条数|integer(int64)||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"list": [
			{
				"approvalResult": "",
				"authBarCode": "123",
				"authIdentityPid": "123",
				"authTempCard": "123",
				"authVisitorCode": "123",
				"backlogId": "",
				"beVisitorGroupId": "123",
				"beVisitorGroupName": "123",
				"beVisitorOpenId": "123",
				"beVisitorPersonId": "123",
				"beVisitorPersonName": "123",
				"beVisitorPhoneNum": "123",
				"beVisitorUserId": "",
				"createTime": "123",
				"createUserType": 123,
				"disorder": 123,
				"endTime": "123",
				"endTimeDifference": "123",
				"endTimeUTC": 123,
				"orderId": "123",
				"orderModel": "person",
				"processId": "123",
				"processItemId": "123",
				"processRemark": "123",
				"productId": "123",
				"projectId": "123",
				"realEndTime": "123",
				"realEndTimeDifference": "123",
				"realEndTimeUTC": 123,
				"registerPlace": "123",
				"registerTime": "123",
				"registerTimeDifference": "123",
				"registerTimeUTC": 123,
				"startTime": "123",
				"startTimeDifference": "123",
				"startTimeUTC": 123,
				"status": 123,
				"svrCodeIdentity": "123",
				"svrCodeScanning": "123",
				"svrCodeVisitor": "123",
				"updateTime": "123",
				"visitBatch": "123",
				"visitorAddress": "123",
				"visitorAllowTimes": 123,
				"visitorBirthplace": "123",
				"visitorCarNumber": "123",
				"visitorCustoma": "123",
				"visitorCustomb": "123",
				"visitorCustomc": "123",
				"visitorCustomd": "123",
				"visitorCustome": "123",
				"visitorCustomf": "123",
				"visitorCustomg": "123",
				"visitorCustomh": "123",
				"visitorCustomi": "123",
				"visitorCustomj": "123",
				"visitorGroupId": "123",
				"visitorIdentityAddr": "123",
				"visitorIdentityIssuer": "123",
				"visitorIdentityNum": "123",
				"visitorIdentityPhoto": "123",
				"visitorIdentityType": 123,
				"visitorName": "123",
				"visitorOpenId": "123",
				"visitorPersonNum": 123,
				"visitorPhoneNum": "123",
				"visitorPhoto": "123",
				"visitorPhotoFlag": "123",
				"visitorPinyin": "123",
				"visitorPrivilegeGroupIds": "123",
				"visitorPurpose": "123",
				"visitorScanningPhoto": "123",
				"visitorSex": 123,
				"visitorTemperature": "123",
				"visitorTemperatureStatus": 123,
				"visitorTypeId": "123",
				"visitorUserId": "",
				"visitorWorkUnit": "123",
				"webLabel": "123"
			}
		],
		"pageNo": 1,
		"pageSize": 20,
		"total": 5
	},
	"msg": "success"
}
```


## 03_访客微信预约修改接口


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/visitor/order/update`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>访客微信预约修改接口。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "beVisitorOpenId": "1253566554",
  "beVisitorPersonId": "6546sdafs56adf",
  "beVisitorPersonName": "aaaa",
  "beVisitorPhoneNum": "123232323",
  "orderId": "6546sdafs56adf",
  "orderModel": "person",
  "projectId": "1112220",
  "visitEndTime": "2004-05-03T18:30:08+08:00",
  "visitStartTime": "2004-05-03T17:30:08+08:00",
  "visitorAddress": "123232323",
  "visitorBirthplace": "123232323",
  "visitorCarNumber": "123",
  "visitorCustoma": "123232323",
  "visitorCustomb": "123232323",
  "visitorCustomc": "123232323",
  "visitorCustomd": "123232323",
  "visitorCustome": "123232323",
  "visitorCustomf": "123",
  "visitorCustomg": "123",
  "visitorCustomh": "123",
  "visitorCustomi": "123",
  "visitorCustomj": "123",
  "visitorIdentityAddr": "123232323",
  "visitorIdentityIssuer": "123232323",
  "visitorIdentityNum": "123232323",
  "visitorIdentityType": "111",
  "visitorOpenId": "1253566554",
  "visitorPersonNum": "10",
  "visitorPrivilegeGroupIds": "123232323,2222222,33333333",
  "visitorPurpose": "参观",
  "visitorUserId": "",
  "visitorWorkUnit": "123232323"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|visitorInfoDto|访客微信预约信息对象|body|true|VisitorInfoDto|VisitorInfoDto|
|&emsp;&emsp;beVisitorOpenId|被访人微信openId||false|object||
|&emsp;&emsp;beVisitorPersonId|被访人唯一标识(该字段必填)||false|object||
|&emsp;&emsp;beVisitorPersonName|被访人姓名||false|object||
|&emsp;&emsp;beVisitorPhoneNum|被访人手机号||false|object||
|&emsp;&emsp;orderId|预约单Id||false|object||
|&emsp;&emsp;orderModel|预约模式 person:指定人员预约 space:场地预约||false|string||
|&emsp;&emsp;projectId|项目编号||false|object||
|&emsp;&emsp;visitEndTime|预计离开时间,必须晚于当前时间和预计来访时间||false|object||
|&emsp;&emsp;visitStartTime|预计来访时间||false|object||
|&emsp;&emsp;visitorAddress|访客住址||false|object||
|&emsp;&emsp;visitorBirthplace|籍贯||false|object||
|&emsp;&emsp;visitorCarNumber|车牌号||false|string||
|&emsp;&emsp;visitorCustoma|自定义字段a：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|object||
|&emsp;&emsp;visitorCustomb|自定义字段b：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|object||
|&emsp;&emsp;visitorCustomc|自定义字段c：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|object||
|&emsp;&emsp;visitorCustomd|自定义字段d：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|object||
|&emsp;&emsp;visitorCustome|自定义字段e：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|object||
|&emsp;&emsp;visitorCustomf|自定义字段f：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|string||
|&emsp;&emsp;visitorCustomg|自定义字段g：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|string||
|&emsp;&emsp;visitorCustomh|自定义字段h：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|string||
|&emsp;&emsp;visitorCustomi|自定义字段i：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|string||
|&emsp;&emsp;visitorCustomj|自定义字段j：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|string||
|&emsp;&emsp;visitorIdentityAddr|证件地址||false|object||
|&emsp;&emsp;visitorIdentityIssuer|发证机关||false|object||
|&emsp;&emsp;visitorIdentityNum|证件号码||false|object||
|&emsp;&emsp;visitorIdentityType|证件类型||false|object||
|&emsp;&emsp;visitorOpenId|访客微信openId||false|object||
|&emsp;&emsp;visitorPersonNum|访客人数：默认1||false|object||
|&emsp;&emsp;visitorPrivilegeGroupIds|访客权限组ids，以,分割权限组id||false|object||
|&emsp;&emsp;visitorPurpose|来访事由,长度为1～128个字符||false|object||
|&emsp;&emsp;visitorUserId|||false|string||
|&emsp;&emsp;visitorWorkUnit|访客来访单位||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 14_公众号端获取预约模式内容


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/visitor/orderModel/config`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>1.公众号端获取预约模式内容
发布版本：V1.0.0</p>



**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«OrderModelConfig»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|OrderModelConfig|OrderModelConfig|
|&emsp;&emsp;beVisitorPersonId|场地模式状态下-被访人唯一标识(该字段必填)|object||
|&emsp;&emsp;beVisitorPersonName|场地模式状态下-被访人姓名|object||
|&emsp;&emsp;beVisitorPhoneNum|场地模式状态下-被访人手机号|object||
|&emsp;&emsp;personModelStatus|人员模式状态 close:关闭 open:打开|string||
|&emsp;&emsp;spaceModelList|场地列表|array|OrderSpaceModel|
|&emsp;&emsp;&emsp;&emsp;beVisitorPersonId|场地模式状态下-被访人唯一标识(该字段必填)|object||
|&emsp;&emsp;&emsp;&emsp;beVisitorPersonName|场地模式状态下-被访人姓名|object||
|&emsp;&emsp;&emsp;&emsp;beVisitorPhoneNum|场地模式状态下-被访人手机号|object||
|&emsp;&emsp;&emsp;&emsp;spaceName|场地名称|string||
|&emsp;&emsp;spaceModelStatus|场地模式状态 close:关闭 open:打开|string||
|&emsp;&emsp;spaceName|场地名称|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"beVisitorPersonId": "6546sdafs56adf",
		"beVisitorPersonName": "aaaa",
		"beVisitorPhoneNum": "123232323",
		"personModelStatus": "close",
		"spaceModelList": "close",
		"spaceModelStatus": "close",
		"spaceName": "close"
	},
	"msg": "success"
}
```


## 12_获取访客通行证配置


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/visitor/phConfig/info`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>获取访客通行证配置。
 发布版本：V1.0.0</p>



**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PhConfigWebResponse»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PhConfigWebResponse|PhConfigWebResponse|
|&emsp;&emsp;backPicName|通行证的背景图名称|string||
|&emsp;&emsp;backPicUrl|通行证的背景图片|string||
|&emsp;&emsp;configStatus|通行证的配置开启或者关闭状态 open:开启 close:关闭(默认)|string||
|&emsp;&emsp;endContent|通行证的末尾内容|string||
|&emsp;&emsp;phConfigId|通行证的配置id|string||
|&emsp;&emsp;phItems|通行证的内容选项集合|array|PhItem|
|&emsp;&emsp;&emsp;&emsp;format|格式:比如时间的格式 yyyy-MM-dd / yyyy-MM-dd HH:mm:ss /yyyy年MM月dd日|string||
|&emsp;&emsp;&emsp;&emsp;key|入园通行证的key值 头像：visitorPhoto  姓名：visitorName  手机号码: visitorPhoneNum  车牌号 ：visitorCarNumber  证件号码：visitorIdentityNum  来访事由：visitorPurpose  来访单位：visitorWorkUnit   被访对象的姓名：beVisitorPersonName 被访对象的组织：beVisitorGroupName  被访对象的手机号码：beVisitorPhoneNum 有效期的开始时间：startTime 有效期的结束时间：endTime 审批状态：approvalResult  登记时间: registerTime   二维码：authBarCode 分割线:separator  空行:blankLine |string||
|&emsp;&emsp;&emsp;&emsp;name|通行证选项对应的名称:比如姓名/手机号码;二维码、头像、分割线、空行的name不存在的|string||
|&emsp;&emsp;&emsp;&emsp;value|通行证选项对应的值:比如姓名对应的值|string||
|&emsp;&emsp;productCode|产品编号|string||
|&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;title|通行证的标题|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"backPicName": "通行证",
		"backPicUrl": "http://7412f756-1625137475555876-face.oss-cn-hangzhou.aliyuncs.com/photo/783210920129584.jpg",
		"configStatus": "close",
		"endContent": "欢迎来到烟台工程职业技术学院",
		"phConfigId": "5d5f434c4543accda02680b600afe6b3",
		"phItems": "[]",
		"productCode": "1625137405416832",
		"projectId": "1805308421418544",
		"title": "高职学院的入园通行证"
	},
	"msg": "success"
}
```


## 07_获取访客权限组信息


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/visitor/privilege/info`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>查询访客权限组数据。
 发布版本：V1.0.0</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|openId|openId|query|true|string||
|type|操作类型：0：访客，1：被访人|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«List«PrivilegeResponse»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|array|PrivilegeResponse|
|&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;disorder|更新序号|integer(int32)||
|&emsp;&emsp;groupId|权限组ID|string||
|&emsp;&emsp;groupName|权限组名称|string||
|&emsp;&emsp;isDefault|是否默认权限组|string||
|&emsp;&emsp;productId|产品编号|string||
|&emsp;&emsp;projectId|项目编号|string||
|&emsp;&emsp;remark|备注说明|string||
|&emsp;&emsp;select||boolean||
|&emsp;&emsp;status|状态：0正常 -1已删除|integer(int32)||
|&emsp;&emsp;updateTime|更新时间|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": [
		{
			"createTime": "2021-07-01 12:00:00",
			"disorder": 123,
			"groupId": "ccc",
			"groupName": "园区北门",
			"isDefault": "0",
			"productId": "bbb",
			"projectId": "aaa",
			"remark": "拜访",
			"select": true,
			"status": 0,
			"updateTime": "2021-07-11 12:00:00"
		}
	],
	"msg": "success"
}
```


## 11_公众号端获取防疫承诺配置信息


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/visitor/promise/info`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>1.公众号端获取防疫承诺配置信息
发布版本：V1.0.0</p>



**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PromiseAllResponse»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PromiseAllResponse|PromiseAllResponse|
|&emsp;&emsp;beforeDetails|预约前防疫承诺详情List|array|PromiseDetailDto|
|&emsp;&emsp;&emsp;&emsp;detailsContent|详情内容，子页面中的承诺内容|string||
|&emsp;&emsp;&emsp;&emsp;detailsFlag|详情选项（承诺类型为2单选时存在，返回选择的该是或否）|boolean||
|&emsp;&emsp;&emsp;&emsp;promiseType|承诺类型（1末尾提示，2单选）|integer||
|&emsp;&emsp;inDetails|预约时防疫承诺详情List|array|PromiseDetailDto|
|&emsp;&emsp;&emsp;&emsp;detailsContent|详情内容，子页面中的承诺内容|string||
|&emsp;&emsp;&emsp;&emsp;detailsFlag|详情选项（承诺类型为2单选时存在，返回选择的该是或否）|boolean||
|&emsp;&emsp;&emsp;&emsp;promiseType|承诺类型（1末尾提示，2单选）|integer||
|&emsp;&emsp;informDetails|告知书详情|PromiseInformDto|PromiseInformDto|
|&emsp;&emsp;&emsp;&emsp;detailsContent|详情内容，子页面中的承诺内容|string||
|&emsp;&emsp;&emsp;&emsp;detailsName|详情名称，(当承诺类型为3告知书时，存在)|string||
|&emsp;&emsp;showBeforeFlag|预约前是否弹框标志|boolean||
|&emsp;&emsp;showInFlag|预约时展示在访客预约字段后面的标志|boolean||
|&emsp;&emsp;showInformFlag|告知书是否弹框标志|boolean||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"beforeDetails": "xxx",
		"inDetails": "xxx",
		"informDetails": {
			"detailsContent": "详情内容",
			"detailsName": ""
		},
		"showBeforeFlag": true,
		"showInFlag": true,
		"showInformFlag": true
	},
	"msg": "success"
}
```


## 09_访客获取二维码接口


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/visitor/qrCode`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>访客获取二维码接口。
 发布版本：V1.0.0</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|orderId|orderId|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«string»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": "",
	"msg": "success"
}
```


## 10_公众号消息界面登录


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/visitor/visitor/msg/login`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.公众号消息界面自动登陆
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "orderId": "123",
  "personId": "personId",
  "type": "visitor"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|msgLoginRequest|消息界面登陆参数|body|true|MsgLoginRequest|MsgLoginRequest|
|&emsp;&emsp;orderId|orderId||true|string||
|&emsp;&emsp;personId|登录方(为员工:person时要带上personId)||true|string||
|&emsp;&emsp;type|登录方(访客：visitor、员工:person)||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«TokenMpResponse»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|TokenMpResponse|TokenMpResponse|
|&emsp;&emsp;isAllowLogin|是否允许注册1：允许，0：不允许|string||
|&emsp;&emsp;reason|不允许注册时返回原因，前端可用于界面提示信息|string||
|&emsp;&emsp;token|Token信息|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"isAllowLogin": "0",
		"reason": "项目授权已过期",
		"token": "0003b19335524b0387a01e91dd6946ea"
	},
	"msg": "success"
}
```


# 11_微信小程序_个人中心


## 09_获取工作单位列表


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/my/enterprise/list`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.获取检索出的工作单位，只显示10个，若要缩小请录入详细查询条件
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "enterpriseName": "海康威视"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaEnterpriseGetRequest|工作单位列表请求参数|body|true|WcMaEnterpriseGetRequest|WcMaEnterpriseGetRequest|
|&emsp;&emsp;enterpriseName|企业名称(>=2)||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«WcMaEnterpriseGetResponse»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|WcMaEnterpriseGetResponse|WcMaEnterpriseGetResponse|
|&emsp;&emsp;enterpriseList|工作单位列表|array|WcMaEnterpriseGetDto|
|&emsp;&emsp;&emsp;&emsp;enterpriseCode|企业编号|string||
|&emsp;&emsp;&emsp;&emsp;enterpriseName|企业名称|string||
|&emsp;&emsp;&emsp;&emsp;productId|产品编号|string||
|&emsp;&emsp;&emsp;&emsp;projectId|租户编号|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"enterpriseList": [
			{
				"enterpriseCode": "122228959455556",
				"enterpriseName": "海康威视",
				"productId": "122228959455556",
				"projectId": "122228959455556"
			}
		]
	},
	"msg": "success"
}
```


## 08_获取访客权限组列表


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/my/privilege/group`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>1.访客权限组列表
发布版本：V1.0.0</p>



**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«WcMaPrivilegeGroupResponse»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|WcMaPrivilegeGroupResponse|WcMaPrivilegeGroupResponse|
|&emsp;&emsp;groupList|权限组列表|array|WcMaPrivilegeGroupDto|
|&emsp;&emsp;&emsp;&emsp;groupId|权限组编号(<=32)|string||
|&emsp;&emsp;&emsp;&emsp;groupName|权限组名称(<=32)|string||
|&emsp;&emsp;&emsp;&emsp;isDefault|是否是默认拜访区域，1-是，0-否|object||
|&emsp;&emsp;&emsp;&emsp;select||boolean||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"groupList": [
			{
				"groupId": "9c6adaf7-40f0-4e97-9af0-ea16369b9315",
				"groupName": "停车场",
				"isDefault": "1",
				"select": true
			}
		]
	},
	"msg": "success"
}
```


## 07_获取事由列表


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/my/purpose`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.事由列表
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "projectId": "122228959455556"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaPurposeRequest|获取事由列表请求参数|body|true|WcMaPurposeRequest|WcMaPurposeRequest|
|&emsp;&emsp;projectId|租户编号(从选择工作单位的类别中获取，若没有工作单位列表选择可为空)||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«WcMaPurposeResponse»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|WcMaPurposeResponse|WcMaPurposeResponse|
|&emsp;&emsp;purposeList|事由列表|array|WcMaPurposeDto|
|&emsp;&emsp;&emsp;&emsp;purposeDesc|事由描述|string||
|&emsp;&emsp;&emsp;&emsp;purposeId|事由编号(<=32)|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"purposeList": [
			{
				"purposeDesc": "参观",
				"purposeId": "bdf2f958-8f4a-4d26-b7e4-5179215b7fba"
			}
		]
	},
	"msg": "success"
}
```


## 14_获取时间类型格式


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/my/timeDisplay`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>1.小程序端获取预约模式内容
发布版本：V1.0.0</p>



**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«TimeDisplayDto»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|TimeDisplayDto|TimeDisplayDto|
|&emsp;&emsp;timeDisplayType|预约/邀约时间选择类型(0仅选日期 1时分精确选择)|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"timeDisplayType": "0"
	},
	"msg": "success"
}
```


## 13_获取访客类型列表


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/my/visitor/type`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>1.访客权限组列表
发布版本：V1.0.0</p>



**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«WcMaVisitorTypeResponse»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|WcMaVisitorTypeResponse|WcMaVisitorTypeResponse|
|&emsp;&emsp;typeList|权限组列表|array|WcMaVisitorTypeDto|
|&emsp;&emsp;&emsp;&emsp;typeId|类型编号(<=32)|string||
|&emsp;&emsp;&emsp;&emsp;typeName|类型名称(<=32)|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"typeList": [
			{
				"typeId": "9c6adaf7-40f0-4e97-9af0-ea16369b9315",
				"typeName": "贵宾"
			}
		]
	},
	"msg": "success"
}
```


# 12_微信小程序_访客预约端


## 13_查询访客信息字段


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/visitor/field/info`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>查询访客信息字段(基础字段，自定义字段，来访事由，访客类型)。
 发布版本：V1.0.0</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|projectId|projectId|query|true|string||
|type|操作类型：0：访客，1：被访人|query|true|string||
|orderModel|orderModel|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«List«FieldResponse»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|array|FieldResponse|
|&emsp;&emsp;dataList||array|DataDictionarySingleDto|
|&emsp;&emsp;&emsp;&emsp;selected||boolean||
|&emsp;&emsp;&emsp;&emsp;text||string||
|&emsp;&emsp;&emsp;&emsp;value||object||
|&emsp;&emsp;fieldInfoDto||FieldInfoDto|FieldInfoDto|
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;customOption|自定义选择框的枚举值|object||
|&emsp;&emsp;&emsp;&emsp;dataValue|关联的枚举值|string||
|&emsp;&emsp;&emsp;&emsp;defaultValue|默认字段|string||
|&emsp;&emsp;&emsp;&emsp;disorder|更新顺序|integer||
|&emsp;&emsp;&emsp;&emsp;display|是否可见，0表示可见，1表示不可见|string||
|&emsp;&emsp;&emsp;&emsp;fieldProperties|字段属性：0：访客信息字段，1：被访人信息字段|string||
|&emsp;&emsp;&emsp;&emsp;fieldType|参数类型|string||
|&emsp;&emsp;&emsp;&emsp;hint|表单项的提示信息|string||
|&emsp;&emsp;&emsp;&emsp;maxLength|最大字段长度|integer||
|&emsp;&emsp;&emsp;&emsp;overseas|是否支持海外|string||
|&emsp;&emsp;&emsp;&emsp;paraId|paraId|string||
|&emsp;&emsp;&emsp;&emsp;paraKey|表单项名称key|string||
|&emsp;&emsp;&emsp;&emsp;paraName|表单项名称|string||
|&emsp;&emsp;&emsp;&emsp;placeholder|表单项的placeholder，vue-i18n多语言的key，比如人员民族中的请选择提示|string||
|&emsp;&emsp;&emsp;&emsp;productId|产品编号|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目编号|string||
|&emsp;&emsp;&emsp;&emsp;readOnly|是否可修改，0表示不可修改,1表示可修改|string||
|&emsp;&emsp;&emsp;&emsp;regular|表单的正则表达式|string||
|&emsp;&emsp;&emsp;&emsp;required|是否必填，0表示必填，1表示非必填|string||
|&emsp;&emsp;&emsp;&emsp;showType|表单项类型。1：input；2：select；3：data-picker；6：pic|string||
|&emsp;&emsp;&emsp;&emsp;status|访客字段状态：0正常 -1已删除|integer||
|&emsp;&emsp;&emsp;&emsp;tips|提示信息|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;subHint||string||
|&emsp;&emsp;subParaKey||string||
|&emsp;&emsp;subParaName||string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": [
		{
			"dataList": [
				{
					"selected": true,
					"text": "",
					"value": {}
				}
			],
			"fieldInfoDto": {
				"createTime": "2021-07-01 12:00:00",
				"customOption": "123",
				"dataValue": "123",
				"defaultValue": "其他",
				"disorder": 1,
				"display": "1",
				"fieldProperties": "0",
				"fieldType": "1",
				"hint": "123",
				"maxLength": 11,
				"overseas": "1",
				"paraId": "ccc",
				"paraKey": "123",
				"paraName": "aaa",
				"placeholder": "123",
				"productId": "bbb",
				"projectId": "aaa",
				"readOnly": "1",
				"regular": "123",
				"required": "1",
				"showType": "1",
				"status": 0,
				"tips": "输入车牌号码信息可作为您去拜访时的停车凭证",
				"updateTime": "2021-07-11 12:00:00"
			},
			"subHint": "",
			"subParaKey": "",
			"subParaName": ""
		}
	],
	"msg": "success"
}
```


## 15_小程序上传预约表单中的图片


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/visitor/image/upload`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.上传图片
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "imageData": "dgfrgrttr",
  "productId": "bbb",
  "projectId": "aaa",
  "type": "passback"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|pictureRequest|PictureRequest|body|true|PictureRequest|PictureRequest|
|&emsp;&emsp;imageData|图片数据，base64编码(不含data:image/jpg;base64)||true|object||
|&emsp;&emsp;productId|产品编号||false|string||
|&emsp;&emsp;projectId|项目编号||false|string||
|&emsp;&emsp;type|visitor/diy：预约字段||true|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«AcscImageUploadResponse»|
|201|Created|ActionErrorResult|
|204|No Content||
|401|Unauthorized|ActionErrorResult|
|403|Forbidden|ActionErrorResult|
|404|Not Found|ActionErrorResult|


**响应状态码-200**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|AcscImageUploadResponse|AcscImageUploadResponse|
|&emsp;&emsp;faceId|人脸专用：人脸图片编号|string||
|&emsp;&emsp;faceLevel|人脸专用：人脸质量级别(高>=80分，中>=70分 低>=60分 不合格<60)|string||
|&emsp;&emsp;faceScore|人脸专用：人脸评分值|integer(int32)||
|&emsp;&emsp;imageUrl|图片地址|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"faceId": "1179524873320912",
		"faceLevel": "中",
		"faceScore": 20,
		"imageUrl": "http://aliyun.com/image/122ssss.jpg"
	},
	"msg": "success"
}
```


**响应状态码-201**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-401**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-403**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-404**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


## 04_获取被访人信息


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/visitor/order/bevisitor/matching`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>通过工作单位和手机号获取被访人信息。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "beVisitorPhoneNum": "18962214556",
  "enterpriseCode": "133455556",
  "enterpriseName": "海康威视",
  "projectId": "122228959455556"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaBeVisitorGetRequest|获取被访人请求参数|body|true|WcMaBeVisitorGetRequest|WcMaBeVisitorGetRequest|
|&emsp;&emsp;beVisitorPhoneNum|被访人手机号||true|string||
|&emsp;&emsp;enterpriseCode|企业编号||false|string||
|&emsp;&emsp;enterpriseName|企业名称||true|string||
|&emsp;&emsp;projectId|租户编号||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«WcMaBeVisitorGetResponse»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|WcMaBeVisitorGetResponse|WcMaBeVisitorGetResponse|
|&emsp;&emsp;beVisitorPersonName|被访人姓名|string||
|&emsp;&emsp;beVisitorPhoneNum|被访人手机号|string||
|&emsp;&emsp;beVisitorUserId|被访人唯一标识(该字段必填)|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"beVisitorPersonName": "家父张二河",
		"beVisitorPhoneNum": "18962214556",
		"beVisitorUserId": "6546sdafs56adf"
	},
	"msg": "success"
}
```


## 10_访客取消预约


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/visitor/order/cancel`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>访客取消预约接口。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "orderId": "122228959455556"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaVisitorOrderCancelRequest|访客预约取消请求参数|body|true|WcMaVisitorOrderCancelRequest|WcMaVisitorOrderCancelRequest|
|&emsp;&emsp;orderId|预约单编号||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 03_获取预约记录详情


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/visitor/order/detail`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>查询被访记录详情接口。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "orderId": "122228959455556",
  "visitorBatch": "122228959455556"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaVisitorOrderDetailRequest|获取预约单详情请求参数|body|true|WcMaVisitorOrderDetailRequest|WcMaVisitorOrderDetailRequest|
|&emsp;&emsp;orderId|预约单编号||true|string||
|&emsp;&emsp;visitorBatch|预约单批次||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«WcMaVisitorOrderDetailResponse»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|WcMaVisitorOrderDetailResponse|WcMaVisitorOrderDetailResponse|
|&emsp;&emsp;approvalResult||string||
|&emsp;&emsp;authBarCode|二维码凭证(预约单:正常、迟到才有)|string||
|&emsp;&emsp;authIdentityPid|身份证序列号|string||
|&emsp;&emsp;authTempCard|访客卡号|string||
|&emsp;&emsp;authVisitorCode|访客验证码|string||
|&emsp;&emsp;backlogId||string||
|&emsp;&emsp;beVisitorEnterpriseName|员工所属单位|string||
|&emsp;&emsp;beVisitorGroupId|被访人部门ID|string||
|&emsp;&emsp;beVisitorGroupName|被访人部门名称|string||
|&emsp;&emsp;beVisitorOpenId|被访人openid|string||
|&emsp;&emsp;beVisitorPersonId|被访人ID|string||
|&emsp;&emsp;beVisitorPersonName|员工姓名|string||
|&emsp;&emsp;beVisitorPhoneNum|员工手机号|string||
|&emsp;&emsp;beVisitorUserId|被访人唯一标识(该字段必填)|string||
|&emsp;&emsp;buttonList|操作按钮集合|array|WcMaOperateButtonDto|
|&emsp;&emsp;&emsp;&emsp;buttonKey|按钮Key|string||
|&emsp;&emsp;&emsp;&emsp;buttonName|按钮名称|string||
|&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;createUserType|创建者身份类型：1-平台用户，2-内部人员，3-来访人员|integer(int32)||
|&emsp;&emsp;disorder|添加序号|integer(int32)||
|&emsp;&emsp;endTime|拜访时间:预计离开时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;endTimeDifference|预计离开时间时差|string||
|&emsp;&emsp;endTimeUTC|预计离开时间UTC|integer(int64)||
|&emsp;&emsp;leaderVisitor|预约人员|WcMaRetinueVisitorDto|WcMaRetinueVisitorDto|
|&emsp;&emsp;&emsp;&emsp;orderModel|预约模式 person:指定人员预约 space:场地预约|string||
|&emsp;&emsp;&emsp;&emsp;status|同行人状态|string||
|&emsp;&emsp;&emsp;&emsp;visitorAddress|访客住址|string||
|&emsp;&emsp;&emsp;&emsp;visitorBirthplace|籍贯|string||
|&emsp;&emsp;&emsp;&emsp;visitorCarNumber|车牌号|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustoma|自定义字段a|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomb|自定义字段b|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomc|自定义字段c|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomd|自定义字段d|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustome|自定义字段e|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomf|自定义字段f|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomg|自定义字段g|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomh|自定义字段h|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomi|自定义字段i|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomj|自定义字段j|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityAddr|证件地址|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityIssuer|发证机关|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityNum|证件号码|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityType|证件类型|integer||
|&emsp;&emsp;&emsp;&emsp;visitorName|访客姓名|string||
|&emsp;&emsp;&emsp;&emsp;visitorPhoneNum|手机号码|string||
|&emsp;&emsp;&emsp;&emsp;visitorPhoto|访客头像|string||
|&emsp;&emsp;&emsp;&emsp;visitorSex|性别：1、男；2、女|integer||
|&emsp;&emsp;&emsp;&emsp;visitorWorkUnit|访客所属单位|string||
|&emsp;&emsp;orderId|预约单编号|string||
|&emsp;&emsp;orderModel|预约模式 person:指定人员预约 space:场地预约|string||
|&emsp;&emsp;processId|审批规则id|string||
|&emsp;&emsp;processItemId|审批规则实例id|string||
|&emsp;&emsp;processRemark|退回原因|string||
|&emsp;&emsp;productId|产品编号|string||
|&emsp;&emsp;projectId|租户编号|string||
|&emsp;&emsp;realEndTime|签离时间|string||
|&emsp;&emsp;realEndTimeDifference|签离时间时差|string||
|&emsp;&emsp;realEndTimeUTC|签离时间UTC|integer(int64)||
|&emsp;&emsp;registerPlace|访客登记地点|string||
|&emsp;&emsp;registerTime|登记时间|string||
|&emsp;&emsp;registerTimeDifference|登记时间时差|string||
|&emsp;&emsp;registerTimeUTC|登记时间UTC|integer(int64)||
|&emsp;&emsp;retinueList|同行人列表|array|WcMaRetinueVisitorDto|
|&emsp;&emsp;&emsp;&emsp;orderModel|预约模式 person:指定人员预约 space:场地预约|string||
|&emsp;&emsp;&emsp;&emsp;status|同行人状态|string||
|&emsp;&emsp;&emsp;&emsp;visitorAddress|访客住址|string||
|&emsp;&emsp;&emsp;&emsp;visitorBirthplace|籍贯|string||
|&emsp;&emsp;&emsp;&emsp;visitorCarNumber|车牌号|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustoma|自定义字段a|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomb|自定义字段b|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomc|自定义字段c|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomd|自定义字段d|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustome|自定义字段e|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomf|自定义字段f|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomg|自定义字段g|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomh|自定义字段h|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomi|自定义字段i|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomj|自定义字段j|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityAddr|证件地址|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityIssuer|发证机关|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityNum|证件号码|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityType|证件类型|integer||
|&emsp;&emsp;&emsp;&emsp;visitorName|访客姓名|string||
|&emsp;&emsp;&emsp;&emsp;visitorPhoneNum|手机号码|string||
|&emsp;&emsp;&emsp;&emsp;visitorPhoto|访客头像|string||
|&emsp;&emsp;&emsp;&emsp;visitorSex|性别：1、男；2、女|integer||
|&emsp;&emsp;&emsp;&emsp;visitorWorkUnit|访客所属单位|string||
|&emsp;&emsp;startTime|拜访时间:预计来访时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;startTimeDifference|预计来访时间时差|string||
|&emsp;&emsp;startTimeUTC|预计来访时间UTC|integer(int64)||
|&emsp;&emsp;status|预约单状态|string||
|&emsp;&emsp;svrCodeIdentity|证件照对应图片服务器serviceNodes|string||
|&emsp;&emsp;svrCodeScanning|证件扫描照对应图片服务器serviceNodes|string||
|&emsp;&emsp;svrCodeVisitor|访客头像对应图片服务器serviceNodes|string||
|&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;visitBatch|访客批次|string||
|&emsp;&emsp;visitorAddress|访客住址|string||
|&emsp;&emsp;visitorAllowTimes|访客进入次数|integer(int32)||
|&emsp;&emsp;visitorBatch|预约单批次|string||
|&emsp;&emsp;visitorBirthplace|籍贯|string||
|&emsp;&emsp;visitorCarNumber|车牌号|string||
|&emsp;&emsp;visitorCustoma|自定义字段a：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomb|自定义字段b：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomc|自定义字段c：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomd|自定义字段d：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustome|自定义字段e：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomf|自定义字段f：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomg|自定义字段g：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomh|自定义字段h：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomi|自定义字段i：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomj|自定义字段j：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorGroupId|访客名单分组ID|string||
|&emsp;&emsp;visitorIdentityAddr|证件地址|string||
|&emsp;&emsp;visitorIdentityIssuer|发证机关|string||
|&emsp;&emsp;visitorIdentityNum|证件号码|string||
|&emsp;&emsp;visitorIdentityPhoto|证件照片|string||
|&emsp;&emsp;visitorIdentityType|证件类型：111、身份证|integer(int32)||
|&emsp;&emsp;visitorLeader|访客团体领队:0 同行人 1领队|string||
|&emsp;&emsp;visitorName|姓名|string||
|&emsp;&emsp;visitorOpenId|访客微信公众号唯一标识|string||
|&emsp;&emsp;visitorPersonNum|来访人数|integer(int32)||
|&emsp;&emsp;visitorPhoneNum|手机号|string||
|&emsp;&emsp;visitorPhoto|访客头像|string||
|&emsp;&emsp;visitorPhotoFlag|人脸质量合格标识。0：合格；1：不合格|string||
|&emsp;&emsp;visitorPinyin|访客名首字母缩写|string||
|&emsp;&emsp;visitorPrivilegeGroupIds|访客权限组ids|string||
|&emsp;&emsp;visitorPurpose|事由|string||
|&emsp;&emsp;visitorScanningPhoto|证件扫描照片|string||
|&emsp;&emsp;visitorSex|性别：1、男；2、女|integer(int32)||
|&emsp;&emsp;visitorTemperature|访客体温|string||
|&emsp;&emsp;visitorTemperatureStatus|访客体温状态|integer(int32)||
|&emsp;&emsp;visitorTypeId|访客类型id|string||
|&emsp;&emsp;visitorUserId||string||
|&emsp;&emsp;visitorWorkUnit|访客来访单位|string||
|&emsp;&emsp;webLabel|记录状态描述-web端|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"approvalResult": "",
		"authBarCode": "123",
		"authIdentityPid": "123",
		"authTempCard": "123",
		"authVisitorCode": "123",
		"backlogId": "",
		"beVisitorEnterpriseName": "海康威视",
		"beVisitorGroupId": "123",
		"beVisitorGroupName": "123",
		"beVisitorOpenId": "123",
		"beVisitorPersonId": "123",
		"beVisitorPersonName": "陈大鹏",
		"beVisitorPhoneNum": "123",
		"beVisitorUserId": "6546sdafs56adf",
		"buttonList": [
			{
				"buttonKey": "InvitationFoundByBeVisitor",
				"buttonName": "重新邀约"
			}
		],
		"createTime": "123",
		"createUserType": 123,
		"disorder": 123,
		"endTime": "2021-12-23 18:22:12",
		"endTimeDifference": "123",
		"endTimeUTC": 123,
		"leaderVisitor": {
			"orderModel": "person",
			"status": "已取消",
			"visitorAddress": "中南海",
			"visitorBirthplace": "安徽",
			"visitorCarNumber": "浙A12345",
			"visitorCustoma": "123232323",
			"visitorCustomb": "123232323",
			"visitorCustomc": "123232323",
			"visitorCustomd": "123232323",
			"visitorCustome": "123232323",
			"visitorCustomf": "123232323",
			"visitorCustomg": "123232323",
			"visitorCustomh": "123232323",
			"visitorCustomi": "123232323",
			"visitorCustomj": "123232323",
			"visitorIdentityAddr": "安徽芜湖",
			"visitorIdentityIssuer": "芜湖公安",
			"visitorIdentityNum": "123232323",
			"visitorIdentityType": 111,
			"visitorName": "陈绍鹏",
			"visitorPhoneNum": "18966175813",
			"visitorPhoto": "123",
			"visitorSex": 1,
			"visitorWorkUnit": "大碗娱乐无限责任公司"
		},
		"orderId": "122228959455556",
		"orderModel": "person",
		"processId": "123",
		"processItemId": "123",
		"processRemark": "122228959455556",
		"productId": "123",
		"projectId": "122228959455556",
		"realEndTime": "123",
		"realEndTimeDifference": "123",
		"realEndTimeUTC": 123,
		"registerPlace": "123",
		"registerTime": "123",
		"registerTimeDifference": "123",
		"registerTimeUTC": 123,
		"retinueList": [
			{
				"orderModel": "person",
				"status": "已取消",
				"visitorAddress": "中南海",
				"visitorBirthplace": "安徽",
				"visitorCarNumber": "浙A12345",
				"visitorCustoma": "123232323",
				"visitorCustomb": "123232323",
				"visitorCustomc": "123232323",
				"visitorCustomd": "123232323",
				"visitorCustome": "123232323",
				"visitorCustomf": "123232323",
				"visitorCustomg": "123232323",
				"visitorCustomh": "123232323",
				"visitorCustomi": "123232323",
				"visitorCustomj": "123232323",
				"visitorIdentityAddr": "安徽芜湖",
				"visitorIdentityIssuer": "芜湖公安",
				"visitorIdentityNum": "123232323",
				"visitorIdentityType": 111,
				"visitorName": "陈绍鹏",
				"visitorPhoneNum": "18966175813",
				"visitorPhoto": "123",
				"visitorSex": 1,
				"visitorWorkUnit": "大碗娱乐无限责任公司"
			}
		],
		"startTime": "2021-12-22 18:22:12",
		"startTimeDifference": "123",
		"startTimeUTC": 123,
		"status": "待审批",
		"svrCodeIdentity": "123",
		"svrCodeScanning": "123",
		"svrCodeVisitor": "123",
		"updateTime": "123",
		"visitBatch": "123",
		"visitorAddress": "123",
		"visitorAllowTimes": 123,
		"visitorBatch": "122228959455556",
		"visitorBirthplace": "123",
		"visitorCarNumber": "浙A12345",
		"visitorCustoma": "123",
		"visitorCustomb": "123",
		"visitorCustomc": "123",
		"visitorCustomd": "123",
		"visitorCustome": "123",
		"visitorCustomf": "123",
		"visitorCustomg": "123",
		"visitorCustomh": "123",
		"visitorCustomi": "123",
		"visitorCustomj": "123",
		"visitorGroupId": "123",
		"visitorIdentityAddr": "123",
		"visitorIdentityIssuer": "123",
		"visitorIdentityNum": "123",
		"visitorIdentityPhoto": "123",
		"visitorIdentityType": 123,
		"visitorLeader": "0",
		"visitorName": "123",
		"visitorOpenId": "123",
		"visitorPersonNum": 123,
		"visitorPhoneNum": "123",
		"visitorPhoto": "123",
		"visitorPhotoFlag": "123",
		"visitorPinyin": "123",
		"visitorPrivilegeGroupIds": "123",
		"visitorPurpose": "参观",
		"visitorScanningPhoto": "123",
		"visitorSex": 123,
		"visitorTemperature": "123",
		"visitorTemperatureStatus": 123,
		"visitorTypeId": "123",
		"visitorUserId": "",
		"visitorWorkUnit": "123",
		"webLabel": "123"
	},
	"msg": "success"
}
```


## 05_访客预约


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/visitor/order/founding`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>访客访客预约接口。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "beVisitorPersonName": "家父张二河",
  "beVisitorPhoneNum": "18962214556",
  "beVisitorUserId": "6546sdafs56adf",
  "endTime": "2021-12-23 18:22",
  "orderId": "6546sdafs56adf",
  "orderModel": "person",
  "projectId": "122228959455556",
  "startTime": "2021-12-22 18:22",
  "visitEndTime": "2004-05-03T18:30:08+08:00",
  "visitStartTime": "2004-05-03T17:30:08+08:00",
  "visitorAddress": "123232323",
  "visitorBirthplace": "123232323",
  "visitorCarNumber": "浙A12232",
  "visitorCustoma": "123232323",
  "visitorCustomb": "123232323",
  "visitorCustomc": "123232323",
  "visitorCustomd": "123232323",
  "visitorCustome": "123232323",
  "visitorCustomf": "123",
  "visitorCustomg": "123",
  "visitorCustomh": "123",
  "visitorCustomi": "123",
  "visitorCustomj": "123",
  "visitorIdentityAddr": "123232323",
  "visitorIdentityIssuer": "123232323",
  "visitorIdentityNum": "123232323",
  "visitorIdentityType": "111",
  "visitorPersonNum": "10",
  "visitorPrivilegeGroupIds": "123232323,2222222,33333333",
  "visitorPurpose": "参观",
  "visitorUserId": "",
  "visitorWorkUnit": "123232323"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaVisitorStartRequest|访客预约请求参数|body|true|WcMaVisitorStartRequest|WcMaVisitorStartRequest|
|&emsp;&emsp;beVisitorPersonName|被访人姓名||true|string||
|&emsp;&emsp;beVisitorPhoneNum|被访人手机号||true|string||
|&emsp;&emsp;beVisitorUserId|被访人唯一标识(该字段必填)||true|string||
|&emsp;&emsp;endTime|拜访时间:预计离开时间(yyyy-MM-dd HH:mm)||false|string||
|&emsp;&emsp;orderId|预约单Id||false|object||
|&emsp;&emsp;orderModel|预约模式 person:指定人员预约 space:场地预约||false|string||
|&emsp;&emsp;projectId|租户编号||true|string||
|&emsp;&emsp;startTime|拜访时间:预计来访时间(yyyy-MM-dd HH:mm)||false|string||
|&emsp;&emsp;visitEndTime|预计离开时间,必须晚于当前时间和预计来访时间||false|object||
|&emsp;&emsp;visitStartTime|预计来访时间||false|object||
|&emsp;&emsp;visitorAddress|访客住址||false|object||
|&emsp;&emsp;visitorBirthplace|籍贯||false|object||
|&emsp;&emsp;visitorCarNumber|车牌号||false|string||
|&emsp;&emsp;visitorCustoma|自定义字段a：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|object||
|&emsp;&emsp;visitorCustomb|自定义字段b：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|object||
|&emsp;&emsp;visitorCustomc|自定义字段c：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|object||
|&emsp;&emsp;visitorCustomd|自定义字段d：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|object||
|&emsp;&emsp;visitorCustome|自定义字段e：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|object||
|&emsp;&emsp;visitorCustomf|自定义字段f：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|string||
|&emsp;&emsp;visitorCustomg|自定义字段g：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|string||
|&emsp;&emsp;visitorCustomh|自定义字段h：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|string||
|&emsp;&emsp;visitorCustomi|自定义字段i：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|string||
|&emsp;&emsp;visitorCustomj|自定义字段j：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|string||
|&emsp;&emsp;visitorIdentityAddr|证件地址||false|object||
|&emsp;&emsp;visitorIdentityIssuer|发证机关||false|object||
|&emsp;&emsp;visitorIdentityNum|证件号码||false|object||
|&emsp;&emsp;visitorIdentityType|证件类型||false|object||
|&emsp;&emsp;visitorPersonNum|访客人数：默认1||false|object||
|&emsp;&emsp;visitorPrivilegeGroupIds|访客权限组ids，以,分割权限组id||false|object||
|&emsp;&emsp;visitorPurpose|来访事由,长度为1～128个字符||false|string||
|&emsp;&emsp;visitorUserId|||false|string||
|&emsp;&emsp;visitorWorkUnit|访客来访单位||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 01_获取待拜访记录


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/visitor/order/go/log/doing`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>获取待拜访,根据被访者openid和预约单:正常和迟到、访客已登记、待审批、审批退回 过滤数据，按来访时间顺序。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "pageNo": 1,
  "pageSize": 20
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaVisitorGoingRequest|访客待拜访请求参数|body|true|WcMaVisitorGoingRequest|WcMaVisitorGoingRequest|
|&emsp;&emsp;pageNo|页码（pageNo>0）||true|integer(int32)||
|&emsp;&emsp;pageSize|页大小（0<pageSize<=1000）||true|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PageResult«WcMaVisitorOrderCardDto»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PageResult«WcMaVisitorOrderCardDto»|PageResult«WcMaVisitorOrderCardDto»|
|&emsp;&emsp;list|数据信息|array|WcMaVisitorOrderCardDto|
|&emsp;&emsp;&emsp;&emsp;backlogId||string||
|&emsp;&emsp;&emsp;&emsp;beVisitorEnterpriseName|员工所属单位|string||
|&emsp;&emsp;&emsp;&emsp;beVisitorPersonName|员工姓名|string||
|&emsp;&emsp;&emsp;&emsp;buttonList|操作按钮集合|array|WcMaOperateButtonDto|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;buttonKey|按钮Key|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;buttonName|按钮名称|string||
|&emsp;&emsp;&emsp;&emsp;endTime|预计离开时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;&emsp;&emsp;orderId|预约单编号|string||
|&emsp;&emsp;&emsp;&emsp;orderModel|预约模式 person:指定人员预约 space:场地预约|string||
|&emsp;&emsp;&emsp;&emsp;projectId|租户编号|string||
|&emsp;&emsp;&emsp;&emsp;startTime|预计来访时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;&emsp;&emsp;status|预约单状态|string||
|&emsp;&emsp;&emsp;&emsp;visitorBatch|预约单批次|string||
|&emsp;&emsp;&emsp;&emsp;visitorPurpose|事由|string||
|&emsp;&emsp;pageNo|页码|integer(int32)||
|&emsp;&emsp;pageSize|页大小|integer(int32)||
|&emsp;&emsp;total|总条数|integer(int64)||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"list": [
			{
				"backlogId": "",
				"beVisitorEnterpriseName": "海康威视",
				"beVisitorPersonName": "陈大鹏",
				"buttonList": [
					{
						"buttonKey": "InvitationFoundByBeVisitor",
						"buttonName": "重新邀约"
					}
				],
				"endTime": "2021-12-23 18:22:12",
				"orderId": "122228959455556",
				"orderModel": "person",
				"projectId": "122228959455556",
				"startTime": "2021-12-22 18:22:12",
				"status": "待审批",
				"visitorBatch": "122228959455556",
				"visitorPurpose": "参观"
			}
		],
		"pageNo": 1,
		"pageSize": 20,
		"total": 5
	},
	"msg": "success"
}
```


## 02_获取拜访历史记录


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/visitor/order/go/log/history`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>获取受访历史记录,根据被访者openid和预约单:逾期(系统) 预约单:超期自动签离(系统)、访客签离和超期未签离(系统) 过滤数据，按来访时间倒序。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "beVisitorPersonName": "陈大鹏",
  "pageNo": 1,
  "pageSize": 20,
  "tabKey": "陈大鹏"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaVisitorGoHistoryRequest|员工拜访历史记录请求参数|body|true|WcMaVisitorGoHistoryRequest|WcMaVisitorGoHistoryRequest|
|&emsp;&emsp;beVisitorPersonName|员工姓名||false|string||
|&emsp;&emsp;pageNo|页码（pageNo>0）||true|integer(int32)||
|&emsp;&emsp;pageSize|页大小（0<pageSize<=1000）||true|integer(int32)||
|&emsp;&emsp;tabKey|TAB类型(0全部 1已失效 2已拜访)||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PageResult«WcMaVisitorOrderCardDto»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PageResult«WcMaVisitorOrderCardDto»|PageResult«WcMaVisitorOrderCardDto»|
|&emsp;&emsp;list|数据信息|array|WcMaVisitorOrderCardDto|
|&emsp;&emsp;&emsp;&emsp;backlogId||string||
|&emsp;&emsp;&emsp;&emsp;beVisitorEnterpriseName|员工所属单位|string||
|&emsp;&emsp;&emsp;&emsp;beVisitorPersonName|员工姓名|string||
|&emsp;&emsp;&emsp;&emsp;buttonList|操作按钮集合|array|WcMaOperateButtonDto|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;buttonKey|按钮Key|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;buttonName|按钮名称|string||
|&emsp;&emsp;&emsp;&emsp;endTime|预计离开时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;&emsp;&emsp;orderId|预约单编号|string||
|&emsp;&emsp;&emsp;&emsp;orderModel|预约模式 person:指定人员预约 space:场地预约|string||
|&emsp;&emsp;&emsp;&emsp;projectId|租户编号|string||
|&emsp;&emsp;&emsp;&emsp;startTime|预计来访时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;&emsp;&emsp;status|预约单状态|string||
|&emsp;&emsp;&emsp;&emsp;visitorBatch|预约单批次|string||
|&emsp;&emsp;&emsp;&emsp;visitorPurpose|事由|string||
|&emsp;&emsp;pageNo|页码|integer(int32)||
|&emsp;&emsp;pageSize|页大小|integer(int32)||
|&emsp;&emsp;total|总条数|integer(int64)||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"list": [
			{
				"backlogId": "",
				"beVisitorEnterpriseName": "海康威视",
				"beVisitorPersonName": "陈大鹏",
				"buttonList": [
					{
						"buttonKey": "InvitationFoundByBeVisitor",
						"buttonName": "重新邀约"
					}
				],
				"endTime": "2021-12-23 18:22:12",
				"orderId": "122228959455556",
				"orderModel": "person",
				"projectId": "122228959455556",
				"startTime": "2021-12-22 18:22:12",
				"status": "待审批",
				"visitorBatch": "122228959455556",
				"visitorPurpose": "参观"
			}
		],
		"pageNo": 1,
		"pageSize": 20,
		"total": 5
	},
	"msg": "success"
}
```


## 09_接受邀约


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/visitor/order/invitation/accepting`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.访客点击邀约请求，接受邀约
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "visitorAddress": "中南海",
  "visitorBatch": "122228959455556",
  "visitorBirthplace": "安徽",
  "visitorCarNumber": "浙A12345",
  "visitorCustoma": "123232323",
  "visitorCustomb": "123232323",
  "visitorCustomc": "123232323",
  "visitorCustomd": "123232323",
  "visitorCustome": "123232323",
  "visitorCustomf": "123232323",
  "visitorCustomg": "123232323",
  "visitorCustomh": "123232323",
  "visitorCustomi": "123232323",
  "visitorCustomj": "123232323",
  "visitorIdentityAddr": "安徽芜湖",
  "visitorIdentityIssuer": "芜湖公安",
  "visitorIdentityNum": "123232323",
  "visitorIdentityType": 111
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaInvitationAcceptRequest|员工应邀请求参数|body|true|WcMaInvitationAcceptRequest|WcMaInvitationAcceptRequest|
|&emsp;&emsp;visitorAddress|访客住址||false|string||
|&emsp;&emsp;visitorBatch|预约单批次||true|string||
|&emsp;&emsp;visitorBirthplace|籍贯||false|string||
|&emsp;&emsp;visitorCarNumber|车牌号||false|string||
|&emsp;&emsp;visitorCustoma|自定义字段a||false|string||
|&emsp;&emsp;visitorCustomb|自定义字段b||false|string||
|&emsp;&emsp;visitorCustomc|自定义字段c||false|string||
|&emsp;&emsp;visitorCustomd|自定义字段d||false|string||
|&emsp;&emsp;visitorCustome|自定义字段e||false|string||
|&emsp;&emsp;visitorCustomf|自定义字段f||false|string||
|&emsp;&emsp;visitorCustomg|自定义字段g||false|string||
|&emsp;&emsp;visitorCustomh|自定义字段h||false|string||
|&emsp;&emsp;visitorCustomi|自定义字段i||false|string||
|&emsp;&emsp;visitorCustomj|自定义字段j||false|string||
|&emsp;&emsp;visitorIdentityAddr|证件地址||false|string||
|&emsp;&emsp;visitorIdentityIssuer|发证机关||false|string||
|&emsp;&emsp;visitorIdentityNum|证件号码||false|string||
|&emsp;&emsp;visitorIdentityType|证件类型||false|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 08_邀约预览


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/visitor/order/invitation/preview`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.访客邀约信息预览
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "visitorBatch": "122228959455556"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaInvitationPreviewRequest|邀约预览请求参数|body|true|WcMaInvitationPreviewRequest|WcMaInvitationPreviewRequest|
|&emsp;&emsp;visitorBatch|预约单批次号||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«WcMaInvitationPreviewResponse»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|WcMaInvitationPreviewResponse|WcMaInvitationPreviewResponse|
|&emsp;&emsp;beVisitorEnterpriseName|员工所属单位|string||
|&emsp;&emsp;beVisitorPersonName|员工姓名|string||
|&emsp;&emsp;beVisitorPhoneNum|员工手机号|string||
|&emsp;&emsp;endTime|拜访时间:预计离开时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;projectId|项目编号|string||
|&emsp;&emsp;startTime|拜访时间:预计来访时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;visitorBatch|预约单批次号|string||
|&emsp;&emsp;visitorPurpose|事由|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"beVisitorEnterpriseName": "海康威视",
		"beVisitorPersonName": "陈大鹏",
		"beVisitorPhoneNum": "123",
		"endTime": "2021-12-23 18:22:12",
		"projectId": "aaa",
		"startTime": "2021-12-22 18:22:12",
		"visitorBatch": "122228959455556",
		"visitorPurpose": "参观"
	},
	"msg": "success"
}
```


## 12_获取二维码凭证


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/visitor/order/qrcode/refresh`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>访客获取二维码接口。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "orderId": "122228959455556"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaVisitorQrCodeGetRequest|访客获取二维码凭证请求参数|body|true|WcMaVisitorQrCodeGetRequest|WcMaVisitorQrCodeGetRequest|
|&emsp;&emsp;orderId|预约单编号||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«WcMaVisitorQrCodeGetResponse»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|WcMaVisitorQrCodeGetResponse|WcMaVisitorQrCodeGetResponse|
|&emsp;&emsp;authBarCode|二维码凭证(预约单:正常、迟到才有)|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"authBarCode": "123"
	},
	"msg": "success"
}
```


## 07_确认同行


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/visitor/order/retinue/confirm`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.访客点击确认同行，接受同行人邀请
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "visitorAddress": "中南海",
  "visitorBatch": "122228959455556",
  "visitorBirthplace": "安徽",
  "visitorCarNumber": "浙A12345",
  "visitorCustoma": "123232323",
  "visitorCustomb": "123232323",
  "visitorCustomc": "123232323",
  "visitorCustomd": "123232323",
  "visitorCustome": "123232323",
  "visitorCustomf": "123232323",
  "visitorCustomg": "123232323",
  "visitorCustomh": "123232323",
  "visitorCustomi": "123232323",
  "visitorCustomj": "123232323",
  "visitorIdentityAddr": "安徽芜湖",
  "visitorIdentityIssuer": "芜湖公安",
  "visitorIdentityNum": "123232323",
  "visitorIdentityType": 111
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaRetinueConfirmRequest|同行预览请求参数|body|true|WcMaRetinueConfirmRequest|WcMaRetinueConfirmRequest|
|&emsp;&emsp;visitorAddress|访客住址||false|string||
|&emsp;&emsp;visitorBatch|预约单批次||true|string||
|&emsp;&emsp;visitorBirthplace|籍贯||false|string||
|&emsp;&emsp;visitorCarNumber|车牌号||false|string||
|&emsp;&emsp;visitorCustoma|自定义字段a||false|string||
|&emsp;&emsp;visitorCustomb|自定义字段b||false|string||
|&emsp;&emsp;visitorCustomc|自定义字段c||false|string||
|&emsp;&emsp;visitorCustomd|自定义字段d||false|string||
|&emsp;&emsp;visitorCustome|自定义字段e||false|string||
|&emsp;&emsp;visitorCustomf|自定义字段f||false|string||
|&emsp;&emsp;visitorCustomg|自定义字段g||false|string||
|&emsp;&emsp;visitorCustomh|自定义字段h||false|string||
|&emsp;&emsp;visitorCustomi|自定义字段i||false|string||
|&emsp;&emsp;visitorCustomj|自定义字段j||false|string||
|&emsp;&emsp;visitorIdentityAddr|证件地址||false|string||
|&emsp;&emsp;visitorIdentityIssuer|发证机关||false|string||
|&emsp;&emsp;visitorIdentityNum|证件号码||false|string||
|&emsp;&emsp;visitorIdentityType|证件类型||false|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 06_同行人邀请预览


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/visitor/order/retinue/preview`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.访客同行人邀请预览
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "visitorBatch": "122228959455556"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaRetinuePreviewRequest|同行预览请求参数|body|true|WcMaRetinuePreviewRequest|WcMaRetinuePreviewRequest|
|&emsp;&emsp;visitorBatch|预约单批次||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«WcMaRetinuePreviewResponse»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|WcMaRetinuePreviewResponse|WcMaRetinuePreviewResponse|
|&emsp;&emsp;beVisitorEnterpriseName|员工所属单位|string||
|&emsp;&emsp;beVisitorPersonName|员工姓名|string||
|&emsp;&emsp;beVisitorPhoneNum|员工手机号|string||
|&emsp;&emsp;endTime|拜访时间:预计离开时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;startTime|拜访时间:预计来访时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;visitorBatch|预约单批次|string||
|&emsp;&emsp;visitorPurpose|事由|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"beVisitorEnterpriseName": "海康威视",
		"beVisitorPersonName": "陈大鹏",
		"beVisitorPhoneNum": "123",
		"endTime": "2021-12-23 18:22:12",
		"startTime": "2021-12-22 18:22:12",
		"visitorBatch": "122228959455556",
		"visitorPurpose": "参观"
	},
	"msg": "success"
}
```


## 05_访客提交预约


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/visitor/order/submit`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>访客提交预约接口，带同行人，状态为待提交时的提交操作。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "orderId": "122228959455556"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaVisitorOrderCancelRequest|访客预约取消请求参数|body|true|WcMaVisitorOrderCancelRequest|WcMaVisitorOrderCancelRequest|
|&emsp;&emsp;orderId|预约单编号||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 11_访客修改预约


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/visitor/order/update`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>访客修改预约接口。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "beVisitorPersonName": "家父张二河",
  "beVisitorPhoneNum": "18962214556",
  "beVisitorUserId": "6546sdafs56adf",
  "endTime": "2021-12-23 18:22",
  "orderId": "6546sdafs56adf",
  "orderModel": "person",
  "projectId": "122228959455556",
  "startTime": "2021-12-22 18:22",
  "visitEndTime": "2004-05-03T18:30:08+08:00",
  "visitStartTime": "2004-05-03T17:30:08+08:00",
  "visitorAddress": "123232323",
  "visitorBirthplace": "123232323",
  "visitorCarNumber": "浙A12232",
  "visitorCustoma": "123232323",
  "visitorCustomb": "123232323",
  "visitorCustomc": "123232323",
  "visitorCustomd": "123232323",
  "visitorCustome": "123232323",
  "visitorCustomf": "123",
  "visitorCustomg": "123",
  "visitorCustomh": "123",
  "visitorCustomi": "123",
  "visitorCustomj": "123",
  "visitorIdentityAddr": "123232323",
  "visitorIdentityIssuer": "123232323",
  "visitorIdentityNum": "123232323",
  "visitorIdentityType": "111",
  "visitorPersonNum": "10",
  "visitorPrivilegeGroupIds": "123232323,2222222,33333333",
  "visitorPurpose": "参观",
  "visitorUserId": "",
  "visitorWorkUnit": "123232323"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaVisitorStartRequest|访客预约请求参数|body|true|WcMaVisitorStartRequest|WcMaVisitorStartRequest|
|&emsp;&emsp;beVisitorPersonName|被访人姓名||true|string||
|&emsp;&emsp;beVisitorPhoneNum|被访人手机号||true|string||
|&emsp;&emsp;beVisitorUserId|被访人唯一标识(该字段必填)||true|string||
|&emsp;&emsp;endTime|拜访时间:预计离开时间(yyyy-MM-dd HH:mm)||false|string||
|&emsp;&emsp;orderId|预约单Id||false|object||
|&emsp;&emsp;orderModel|预约模式 person:指定人员预约 space:场地预约||false|string||
|&emsp;&emsp;projectId|租户编号||true|string||
|&emsp;&emsp;startTime|拜访时间:预计来访时间(yyyy-MM-dd HH:mm)||false|string||
|&emsp;&emsp;visitEndTime|预计离开时间,必须晚于当前时间和预计来访时间||false|object||
|&emsp;&emsp;visitStartTime|预计来访时间||false|object||
|&emsp;&emsp;visitorAddress|访客住址||false|object||
|&emsp;&emsp;visitorBirthplace|籍贯||false|object||
|&emsp;&emsp;visitorCarNumber|车牌号||false|string||
|&emsp;&emsp;visitorCustoma|自定义字段a：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|object||
|&emsp;&emsp;visitorCustomb|自定义字段b：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|object||
|&emsp;&emsp;visitorCustomc|自定义字段c：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|object||
|&emsp;&emsp;visitorCustomd|自定义字段d：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|object||
|&emsp;&emsp;visitorCustome|自定义字段e：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|object||
|&emsp;&emsp;visitorCustomf|自定义字段f：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|string||
|&emsp;&emsp;visitorCustomg|自定义字段g：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|string||
|&emsp;&emsp;visitorCustomh|自定义字段h：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|string||
|&emsp;&emsp;visitorCustomi|自定义字段i：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|string||
|&emsp;&emsp;visitorCustomj|自定义字段j：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片||false|string||
|&emsp;&emsp;visitorIdentityAddr|证件地址||false|object||
|&emsp;&emsp;visitorIdentityIssuer|发证机关||false|object||
|&emsp;&emsp;visitorIdentityNum|证件号码||false|object||
|&emsp;&emsp;visitorIdentityType|证件类型||false|object||
|&emsp;&emsp;visitorPersonNum|访客人数：默认1||false|object||
|&emsp;&emsp;visitorPrivilegeGroupIds|访客权限组ids，以,分割权限组id||false|object||
|&emsp;&emsp;visitorPurpose|来访事由,长度为1～128个字符||false|string||
|&emsp;&emsp;visitorUserId|||false|string||
|&emsp;&emsp;visitorWorkUnit|访客来访单位||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 17_小程序端获取预约模式内容


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/visitor/orderModel/config`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>1.小程序端获取预约模式内容
发布版本：V1.0.0</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|projectId|projectId|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«OrderModelConfig»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|OrderModelConfig|OrderModelConfig|
|&emsp;&emsp;beVisitorPersonId|场地模式状态下-被访人唯一标识(该字段必填)|object||
|&emsp;&emsp;beVisitorPersonName|场地模式状态下-被访人姓名|object||
|&emsp;&emsp;beVisitorPhoneNum|场地模式状态下-被访人手机号|object||
|&emsp;&emsp;personModelStatus|人员模式状态 close:关闭 open:打开|string||
|&emsp;&emsp;spaceModelList|场地列表|array|OrderSpaceModel|
|&emsp;&emsp;&emsp;&emsp;beVisitorPersonId|场地模式状态下-被访人唯一标识(该字段必填)|object||
|&emsp;&emsp;&emsp;&emsp;beVisitorPersonName|场地模式状态下-被访人姓名|object||
|&emsp;&emsp;&emsp;&emsp;beVisitorPhoneNum|场地模式状态下-被访人手机号|object||
|&emsp;&emsp;&emsp;&emsp;spaceName|场地名称|string||
|&emsp;&emsp;spaceModelStatus|场地模式状态 close:关闭 open:打开|string||
|&emsp;&emsp;spaceName|场地名称|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"beVisitorPersonId": "6546sdafs56adf",
		"beVisitorPersonName": "aaaa",
		"beVisitorPhoneNum": "123232323",
		"personModelStatus": "close",
		"spaceModelList": "close",
		"spaceModelStatus": "close",
		"spaceName": "close"
	},
	"msg": "success"
}
```


## 16_获取访客通行证配置


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/visitor/phConfig/info`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>获取访客通行证配置。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "projectId": "122228959455556"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaPhConfigRequest|获取通行证配置的参数|body|true|WcMaPhConfigRequest|WcMaPhConfigRequest|
|&emsp;&emsp;projectId|租户编号||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PhConfigWebResponse»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PhConfigWebResponse|PhConfigWebResponse|
|&emsp;&emsp;backPicName|通行证的背景图名称|string||
|&emsp;&emsp;backPicUrl|通行证的背景图片|string||
|&emsp;&emsp;configStatus|通行证的配置开启或者关闭状态 open:开启 close:关闭(默认)|string||
|&emsp;&emsp;endContent|通行证的末尾内容|string||
|&emsp;&emsp;phConfigId|通行证的配置id|string||
|&emsp;&emsp;phItems|通行证的内容选项集合|array|PhItem|
|&emsp;&emsp;&emsp;&emsp;format|格式:比如时间的格式 yyyy-MM-dd / yyyy-MM-dd HH:mm:ss /yyyy年MM月dd日|string||
|&emsp;&emsp;&emsp;&emsp;key|入园通行证的key值 头像：visitorPhoto  姓名：visitorName  手机号码: visitorPhoneNum  车牌号 ：visitorCarNumber  证件号码：visitorIdentityNum  来访事由：visitorPurpose  来访单位：visitorWorkUnit   被访对象的姓名：beVisitorPersonName 被访对象的组织：beVisitorGroupName  被访对象的手机号码：beVisitorPhoneNum 有效期的开始时间：startTime 有效期的结束时间：endTime 审批状态：approvalResult  登记时间: registerTime   二维码：authBarCode 分割线:separator  空行:blankLine |string||
|&emsp;&emsp;&emsp;&emsp;name|通行证选项对应的名称:比如姓名/手机号码;二维码、头像、分割线、空行的name不存在的|string||
|&emsp;&emsp;&emsp;&emsp;value|通行证选项对应的值:比如姓名对应的值|string||
|&emsp;&emsp;productCode|产品编号|string||
|&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;title|通行证的标题|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"backPicName": "通行证",
		"backPicUrl": "http://7412f756-1625137475555876-face.oss-cn-hangzhou.aliyuncs.com/photo/783210920129584.jpg",
		"configStatus": "close",
		"endContent": "欢迎来到烟台工程职业技术学院",
		"phConfigId": "5d5f434c4543accda02680b600afe6b3",
		"phItems": "[]",
		"productCode": "1625137405416832",
		"projectId": "1805308421418544",
		"title": "高职学院的入园通行证"
	},
	"msg": "success"
}
```


## 14_小程序端获取防疫承诺配置信息


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/visitor/promise/info`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.小程序端获取防疫承诺配置信息
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "projectId": "122228959455556"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaPurposeRequest|获取事由列表请求参数|body|true|WcMaPurposeRequest|WcMaPurposeRequest|
|&emsp;&emsp;projectId|租户编号(从选择工作单位的类别中获取，若没有工作单位列表选择可为空)||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PromiseAllResponse»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PromiseAllResponse|PromiseAllResponse|
|&emsp;&emsp;beforeDetails|预约前防疫承诺详情List|array|PromiseDetailDto|
|&emsp;&emsp;&emsp;&emsp;detailsContent|详情内容，子页面中的承诺内容|string||
|&emsp;&emsp;&emsp;&emsp;detailsFlag|详情选项（承诺类型为2单选时存在，返回选择的该是或否）|boolean||
|&emsp;&emsp;&emsp;&emsp;promiseType|承诺类型（1末尾提示，2单选）|integer||
|&emsp;&emsp;inDetails|预约时防疫承诺详情List|array|PromiseDetailDto|
|&emsp;&emsp;&emsp;&emsp;detailsContent|详情内容，子页面中的承诺内容|string||
|&emsp;&emsp;&emsp;&emsp;detailsFlag|详情选项（承诺类型为2单选时存在，返回选择的该是或否）|boolean||
|&emsp;&emsp;&emsp;&emsp;promiseType|承诺类型（1末尾提示，2单选）|integer||
|&emsp;&emsp;informDetails|告知书详情|PromiseInformDto|PromiseInformDto|
|&emsp;&emsp;&emsp;&emsp;detailsContent|详情内容，子页面中的承诺内容|string||
|&emsp;&emsp;&emsp;&emsp;detailsName|详情名称，(当承诺类型为3告知书时，存在)|string||
|&emsp;&emsp;showBeforeFlag|预约前是否弹框标志|boolean||
|&emsp;&emsp;showInFlag|预约时展示在访客预约字段后面的标志|boolean||
|&emsp;&emsp;showInformFlag|告知书是否弹框标志|boolean||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"beforeDetails": "xxx",
		"inDetails": "xxx",
		"informDetails": {
			"detailsContent": "详情内容",
			"detailsName": ""
		},
		"showBeforeFlag": true,
		"showInFlag": true,
		"showInformFlag": true
	},
	"msg": "success"
}
```


# 13_微信小程序_访客审核端


## 16_员工重发邀约短信


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/bevisitor/invitation/again/send/sms`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.员工重发邀约短信 (入参只需（visitorBatch）)
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "shareStatus": "122228959455556",
  "visitorBatch": "122228959455556"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaOrderShareRequest|WcMaOrderShareRequest|body|true|WcMaOrderShareRequest|WcMaOrderShareRequest|
|&emsp;&emsp;shareStatus|链接状态 0废弃 1正常||false|string||
|&emsp;&emsp;visitorBatch|预约单批次||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 10_员工取消预约


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/bevisitor/order/cancel`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>员工预约取消接口。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "visitorBatch": "122228959455556"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaBeVisitorOrderCancelRequest|员工预约取消请求参数|body|true|WcMaBeVisitorOrderCancelRequest|WcMaBeVisitorOrderCancelRequest|
|&emsp;&emsp;visitorBatch|预约单批次||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 07_获取预约记录详情


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/bevisitor/order/detail`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>查询被访记录详情接口。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "visitorBatch": "122228959455556"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaBeVisitorOrderDetailRequest|获取预约单详情请求参数|body|true|WcMaBeVisitorOrderDetailRequest|WcMaBeVisitorOrderDetailRequest|
|&emsp;&emsp;visitorBatch|预约单批次||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«WcMaVisitorOrderDetailResponse»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|WcMaVisitorOrderDetailResponse|WcMaVisitorOrderDetailResponse|
|&emsp;&emsp;approvalResult||string||
|&emsp;&emsp;authBarCode|二维码凭证(预约单:正常、迟到才有)|string||
|&emsp;&emsp;authIdentityPid|身份证序列号|string||
|&emsp;&emsp;authTempCard|访客卡号|string||
|&emsp;&emsp;authVisitorCode|访客验证码|string||
|&emsp;&emsp;backlogId||string||
|&emsp;&emsp;beVisitorEnterpriseName|员工所属单位|string||
|&emsp;&emsp;beVisitorGroupId|被访人部门ID|string||
|&emsp;&emsp;beVisitorGroupName|被访人部门名称|string||
|&emsp;&emsp;beVisitorOpenId|被访人openid|string||
|&emsp;&emsp;beVisitorPersonId|被访人ID|string||
|&emsp;&emsp;beVisitorPersonName|员工姓名|string||
|&emsp;&emsp;beVisitorPhoneNum|员工手机号|string||
|&emsp;&emsp;beVisitorUserId|被访人唯一标识(该字段必填)|string||
|&emsp;&emsp;buttonList|操作按钮集合|array|WcMaOperateButtonDto|
|&emsp;&emsp;&emsp;&emsp;buttonKey|按钮Key|string||
|&emsp;&emsp;&emsp;&emsp;buttonName|按钮名称|string||
|&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;createUserType|创建者身份类型：1-平台用户，2-内部人员，3-来访人员|integer(int32)||
|&emsp;&emsp;disorder|添加序号|integer(int32)||
|&emsp;&emsp;endTime|拜访时间:预计离开时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;endTimeDifference|预计离开时间时差|string||
|&emsp;&emsp;endTimeUTC|预计离开时间UTC|integer(int64)||
|&emsp;&emsp;leaderVisitor|预约人员|WcMaRetinueVisitorDto|WcMaRetinueVisitorDto|
|&emsp;&emsp;&emsp;&emsp;orderModel|预约模式 person:指定人员预约 space:场地预约|string||
|&emsp;&emsp;&emsp;&emsp;status|同行人状态|string||
|&emsp;&emsp;&emsp;&emsp;visitorAddress|访客住址|string||
|&emsp;&emsp;&emsp;&emsp;visitorBirthplace|籍贯|string||
|&emsp;&emsp;&emsp;&emsp;visitorCarNumber|车牌号|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustoma|自定义字段a|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomb|自定义字段b|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomc|自定义字段c|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomd|自定义字段d|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustome|自定义字段e|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomf|自定义字段f|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomg|自定义字段g|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomh|自定义字段h|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomi|自定义字段i|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomj|自定义字段j|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityAddr|证件地址|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityIssuer|发证机关|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityNum|证件号码|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityType|证件类型|integer||
|&emsp;&emsp;&emsp;&emsp;visitorName|访客姓名|string||
|&emsp;&emsp;&emsp;&emsp;visitorPhoneNum|手机号码|string||
|&emsp;&emsp;&emsp;&emsp;visitorPhoto|访客头像|string||
|&emsp;&emsp;&emsp;&emsp;visitorSex|性别：1、男；2、女|integer||
|&emsp;&emsp;&emsp;&emsp;visitorWorkUnit|访客所属单位|string||
|&emsp;&emsp;orderId|预约单编号|string||
|&emsp;&emsp;orderModel|预约模式 person:指定人员预约 space:场地预约|string||
|&emsp;&emsp;processId|审批规则id|string||
|&emsp;&emsp;processItemId|审批规则实例id|string||
|&emsp;&emsp;processRemark|退回原因|string||
|&emsp;&emsp;productId|产品编号|string||
|&emsp;&emsp;projectId|租户编号|string||
|&emsp;&emsp;realEndTime|签离时间|string||
|&emsp;&emsp;realEndTimeDifference|签离时间时差|string||
|&emsp;&emsp;realEndTimeUTC|签离时间UTC|integer(int64)||
|&emsp;&emsp;registerPlace|访客登记地点|string||
|&emsp;&emsp;registerTime|登记时间|string||
|&emsp;&emsp;registerTimeDifference|登记时间时差|string||
|&emsp;&emsp;registerTimeUTC|登记时间UTC|integer(int64)||
|&emsp;&emsp;retinueList|同行人列表|array|WcMaRetinueVisitorDto|
|&emsp;&emsp;&emsp;&emsp;orderModel|预约模式 person:指定人员预约 space:场地预约|string||
|&emsp;&emsp;&emsp;&emsp;status|同行人状态|string||
|&emsp;&emsp;&emsp;&emsp;visitorAddress|访客住址|string||
|&emsp;&emsp;&emsp;&emsp;visitorBirthplace|籍贯|string||
|&emsp;&emsp;&emsp;&emsp;visitorCarNumber|车牌号|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustoma|自定义字段a|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomb|自定义字段b|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomc|自定义字段c|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomd|自定义字段d|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustome|自定义字段e|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomf|自定义字段f|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomg|自定义字段g|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomh|自定义字段h|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomi|自定义字段i|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomj|自定义字段j|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityAddr|证件地址|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityIssuer|发证机关|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityNum|证件号码|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityType|证件类型|integer||
|&emsp;&emsp;&emsp;&emsp;visitorName|访客姓名|string||
|&emsp;&emsp;&emsp;&emsp;visitorPhoneNum|手机号码|string||
|&emsp;&emsp;&emsp;&emsp;visitorPhoto|访客头像|string||
|&emsp;&emsp;&emsp;&emsp;visitorSex|性别：1、男；2、女|integer||
|&emsp;&emsp;&emsp;&emsp;visitorWorkUnit|访客所属单位|string||
|&emsp;&emsp;startTime|拜访时间:预计来访时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;startTimeDifference|预计来访时间时差|string||
|&emsp;&emsp;startTimeUTC|预计来访时间UTC|integer(int64)||
|&emsp;&emsp;status|预约单状态|string||
|&emsp;&emsp;svrCodeIdentity|证件照对应图片服务器serviceNodes|string||
|&emsp;&emsp;svrCodeScanning|证件扫描照对应图片服务器serviceNodes|string||
|&emsp;&emsp;svrCodeVisitor|访客头像对应图片服务器serviceNodes|string||
|&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;visitBatch|访客批次|string||
|&emsp;&emsp;visitorAddress|访客住址|string||
|&emsp;&emsp;visitorAllowTimes|访客进入次数|integer(int32)||
|&emsp;&emsp;visitorBatch|预约单批次|string||
|&emsp;&emsp;visitorBirthplace|籍贯|string||
|&emsp;&emsp;visitorCarNumber|车牌号|string||
|&emsp;&emsp;visitorCustoma|自定义字段a：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomb|自定义字段b：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomc|自定义字段c：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomd|自定义字段d：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustome|自定义字段e：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomf|自定义字段f：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomg|自定义字段g：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomh|自定义字段h：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomi|自定义字段i：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomj|自定义字段j：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorGroupId|访客名单分组ID|string||
|&emsp;&emsp;visitorIdentityAddr|证件地址|string||
|&emsp;&emsp;visitorIdentityIssuer|发证机关|string||
|&emsp;&emsp;visitorIdentityNum|证件号码|string||
|&emsp;&emsp;visitorIdentityPhoto|证件照片|string||
|&emsp;&emsp;visitorIdentityType|证件类型：111、身份证|integer(int32)||
|&emsp;&emsp;visitorLeader|访客团体领队:0 同行人 1领队|string||
|&emsp;&emsp;visitorName|姓名|string||
|&emsp;&emsp;visitorOpenId|访客微信公众号唯一标识|string||
|&emsp;&emsp;visitorPersonNum|来访人数|integer(int32)||
|&emsp;&emsp;visitorPhoneNum|手机号|string||
|&emsp;&emsp;visitorPhoto|访客头像|string||
|&emsp;&emsp;visitorPhotoFlag|人脸质量合格标识。0：合格；1：不合格|string||
|&emsp;&emsp;visitorPinyin|访客名首字母缩写|string||
|&emsp;&emsp;visitorPrivilegeGroupIds|访客权限组ids|string||
|&emsp;&emsp;visitorPurpose|事由|string||
|&emsp;&emsp;visitorScanningPhoto|证件扫描照片|string||
|&emsp;&emsp;visitorSex|性别：1、男；2、女|integer(int32)||
|&emsp;&emsp;visitorTemperature|访客体温|string||
|&emsp;&emsp;visitorTemperatureStatus|访客体温状态|integer(int32)||
|&emsp;&emsp;visitorTypeId|访客类型id|string||
|&emsp;&emsp;visitorUserId||string||
|&emsp;&emsp;visitorWorkUnit|访客来访单位|string||
|&emsp;&emsp;webLabel|记录状态描述-web端|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"approvalResult": "",
		"authBarCode": "123",
		"authIdentityPid": "123",
		"authTempCard": "123",
		"authVisitorCode": "123",
		"backlogId": "",
		"beVisitorEnterpriseName": "海康威视",
		"beVisitorGroupId": "123",
		"beVisitorGroupName": "123",
		"beVisitorOpenId": "123",
		"beVisitorPersonId": "123",
		"beVisitorPersonName": "陈大鹏",
		"beVisitorPhoneNum": "123",
		"beVisitorUserId": "6546sdafs56adf",
		"buttonList": [
			{
				"buttonKey": "InvitationFoundByBeVisitor",
				"buttonName": "重新邀约"
			}
		],
		"createTime": "123",
		"createUserType": 123,
		"disorder": 123,
		"endTime": "2021-12-23 18:22:12",
		"endTimeDifference": "123",
		"endTimeUTC": 123,
		"leaderVisitor": {
			"orderModel": "person",
			"status": "已取消",
			"visitorAddress": "中南海",
			"visitorBirthplace": "安徽",
			"visitorCarNumber": "浙A12345",
			"visitorCustoma": "123232323",
			"visitorCustomb": "123232323",
			"visitorCustomc": "123232323",
			"visitorCustomd": "123232323",
			"visitorCustome": "123232323",
			"visitorCustomf": "123232323",
			"visitorCustomg": "123232323",
			"visitorCustomh": "123232323",
			"visitorCustomi": "123232323",
			"visitorCustomj": "123232323",
			"visitorIdentityAddr": "安徽芜湖",
			"visitorIdentityIssuer": "芜湖公安",
			"visitorIdentityNum": "123232323",
			"visitorIdentityType": 111,
			"visitorName": "陈绍鹏",
			"visitorPhoneNum": "18966175813",
			"visitorPhoto": "123",
			"visitorSex": 1,
			"visitorWorkUnit": "大碗娱乐无限责任公司"
		},
		"orderId": "122228959455556",
		"orderModel": "person",
		"processId": "123",
		"processItemId": "123",
		"processRemark": "122228959455556",
		"productId": "123",
		"projectId": "122228959455556",
		"realEndTime": "123",
		"realEndTimeDifference": "123",
		"realEndTimeUTC": 123,
		"registerPlace": "123",
		"registerTime": "123",
		"registerTimeDifference": "123",
		"registerTimeUTC": 123,
		"retinueList": [
			{
				"orderModel": "person",
				"status": "已取消",
				"visitorAddress": "中南海",
				"visitorBirthplace": "安徽",
				"visitorCarNumber": "浙A12345",
				"visitorCustoma": "123232323",
				"visitorCustomb": "123232323",
				"visitorCustomc": "123232323",
				"visitorCustomd": "123232323",
				"visitorCustome": "123232323",
				"visitorCustomf": "123232323",
				"visitorCustomg": "123232323",
				"visitorCustomh": "123232323",
				"visitorCustomi": "123232323",
				"visitorCustomj": "123232323",
				"visitorIdentityAddr": "安徽芜湖",
				"visitorIdentityIssuer": "芜湖公安",
				"visitorIdentityNum": "123232323",
				"visitorIdentityType": 111,
				"visitorName": "陈绍鹏",
				"visitorPhoneNum": "18966175813",
				"visitorPhoto": "123",
				"visitorSex": 1,
				"visitorWorkUnit": "大碗娱乐无限责任公司"
			}
		],
		"startTime": "2021-12-22 18:22:12",
		"startTimeDifference": "123",
		"startTimeUTC": 123,
		"status": "待审批",
		"svrCodeIdentity": "123",
		"svrCodeScanning": "123",
		"svrCodeVisitor": "123",
		"updateTime": "123",
		"visitBatch": "123",
		"visitorAddress": "123",
		"visitorAllowTimes": 123,
		"visitorBatch": "122228959455556",
		"visitorBirthplace": "123",
		"visitorCarNumber": "浙A12345",
		"visitorCustoma": "123",
		"visitorCustomb": "123",
		"visitorCustomc": "123",
		"visitorCustomd": "123",
		"visitorCustome": "123",
		"visitorCustomf": "123",
		"visitorCustomg": "123",
		"visitorCustomh": "123",
		"visitorCustomi": "123",
		"visitorCustomj": "123",
		"visitorGroupId": "123",
		"visitorIdentityAddr": "123",
		"visitorIdentityIssuer": "123",
		"visitorIdentityNum": "123",
		"visitorIdentityPhoto": "123",
		"visitorIdentityType": 123,
		"visitorLeader": "0",
		"visitorName": "123",
		"visitorOpenId": "123",
		"visitorPersonNum": 123,
		"visitorPhoneNum": "123",
		"visitorPhoto": "123",
		"visitorPhotoFlag": "123",
		"visitorPinyin": "123",
		"visitorPrivilegeGroupIds": "123",
		"visitorPurpose": "参观",
		"visitorScanningPhoto": "123",
		"visitorSex": 123,
		"visitorTemperature": "123",
		"visitorTemperatureStatus": 123,
		"visitorTypeId": "123",
		"visitorUserId": "",
		"visitorWorkUnit": "123",
		"webLabel": "123"
	},
	"msg": "success"
}
```


## 01_获取待审批记录


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/bevisitor/order/examine/log/doing`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>获取待审批的记录,根据被访者openid和审批:员工待审批过滤数据，按来访时间顺序。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "pageNo": 1,
  "pageSize": 20
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaBeVisitorExamineIngRequest|员工待审核请求参数|body|true|WcMaBeVisitorExamineIngRequest|WcMaBeVisitorExamineIngRequest|
|&emsp;&emsp;pageNo|页码（pageNo>0）||true|integer(int32)||
|&emsp;&emsp;pageSize|页大小（0<pageSize<=1000）||true|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PageResult«WcMaBeVisitorOrderCardDto»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PageResult«WcMaBeVisitorOrderCardDto»|PageResult«WcMaBeVisitorOrderCardDto»|
|&emsp;&emsp;list|数据信息|array|WcMaBeVisitorOrderCardDto|
|&emsp;&emsp;&emsp;&emsp;backLogId||string||
|&emsp;&emsp;&emsp;&emsp;buttonList|操作按钮集合|array|WcMaOperateButtonDto|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;buttonKey|按钮Key|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;buttonName|按钮名称|string||
|&emsp;&emsp;&emsp;&emsp;endTime|预计离开时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;&emsp;&emsp;projectId|projectId|string||
|&emsp;&emsp;&emsp;&emsp;startTime|预计来访时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;&emsp;&emsp;status|预约单状态|string||
|&emsp;&emsp;&emsp;&emsp;visitorBatch|预约单批次|string||
|&emsp;&emsp;&emsp;&emsp;visitorName|访客姓名|string||
|&emsp;&emsp;&emsp;&emsp;visitorPurpose|事由|string||
|&emsp;&emsp;&emsp;&emsp;visitorWorkUnit|访客所属单位|string||
|&emsp;&emsp;pageNo|页码|integer(int32)||
|&emsp;&emsp;pageSize|页大小|integer(int32)||
|&emsp;&emsp;total|总条数|integer(int64)||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"list": [
			{
				"backLogId": "",
				"buttonList": [
					{
						"buttonKey": "InvitationFoundByBeVisitor",
						"buttonName": "重新邀约"
					}
				],
				"endTime": "2021-12-23 18:22:12",
				"projectId": "cccdddd",
				"startTime": "2021-12-22 18:22:12",
				"status": "待审批",
				"visitorBatch": "122228959455556",
				"visitorName": "陈绍鹏",
				"visitorPurpose": "参观",
				"visitorWorkUnit": "大碗娱乐无限责任公司"
			}
		],
		"pageNo": 1,
		"pageSize": 20,
		"total": 5
	},
	"msg": "success"
}
```


## 02_获取审批逾期记录


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/bevisitor/order/examine/log/expires`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>获取审批逾期,根据被访者openid和审批:逾期 或待审批并且离开时间小于当前时间 批过滤数据，按离开时间倒序。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "pageNo": 1,
  "pageSize": 20,
  "visitorName": "陈绍鹏"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaBeVisitorExamineExpireRequest|员工审核逾期请求参数|body|true|WcMaBeVisitorExamineExpireRequest|WcMaBeVisitorExamineExpireRequest|
|&emsp;&emsp;pageNo|页码（pageNo>0）||true|integer(int32)||
|&emsp;&emsp;pageSize|页大小（0<pageSize<=1000）||true|integer(int32)||
|&emsp;&emsp;visitorName|拜访人姓名||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PageResult«WcMaBeVisitorOrderCardDto»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PageResult«WcMaBeVisitorOrderCardDto»|PageResult«WcMaBeVisitorOrderCardDto»|
|&emsp;&emsp;list|数据信息|array|WcMaBeVisitorOrderCardDto|
|&emsp;&emsp;&emsp;&emsp;backLogId||string||
|&emsp;&emsp;&emsp;&emsp;buttonList|操作按钮集合|array|WcMaOperateButtonDto|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;buttonKey|按钮Key|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;buttonName|按钮名称|string||
|&emsp;&emsp;&emsp;&emsp;endTime|预计离开时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;&emsp;&emsp;projectId|projectId|string||
|&emsp;&emsp;&emsp;&emsp;startTime|预计来访时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;&emsp;&emsp;status|预约单状态|string||
|&emsp;&emsp;&emsp;&emsp;visitorBatch|预约单批次|string||
|&emsp;&emsp;&emsp;&emsp;visitorName|访客姓名|string||
|&emsp;&emsp;&emsp;&emsp;visitorPurpose|事由|string||
|&emsp;&emsp;&emsp;&emsp;visitorWorkUnit|访客所属单位|string||
|&emsp;&emsp;pageNo|页码|integer(int32)||
|&emsp;&emsp;pageSize|页大小|integer(int32)||
|&emsp;&emsp;total|总条数|integer(int64)||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"list": [
			{
				"backLogId": "",
				"buttonList": [
					{
						"buttonKey": "InvitationFoundByBeVisitor",
						"buttonName": "重新邀约"
					}
				],
				"endTime": "2021-12-23 18:22:12",
				"projectId": "cccdddd",
				"startTime": "2021-12-22 18:22:12",
				"status": "待审批",
				"visitorBatch": "122228959455556",
				"visitorName": "陈绍鹏",
				"visitorPurpose": "参观",
				"visitorWorkUnit": "大碗娱乐无限责任公司"
			}
		],
		"pageNo": 1,
		"pageSize": 20,
		"total": 5
	},
	"msg": "success"
}
```


## 13_员工取消邀约


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/bevisitor/order/invitation/cancel`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.员工点击邀约中状态的信息，可以取消邀约
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "visitorBatch": "122228959455556"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaInvitationCancelRequest|员工取消邀约请求参数|body|true|WcMaInvitationCancelRequest|WcMaInvitationCancelRequest|
|&emsp;&emsp;visitorBatch|预约单批次||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 12_员工发起邀约


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/bevisitor/order/invitation/founding`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.员工发起邀约请求
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "endTime": "2021-12-23 18:22",
  "startTime": "2021-12-22 18:22",
  "visitorName": "小红",
  "visitorPhoneNum": "123",
  "visitorPrivilegeGroupIds": "123,1231",
  "visitorPurpose": "参观",
  "visitorTypeId": "1"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaInvitationStartRequest|员工发起邀约请求参数|body|true|WcMaInvitationStartRequest|WcMaInvitationStartRequest|
|&emsp;&emsp;endTime|预计离开时间(yyyy-MM-dd HH:mm)||true|string||
|&emsp;&emsp;startTime|预计来访时间(yyyy-MM-dd HH:mm)||true|string||
|&emsp;&emsp;visitorName|访客姓名||true|string||
|&emsp;&emsp;visitorPhoneNum|访客手机号码||true|string||
|&emsp;&emsp;visitorPrivilegeGroupIds|访客拜访区域编号集合||true|string||
|&emsp;&emsp;visitorPurpose|邀请事由||true|string||
|&emsp;&emsp;visitorTypeId|访客类型||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«WcMaInvitationStartResponse»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|WcMaInvitationStartResponse|WcMaInvitationStartResponse|
|&emsp;&emsp;visitorBatch|预约单批次|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"visitorBatch": "122228959455556"
	},
	"msg": "success"
}
```


## 03_获取待受访记录


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/bevisitor/order/reception/log/doing`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>获取待受访,根据被访者openid和预约单:正常和迟到、访客已登记 过滤数据，按来访时间顺序。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "pageNo": 1,
  "pageSize": 20
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaBeVisitorReceptionIngRequest|员工待受访请求参数|body|true|WcMaBeVisitorReceptionIngRequest|WcMaBeVisitorReceptionIngRequest|
|&emsp;&emsp;pageNo|页码（pageNo>0）||true|integer(int32)||
|&emsp;&emsp;pageSize|页大小（0<pageSize<=1000）||true|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PageResult«WcMaBeVisitorOrderCardDto»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PageResult«WcMaBeVisitorOrderCardDto»|PageResult«WcMaBeVisitorOrderCardDto»|
|&emsp;&emsp;list|数据信息|array|WcMaBeVisitorOrderCardDto|
|&emsp;&emsp;&emsp;&emsp;backLogId||string||
|&emsp;&emsp;&emsp;&emsp;buttonList|操作按钮集合|array|WcMaOperateButtonDto|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;buttonKey|按钮Key|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;buttonName|按钮名称|string||
|&emsp;&emsp;&emsp;&emsp;endTime|预计离开时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;&emsp;&emsp;projectId|projectId|string||
|&emsp;&emsp;&emsp;&emsp;startTime|预计来访时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;&emsp;&emsp;status|预约单状态|string||
|&emsp;&emsp;&emsp;&emsp;visitorBatch|预约单批次|string||
|&emsp;&emsp;&emsp;&emsp;visitorName|访客姓名|string||
|&emsp;&emsp;&emsp;&emsp;visitorPurpose|事由|string||
|&emsp;&emsp;&emsp;&emsp;visitorWorkUnit|访客所属单位|string||
|&emsp;&emsp;pageNo|页码|integer(int32)||
|&emsp;&emsp;pageSize|页大小|integer(int32)||
|&emsp;&emsp;total|总条数|integer(int64)||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"list": [
			{
				"backLogId": "",
				"buttonList": [
					{
						"buttonKey": "InvitationFoundByBeVisitor",
						"buttonName": "重新邀约"
					}
				],
				"endTime": "2021-12-23 18:22:12",
				"projectId": "cccdddd",
				"startTime": "2021-12-22 18:22:12",
				"status": "待审批",
				"visitorBatch": "122228959455556",
				"visitorName": "陈绍鹏",
				"visitorPurpose": "参观",
				"visitorWorkUnit": "大碗娱乐无限责任公司"
			}
		],
		"pageNo": 1,
		"pageSize": 20,
		"total": 5
	},
	"msg": "success"
}
```


## 04_获取受访历史记录


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/bevisitor/order/reception/log/history`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>获取受访历史记录,根据被访者openid和预约单:超期自动签离(系统)、访客签离和超期未签离(系统) 过滤数据，按离开时间倒序。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "pageNo": 1,
  "pageSize": 20,
  "visitorName": "陈绍鹏"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaBeVisitorReceptionHistoryRequest|员工受访历史记录请求参数|body|true|WcMaBeVisitorReceptionHistoryRequest|WcMaBeVisitorReceptionHistoryRequest|
|&emsp;&emsp;pageNo|页码（pageNo>0）||true|integer(int32)||
|&emsp;&emsp;pageSize|页大小（0<pageSize<=1000）||true|integer(int32)||
|&emsp;&emsp;visitorName|访客姓名||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PageResult«WcMaBeVisitorOrderCardDto»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PageResult«WcMaBeVisitorOrderCardDto»|PageResult«WcMaBeVisitorOrderCardDto»|
|&emsp;&emsp;list|数据信息|array|WcMaBeVisitorOrderCardDto|
|&emsp;&emsp;&emsp;&emsp;backLogId||string||
|&emsp;&emsp;&emsp;&emsp;buttonList|操作按钮集合|array|WcMaOperateButtonDto|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;buttonKey|按钮Key|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;buttonName|按钮名称|string||
|&emsp;&emsp;&emsp;&emsp;endTime|预计离开时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;&emsp;&emsp;projectId|projectId|string||
|&emsp;&emsp;&emsp;&emsp;startTime|预计来访时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;&emsp;&emsp;status|预约单状态|string||
|&emsp;&emsp;&emsp;&emsp;visitorBatch|预约单批次|string||
|&emsp;&emsp;&emsp;&emsp;visitorName|访客姓名|string||
|&emsp;&emsp;&emsp;&emsp;visitorPurpose|事由|string||
|&emsp;&emsp;&emsp;&emsp;visitorWorkUnit|访客所属单位|string||
|&emsp;&emsp;pageNo|页码|integer(int32)||
|&emsp;&emsp;pageSize|页大小|integer(int32)||
|&emsp;&emsp;total|总条数|integer(int64)||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"list": [
			{
				"backLogId": "",
				"buttonList": [
					{
						"buttonKey": "InvitationFoundByBeVisitor",
						"buttonName": "重新邀约"
					}
				],
				"endTime": "2021-12-23 18:22:12",
				"projectId": "cccdddd",
				"startTime": "2021-12-22 18:22:12",
				"status": "待审批",
				"visitorBatch": "122228959455556",
				"visitorName": "陈绍鹏",
				"visitorPurpose": "参观",
				"visitorWorkUnit": "大碗娱乐无限责任公司"
			}
		],
		"pageNo": 1,
		"pageSize": 20,
		"total": 5
	},
	"msg": "success"
}
```


## 14_获取邀约分享记录


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/bevisitor/order/share/log`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>获取邀约分享记录 包含邀约中和已失效。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "invitationState": "inviting",
  "pageNo": 1,
  "pageSize": 20
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaGetOrderShareRequest|WcMaGetOrderShareRequest|body|true|WcMaGetOrderShareRequest|WcMaGetOrderShareRequest|
|&emsp;&emsp;invitationState|邀约记录状态 邀约中：inviting；到期失效：expire||true|string||
|&emsp;&emsp;pageNo|页码（pageNo>0）||true|integer(int32)||
|&emsp;&emsp;pageSize|页大小（0<pageSize<=1000）||true|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PageResult«WcMaOrderShareResponse»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PageResult«WcMaOrderShareResponse»|PageResult«WcMaOrderShareResponse»|
|&emsp;&emsp;list|数据信息|array|WcMaOrderShareResponse|
|&emsp;&emsp;&emsp;&emsp;endTime|拜访时间:预计离开时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;&emsp;&emsp;mode|分享渠道：短信sms 微信wechat|string||
|&emsp;&emsp;&emsp;&emsp;shareStatus|链接状态 0废弃 1正常|string||
|&emsp;&emsp;&emsp;&emsp;startTime|拜访时间:预计来访时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;&emsp;&emsp;visitorBatch|预约单批次|string||
|&emsp;&emsp;&emsp;&emsp;visitorDtos|已应邀访客信息列表|array|ShareVisitorResponse|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;orderId|value|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;status|访客单状态(状态”待来访“时。才能有取消操作)|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;visitBatch|访客批次|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;visitorCarNumber|车牌号|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;visitorName|访客姓名|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;visitorPhoneNum|手机号码|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;visitorSex|性别：1、男；2、女|integer||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;visitorWorkUnit|访客所属单位|string||
|&emsp;&emsp;&emsp;&emsp;visitorPurpose|来访事由|string||
|&emsp;&emsp;&emsp;&emsp;visitorSmsSendFlag|短信发送状态 0异常 1正常(异常状态才能再发短信)|string||
|&emsp;&emsp;pageNo|页码|integer(int32)||
|&emsp;&emsp;pageSize|页大小|integer(int32)||
|&emsp;&emsp;total|总条数|integer(int64)||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"list": [
			{
				"endTime": "2021-12-23 18:22:12",
				"mode": "122228959455556",
				"shareStatus": "1",
				"startTime": "2021-12-22 18:22:12",
				"visitorBatch": "122228959455556",
				"visitorDtos": [
					{
						"orderId": "1111111",
						"status": "已取消",
						"visitBatch": "1111111",
						"visitorCarNumber": "浙A12345",
						"visitorName": "陈绍鹏",
						"visitorPhoneNum": "18966175813",
						"visitorSex": 1,
						"visitorWorkUnit": "大碗娱乐无限责任公司"
					}
				],
				"visitorPurpose": "122228959455556",
				"visitorSmsSendFlag": "1"
			}
		],
		"pageNo": 1,
		"pageSize": 20,
		"total": 5
	},
	"msg": "success"
}
```


## 15_停止邀约和开启邀约


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/miniapp/bevisitor/order/share/update`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>停止邀约和开启邀约。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "shareStatus": "122228959455556",
  "visitorBatch": "122228959455556"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaOrderShareRequest|WcMaOrderShareRequest|body|true|WcMaOrderShareRequest|WcMaOrderShareRequest|
|&emsp;&emsp;shareStatus|链接状态 0废弃 1正常||false|string||
|&emsp;&emsp;visitorBatch|预约单批次||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


# 14_对外接口


## 01_同步访客入园须知信息


**接口地址**:`/webapi/visitorcs/api/v1/config/park/notice/sync`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>同步同步访客入园须知信息。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "docking": "12221122",
  "parkNotice": "12221122",
  "parkStatus": "0",
  "parkTitle": "12221122",
  "productId": "12221122",
  "projectId": "12221122"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|projectId|项目编号|header|true|string||
|parkNoticeConfigSetRequest|入园须知请求参数|body|true|ParkNoticeConfigSetRequest|ParkNoticeConfigSetRequest|
|&emsp;&emsp;docking|数据来源||true|string||
|&emsp;&emsp;parkNotice|入园须知内容||false|string||
|&emsp;&emsp;parkStatus|入园须知状态0未配置1配置||true|string||
|&emsp;&emsp;parkTitle|入园须知标题||false|string||
|&emsp;&emsp;productId|产品编号(<=32)||true|string||
|&emsp;&emsp;projectId|项目编号(<=32)||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created|ActionErrorResult|
|204|No Content|ActionErrorResult|
|401|Unauthorized|ActionErrorResult|
|403|Forbidden|ActionErrorResult|
|404|Not Found|ActionErrorResult|


**响应状态码-200**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


**响应状态码-201**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-204**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-401**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-403**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-404**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


## 02_同步访客预约状态


**接口地址**:`/webapi/visitorcs/api/v1/order/status/sync`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>同步访客预约状态。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
[
  {
    "orderId": "123",
    "status": 3
  }
]
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|projectId|项目编号|header|true|string||
|orderStatusDtos|访客预约状态同步对象|body|true|array|OrderStatusDto|
|&emsp;&emsp;orderId|预约单id||false|string||
|&emsp;&emsp;status|预约状态||false|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created|ActionErrorResult|
|204|No Content|ActionErrorResult|
|401|Unauthorized|ActionErrorResult|
|403|Forbidden|ActionErrorResult|
|404|Not Found|ActionErrorResult|


**响应状态码-200**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


**响应状态码-201**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-204**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-401**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-403**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-404**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


## 01_分页同步访客预约信息


**接口地址**:`/webapi/visitorcs/api/v1/order/sync`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>根据查询条件，分页查询访客预约数据。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "disorder": 123,
  "pageNo": "3",
  "pageSize": "50"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|projectId|项目编号|header|true|string||
|orderDto|访客预约同步信息对象|body|true|OrderDto|OrderDto|
|&emsp;&emsp;disorder|更新顺序||false|integer(int32)||
|&emsp;&emsp;pageNo|查询时第几页||true|object||
|&emsp;&emsp;pageSize|查询时单页条数,限定大小不能超过1000||true|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PageResult«OrderResponse»»|
|201|Created|ActionErrorResult|
|204|No Content|ActionErrorResult|
|401|Unauthorized|ActionErrorResult|
|403|Forbidden|ActionErrorResult|
|404|Not Found|ActionErrorResult|


**响应状态码-200**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PageResult«OrderResponse»|PageResult«OrderResponse»|
|&emsp;&emsp;list|数据信息|array|OrderResponse|
|&emsp;&emsp;&emsp;&emsp;approvalResult||string||
|&emsp;&emsp;&emsp;&emsp;authBarCode|访客二维码|string||
|&emsp;&emsp;&emsp;&emsp;authIdentityPid|身份证序列号|string||
|&emsp;&emsp;&emsp;&emsp;authTempCard|访客卡号|string||
|&emsp;&emsp;&emsp;&emsp;authVisitorCode|访客验证码|string||
|&emsp;&emsp;&emsp;&emsp;backlogId||string||
|&emsp;&emsp;&emsp;&emsp;beVisitorGroupId|被访人部门ID|string||
|&emsp;&emsp;&emsp;&emsp;beVisitorGroupName|被访人部门名称|string||
|&emsp;&emsp;&emsp;&emsp;beVisitorOpenId|被访人openid|string||
|&emsp;&emsp;&emsp;&emsp;beVisitorPersonId|被访人ID|string||
|&emsp;&emsp;&emsp;&emsp;beVisitorPersonName|被访人名称|string||
|&emsp;&emsp;&emsp;&emsp;beVisitorPhoneNum|被访人手机号|string||
|&emsp;&emsp;&emsp;&emsp;beVisitorUserId||string||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;createUserType|创建者身份类型：1-平台用户，2-内部人员，3-来访人员|integer||
|&emsp;&emsp;&emsp;&emsp;disorder|添加序号|integer||
|&emsp;&emsp;&emsp;&emsp;endTime|预计离开时间|string||
|&emsp;&emsp;&emsp;&emsp;endTimeDifference|预计离开时间时差|string||
|&emsp;&emsp;&emsp;&emsp;endTimeUTC|预计离开时间UTC|integer||
|&emsp;&emsp;&emsp;&emsp;orderId|预约单号|string||
|&emsp;&emsp;&emsp;&emsp;orderModel|预约模式 person:指定人员预约 space:场地预约|string||
|&emsp;&emsp;&emsp;&emsp;processId|审批规则id|string||
|&emsp;&emsp;&emsp;&emsp;processItemId|审批规则实例id|string||
|&emsp;&emsp;&emsp;&emsp;processRemark|备注|string||
|&emsp;&emsp;&emsp;&emsp;productId|产品编号|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目编号|string||
|&emsp;&emsp;&emsp;&emsp;realEndTime|签离时间|string||
|&emsp;&emsp;&emsp;&emsp;realEndTimeDifference|签离时间时差|string||
|&emsp;&emsp;&emsp;&emsp;realEndTimeUTC|签离时间UTC|integer||
|&emsp;&emsp;&emsp;&emsp;registerPlace|访客登记地点|string||
|&emsp;&emsp;&emsp;&emsp;registerTime|登记时间|string||
|&emsp;&emsp;&emsp;&emsp;registerTimeDifference|登记时间时差|string||
|&emsp;&emsp;&emsp;&emsp;registerTimeUTC|登记时间UTC|integer||
|&emsp;&emsp;&emsp;&emsp;startTime|预计来访时间|string||
|&emsp;&emsp;&emsp;&emsp;startTimeDifference|预计来访时间时差|string||
|&emsp;&emsp;&emsp;&emsp;startTimeUTC|预计来访时间UTC|integer||
|&emsp;&emsp;&emsp;&emsp;status|记录状态。0：待审批；1：正常；2：迟到；3：预约逾期；4：审批退回；5：超期自动签离；6：访客签离；7：超期未签离；8：已到达；9：审批逾期；10：邀约中；11：邀约逾期；12：邀约失效(员工取消)；13：邀约失效(访客取消)；14：预约失效(员工取消)；15：预约失效(访客取消)|integer||
|&emsp;&emsp;&emsp;&emsp;svrCodeIdentity|证件照对应图片服务器serviceNodes|string||
|&emsp;&emsp;&emsp;&emsp;svrCodeScanning|证件扫描照对应图片服务器serviceNodes|string||
|&emsp;&emsp;&emsp;&emsp;svrCodeVisitor|访客头像对应图片服务器serviceNodes|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;&emsp;&emsp;visitBatch|访客批次|string||
|&emsp;&emsp;&emsp;&emsp;visitorAddress|访客住址|string||
|&emsp;&emsp;&emsp;&emsp;visitorAllowTimes|访客进入次数|integer||
|&emsp;&emsp;&emsp;&emsp;visitorBirthplace|籍贯|string||
|&emsp;&emsp;&emsp;&emsp;visitorCarNumber|车牌号|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustoma|自定义字段a：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomb|自定义字段b：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomc|自定义字段c：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomd|自定义字段d：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustome|自定义字段e：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomf|自定义字段f：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomg|自定义字段g：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomh|自定义字段h：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomi|自定义字段i：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomj|自定义字段j：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorGroupId|访客名单分组ID|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityAddr|证件地址|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityIssuer|发证机关|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityNum|证件号码|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityPhoto|证件照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityType|证件类型：111、身份证|integer||
|&emsp;&emsp;&emsp;&emsp;visitorName|姓名|string||
|&emsp;&emsp;&emsp;&emsp;visitorOpenId|访客微信公众号唯一标识|string||
|&emsp;&emsp;&emsp;&emsp;visitorPersonNum|来访人数|integer||
|&emsp;&emsp;&emsp;&emsp;visitorPhoneNum|手机号|string||
|&emsp;&emsp;&emsp;&emsp;visitorPhoto|访客头像|string||
|&emsp;&emsp;&emsp;&emsp;visitorPhotoFlag|人脸质量合格标识。0：合格；1：不合格|string||
|&emsp;&emsp;&emsp;&emsp;visitorPinyin|访客名首字母缩写|string||
|&emsp;&emsp;&emsp;&emsp;visitorPrivilegeGroupIds|访客权限组ids|string||
|&emsp;&emsp;&emsp;&emsp;visitorPurpose|来访事由|string||
|&emsp;&emsp;&emsp;&emsp;visitorScanningPhoto|证件扫描照片|string||
|&emsp;&emsp;&emsp;&emsp;visitorSex|性别：1、男；2、女|integer||
|&emsp;&emsp;&emsp;&emsp;visitorTemperature|访客体温|string||
|&emsp;&emsp;&emsp;&emsp;visitorTemperatureStatus|访客体温状态|integer||
|&emsp;&emsp;&emsp;&emsp;visitorTypeId|访客类型id|string||
|&emsp;&emsp;&emsp;&emsp;visitorUserId||string||
|&emsp;&emsp;&emsp;&emsp;visitorWorkUnit|访客来访单位|string||
|&emsp;&emsp;&emsp;&emsp;webLabel|记录状态描述-web端|string||
|&emsp;&emsp;pageNo|页码|integer(int32)||
|&emsp;&emsp;pageSize|页大小|integer(int32)||
|&emsp;&emsp;total|总条数|integer(int64)||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"list": [
			{
				"approvalResult": "",
				"authBarCode": "123",
				"authIdentityPid": "123",
				"authTempCard": "123",
				"authVisitorCode": "123",
				"backlogId": "",
				"beVisitorGroupId": "123",
				"beVisitorGroupName": "123",
				"beVisitorOpenId": "123",
				"beVisitorPersonId": "123",
				"beVisitorPersonName": "123",
				"beVisitorPhoneNum": "123",
				"beVisitorUserId": "",
				"createTime": "123",
				"createUserType": 123,
				"disorder": 123,
				"endTime": "123",
				"endTimeDifference": "123",
				"endTimeUTC": 123,
				"orderId": "123",
				"orderModel": "person",
				"processId": "123",
				"processItemId": "123",
				"processRemark": "123",
				"productId": "123",
				"projectId": "123",
				"realEndTime": "123",
				"realEndTimeDifference": "123",
				"realEndTimeUTC": 123,
				"registerPlace": "123",
				"registerTime": "123",
				"registerTimeDifference": "123",
				"registerTimeUTC": 123,
				"startTime": "123",
				"startTimeDifference": "123",
				"startTimeUTC": 123,
				"status": 123,
				"svrCodeIdentity": "123",
				"svrCodeScanning": "123",
				"svrCodeVisitor": "123",
				"updateTime": "123",
				"visitBatch": "123",
				"visitorAddress": "123",
				"visitorAllowTimes": 123,
				"visitorBirthplace": "123",
				"visitorCarNumber": "123",
				"visitorCustoma": "123",
				"visitorCustomb": "123",
				"visitorCustomc": "123",
				"visitorCustomd": "123",
				"visitorCustome": "123",
				"visitorCustomf": "123",
				"visitorCustomg": "123",
				"visitorCustomh": "123",
				"visitorCustomi": "123",
				"visitorCustomj": "123",
				"visitorGroupId": "123",
				"visitorIdentityAddr": "123",
				"visitorIdentityIssuer": "123",
				"visitorIdentityNum": "123",
				"visitorIdentityPhoto": "123",
				"visitorIdentityType": 123,
				"visitorName": "123",
				"visitorOpenId": "123",
				"visitorPersonNum": 123,
				"visitorPhoneNum": "123",
				"visitorPhoto": "123",
				"visitorPhotoFlag": "123",
				"visitorPinyin": "123",
				"visitorPrivilegeGroupIds": "123",
				"visitorPurpose": "123",
				"visitorScanningPhoto": "123",
				"visitorSex": 123,
				"visitorTemperature": "123",
				"visitorTemperatureStatus": 123,
				"visitorTypeId": "123",
				"visitorUserId": "",
				"visitorWorkUnit": "123",
				"webLabel": "123"
			}
		],
		"pageNo": 1,
		"pageSize": 20,
		"total": 5
	},
	"msg": "success"
}
```


**响应状态码-201**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-204**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-401**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-403**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-404**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


## 01_ISC人员同步


**接口地址**:`/webapi/visitorcs/api/v1/person/syncPersonInfos`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>ISC人员同步。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
[
  {
    "cardNo": "",
    "orgName": "",
    "personIndexCode": "",
    "personName": "",
    "personStatus": 0,
    "phone": "",
    "sex": 0
  }
]
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|iscPersonDtos|IscPersonDto|body|true|array|IscPersonDto|
|&emsp;&emsp;cardNo|||false|string||
|&emsp;&emsp;orgName|||false|string||
|&emsp;&emsp;personIndexCode|||false|string||
|&emsp;&emsp;personName|||false|string||
|&emsp;&emsp;personStatus|||false|integer(int32)||
|&emsp;&emsp;phone|||false|string||
|&emsp;&emsp;sex|||false|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«List«string»»|
|201|Created|ActionErrorResult|
|204|No Content|ActionErrorResult|
|401|Unauthorized|ActionErrorResult|
|403|Forbidden|ActionErrorResult|
|404|Not Found|ActionErrorResult|


**响应状态码-200**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|array||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": [],
	"msg": "success"
}
```


**响应状态码-201**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-204**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-401**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-403**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-404**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


## 01_同步访客权限组信息


**接口地址**:`/webapi/visitorcs/api/v1/privilege/sync`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>同步三方访客权限组数据。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
[
  {
    "createTime": "2021-07-01 12:00:00",
    "disorder": 123,
    "groupId": "ccc",
    "groupName": "园区北门",
    "isDefault": "0",
    "productId": "bbb",
    "projectId": "aaa",
    "remark": "拜访",
    "status": 0
  }
]
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|projectId|项目编号|header|true|string||
|privilegeInfoDtos|访客权限组同步对象|body|true|array|PrivilegeInfoDto|
|&emsp;&emsp;createTime|创建时间||false|string||
|&emsp;&emsp;disorder|更新序号||false|integer(int32)||
|&emsp;&emsp;groupId|权限组ID||false|string||
|&emsp;&emsp;groupName|权限组名称||false|string||
|&emsp;&emsp;isDefault|是否默认权限组||false|string||
|&emsp;&emsp;productId|产品编号||false|string||
|&emsp;&emsp;projectId|项目编号||false|string||
|&emsp;&emsp;remark|备注说明||false|string||
|&emsp;&emsp;status|状态：0正常 -1已删除||false|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created|ActionErrorResult|
|204|No Content|ActionErrorResult|
|401|Unauthorized|ActionErrorResult|
|403|Forbidden|ActionErrorResult|
|404|Not Found|ActionErrorResult|


**响应状态码-200**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


**响应状态码-201**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-204**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-401**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-403**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-404**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


## 01_同步访客信息字段来访事由及访客类型


**接口地址**:`/webapi/visitorcs/api/v1/field/sync`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>同步三方访客信息字段来访事由及访客类型。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
[
  {
    "createTime": "2021-07-01 12:00:00",
    "customOption": "123",
    "dataValue": "123",
    "defaultValue": "其他",
    "disorder": 1,
    "display": "1",
    "fieldProperties": "0",
    "fieldType": "1",
    "hint": "123",
    "maxLength": 11,
    "overseas": "1",
    "paraId": "ccc",
    "paraKey": "123",
    "paraName": "aaa",
    "placeholder": "123",
    "productId": "bbb",
    "projectId": "aaa",
    "readOnly": "1",
    "regular": "123",
    "required": "1",
    "showType": "1",
    "status": 0,
    "tips": "输入车牌号码信息可作为您去拜访时的停车凭证",
    "updateTime": "2021-07-11 12:00:00"
  }
]
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|projectId|项目编号|header|true|string||
|fieldInfoDtos|访客信息字段对象|body|true|array|FieldInfoDto|
|&emsp;&emsp;createTime|创建时间||false|string||
|&emsp;&emsp;customOption|自定义选择框的枚举值||false|object||
|&emsp;&emsp;dataValue|关联的枚举值||false|string||
|&emsp;&emsp;defaultValue|默认字段||false|string||
|&emsp;&emsp;disorder|更新顺序||false|integer(int32)||
|&emsp;&emsp;display|是否可见，0表示可见，1表示不可见||false|string||
|&emsp;&emsp;fieldProperties|字段属性：0：访客信息字段，1：被访人信息字段||false|string||
|&emsp;&emsp;fieldType|参数类型||false|string||
|&emsp;&emsp;hint|表单项的提示信息||false|string||
|&emsp;&emsp;maxLength|最大字段长度||false|integer(int32)||
|&emsp;&emsp;overseas|是否支持海外||false|string||
|&emsp;&emsp;paraId|paraId||false|string||
|&emsp;&emsp;paraKey|表单项名称key||false|string||
|&emsp;&emsp;paraName|表单项名称||false|string||
|&emsp;&emsp;placeholder|表单项的placeholder，vue-i18n多语言的key，比如人员民族中的请选择提示||false|string||
|&emsp;&emsp;productId|产品编号||false|string||
|&emsp;&emsp;projectId|项目编号||false|string||
|&emsp;&emsp;readOnly|是否可修改，0表示不可修改,1表示可修改||false|string||
|&emsp;&emsp;regular|表单的正则表达式||false|string||
|&emsp;&emsp;required|是否必填，0表示必填，1表示非必填||false|string||
|&emsp;&emsp;showType|表单项类型。1：input；2：select；3：data-picker；6：pic||false|string||
|&emsp;&emsp;status|访客字段状态：0正常 -1已删除||false|integer(int32)||
|&emsp;&emsp;tips|提示信息||false|string||
|&emsp;&emsp;updateTime|更新时间||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created|ActionErrorResult|
|204|No Content|ActionErrorResult|
|401|Unauthorized|ActionErrorResult|
|403|Forbidden|ActionErrorResult|
|404|Not Found|ActionErrorResult|


**响应状态码-200**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


**响应状态码-201**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-204**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-401**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-403**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-404**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


# 15_企微应用_员工端


## 4_接受邀约


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/wecom/bevisitor/invitation/accepting`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.访客点击邀约请求，接受邀约
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "faceId": "12221122",
  "openId": "12221122",
  "orderId": "6546sdafs56adf",
  "visitorAddress": "中南海",
  "visitorBirthplace": "安徽",
  "visitorCarNumber": "浙A12321",
  "visitorCustoma": "123232323",
  "visitorCustomb": "123232323",
  "visitorCustomc": "123232323",
  "visitorCustomd": "123232323",
  "visitorCustome": "123232323",
  "visitorCustomf": "123232323",
  "visitorCustomg": "123232323",
  "visitorCustomh": "123232323",
  "visitorCustomi": "123232323",
  "visitorCustomj": "123232323",
  "visitorIdentityAddr": "安徽芜湖",
  "visitorIdentityIssuer": "芜湖公安",
  "visitorIdentityNum": "123232323",
  "visitorIdentityType": 111,
  "visitorName": "小红",
  "visitorPersonNum": 10,
  "visitorWorkUnit": "海康"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|weComInvitationAcceptRequest|访客接受邀约请求参数|body|true|WeComInvitationAcceptRequest|WeComInvitationAcceptRequest|
|&emsp;&emsp;faceId|人脸的id||false|string||
|&emsp;&emsp;openId|访客公众号编号(<=32,可为空,微信公众号号操作时赋值,短信链接,h5不用)||false|string||
|&emsp;&emsp;orderId|预约单Id||true|string||
|&emsp;&emsp;visitorAddress|访客住址||false|string||
|&emsp;&emsp;visitorBirthplace|籍贯||false|string||
|&emsp;&emsp;visitorCarNumber|车牌号||false|string||
|&emsp;&emsp;visitorCustoma|自定义字段a||false|string||
|&emsp;&emsp;visitorCustomb|自定义字段b||false|string||
|&emsp;&emsp;visitorCustomc|自定义字段c||false|string||
|&emsp;&emsp;visitorCustomd|自定义字段d||false|string||
|&emsp;&emsp;visitorCustome|自定义字段e||false|string||
|&emsp;&emsp;visitorCustomf|自定义字段f||false|string||
|&emsp;&emsp;visitorCustomg|自定义字段g||false|string||
|&emsp;&emsp;visitorCustomh|自定义字段h||false|string||
|&emsp;&emsp;visitorCustomi|自定义字段i||false|string||
|&emsp;&emsp;visitorCustomj|自定义字段j||false|string||
|&emsp;&emsp;visitorIdentityAddr|证件地址||false|string||
|&emsp;&emsp;visitorIdentityIssuer|发证机关||false|string||
|&emsp;&emsp;visitorIdentityNum|证件号码||false|string||
|&emsp;&emsp;visitorIdentityType|证件类型||false|integer(int32)||
|&emsp;&emsp;visitorName|访客姓名||true|string||
|&emsp;&emsp;visitorPersonNum|访客人数：默认1||true|integer(int32)||
|&emsp;&emsp;visitorWorkUnit|访客所属单位||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 2_员工取消邀约


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/wecom/bevisitor/invitation/cancel`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.员工点击邀约中状态的信息，可以取消邀约
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "orderId": "6546sdafs56adf"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|weComInvitationCancelRequest|员工取消邀约请求参数|body|true|WeComInvitationCancelRequest|WeComInvitationCancelRequest|
|&emsp;&emsp;orderId|预约单Id||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 3_邀约预览


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/wecom/bevisitor/invitation/wechat/{orderId}/preview`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.访客邀约信息预览
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "sceneshow": "sms"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|orderId|orderId|path|true|string||
|invitationPreviewRequest|邀约预览请求参数|body|true|InvitationPreviewRequest|InvitationPreviewRequest|
|&emsp;&emsp;sceneshow|链接打开场景(sms短信 mp_notice 微信公众号通知 mp_share 微信公众号分享 ma_share 微信小程序分享 log 记录)||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«InvitationPreviewResponse»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|InvitationPreviewResponse|InvitationPreviewResponse|
|&emsp;&emsp;approvalResult||string||
|&emsp;&emsp;authBarCode|访客二维码|string||
|&emsp;&emsp;beVisitorGroupName||string||
|&emsp;&emsp;beVisitorOpenId|被访人微信公众号openid|string||
|&emsp;&emsp;beVisitorPersonName|被访人姓名|string||
|&emsp;&emsp;beVisitorPhoneNum|被访人手机号码|string||
|&emsp;&emsp;endTime||string||
|&emsp;&emsp;startTime||string||
|&emsp;&emsp;status|记录状态。0：待审核；1：正常；2：迟到；3：失效；4：审核退回；5：超期自动签离；6：已签离；7：超期未签离；8：已到达；9：审核失效；10：邀约中；11：邀约失效|integer(int32)||
|&emsp;&emsp;visitorAddress|访客住址|string||
|&emsp;&emsp;visitorBirthplace|籍贯|string||
|&emsp;&emsp;visitorCarNumber|车牌号|string||
|&emsp;&emsp;visitorCustoma|自定义字段a|string||
|&emsp;&emsp;visitorCustomb|自定义字段b|string||
|&emsp;&emsp;visitorCustomc|自定义字段c|string||
|&emsp;&emsp;visitorCustomd|自定义字段d|string||
|&emsp;&emsp;visitorCustome|自定义字段e|string||
|&emsp;&emsp;visitorCustomf|自定义字段f|string||
|&emsp;&emsp;visitorCustomg|自定义字段g|string||
|&emsp;&emsp;visitorCustomh|自定义字段h|string||
|&emsp;&emsp;visitorCustomi|自定义字段i|string||
|&emsp;&emsp;visitorCustomj|自定义字段j|string||
|&emsp;&emsp;visitorEndTime|预计离开时间,必须晚于当前时间和预计来访时间|string||
|&emsp;&emsp;visitorIdentityAddr|证件地址|string||
|&emsp;&emsp;visitorIdentityIssuer|发证机关|string||
|&emsp;&emsp;visitorIdentityNum|证件号码|string||
|&emsp;&emsp;visitorIdentityType|证件类型|integer(int32)||
|&emsp;&emsp;visitorName|访客姓名|string||
|&emsp;&emsp;visitorPersonNum|访客人数：默认1|integer(int32)||
|&emsp;&emsp;visitorPhoneNum||string||
|&emsp;&emsp;visitorPhoto||string||
|&emsp;&emsp;visitorPurpose|来访事由,长度为1～128个字符|string||
|&emsp;&emsp;visitorStartTime|预计来访时间|string||
|&emsp;&emsp;visitorTypeId|访客类型|string||
|&emsp;&emsp;visitorWorkUnit|访客所属单位|string||
|&emsp;&emsp;weChatMpName|公众号名称|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"approvalResult": "",
		"authBarCode": "123",
		"beVisitorGroupName": "",
		"beVisitorOpenId": "12221xsssa",
		"beVisitorPersonName": "小红",
		"beVisitorPhoneNum": "18235642566",
		"endTime": "",
		"startTime": "",
		"status": 123,
		"visitorAddress": "中南海",
		"visitorBirthplace": "安徽",
		"visitorCarNumber": "浙A12321",
		"visitorCustoma": "123232323",
		"visitorCustomb": "123232323",
		"visitorCustomc": "123232323",
		"visitorCustomd": "123232323",
		"visitorCustome": "123232323",
		"visitorCustomf": "123",
		"visitorCustomg": "123",
		"visitorCustomh": "123",
		"visitorCustomi": "123",
		"visitorCustomj": "123",
		"visitorEndTime": "2004-05-03T18:30:08+08:00",
		"visitorIdentityAddr": "安徽芜湖",
		"visitorIdentityIssuer": "芜湖公安",
		"visitorIdentityNum": "123232323",
		"visitorIdentityType": 111,
		"visitorName": "小红",
		"visitorPersonNum": 10,
		"visitorPhoneNum": "",
		"visitorPhoto": "",
		"visitorPurpose": "参观",
		"visitorStartTime": "2004-05-03T17:30:08+08:00",
		"visitorTypeId": "1",
		"visitorWorkUnit": "海康",
		"weChatMpName": "10"
	},
	"msg": "success"
}
```


## 8_员工取消预约


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/wecom/bevisitor/order/cancel`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>员工预约取消接口。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "visitorBatch": "122228959455556"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaBeVisitorOrderCancelRequest|员工预约取消请求参数|body|true|WcMaBeVisitorOrderCancelRequest|WcMaBeVisitorOrderCancelRequest|
|&emsp;&emsp;visitorBatch|预约单批次||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 7_获取预约记录详情


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/wecom/bevisitor/order/detail`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>查询被访记录详情接口。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "visitorBatch": "122228959455556"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaBeVisitorOrderDetailRequest|获取预约单详情请求参数|body|true|WcMaBeVisitorOrderDetailRequest|WcMaBeVisitorOrderDetailRequest|
|&emsp;&emsp;visitorBatch|预约单批次||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«WcMaVisitorOrderDetailResponse»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|WcMaVisitorOrderDetailResponse|WcMaVisitorOrderDetailResponse|
|&emsp;&emsp;approvalResult||string||
|&emsp;&emsp;authBarCode|二维码凭证(预约单:正常、迟到才有)|string||
|&emsp;&emsp;authIdentityPid|身份证序列号|string||
|&emsp;&emsp;authTempCard|访客卡号|string||
|&emsp;&emsp;authVisitorCode|访客验证码|string||
|&emsp;&emsp;backlogId||string||
|&emsp;&emsp;beVisitorEnterpriseName|员工所属单位|string||
|&emsp;&emsp;beVisitorGroupId|被访人部门ID|string||
|&emsp;&emsp;beVisitorGroupName|被访人部门名称|string||
|&emsp;&emsp;beVisitorOpenId|被访人openid|string||
|&emsp;&emsp;beVisitorPersonId|被访人ID|string||
|&emsp;&emsp;beVisitorPersonName|员工姓名|string||
|&emsp;&emsp;beVisitorPhoneNum|员工手机号|string||
|&emsp;&emsp;beVisitorUserId|被访人唯一标识(该字段必填)|string||
|&emsp;&emsp;buttonList|操作按钮集合|array|WcMaOperateButtonDto|
|&emsp;&emsp;&emsp;&emsp;buttonKey|按钮Key|string||
|&emsp;&emsp;&emsp;&emsp;buttonName|按钮名称|string||
|&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;createUserType|创建者身份类型：1-平台用户，2-内部人员，3-来访人员|integer(int32)||
|&emsp;&emsp;disorder|添加序号|integer(int32)||
|&emsp;&emsp;endTime|拜访时间:预计离开时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;endTimeDifference|预计离开时间时差|string||
|&emsp;&emsp;endTimeUTC|预计离开时间UTC|integer(int64)||
|&emsp;&emsp;leaderVisitor|预约人员|WcMaRetinueVisitorDto|WcMaRetinueVisitorDto|
|&emsp;&emsp;&emsp;&emsp;orderModel|预约模式 person:指定人员预约 space:场地预约|string||
|&emsp;&emsp;&emsp;&emsp;status|同行人状态|string||
|&emsp;&emsp;&emsp;&emsp;visitorAddress|访客住址|string||
|&emsp;&emsp;&emsp;&emsp;visitorBirthplace|籍贯|string||
|&emsp;&emsp;&emsp;&emsp;visitorCarNumber|车牌号|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustoma|自定义字段a|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomb|自定义字段b|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomc|自定义字段c|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomd|自定义字段d|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustome|自定义字段e|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomf|自定义字段f|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomg|自定义字段g|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomh|自定义字段h|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomi|自定义字段i|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomj|自定义字段j|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityAddr|证件地址|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityIssuer|发证机关|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityNum|证件号码|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityType|证件类型|integer||
|&emsp;&emsp;&emsp;&emsp;visitorName|访客姓名|string||
|&emsp;&emsp;&emsp;&emsp;visitorPhoneNum|手机号码|string||
|&emsp;&emsp;&emsp;&emsp;visitorPhoto|访客头像|string||
|&emsp;&emsp;&emsp;&emsp;visitorSex|性别：1、男；2、女|integer||
|&emsp;&emsp;&emsp;&emsp;visitorWorkUnit|访客所属单位|string||
|&emsp;&emsp;orderId|预约单编号|string||
|&emsp;&emsp;orderModel|预约模式 person:指定人员预约 space:场地预约|string||
|&emsp;&emsp;processId|审批规则id|string||
|&emsp;&emsp;processItemId|审批规则实例id|string||
|&emsp;&emsp;processRemark|退回原因|string||
|&emsp;&emsp;productId|产品编号|string||
|&emsp;&emsp;projectId|租户编号|string||
|&emsp;&emsp;realEndTime|签离时间|string||
|&emsp;&emsp;realEndTimeDifference|签离时间时差|string||
|&emsp;&emsp;realEndTimeUTC|签离时间UTC|integer(int64)||
|&emsp;&emsp;registerPlace|访客登记地点|string||
|&emsp;&emsp;registerTime|登记时间|string||
|&emsp;&emsp;registerTimeDifference|登记时间时差|string||
|&emsp;&emsp;registerTimeUTC|登记时间UTC|integer(int64)||
|&emsp;&emsp;retinueList|同行人列表|array|WcMaRetinueVisitorDto|
|&emsp;&emsp;&emsp;&emsp;orderModel|预约模式 person:指定人员预约 space:场地预约|string||
|&emsp;&emsp;&emsp;&emsp;status|同行人状态|string||
|&emsp;&emsp;&emsp;&emsp;visitorAddress|访客住址|string||
|&emsp;&emsp;&emsp;&emsp;visitorBirthplace|籍贯|string||
|&emsp;&emsp;&emsp;&emsp;visitorCarNumber|车牌号|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustoma|自定义字段a|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomb|自定义字段b|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomc|自定义字段c|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomd|自定义字段d|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustome|自定义字段e|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomf|自定义字段f|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomg|自定义字段g|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomh|自定义字段h|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomi|自定义字段i|string||
|&emsp;&emsp;&emsp;&emsp;visitorCustomj|自定义字段j|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityAddr|证件地址|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityIssuer|发证机关|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityNum|证件号码|string||
|&emsp;&emsp;&emsp;&emsp;visitorIdentityType|证件类型|integer||
|&emsp;&emsp;&emsp;&emsp;visitorName|访客姓名|string||
|&emsp;&emsp;&emsp;&emsp;visitorPhoneNum|手机号码|string||
|&emsp;&emsp;&emsp;&emsp;visitorPhoto|访客头像|string||
|&emsp;&emsp;&emsp;&emsp;visitorSex|性别：1、男；2、女|integer||
|&emsp;&emsp;&emsp;&emsp;visitorWorkUnit|访客所属单位|string||
|&emsp;&emsp;startTime|拜访时间:预计来访时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;startTimeDifference|预计来访时间时差|string||
|&emsp;&emsp;startTimeUTC|预计来访时间UTC|integer(int64)||
|&emsp;&emsp;status|预约单状态|string||
|&emsp;&emsp;svrCodeIdentity|证件照对应图片服务器serviceNodes|string||
|&emsp;&emsp;svrCodeScanning|证件扫描照对应图片服务器serviceNodes|string||
|&emsp;&emsp;svrCodeVisitor|访客头像对应图片服务器serviceNodes|string||
|&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;visitBatch|访客批次|string||
|&emsp;&emsp;visitorAddress|访客住址|string||
|&emsp;&emsp;visitorAllowTimes|访客进入次数|integer(int32)||
|&emsp;&emsp;visitorBatch|预约单批次|string||
|&emsp;&emsp;visitorBirthplace|籍贯|string||
|&emsp;&emsp;visitorCarNumber|车牌号|string||
|&emsp;&emsp;visitorCustoma|自定义字段a：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomb|自定义字段b：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomc|自定义字段c：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomd|自定义字段d：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustome|自定义字段e：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomf|自定义字段f：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomg|自定义字段g：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomh|自定义字段h：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomi|自定义字段i：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorCustomj|自定义字段j：字段类型为图片时,照片链接以英文逗号分割,最多支持三张照片|string||
|&emsp;&emsp;visitorGroupId|访客名单分组ID|string||
|&emsp;&emsp;visitorIdentityAddr|证件地址|string||
|&emsp;&emsp;visitorIdentityIssuer|发证机关|string||
|&emsp;&emsp;visitorIdentityNum|证件号码|string||
|&emsp;&emsp;visitorIdentityPhoto|证件照片|string||
|&emsp;&emsp;visitorIdentityType|证件类型：111、身份证|integer(int32)||
|&emsp;&emsp;visitorLeader|访客团体领队:0 同行人 1领队|string||
|&emsp;&emsp;visitorName|姓名|string||
|&emsp;&emsp;visitorOpenId|访客微信公众号唯一标识|string||
|&emsp;&emsp;visitorPersonNum|来访人数|integer(int32)||
|&emsp;&emsp;visitorPhoneNum|手机号|string||
|&emsp;&emsp;visitorPhoto|访客头像|string||
|&emsp;&emsp;visitorPhotoFlag|人脸质量合格标识。0：合格；1：不合格|string||
|&emsp;&emsp;visitorPinyin|访客名首字母缩写|string||
|&emsp;&emsp;visitorPrivilegeGroupIds|访客权限组ids|string||
|&emsp;&emsp;visitorPurpose|事由|string||
|&emsp;&emsp;visitorScanningPhoto|证件扫描照片|string||
|&emsp;&emsp;visitorSex|性别：1、男；2、女|integer(int32)||
|&emsp;&emsp;visitorTemperature|访客体温|string||
|&emsp;&emsp;visitorTemperatureStatus|访客体温状态|integer(int32)||
|&emsp;&emsp;visitorTypeId|访客类型id|string||
|&emsp;&emsp;visitorUserId||string||
|&emsp;&emsp;visitorWorkUnit|访客来访单位|string||
|&emsp;&emsp;webLabel|记录状态描述-web端|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"approvalResult": "",
		"authBarCode": "123",
		"authIdentityPid": "123",
		"authTempCard": "123",
		"authVisitorCode": "123",
		"backlogId": "",
		"beVisitorEnterpriseName": "海康威视",
		"beVisitorGroupId": "123",
		"beVisitorGroupName": "123",
		"beVisitorOpenId": "123",
		"beVisitorPersonId": "123",
		"beVisitorPersonName": "陈大鹏",
		"beVisitorPhoneNum": "123",
		"beVisitorUserId": "6546sdafs56adf",
		"buttonList": [
			{
				"buttonKey": "InvitationFoundByBeVisitor",
				"buttonName": "重新邀约"
			}
		],
		"createTime": "123",
		"createUserType": 123,
		"disorder": 123,
		"endTime": "2021-12-23 18:22:12",
		"endTimeDifference": "123",
		"endTimeUTC": 123,
		"leaderVisitor": {
			"orderModel": "person",
			"status": "已取消",
			"visitorAddress": "中南海",
			"visitorBirthplace": "安徽",
			"visitorCarNumber": "浙A12345",
			"visitorCustoma": "123232323",
			"visitorCustomb": "123232323",
			"visitorCustomc": "123232323",
			"visitorCustomd": "123232323",
			"visitorCustome": "123232323",
			"visitorCustomf": "123232323",
			"visitorCustomg": "123232323",
			"visitorCustomh": "123232323",
			"visitorCustomi": "123232323",
			"visitorCustomj": "123232323",
			"visitorIdentityAddr": "安徽芜湖",
			"visitorIdentityIssuer": "芜湖公安",
			"visitorIdentityNum": "123232323",
			"visitorIdentityType": 111,
			"visitorName": "陈绍鹏",
			"visitorPhoneNum": "18966175813",
			"visitorPhoto": "123",
			"visitorSex": 1,
			"visitorWorkUnit": "大碗娱乐无限责任公司"
		},
		"orderId": "122228959455556",
		"orderModel": "person",
		"processId": "123",
		"processItemId": "123",
		"processRemark": "122228959455556",
		"productId": "123",
		"projectId": "122228959455556",
		"realEndTime": "123",
		"realEndTimeDifference": "123",
		"realEndTimeUTC": 123,
		"registerPlace": "123",
		"registerTime": "123",
		"registerTimeDifference": "123",
		"registerTimeUTC": 123,
		"retinueList": [
			{
				"orderModel": "person",
				"status": "已取消",
				"visitorAddress": "中南海",
				"visitorBirthplace": "安徽",
				"visitorCarNumber": "浙A12345",
				"visitorCustoma": "123232323",
				"visitorCustomb": "123232323",
				"visitorCustomc": "123232323",
				"visitorCustomd": "123232323",
				"visitorCustome": "123232323",
				"visitorCustomf": "123232323",
				"visitorCustomg": "123232323",
				"visitorCustomh": "123232323",
				"visitorCustomi": "123232323",
				"visitorCustomj": "123232323",
				"visitorIdentityAddr": "安徽芜湖",
				"visitorIdentityIssuer": "芜湖公安",
				"visitorIdentityNum": "123232323",
				"visitorIdentityType": 111,
				"visitorName": "陈绍鹏",
				"visitorPhoneNum": "18966175813",
				"visitorPhoto": "123",
				"visitorSex": 1,
				"visitorWorkUnit": "大碗娱乐无限责任公司"
			}
		],
		"startTime": "2021-12-22 18:22:12",
		"startTimeDifference": "123",
		"startTimeUTC": 123,
		"status": "待审批",
		"svrCodeIdentity": "123",
		"svrCodeScanning": "123",
		"svrCodeVisitor": "123",
		"updateTime": "123",
		"visitBatch": "123",
		"visitorAddress": "123",
		"visitorAllowTimes": 123,
		"visitorBatch": "122228959455556",
		"visitorBirthplace": "123",
		"visitorCarNumber": "浙A12345",
		"visitorCustoma": "123",
		"visitorCustomb": "123",
		"visitorCustomc": "123",
		"visitorCustomd": "123",
		"visitorCustome": "123",
		"visitorCustomf": "123",
		"visitorCustomg": "123",
		"visitorCustomh": "123",
		"visitorCustomi": "123",
		"visitorCustomj": "123",
		"visitorGroupId": "123",
		"visitorIdentityAddr": "123",
		"visitorIdentityIssuer": "123",
		"visitorIdentityNum": "123",
		"visitorIdentityPhoto": "123",
		"visitorIdentityType": 123,
		"visitorLeader": "0",
		"visitorName": "123",
		"visitorOpenId": "123",
		"visitorPersonNum": 123,
		"visitorPhoneNum": "123",
		"visitorPhoto": "123",
		"visitorPhotoFlag": "123",
		"visitorPinyin": "123",
		"visitorPrivilegeGroupIds": "123",
		"visitorPurpose": "参观",
		"visitorScanningPhoto": "123",
		"visitorSex": 123,
		"visitorTemperature": "123",
		"visitorTemperatureStatus": 123,
		"visitorTypeId": "123",
		"visitorUserId": "",
		"visitorWorkUnit": "123",
		"webLabel": "123"
	},
	"msg": "success"
}
```


## 1_员工发起邀约


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/wecom/bevisitor/order/invitation/founding`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.员工发起邀约请求
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "endTime": "2021-12-23 18:22",
  "startTime": "2021-12-22 18:22",
  "visitorName": "小红",
  "visitorPhoneNum": "123",
  "visitorPrivilegeGroupIds": "123,1231",
  "visitorPurpose": "参观",
  "visitorTypeId": "1"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|weComInvitationStartRequest|员工发起邀约请求参数|body|true|WeComInvitationStartRequest|WeComInvitationStartRequest|
|&emsp;&emsp;endTime|预计离开时间(yyyy-MM-dd HH:mm)||true|string||
|&emsp;&emsp;startTime|预计来访时间(yyyy-MM-dd HH:mm)||true|string||
|&emsp;&emsp;visitorName|访客姓名||true|string||
|&emsp;&emsp;visitorPhoneNum|访客手机号码||true|string||
|&emsp;&emsp;visitorPrivilegeGroupIds|访客拜访区域编号集合||true|string||
|&emsp;&emsp;visitorPurpose|邀请事由||true|string||
|&emsp;&emsp;visitorTypeId|访客类型||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«InvitationStartResponse»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|InvitationStartResponse|InvitationStartResponse|
|&emsp;&emsp;orderId|邀约编号|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"orderId": "12211111111111x"
	},
	"msg": "success"
}
```


## 5_获取待受访记录


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/wecom/bevisitor/order/reception/log/doing`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>获取待受访,根据被访者openid和预约单:正常和迟到、访客已登记 过滤数据，按来访时间顺序。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "pageNo": 1,
  "pageSize": 20
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaBeVisitorReceptionIngRequest|员工待受访请求参数|body|true|WcMaBeVisitorReceptionIngRequest|WcMaBeVisitorReceptionIngRequest|
|&emsp;&emsp;pageNo|页码（pageNo>0）||true|integer(int32)||
|&emsp;&emsp;pageSize|页大小（0<pageSize<=1000）||true|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PageResult«WcMaBeVisitorOrderCardDto»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PageResult«WcMaBeVisitorOrderCardDto»|PageResult«WcMaBeVisitorOrderCardDto»|
|&emsp;&emsp;list|数据信息|array|WcMaBeVisitorOrderCardDto|
|&emsp;&emsp;&emsp;&emsp;backLogId||string||
|&emsp;&emsp;&emsp;&emsp;buttonList|操作按钮集合|array|WcMaOperateButtonDto|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;buttonKey|按钮Key|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;buttonName|按钮名称|string||
|&emsp;&emsp;&emsp;&emsp;endTime|预计离开时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;&emsp;&emsp;projectId|projectId|string||
|&emsp;&emsp;&emsp;&emsp;startTime|预计来访时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;&emsp;&emsp;status|预约单状态|string||
|&emsp;&emsp;&emsp;&emsp;visitorBatch|预约单批次|string||
|&emsp;&emsp;&emsp;&emsp;visitorName|访客姓名|string||
|&emsp;&emsp;&emsp;&emsp;visitorPurpose|事由|string||
|&emsp;&emsp;&emsp;&emsp;visitorWorkUnit|访客所属单位|string||
|&emsp;&emsp;pageNo|页码|integer(int32)||
|&emsp;&emsp;pageSize|页大小|integer(int32)||
|&emsp;&emsp;total|总条数|integer(int64)||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"list": [
			{
				"backLogId": "",
				"buttonList": [
					{
						"buttonKey": "InvitationFoundByBeVisitor",
						"buttonName": "重新邀约"
					}
				],
				"endTime": "2021-12-23 18:22:12",
				"projectId": "cccdddd",
				"startTime": "2021-12-22 18:22:12",
				"status": "待审批",
				"visitorBatch": "122228959455556",
				"visitorName": "陈绍鹏",
				"visitorPurpose": "参观",
				"visitorWorkUnit": "大碗娱乐无限责任公司"
			}
		],
		"pageNo": 1,
		"pageSize": 20,
		"total": 5
	},
	"msg": "success"
}
```


## 6_获取受访历史记录


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/wecom/bevisitor/order/reception/log/history`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>获取受访历史记录,根据被访者openid和预约单:超期自动签离(系统)、访客签离和超期未签离(系统) 过滤数据，按离开时间倒序。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "pageNo": 1,
  "pageSize": 20,
  "visitorName": "陈绍鹏"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wcMaBeVisitorReceptionHistoryRequest|员工受访历史记录请求参数|body|true|WcMaBeVisitorReceptionHistoryRequest|WcMaBeVisitorReceptionHistoryRequest|
|&emsp;&emsp;pageNo|页码（pageNo>0）||true|integer(int32)||
|&emsp;&emsp;pageSize|页大小（0<pageSize<=1000）||true|integer(int32)||
|&emsp;&emsp;visitorName|访客姓名||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PageResult«WcMaBeVisitorOrderCardDto»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PageResult«WcMaBeVisitorOrderCardDto»|PageResult«WcMaBeVisitorOrderCardDto»|
|&emsp;&emsp;list|数据信息|array|WcMaBeVisitorOrderCardDto|
|&emsp;&emsp;&emsp;&emsp;backLogId||string||
|&emsp;&emsp;&emsp;&emsp;buttonList|操作按钮集合|array|WcMaOperateButtonDto|
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;buttonKey|按钮Key|string||
|&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;buttonName|按钮名称|string||
|&emsp;&emsp;&emsp;&emsp;endTime|预计离开时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;&emsp;&emsp;projectId|projectId|string||
|&emsp;&emsp;&emsp;&emsp;startTime|预计来访时间(yyyy-MM-dd HH:mm:ss)|string||
|&emsp;&emsp;&emsp;&emsp;status|预约单状态|string||
|&emsp;&emsp;&emsp;&emsp;visitorBatch|预约单批次|string||
|&emsp;&emsp;&emsp;&emsp;visitorName|访客姓名|string||
|&emsp;&emsp;&emsp;&emsp;visitorPurpose|事由|string||
|&emsp;&emsp;&emsp;&emsp;visitorWorkUnit|访客所属单位|string||
|&emsp;&emsp;pageNo|页码|integer(int32)||
|&emsp;&emsp;pageSize|页大小|integer(int32)||
|&emsp;&emsp;total|总条数|integer(int64)||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"list": [
			{
				"backLogId": "",
				"buttonList": [
					{
						"buttonKey": "InvitationFoundByBeVisitor",
						"buttonName": "重新邀约"
					}
				],
				"endTime": "2021-12-23 18:22:12",
				"projectId": "cccdddd",
				"startTime": "2021-12-22 18:22:12",
				"status": "待审批",
				"visitorBatch": "122228959455556",
				"visitorName": "陈绍鹏",
				"visitorPurpose": "参观",
				"visitorWorkUnit": "大碗娱乐无限责任公司"
			}
		],
		"pageNo": 1,
		"pageSize": 20,
		"total": 5
	},
	"msg": "success"
}
```


# 15_企微应用_员工端-基础数据


## 15_企微上传预约表单中的图片


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/wecom/image/upload`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.上传图片
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "imageData": "dgfrgrttr",
  "productId": "bbb",
  "projectId": "aaa",
  "type": "passback"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|pictureRequest|PictureRequest|body|true|PictureRequest|PictureRequest|
|&emsp;&emsp;imageData|图片数据，base64编码(不含data:image/jpg;base64)||true|object||
|&emsp;&emsp;productId|产品编号||false|string||
|&emsp;&emsp;projectId|项目编号||false|string||
|&emsp;&emsp;type|visitor/diy：预约字段||true|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«AcscImageUploadResponse»|
|201|Created|ActionErrorResult|
|204|No Content||
|401|Unauthorized|ActionErrorResult|
|403|Forbidden|ActionErrorResult|
|404|Not Found|ActionErrorResult|


**响应状态码-200**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|AcscImageUploadResponse|AcscImageUploadResponse|
|&emsp;&emsp;faceId|人脸专用：人脸图片编号|string||
|&emsp;&emsp;faceLevel|人脸专用：人脸质量级别(高>=80分，中>=70分 低>=60分 不合格<60)|string||
|&emsp;&emsp;faceScore|人脸专用：人脸评分值|integer(int32)||
|&emsp;&emsp;imageUrl|图片地址|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"faceId": "1179524873320912",
		"faceLevel": "中",
		"faceScore": 20,
		"imageUrl": "http://aliyun.com/image/122ssss.jpg"
	},
	"msg": "success"
}
```


**响应状态码-201**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-401**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-403**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-404**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


## 02_获取访客权限组列表


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/wecom/my/privilege/group`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>1.访客权限组列表
发布版本：V1.0.0</p>



**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«WcMaPrivilegeGroupResponse»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|WcMaPrivilegeGroupResponse|WcMaPrivilegeGroupResponse|
|&emsp;&emsp;groupList|权限组列表|array|WcMaPrivilegeGroupDto|
|&emsp;&emsp;&emsp;&emsp;groupId|权限组编号(<=32)|string||
|&emsp;&emsp;&emsp;&emsp;groupName|权限组名称(<=32)|string||
|&emsp;&emsp;&emsp;&emsp;isDefault|是否是默认拜访区域，1-是，0-否|object||
|&emsp;&emsp;&emsp;&emsp;select||boolean||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"groupList": [
			{
				"groupId": "9c6adaf7-40f0-4e97-9af0-ea16369b9315",
				"groupName": "停车场",
				"isDefault": "1",
				"select": true
			}
		]
	},
	"msg": "success"
}
```


## 01_获取事由列表


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/wecom/my/purpose`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>1.事由列表
发布版本：V1.0.0</p>



**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«WcMaPurposeResponse»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|WcMaPurposeResponse|WcMaPurposeResponse|
|&emsp;&emsp;purposeList|事由列表|array|WcMaPurposeDto|
|&emsp;&emsp;&emsp;&emsp;purposeDesc|事由描述|string||
|&emsp;&emsp;&emsp;&emsp;purposeId|事由编号(<=32)|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"purposeList": [
			{
				"purposeDesc": "参观",
				"purposeId": "bdf2f958-8f4a-4d26-b7e4-5179215b7fba"
			}
		]
	},
	"msg": "success"
}
```


## 14_获取时间类型格式


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/wecom/my/timeDisplay`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>1.小程序端获取预约模式内容
发布版本：V1.0.0</p>



**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«TimeDisplayDto»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|TimeDisplayDto|TimeDisplayDto|
|&emsp;&emsp;timeDisplayType|预约/邀约时间选择类型(0仅选日期 1时分精确选择)|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"timeDisplayType": "0"
	},
	"msg": "success"
}
```


## 13_获取访客类型列表


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/wecom/my/visitor/type`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>1.访客权限组列表
发布版本：V1.0.0</p>



**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«WcMaVisitorTypeResponse»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|WcMaVisitorTypeResponse|WcMaVisitorTypeResponse|
|&emsp;&emsp;typeList|权限组列表|array|WcMaVisitorTypeDto|
|&emsp;&emsp;&emsp;&emsp;typeId|类型编号(<=32)|string||
|&emsp;&emsp;&emsp;&emsp;typeName|类型名称(<=32)|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"typeList": [
			{
				"typeId": "9c6adaf7-40f0-4e97-9af0-ea16369b9315",
				"typeName": "贵宾"
			}
		]
	},
	"msg": "success"
}
```


# 15_企微应用_访客预约


## 04_上传人脸图片


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/wecom/visitor/facePic/upload`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>上传人脸图片。
 发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "faceData": "33309BD2....3247D8B"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wecomFaceUploadRequest|图片上传参数|body|true|WecomFaceUploadRequest|WecomFaceUploadRequest|
|&emsp;&emsp;faceData|图片数据，base64编码||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«FaceUploadResponse»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|FaceUploadResponse|FaceUploadResponse|
|&emsp;&emsp;faceId|人脸图片编号|string||
|&emsp;&emsp;faceUrl|人员图片地址|string||
|&emsp;&emsp;level|人脸质量级别(高>=80分，中>=70分 低>=60分 不合格<60)|string||
|&emsp;&emsp;score|人脸评分值|integer(int32)||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"faceId": "中",
		"faceUrl": "11111",
		"level": "中",
		"score": 20
	},
	"msg": "success"
}
```


## 03_查询访客信息字段


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/wecom/visitor/field/info`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>查询访客信息字段(基础字段，自定义字段，来访事由，访客类型)。
 发布版本：V1.0.0</p>



**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«List«FieldResponse»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|array|FieldResponse|
|&emsp;&emsp;dataList||array|DataDictionarySingleDto|
|&emsp;&emsp;&emsp;&emsp;selected||boolean||
|&emsp;&emsp;&emsp;&emsp;text||string||
|&emsp;&emsp;&emsp;&emsp;value||object||
|&emsp;&emsp;fieldInfoDto||FieldInfoDto|FieldInfoDto|
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;customOption|自定义选择框的枚举值|object||
|&emsp;&emsp;&emsp;&emsp;dataValue|关联的枚举值|string||
|&emsp;&emsp;&emsp;&emsp;defaultValue|默认字段|string||
|&emsp;&emsp;&emsp;&emsp;disorder|更新顺序|integer||
|&emsp;&emsp;&emsp;&emsp;display|是否可见，0表示可见，1表示不可见|string||
|&emsp;&emsp;&emsp;&emsp;fieldProperties|字段属性：0：访客信息字段，1：被访人信息字段|string||
|&emsp;&emsp;&emsp;&emsp;fieldType|参数类型|string||
|&emsp;&emsp;&emsp;&emsp;hint|表单项的提示信息|string||
|&emsp;&emsp;&emsp;&emsp;maxLength|最大字段长度|integer||
|&emsp;&emsp;&emsp;&emsp;overseas|是否支持海外|string||
|&emsp;&emsp;&emsp;&emsp;paraId|paraId|string||
|&emsp;&emsp;&emsp;&emsp;paraKey|表单项名称key|string||
|&emsp;&emsp;&emsp;&emsp;paraName|表单项名称|string||
|&emsp;&emsp;&emsp;&emsp;placeholder|表单项的placeholder，vue-i18n多语言的key，比如人员民族中的请选择提示|string||
|&emsp;&emsp;&emsp;&emsp;productId|产品编号|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目编号|string||
|&emsp;&emsp;&emsp;&emsp;readOnly|是否可修改，0表示不可修改,1表示可修改|string||
|&emsp;&emsp;&emsp;&emsp;regular|表单的正则表达式|string||
|&emsp;&emsp;&emsp;&emsp;required|是否必填，0表示必填，1表示非必填|string||
|&emsp;&emsp;&emsp;&emsp;showType|表单项类型。1：input；2：select；3：data-picker；6：pic|string||
|&emsp;&emsp;&emsp;&emsp;status|访客字段状态：0正常 -1已删除|integer||
|&emsp;&emsp;&emsp;&emsp;tips|提示信息|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;subHint||string||
|&emsp;&emsp;subParaKey||string||
|&emsp;&emsp;subParaName||string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": [
		{
			"dataList": [
				{
					"selected": true,
					"text": "",
					"value": {}
				}
			],
			"fieldInfoDto": {
				"createTime": "2021-07-01 12:00:00",
				"customOption": "123",
				"dataValue": "123",
				"defaultValue": "其他",
				"disorder": 1,
				"display": "1",
				"fieldProperties": "0",
				"fieldType": "1",
				"hint": "123",
				"maxLength": 11,
				"overseas": "1",
				"paraId": "ccc",
				"paraKey": "123",
				"paraName": "aaa",
				"placeholder": "123",
				"productId": "bbb",
				"projectId": "aaa",
				"readOnly": "1",
				"regular": "123",
				"required": "1",
				"showType": "1",
				"status": 0,
				"tips": "输入车牌号码信息可作为您去拜访时的停车凭证",
				"updateTime": "2021-07-11 12:00:00"
			},
			"subHint": "",
			"subParaKey": "",
			"subParaName": ""
		}
	],
	"msg": "success"
}
```


## 02_访客获取二维码接口


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/wecom/visitor/qrCode`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>访客获取二维码接口。
 发布版本：V1.0.0</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|orderId|orderId|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«string»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": "",
	"msg": "success"
}
```


## 1_公众号消息界面登录


**接口地址**:`/webapi/visitorcs/ui/v1/wechat/wecom/visitor/visitor/msg/login`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.公众号消息界面自动登陆
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "orderId": "123"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|wecomMsgLoginRequest|消息界面登陆参数|body|true|WecomMsgLoginRequest|WecomMsgLoginRequest|
|&emsp;&emsp;orderId|orderId||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«TokenWeComResponse»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|TokenWeComResponse|TokenWeComResponse|
|&emsp;&emsp;isAllowLogin|是否允许注册1：允许，0：不允许|string||
|&emsp;&emsp;reason|不允许注册时返回原因，前端可用于界面提示信息|string||
|&emsp;&emsp;token|Token信息|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"isAllowLogin": "0",
		"reason": "项目授权已过期",
		"token": "0003b19335524b0387a01e91dd6946ea"
	},
	"msg": "success"
}
```


# 15_客户端接口


## 查询访客权限下载结果


**接口地址**:`/webapi/visitorcs/api/v1/clientService/authResult`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>查询访客权限下载结果</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|orderId|访客预约单id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«Map«string,List«AuthResultDto»»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|AuthResultDto|AuthResultDto|
|&emsp;&emsp;authStatus|下载结果:0无介质 1待下发 2正在下发 3已下发 4下发失败 -1待删除 -2正在删除 -3已删除 -4删除失败|object||
|&emsp;&emsp;cardType|授权类型:0：身份证号；1：身份证序列号；2：IC卡；3：二维码；4：车牌号码；5:人脸|object||
|&emsp;&emsp;deviceDesc|设备名称|object||
|&emsp;&emsp;orderId|访客id|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"additionalProperties1": {
			"authStatus": "1",
			"cardType": "1",
			"deviceDesc": "门禁一体机",
			"orderId": "123e3522-0033-11e8-9d66-9366fb50212"
		}
	},
	"msg": "success"
}
```


## 重新下发权限


**接口地址**:`/webapi/visitorcs/api/v1/clientService/authResult/download`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>权限重新下发功能</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|orderId|访客单id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 分页查询黑名单人员信息


**接口地址**:`/webapi/visitorcs/api/v1/clientService/blackList`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>分页查询黑名单人员信息</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|pageNo|当前页,大于0|query|true|integer(int32)||
|pageSize|分页大小,大于0且不超过1000|query|true|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PageResult«GroupPersonInfoDto»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PageResult«GroupPersonInfoDto»|PageResult«GroupPersonInfoDto»|
|&emsp;&emsp;list|数据信息|array|GroupPersonInfoDto|
|&emsp;&emsp;&emsp;&emsp;identityId|证件类型:111身份证，335驾驶证，131工作证，133学生证，114军官证，414护照，990其他|object||
|&emsp;&emsp;&emsp;&emsp;identityNum|证件号码|object||
|&emsp;&emsp;&emsp;&emsp;phoneNum|手机号码|object||
|&emsp;&emsp;pageNo|页码|integer(int32)||
|&emsp;&emsp;pageSize|页大小|integer(int32)||
|&emsp;&emsp;total|总条数|integer(int64)||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"list": [
			{
				"identityId": "111",
				"identityNum": "465465116845",
				"phoneNum": "188800993565"
			}
		],
		"pageNo": 1,
		"pageSize": 20,
		"total": 5
	},
	"msg": "success"
}
```


## 获取访客的入园须知配置


**接口地址**:`/webapi/visitorcs/api/v1/clientService/getNoteAdmission`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>获取访客的入园须知配置</p>



**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«NoteAdmissionDto»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|NoteAdmissionDto|NoteAdmissionDto|
|&emsp;&emsp;content|内容:在开启状态下才有值|object||
|&emsp;&emsp;status|状态  0:关闭 1:开启|object||
|&emsp;&emsp;title|标题:在开启状态下才有值|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"content": "1.遵守XXXX",
		"status": "0",
		"title": "XXX公司的入园须知"
	},
	"msg": "success"
}
```


## 获取当前系统时间


**接口地址**:`/webapi/visitorcs/api/v1/clientService/getSysTime`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>返回当前系统时间（包含iso格式，utc格式）和时差</p>



**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«SysTimeDto»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|SysTimeDto|SysTimeDto|
|&emsp;&emsp;sysTime|系统ISO时间|object||
|&emsp;&emsp;sysTimeDifference|系统时间时差|object||
|&emsp;&emsp;sysTimeUTC|系统UTC时间|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"sysTime": "2018-10-29T15:33:07+08:00",
		"sysTimeDifference": "+08:00",
		"sysTimeUTC": "12131231231231"
	},
	"msg": "success"
}
```


## 根据证件信息查询最近一次历史访客记录


**接口地址**:`/webapi/visitorcs/api/v1/clientService/lastVisitor/inquiry`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>根据证件信息查询最近一次历史访客记录，本接口支持访客自定义属性的返回，通过获取访客字段的配置信息接口获取平台已支持访客自定义属性的说明</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|identityId|证件类型|query|true|integer(int32)||
|identityNum|证件号码，小于20位|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«VisitorBaseInfo»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|VisitorBaseInfo|VisitorBaseInfo|
|&emsp;&emsp;beVisitPersonId|被访人id|object||
|&emsp;&emsp;birthplace|籍贯|object||
|&emsp;&emsp;carNumber|车牌号|object||
|&emsp;&emsp;certAddr|证件地址|object||
|&emsp;&emsp;certIssuer|发证机关|object||
|&emsp;&emsp;identityId|证件类型：111身份证，335驾驶证，131工作证，133学生证，114军官证，414护照，990其他|object||
|&emsp;&emsp;identityNum|证件号码|object||
|&emsp;&emsp;name|访客姓名|object||
|&emsp;&emsp;openId|微信H5使用时为必填字段，用户页面授权唯一编码：openId|object||
|&emsp;&emsp;orderId|访客记录orderId|object||
|&emsp;&emsp;phoneNum|手机号|object||
|&emsp;&emsp;purpose|访客事由|object||
|&emsp;&emsp;sex|性别,1男,2女|object||
|&emsp;&emsp;visitorAddress|访客住址|object||
|&emsp;&emsp;visitorTypeId|访客类型id|object||
|&emsp;&emsp;visitorWorkUnit|访客来访单位|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"beVisitPersonId": "123123123-4323412-12312",
		"birthplace": "杭州滨江",
		"carNumber": "浙A32216",
		"certAddr": "某个地址",
		"certIssuer": "某个机关单位",
		"identityId": "111",
		"identityNum": "32165165165161",
		"name": "小红",
		"openId": "1253566554",
		"orderId": "123123123-4323412-12312",
		"phoneNum": "1253566554",
		"purpose": "实习",
		"sex": "1",
		"visitorAddress": "我是访客住址",
		"visitorTypeId": "访客所在公司",
		"visitorWorkUnit": "某个公司"
	},
	"msg": "success"
}
```


## 客户端登出


**接口地址**:`/webapi/visitorcs/api/v1/clientService/logOut`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>客户端注销前调用，去除平台保存的登录信息</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|clientMacAddress|客户端MAC地址|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 登录查询授权信息


**接口地址**:`/webapi/visitorcs/api/v1/clientService/login`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>登录查询授权信息，建议客户端在云耀登陆后调用此接口，用户切换回主页也要查询下，防止项目授权过期了还一直在登录</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|clientMacAddress|客户端MAC地址|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«AuthorizationInfo»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|AuthorizationInfo|AuthorizationInfo|
|&emsp;&emsp;loginResult|登录结果：0：正常登陆，1：授权异常，不能登录|object||
|&emsp;&emsp;tips|提示信息：在授权异常时提示具体原因：如：访客机登录数量超限，项目授权过期等|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"loginResult": "0",
		"tips": "访客机登录数量超限"
	},
	"msg": "success"
}
```


## 离线数据上传


**接口地址**:`/webapi/visitorcs/api/v1/clientService/offline/data/synchron`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>离线数据上传, 本接口支持访客信息的自定义字段，按照属性定义key:value上传到入参中即可，通过获取访客字段的配置信息接口获取平台已支持访客自定义属性的说明。,</p>



**请求示例**:


```javascript
{
  "disorder": 123,
  "pageNo": "3",
  "pageSize": "50"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|orderDto|访客预约同步信息对象|body|true|OrderDto|OrderDto|
|&emsp;&emsp;disorder|更新顺序||false|integer(int32)||
|&emsp;&emsp;pageNo|查询时第几页||true|object||
|&emsp;&emsp;pageSize|查询时单页条数,限定大小不能超过1000||true|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«object»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 访客登记


**接口地址**:`/webapi/visitorcs/api/v1/clientService/order/register`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>支持未预约登记,已预约登记,同行人登记,本接口支持访客信息的自定义字段，按照属性定义key:value上传到入参中即可，通过获取访客字段的配置信息接口获取平台已支持访客自定义属性的说明。</p>



**请求示例**:


```javascript
{
  "beVisitPersonId": "6546sdafs56adf",
  "birthplace": "杭州萧山",
  "carNumber": "浙A32216",
  "cardNo": "12345678",
  "certAddr": "访客所在公司",
  "certIssuer": "杭州滨江公安局分局",
  "certifyFlag": "1",
  "clientUserType": "1",
  "defaultPrivilegeFlag": "1",
  "endTimeISO": "2018-10-29T15:33:07+08:00",
  "faceId": "http://...",
  "identityId": "111",
  "identityNum": "32165165165161",
  "identityPhoto": "http://...",
  "identityPid": "123456615",
  "name": "小红",
  "orderId": "6546sdafs56adf",
  "personNum": "1",
  "phoneNum": "1253566554",
  "privilegeGroupIds": {},
  "productId": "访客所在公司",
  "projectId": "访客所在公司",
  "purpose": "参观",
  "receptionistOrgCode": "98937520-cf8d-11e9-bfbe-2b8d70e41a6b",
  "registerPlace": "XX访客机",
  "registerType": "0",
  "scanningPhoto": "http://...",
  "sex": "1",
  "temperatureStatus": "0",
  "visitorAddress": "杭州萧山",
  "visitorAllowTimes": "0",
  "visitorPhoto": "http://...",
  "visitorTemperature": "36.5",
  "visitorTypeId": "访客所在公司",
  "visitorWorkUnit": "某个公司"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|registerInfo|客户端提交访客单模型DTO|body|true|RegisterInfo|RegisterInfo|
|&emsp;&emsp;beVisitPersonId|被访人ID||false|object||
|&emsp;&emsp;birthplace|籍贯||false|object||
|&emsp;&emsp;carNumber|车牌号||false|object||
|&emsp;&emsp;cardNo|卡号||false|object||
|&emsp;&emsp;certAddr|证件地址||false|object||
|&emsp;&emsp;certIssuer|发证机关||false|object||
|&emsp;&emsp;certifyFlag|是否人脸采集||false|object||
|&emsp;&emsp;clientUserType|接口调用方||false|object||
|&emsp;&emsp;defaultPrivilegeFlag|是否下载默认权限组||false|object||
|&emsp;&emsp;endTimeISO|预计离开时间||false|object||
|&emsp;&emsp;faceId|访客头像id||false|object||
|&emsp;&emsp;identityId|证件类型：111身份证，335驾驶证，131工作证，133学生证，114军官证，414护照，990其他||false|object||
|&emsp;&emsp;identityNum|证件号码||false|object||
|&emsp;&emsp;identityPhoto|证件照片||false|object||
|&emsp;&emsp;identityPid|证件序列号||false|object||
|&emsp;&emsp;name|访客姓名||false|object||
|&emsp;&emsp;orderId|预约单ID||false|object||
|&emsp;&emsp;personNum|来访人数||false|object||
|&emsp;&emsp;phoneNum|手机号||false|object||
|&emsp;&emsp;privilegeGroupIds|权限组数组||false|object||
|&emsp;&emsp;productId|产品id||false|object||
|&emsp;&emsp;projectId|项目id||false|object||
|&emsp;&emsp;purpose|来访事由||false|object||
|&emsp;&emsp;receptionistOrgCode|被访人所属组织||false|object||
|&emsp;&emsp;registerPlace|访客登记地点||false|object||
|&emsp;&emsp;registerType|登记类型，1-未预约登记，2-已预约登记||false|object||
|&emsp;&emsp;scanningPhoto|证件扫描照片||false|object||
|&emsp;&emsp;sex|性别,1男,2女||false|object||
|&emsp;&emsp;temperatureStatus|访客体温状态：0：正常，1：异常||false|object||
|&emsp;&emsp;visitorAddress|访客住址||false|object||
|&emsp;&emsp;visitorAllowTimes|访客出入次数(0:不限制次数，其他数字代表具体次数)||false|object||
|&emsp;&emsp;visitorPhoto|访客头像||false|object||
|&emsp;&emsp;visitorTemperature|访客体温||false|object||
|&emsp;&emsp;visitorTypeId|访客类型id||false|object||
|&emsp;&emsp;visitorWorkUnit|访客来访单位||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«VisitorInfo»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|VisitorInfo|VisitorInfo|
|&emsp;&emsp;approvalResult|访客单中的审批状态|object||
|&emsp;&emsp;barCode|访客二维码|object||
|&emsp;&emsp;beVisitGroupId|访问部门id|object||
|&emsp;&emsp;beVisitGroupName|访问部门名称|object||
|&emsp;&emsp;beVisitOrgPathName|访问部门全路径名称,前台展示全路径部门信息|object||
|&emsp;&emsp;beVisitPersonId|被访人ID|object||
|&emsp;&emsp;beVisitPersonName|被访人名称|object||
|&emsp;&emsp;beVisitPhoneNum|被访人手机号|object||
|&emsp;&emsp;birthplace|籍贯|object||
|&emsp;&emsp;carNumber|车牌号|object||
|&emsp;&emsp;certAddr|证件地址|object||
|&emsp;&emsp;certIssuer|发证机关|object||
|&emsp;&emsp;certifyFlag||string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;customf|自定义字段f|object||
|&emsp;&emsp;customg|自定义字段g|object||
|&emsp;&emsp;customh|自定义字段h|object||
|&emsp;&emsp;customi|自定义字段i|object||
|&emsp;&emsp;customj|自定义字段j|object||
|&emsp;&emsp;endTime|预计离开时间|string(date-time)||
|&emsp;&emsp;endTimeDifference|预计离开时间时差|object||
|&emsp;&emsp;endTimeISO|预计离开ISO时间|object||
|&emsp;&emsp;endTimeUTC|预计离开UTC时间|object||
|&emsp;&emsp;followFlag||integer(int32)||
|&emsp;&emsp;groupId|访客组Id|object||
|&emsp;&emsp;identityId|证件类型：111身份证，335驾驶证，131工作证，133学生证，114军官证，414护照，990其他|object||
|&emsp;&emsp;identityNum|证件号码|object||
|&emsp;&emsp;identityPhoto|证件照片|object||
|&emsp;&emsp;identityPid|身份证序列号|object||
|&emsp;&emsp;name|访客姓名|object||
|&emsp;&emsp;orderId|访客单ID|object||
|&emsp;&emsp;personNum|来访人数|object||
|&emsp;&emsp;phoneNum|手机号|object||
|&emsp;&emsp;pinyin|访客拼音|object||
|&emsp;&emsp;privilegeGroupIds|当前访客单权限组ids|object||
|&emsp;&emsp;purpose|来访事由|object||
|&emsp;&emsp;qrCode|访客单中的二维码|object||
|&emsp;&emsp;realEndTime|签离时间|string(date-time)||
|&emsp;&emsp;realEndTimeDifference|签离时间时间时差|object||
|&emsp;&emsp;realEndTimeISO|签离ISO时间|object||
|&emsp;&emsp;realEndTimeUTC|签离UTC时间|object||
|&emsp;&emsp;registerFlag|是否可提前登记标识|object||
|&emsp;&emsp;registerPlace||string||
|&emsp;&emsp;registerTime|登记时间|string(date-time)||
|&emsp;&emsp;registerTimeDifference|登记时间时差|object||
|&emsp;&emsp;registerTimeISO|登记ISO时间|object||
|&emsp;&emsp;registerTimeUTC|登记UTC时间|object||
|&emsp;&emsp;scanningPhoto|证件扫描照片|object||
|&emsp;&emsp;sex|性别:1男,2女|object||
|&emsp;&emsp;startTime|预计来访时间|string(date-time)||
|&emsp;&emsp;startTimeDifference|预计来访时间时差|object||
|&emsp;&emsp;startTimeISO|预计来访ISO时间|object||
|&emsp;&emsp;startTimeUTC|预计来访UTC时间|object||
|&emsp;&emsp;status|访客状态 ：0:审批中、1：正常、2：迟到、 3：超时 7：超期未签离、8：已到达|object||
|&emsp;&emsp;tempCard|访客卡号|object||
|&emsp;&emsp;temperatureStatus||integer(int32)||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||
|&emsp;&emsp;userType|创建者身份类型：1-平台用户，2-内部人员，3-来访人员|object||
|&emsp;&emsp;visitBatch|访客批次|object||
|&emsp;&emsp;visitorAddress|访客住址|object||
|&emsp;&emsp;visitorAllowTimes|访客进入次数|object||
|&emsp;&emsp;visitorCode|访客验证码|object||
|&emsp;&emsp;visitorId|访客Id|object||
|&emsp;&emsp;visitorPhoto|访客头像|object||
|&emsp;&emsp;visitorTemperature||string||
|&emsp;&emsp;visitorTypeId|访客类型id|object||
|&emsp;&emsp;visitorTypeName|访客类型名称|object||
|&emsp;&emsp;visitorWorkUnit|访客来访单位|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"approvalResult": "审批通过",
		"barCode": "123456615",
		"beVisitGroupId": "ASDF454SDAF5656",
		"beVisitGroupName": "ASDF454SDAF5656",
		"beVisitOrgPathName": "123123sfsdfdf/ASDF454SDAF5656",
		"beVisitPersonId": "6546sdafse-we56adf",
		"beVisitPersonName": "小红",
		"beVisitPhoneNum": "15244445863",
		"birthplace": "杭州滨江",
		"carNumber": "浙A32216",
		"certAddr": "浙江省杭州市萧山区",
		"certIssuer": "杭州市公安局滨江分局",
		"certifyFlag": "",
		"createTime": "",
		"customf": "1253566554",
		"customg": "1253566554",
		"customh": "1253566554",
		"customi": "1253566554",
		"customj": "1253566554",
		"endTime": "",
		"endTimeDifference": "+08:00",
		"endTimeISO": "2018-10-29T16:33:07+08:00",
		"endTimeUTC": "2131231231231",
		"followFlag": 0,
		"groupId": "ASDF454SDAF5656",
		"identityId": "111",
		"identityNum": "32165165165161",
		"identityPhoto": "/visitor/1.jpg",
		"identityPid": "123456615",
		"name": "小红",
		"orderId": "6546sdafs56adf",
		"personNum": "1",
		"phoneNum": "1253566554",
		"pinyin": "xh",
		"privilegeGroupIds": "123123123,3434343434123123",
		"purpose": "参观",
		"qrCode": "casdvbdfhbtgdrt",
		"realEndTime": "",
		"realEndTimeDifference": "+08:00",
		"realEndTimeISO": "2018-10-29T16:33:07+08:00",
		"realEndTimeUTC": "2131231231231",
		"registerFlag": "1是可以 0 不可以",
		"registerPlace": "",
		"registerTime": "",
		"registerTimeDifference": "+08:00",
		"registerTimeISO": "2018-10-29T15:33:07+08:00",
		"registerTimeUTC": "2131231231231",
		"scanningPhoto": "http://...",
		"sex": "1",
		"startTime": "",
		"startTimeDifference": "+08:00",
		"startTimeISO": "2018-10-29T15:23:07+08:00",
		"startTimeUTC": "2131231231231",
		"status": "8",
		"tempCard": "123456615",
		"temperatureStatus": 0,
		"updateTime": "",
		"userType": "1",
		"visitBatch": "asdghasdgasd",
		"visitorAddress": "杭州滨江",
		"visitorAllowTimes": "0",
		"visitorCode": "1234",
		"visitorId": "ASDF454SDAF5656",
		"visitorPhoto": "/visitor/1.jpg",
		"visitorTemperature": "",
		"visitorTypeId": "访客所在公司",
		"visitorTypeName": "访客所在公司",
		"visitorWorkUnit": "某个公司"
	},
	"msg": "success"
}
```


## 根据员工卡获取员工信息


**接口地址**:`/webapi/visitorcs/api/v1/clientService/person`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>根据员工卡获取员工信息</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|cardNo|员工卡号|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PersonInfo»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PersonInfo|PersonInfo|
|&emsp;&emsp;name|姓名|object||
|&emsp;&emsp;orgPathName|组织全路径名称|object||
|&emsp;&emsp;organizationId|部门组织id|object||
|&emsp;&emsp;organizationName|部门名称|object||
|&emsp;&emsp;personId|员工ID|object||
|&emsp;&emsp;phone|员工手机号码|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"name": "无双",
		"orgPathName": "12/33/44/556/1231233-dfsdf34-ryty0",
		"organizationId": "22223221231231232",
		"organizationName": "一卡通",
		"personId": "6546sdafs56adf",
		"phone": "13325714545"
	},
	"msg": "success"
}
```


## 根据被访人id和组织查询被访人人脸信息


**接口地址**:`/webapi/visitorcs/api/v1/clientService/personFace/query`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>根据被访人id和组织查询被访人人脸信息，如果存在人脸信息，返回图片流</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|orgIndexCode|被访人所属组织code|query|false|string||
|personId|被访人id|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PersonFaceInfo»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PersonFaceInfo|PersonFaceInfo|
|&emsp;&emsp;faceUrl|员工人脸图片完整url链接|object||
|&emsp;&emsp;name|姓名|object||
|&emsp;&emsp;orgPathName|组织全路径名称|object||
|&emsp;&emsp;organizationId|部门组织id|object||
|&emsp;&emsp;organizationName|部门名称|object||
|&emsp;&emsp;personId|员工ID|object||
|&emsp;&emsp;phone|员工手机号码|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"faceUrl": "http://pic.....",
		"name": "无双",
		"orgPathName": "12/33/44/556/1231233-dfsdf34-ryty0",
		"organizationId": "22223221231231232",
		"organizationName": "一卡通",
		"personId": "6546sdafs56adf",
		"phone": "13325714545"
	},
	"msg": "success"
}
```


## 根据姓名和手机号模糊搜索被访人


**接口地址**:`/webapi/visitorcs/api/v1/clientService/personInfo/query`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>根据姓名和手机号模糊搜索被访人,最多返回200人</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|queryInfo|姓名或者手机号,不填写返回空集合|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«Map«string,List«PersonInfo»»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PersonInfo|PersonInfo|
|&emsp;&emsp;name|姓名|object||
|&emsp;&emsp;orgPathName|组织全路径名称|object||
|&emsp;&emsp;organizationId|部门组织id|object||
|&emsp;&emsp;organizationName|部门名称|object||
|&emsp;&emsp;personId|员工ID|object||
|&emsp;&emsp;phone|员工手机号码|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"additionalProperties1": {
			"name": "无双",
			"orgPathName": "12/33/44/556/1231233-dfsdf34-ryty0",
			"organizationId": "22223221231231232",
			"organizationName": "一卡通",
			"personId": "6546sdafs56adf",
			"phone": "13325714545"
		}
	},
	"msg": "success"
}
```


## 获取访客单打印模板


**接口地址**:`/webapi/visitorcs/api/v1/clientService/phConfig/info`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>获取访客单打印模板</p>



**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PhConfigWebResponse»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PhConfigWebResponse|PhConfigWebResponse|
|&emsp;&emsp;backPicName|通行证的背景图名称|string||
|&emsp;&emsp;backPicUrl|通行证的背景图片|string||
|&emsp;&emsp;configStatus|通行证的配置开启或者关闭状态 open:开启 close:关闭(默认)|string||
|&emsp;&emsp;endContent|通行证的末尾内容|string||
|&emsp;&emsp;phConfigId|通行证的配置id|string||
|&emsp;&emsp;phItems|通行证的内容选项集合|array|PhItem|
|&emsp;&emsp;&emsp;&emsp;format|格式:比如时间的格式 yyyy-MM-dd / yyyy-MM-dd HH:mm:ss /yyyy年MM月dd日|string||
|&emsp;&emsp;&emsp;&emsp;key|入园通行证的key值 头像：visitorPhoto  姓名：visitorName  手机号码: visitorPhoneNum  车牌号 ：visitorCarNumber  证件号码：visitorIdentityNum  来访事由：visitorPurpose  来访单位：visitorWorkUnit   被访对象的姓名：beVisitorPersonName 被访对象的组织：beVisitorGroupName  被访对象的手机号码：beVisitorPhoneNum 有效期的开始时间：startTime 有效期的结束时间：endTime 审批状态：approvalResult  登记时间: registerTime   二维码：authBarCode 分割线:separator  空行:blankLine |string||
|&emsp;&emsp;&emsp;&emsp;name|通行证选项对应的名称:比如姓名/手机号码;二维码、头像、分割线、空行的name不存在的|string||
|&emsp;&emsp;&emsp;&emsp;value|通行证选项对应的值:比如姓名对应的值|string||
|&emsp;&emsp;productCode|产品编号|string||
|&emsp;&emsp;projectId|项目id|string||
|&emsp;&emsp;title|通行证的标题|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"backPicName": "通行证",
		"backPicUrl": "http://7412f756-1625137475555876-face.oss-cn-hangzhou.aliyuncs.com/photo/783210920129584.jpg",
		"configStatus": "close",
		"endContent": "欢迎来到烟台工程职业技术学院",
		"phConfigId": "5d5f434c4543accda02680b600afe6b3",
		"phItems": "[]",
		"productCode": "1625137405416832",
		"projectId": "1805308421418544",
		"title": "高职学院的入园通行证"
	},
	"msg": "success"
}
```


## 获取访客权限组


**接口地址**:`/webapi/visitorcs/api/v1/clientService/privilegeGroup`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>返回默认权限组和具有所有权限项区域权限的权限组，包括空的权限组</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|pageNo|当前页|query|true|integer(int32)||
|pageSize|当前分页大小,限定大小不能超过1000,且记录起始数必须小于2147483647|query|true|integer(int32)||
|name|访客权限组名|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PageResult«PrivilegeGroup»»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PageResult«PrivilegeGroup»|PageResult«PrivilegeGroup»|
|&emsp;&emsp;list|数据信息|array|PrivilegeGroup|
|&emsp;&emsp;&emsp;&emsp;isDefault|是否是默认拜访区域，0-是，1-否|object||
|&emsp;&emsp;&emsp;&emsp;privilegeGroupId|拜访区域ID|object||
|&emsp;&emsp;&emsp;&emsp;privilegeGroupName|拜访区域名称|object||
|&emsp;&emsp;&emsp;&emsp;remark|描述|object||
|&emsp;&emsp;pageNo|页码|integer(int32)||
|&emsp;&emsp;pageSize|页大小|integer(int32)||
|&emsp;&emsp;total|总条数|integer(int64)||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"list": [
			{
				"isDefault": "1",
				"privilegeGroupId": "731bb582-fc49-11e7-83de-2ffbc13dcaba",
				"privilegeGroupName": "访客基本权限组",
				"remark": "访客仅可进入大厅区域"
			}
		],
		"pageNo": 1,
		"pageSize": 20,
		"total": 5
	},
	"msg": "success"
}
```


## 获取来访事由


**接口地址**:`/webapi/visitorcs/api/v1/clientService/purpose`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>获取访客来访事由</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|pageNo|当前页数|query|true|integer(int32)||
|pageSize|页面大小,限定大小不能超过1000,且记录起始数必须小于2147483647|query|true|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PageResult«PurposeResponse»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PageResult«PurposeResponse»|PageResult«PurposeResponse»|
|&emsp;&emsp;list|数据信息|array|PurposeResponse|
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;disorder|更新顺序|integer||
|&emsp;&emsp;&emsp;&emsp;productId|产品编号|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目编号|string||
|&emsp;&emsp;&emsp;&emsp;purposeDesc|事由描述|string||
|&emsp;&emsp;&emsp;&emsp;purposeId|事由ID|string||
|&emsp;&emsp;&emsp;&emsp;status|事由状态：0正常 -1已删除|integer||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;pageNo|页码|integer(int32)||
|&emsp;&emsp;pageSize|页大小|integer(int32)||
|&emsp;&emsp;total|总条数|integer(int64)||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"list": [
			{
				"createTime": "2021-07-01 12:00:00",
				"disorder": 123,
				"productId": "bbb",
				"projectId": "aaa",
				"purposeDesc": "拜访",
				"purposeId": "ccc",
				"status": 0,
				"updateTime": "2021-07-11 12:00:00"
			}
		],
		"pageNo": 1,
		"pageSize": 20,
		"total": 5
	},
	"msg": "success"
}
```


## 添加来访事由


**接口地址**:`/webapi/visitorcs/api/v1/clientService/purpose/add`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>添加来访事由信息</p>



**请求示例**:


```javascript
{
  "createTime": "2015-05-18 15:00:00",
  "purposeDesc": "参观",
  "purposeId": "sjdfosias021934"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|purpose|来访事由对象DTO|body|true|Purpose|Purpose|
|&emsp;&emsp;createTime|查询记录创建结束时间||false|object||
|&emsp;&emsp;purposeDesc|来访事由名称||true|object||
|&emsp;&emsp;purposeId|来访事由Id||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 访客权限修改


**接口地址**:`/webapi/visitorcs/api/v1/clientService/register/edit`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>修改已登记访客权限</p>



**请求示例**:


```javascript
{
  "endTimeISO": "2018-10-29T15:33:07+08:00",
  "orderId": "6546sdafs56adf",
  "privilegeGroupIds": {},
  "registerPlace": "XX访客机"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|privilegeEditInfo|权限变更入参对象模型DTO|body|true|PrivilegeEditInfo|PrivilegeEditInfo|
|&emsp;&emsp;endTimeISO|预计离开时间||true|object||
|&emsp;&emsp;orderId|访客单ID||true|object||
|&emsp;&emsp;privilegeGroupIds|权限组数组||false|object||
|&emsp;&emsp;registerPlace|访客登记地点||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 添加来访单位


**接口地址**:`/webapi/visitorcs/api/v1/clientService/save`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>添加来访单位信息</p>



**请求示例**:


```javascript
{
  "createTime": "2020-10-18 15:00:00",
  "unitDesc": "参观",
  "unitId": "sjdfosias021934"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|unit|来访单位对象DTO|body|true|Unit|Unit|
|&emsp;&emsp;createTime|创建时间||false|object||
|&emsp;&emsp;unitDesc|来访单位名称||true|object||
|&emsp;&emsp;unitId|来访单位Id||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 访客app图片上传接口


**接口地址**:`/webapi/visitorcs/api/v1/clientService/savePicForApp`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>返回上传后图片地址及照片质量信息</p>



**请求示例**:


```javascript
{
  "checkQuality": "1",
  "picData": "9dd351ia3-e*8634503d1165m3ep=t=i1p*i=d1s*i=d3b*i8da0*c74818542-9445fb--0874a79z189s=7ie4="
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|uploadPicturesParam|访客app图片上传接口入参对象|body|true|UploadPicturesParam|UploadPicturesParam|
|&emsp;&emsp;checkQuality|是否校验图片质量：1不校验，其他校验（目前上传证件照时用1）||true|string||
|&emsp;&emsp;picData|加密后的图片Base64编码字节流,图片最大200K，仅支持jpg格式||true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«UploadPicturesResponse»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|UploadPicturesResponse|UploadPicturesResponse|
|&emsp;&emsp;faceId|人脸编号|string||
|&emsp;&emsp;faceUrl|图片地址|string||
|&emsp;&emsp;level|人脸质量级别(高>=80分，中>=70分 低>=60分 不合格<60)|string||
|&emsp;&emsp;score|人脸评分值|integer(int32)||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"faceId": "123456",
		"faceUrl": "https://www.sensoro.com/zh/img/intelligent/ai_business@2x.png",
		"level": "中",
		"score": 20
	},
	"msg": "success"
}
```


## 获取场景参数配置信息


**接口地址**:`/webapi/visitorcs/api/v1/clientService/sceneConfig`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>获取场景参数配置信息</p>



**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«Map«string,List«ParamConfigInfo»»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|ParamConfigInfo|ParamConfigInfo|
|&emsp;&emsp;content|参数值A|object||
|&emsp;&emsp;paramName|配置名称|object||
|&emsp;&emsp;subContent|参数值B|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"additionalProperties1": {
			"content": "json格式字符串",
			"paramName": "isSmsForVisitor",
			"subContent": "json格式字符串"
		}
	},
	"msg": "success"
}
```


## 签离


**接口地址**:`/webapi/visitorcs/api/v1/clientService/signOut`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>访客签离</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|orderId|访客预约单id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 获取当前被访人的有效访客记录


**接口地址**:`/webapi/visitorcs/api/v1/clientService/validVisitorInfo/pageInfo`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>获取当前被访人的有效访客记录，本接口支持访客自定义属性的返回，通过获取访客字段的配置信息接口获取平台已支持访客自定义属性的说明</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|pageNo|当前页数|query|true|integer(int32)||
|pageSize|分页大小，限定大小不能超过1000|query|true|integer(int32)||
|personId|被访人Id|query|true|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PageResult«SimpleVisitorInfo»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PageResult«SimpleVisitorInfo»|PageResult«SimpleVisitorInfo»|
|&emsp;&emsp;list|数据信息|array|SimpleVisitorInfo|
|&emsp;&emsp;&emsp;&emsp;barCode|访客二维码|object||
|&emsp;&emsp;&emsp;&emsp;beVisitPersonId|被访人ID|object||
|&emsp;&emsp;&emsp;&emsp;birthplace|籍贯|object||
|&emsp;&emsp;&emsp;&emsp;certAddr|证件地址|object||
|&emsp;&emsp;&emsp;&emsp;certIssuer|发证机关|object||
|&emsp;&emsp;&emsp;&emsp;endTimeISO|预计离开ISO时间|object||
|&emsp;&emsp;&emsp;&emsp;identityId|证件类型：111、身份证|object||
|&emsp;&emsp;&emsp;&emsp;identityNum|身份证号码|object||
|&emsp;&emsp;&emsp;&emsp;name|访客姓名|object||
|&emsp;&emsp;&emsp;&emsp;orderId|访客单ID|object||
|&emsp;&emsp;&emsp;&emsp;personNum|来访人数|object||
|&emsp;&emsp;&emsp;&emsp;phoneNum|手机号|object||
|&emsp;&emsp;&emsp;&emsp;privilegeGroupIds|当前访客单权限组ids|object||
|&emsp;&emsp;&emsp;&emsp;purpose|来访事由|object||
|&emsp;&emsp;&emsp;&emsp;registerPlace|访客登记地点|object||
|&emsp;&emsp;&emsp;&emsp;registerTimeISO|登记ISO时间|object||
|&emsp;&emsp;&emsp;&emsp;scanningPhoto|证件扫描照片|object||
|&emsp;&emsp;&emsp;&emsp;sex|性别:1男,2女|object||
|&emsp;&emsp;&emsp;&emsp;status|访客状态|object||
|&emsp;&emsp;&emsp;&emsp;temperatureStatus|访客体温状态：0：正常，1：异常|object||
|&emsp;&emsp;&emsp;&emsp;visitorAddress|访客住址|object||
|&emsp;&emsp;&emsp;&emsp;visitorAllowTimes|访客进入次数|object||
|&emsp;&emsp;&emsp;&emsp;visitorTemperature|访客体温|object||
|&emsp;&emsp;&emsp;&emsp;visitorTypeId|访客类型id|object||
|&emsp;&emsp;pageNo|页码|integer(int32)||
|&emsp;&emsp;pageSize|页大小|integer(int32)||
|&emsp;&emsp;total|总条数|integer(int64)||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"list": [
			{
				"barCode": "123456615",
				"beVisitPersonId": "6546sdafse-we56adf",
				"birthplace": "杭州滨江",
				"certAddr": "浙江省杭州市萧山区",
				"certIssuer": "杭州市公安局滨江分局",
				"endTimeISO": "2018-10-29T16:33:07+08:00",
				"identityId": "111",
				"identityNum": "32165165165161",
				"name": "小红",
				"orderId": "6546sdafs56adf",
				"personNum": "1",
				"phoneNum": "1253566554",
				"privilegeGroupIds": "123123123,3434343434123123",
				"purpose": "参观",
				"registerPlace": "1253566554",
				"registerTimeISO": "2018-10-29T15:33:07+08:00",
				"scanningPhoto": "http://...",
				"sex": "1",
				"status": "8",
				"temperatureStatus": "0",
				"visitorAddress": "杭州滨江",
				"visitorAllowTimes": "0",
				"visitorTemperature": "36.5",
				"visitorTypeId": "访客所在公司"
			}
		],
		"pageNo": 1,
		"pageSize": 20,
		"total": 5
	},
	"msg": "success"
}
```


## 获取访客详情


**接口地址**:`/webapi/visitorcs/api/v1/clientService/visitor/details`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>获取访客详情,支持加密二维码</p>



**请求示例**:


```javascript
{
  "code": "8888",
  "codeType": "2",
  "macAddress": "1",
  "statusList": "0",
  "subParamCode": "111",
  "type": "1"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|visitorClientQueryDto|客户端查询访客详情封装对象|body|true|VisitorClientQueryDto|VisitorClientQueryDto|
|&emsp;&emsp;code|不同查询类型对应的值||false|object||
|&emsp;&emsp;codeType|查询类型：0-预约单号，1-预约码，2-手机号后四位，3-二维码，4-访客卡，5-证件号码，6-车牌号码||false|object||
|&emsp;&emsp;macAddress|机器的mac地址||false|object||
|&emsp;&emsp;statusList|预约状态的集合，审批中：0:审批中、1：正常、2：迟到、3：失效、4：已退回、5：超期自动签离、6：已签离、7：超期未签离、8：已到达||false|object||
|&emsp;&emsp;subParamCode|查询类型为5时，对应的证件类型值||false|object||
|&emsp;&emsp;type|查询记录的类型 1:被访人模式(可以不传，默认是1) 2:机器模式||false|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«Map«string,List«VisitorInfo»»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|VisitorInfo|VisitorInfo|
|&emsp;&emsp;approvalResult|访客单中的审批状态|object||
|&emsp;&emsp;barCode|访客二维码|object||
|&emsp;&emsp;beVisitGroupId|访问部门id|object||
|&emsp;&emsp;beVisitGroupName|访问部门名称|object||
|&emsp;&emsp;beVisitOrgPathName|访问部门全路径名称,前台展示全路径部门信息|object||
|&emsp;&emsp;beVisitPersonId|被访人ID|object||
|&emsp;&emsp;beVisitPersonName|被访人名称|object||
|&emsp;&emsp;beVisitPhoneNum|被访人手机号|object||
|&emsp;&emsp;birthplace|籍贯|object||
|&emsp;&emsp;carNumber|车牌号|object||
|&emsp;&emsp;certAddr|证件地址|object||
|&emsp;&emsp;certIssuer|发证机关|object||
|&emsp;&emsp;certifyFlag||string||
|&emsp;&emsp;createTime|创建时间|string(date-time)||
|&emsp;&emsp;customf|自定义字段f|object||
|&emsp;&emsp;customg|自定义字段g|object||
|&emsp;&emsp;customh|自定义字段h|object||
|&emsp;&emsp;customi|自定义字段i|object||
|&emsp;&emsp;customj|自定义字段j|object||
|&emsp;&emsp;endTime|预计离开时间|string(date-time)||
|&emsp;&emsp;endTimeDifference|预计离开时间时差|object||
|&emsp;&emsp;endTimeISO|预计离开ISO时间|object||
|&emsp;&emsp;endTimeUTC|预计离开UTC时间|object||
|&emsp;&emsp;followFlag||integer(int32)||
|&emsp;&emsp;groupId|访客组Id|object||
|&emsp;&emsp;identityId|证件类型：111身份证，335驾驶证，131工作证，133学生证，114军官证，414护照，990其他|object||
|&emsp;&emsp;identityNum|证件号码|object||
|&emsp;&emsp;identityPhoto|证件照片|object||
|&emsp;&emsp;identityPid|身份证序列号|object||
|&emsp;&emsp;name|访客姓名|object||
|&emsp;&emsp;orderId|访客单ID|object||
|&emsp;&emsp;personNum|来访人数|object||
|&emsp;&emsp;phoneNum|手机号|object||
|&emsp;&emsp;pinyin|访客拼音|object||
|&emsp;&emsp;privilegeGroupIds|当前访客单权限组ids|object||
|&emsp;&emsp;purpose|来访事由|object||
|&emsp;&emsp;qrCode|访客单中的二维码|object||
|&emsp;&emsp;realEndTime|签离时间|string(date-time)||
|&emsp;&emsp;realEndTimeDifference|签离时间时间时差|object||
|&emsp;&emsp;realEndTimeISO|签离ISO时间|object||
|&emsp;&emsp;realEndTimeUTC|签离UTC时间|object||
|&emsp;&emsp;registerFlag|是否可提前登记标识|object||
|&emsp;&emsp;registerPlace||string||
|&emsp;&emsp;registerTime|登记时间|string(date-time)||
|&emsp;&emsp;registerTimeDifference|登记时间时差|object||
|&emsp;&emsp;registerTimeISO|登记ISO时间|object||
|&emsp;&emsp;registerTimeUTC|登记UTC时间|object||
|&emsp;&emsp;scanningPhoto|证件扫描照片|object||
|&emsp;&emsp;sex|性别:1男,2女|object||
|&emsp;&emsp;startTime|预计来访时间|string(date-time)||
|&emsp;&emsp;startTimeDifference|预计来访时间时差|object||
|&emsp;&emsp;startTimeISO|预计来访ISO时间|object||
|&emsp;&emsp;startTimeUTC|预计来访UTC时间|object||
|&emsp;&emsp;status|访客状态 ：0:审批中、1：正常、2：迟到、 3：超时 7：超期未签离、8：已到达|object||
|&emsp;&emsp;tempCard|访客卡号|object||
|&emsp;&emsp;temperatureStatus||integer(int32)||
|&emsp;&emsp;updateTime|更新时间|string(date-time)||
|&emsp;&emsp;userType|创建者身份类型：1-平台用户，2-内部人员，3-来访人员|object||
|&emsp;&emsp;visitBatch|访客批次|object||
|&emsp;&emsp;visitorAddress|访客住址|object||
|&emsp;&emsp;visitorAllowTimes|访客进入次数|object||
|&emsp;&emsp;visitorCode|访客验证码|object||
|&emsp;&emsp;visitorId|访客Id|object||
|&emsp;&emsp;visitorPhoto|访客头像|object||
|&emsp;&emsp;visitorTemperature||string||
|&emsp;&emsp;visitorTypeId|访客类型id|object||
|&emsp;&emsp;visitorTypeName|访客类型名称|object||
|&emsp;&emsp;visitorWorkUnit|访客来访单位|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"additionalProperties1": {
			"approvalResult": "审批通过",
			"barCode": "123456615",
			"beVisitGroupId": "ASDF454SDAF5656",
			"beVisitGroupName": "ASDF454SDAF5656",
			"beVisitOrgPathName": "123123sfsdfdf/ASDF454SDAF5656",
			"beVisitPersonId": "6546sdafse-we56adf",
			"beVisitPersonName": "小红",
			"beVisitPhoneNum": "15244445863",
			"birthplace": "杭州滨江",
			"carNumber": "浙A32216",
			"certAddr": "浙江省杭州市萧山区",
			"certIssuer": "杭州市公安局滨江分局",
			"certifyFlag": "",
			"createTime": "",
			"customf": "1253566554",
			"customg": "1253566554",
			"customh": "1253566554",
			"customi": "1253566554",
			"customj": "1253566554",
			"endTime": "",
			"endTimeDifference": "+08:00",
			"endTimeISO": "2018-10-29T16:33:07+08:00",
			"endTimeUTC": "2131231231231",
			"followFlag": 0,
			"groupId": "ASDF454SDAF5656",
			"identityId": "111",
			"identityNum": "32165165165161",
			"identityPhoto": "/visitor/1.jpg",
			"identityPid": "123456615",
			"name": "小红",
			"orderId": "6546sdafs56adf",
			"personNum": "1",
			"phoneNum": "1253566554",
			"pinyin": "xh",
			"privilegeGroupIds": "123123123,3434343434123123",
			"purpose": "参观",
			"qrCode": "casdvbdfhbtgdrt",
			"realEndTime": "",
			"realEndTimeDifference": "+08:00",
			"realEndTimeISO": "2018-10-29T16:33:07+08:00",
			"realEndTimeUTC": "2131231231231",
			"registerFlag": "1是可以 0 不可以",
			"registerPlace": "",
			"registerTime": "",
			"registerTimeDifference": "+08:00",
			"registerTimeISO": "2018-10-29T15:33:07+08:00",
			"registerTimeUTC": "2131231231231",
			"scanningPhoto": "http://...",
			"sex": "1",
			"startTime": "",
			"startTimeDifference": "+08:00",
			"startTimeISO": "2018-10-29T15:23:07+08:00",
			"startTimeUTC": "2131231231231",
			"status": "8",
			"tempCard": "123456615",
			"temperatureStatus": 0,
			"updateTime": "",
			"userType": "1",
			"visitBatch": "asdghasdgasd",
			"visitorAddress": "杭州滨江",
			"visitorAllowTimes": "0",
			"visitorCode": "1234",
			"visitorId": "ASDF454SDAF5656",
			"visitorPhoto": "/visitor/1.jpg",
			"visitorTemperature": "",
			"visitorTypeId": "访客所在公司",
			"visitorTypeName": "访客所在公司",
			"visitorWorkUnit": "某个公司"
		}
	},
	"msg": "success"
}
```


## 添加自定义枚举字段选项


**接口地址**:`/webapi/visitorcs/api/v1/clientService/visitorField/edition`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>添加自定义枚举字段选项值</p>



**请求示例**:


```javascript
{
  "optionList": "[\"贵宾\",\"VIP\"]",
  "paraId": "1233"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|visitorSelfFieldInfoClient|客户端添加下拉框选项对象|body|true|VisitorSelfFieldInfoClient|VisitorSelfFieldInfoClient|
|&emsp;&emsp;optionList|添加的下拉框选项||true|object||
|&emsp;&emsp;paraId|修改的枚举字段编号||true|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


## 根据身份证号或者手机号查询访客属性


**接口地址**:`/webapi/visitorcs/api/v1/clientService/visitorGroup/judge`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>根据身份证号查询访客属性</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|identityId|证件类型|query|false|string||
|identityNum|证件号码|query|false|string||
|phoneNum|手机号码|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«VisitorGroupRelInfo»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|VisitorGroupRelInfo|VisitorGroupRelInfo|
|&emsp;&emsp;identityId|证件类型:111身份证，335驾驶证，131工作证，133学生证，114军官证，414护照，990其他|object||
|&emsp;&emsp;identityNum|证件号码|object||
|&emsp;&emsp;isRefuseRegister|人员类型，0普通1黑名单人员|object||
|&emsp;&emsp;name|访客人员姓名|object||
|&emsp;&emsp;phoneNum|手机号|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"identityId": "111",
		"identityNum": "465465116845",
		"isRefuseRegister": "0",
		"name": "小红",
		"phoneNum": "18100199863"
	},
	"msg": "success"
}
```


## 分页展示访客信息


**接口地址**:`/webapi/visitorcs/api/v1/clientService/visitorInfo`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>支持按访客姓名拼音或手机号搜索,只展示当天的记录,本接口支持访客自定义属性的返回，通过获取访客字段的配置信息接口获取平台已支持访客自定义属性的说明。</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|pageNo|当前页|query|true|integer(int32)||
|pageSize|当前分页大小,限定大小不能超过1000,且记录起始数必须小于2147483647|query|true|integer(int32)||
|visitType|visitType值有四种,total,visiting,unRegister, signOut|query|true|string||
|macAddress|macAddress 访客机的mac地址|query|false|string||
|queryInfo|分页展示访客信息,支持按访客姓名拼音或手机号搜索|query|false|string||
|type|type 1:被访人模式(可以不传，默认是1) 2:机器模式|query|false|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PageResult«VisitorInfo»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PageResult«VisitorInfo»|PageResult«VisitorInfo»|
|&emsp;&emsp;list|数据信息|array|VisitorInfo|
|&emsp;&emsp;&emsp;&emsp;approvalResult|访客单中的审批状态|object||
|&emsp;&emsp;&emsp;&emsp;barCode|访客二维码|object||
|&emsp;&emsp;&emsp;&emsp;beVisitGroupId|访问部门id|object||
|&emsp;&emsp;&emsp;&emsp;beVisitGroupName|访问部门名称|object||
|&emsp;&emsp;&emsp;&emsp;beVisitOrgPathName|访问部门全路径名称,前台展示全路径部门信息|object||
|&emsp;&emsp;&emsp;&emsp;beVisitPersonId|被访人ID|object||
|&emsp;&emsp;&emsp;&emsp;beVisitPersonName|被访人名称|object||
|&emsp;&emsp;&emsp;&emsp;beVisitPhoneNum|被访人手机号|object||
|&emsp;&emsp;&emsp;&emsp;birthplace|籍贯|object||
|&emsp;&emsp;&emsp;&emsp;carNumber|车牌号|object||
|&emsp;&emsp;&emsp;&emsp;certAddr|证件地址|object||
|&emsp;&emsp;&emsp;&emsp;certIssuer|发证机关|object||
|&emsp;&emsp;&emsp;&emsp;certifyFlag||string||
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;customf|自定义字段f|object||
|&emsp;&emsp;&emsp;&emsp;customg|自定义字段g|object||
|&emsp;&emsp;&emsp;&emsp;customh|自定义字段h|object||
|&emsp;&emsp;&emsp;&emsp;customi|自定义字段i|object||
|&emsp;&emsp;&emsp;&emsp;customj|自定义字段j|object||
|&emsp;&emsp;&emsp;&emsp;endTime|预计离开时间|string||
|&emsp;&emsp;&emsp;&emsp;endTimeDifference|预计离开时间时差|object||
|&emsp;&emsp;&emsp;&emsp;endTimeISO|预计离开ISO时间|object||
|&emsp;&emsp;&emsp;&emsp;endTimeUTC|预计离开UTC时间|object||
|&emsp;&emsp;&emsp;&emsp;followFlag||integer||
|&emsp;&emsp;&emsp;&emsp;groupId|访客组Id|object||
|&emsp;&emsp;&emsp;&emsp;identityId|证件类型：111身份证，335驾驶证，131工作证，133学生证，114军官证，414护照，990其他|object||
|&emsp;&emsp;&emsp;&emsp;identityNum|证件号码|object||
|&emsp;&emsp;&emsp;&emsp;identityPhoto|证件照片|object||
|&emsp;&emsp;&emsp;&emsp;identityPid|身份证序列号|object||
|&emsp;&emsp;&emsp;&emsp;name|访客姓名|object||
|&emsp;&emsp;&emsp;&emsp;orderId|访客单ID|object||
|&emsp;&emsp;&emsp;&emsp;personNum|来访人数|object||
|&emsp;&emsp;&emsp;&emsp;phoneNum|手机号|object||
|&emsp;&emsp;&emsp;&emsp;pinyin|访客拼音|object||
|&emsp;&emsp;&emsp;&emsp;privilegeGroupIds|当前访客单权限组ids|object||
|&emsp;&emsp;&emsp;&emsp;purpose|来访事由|object||
|&emsp;&emsp;&emsp;&emsp;qrCode|访客单中的二维码|object||
|&emsp;&emsp;&emsp;&emsp;realEndTime|签离时间|string||
|&emsp;&emsp;&emsp;&emsp;realEndTimeDifference|签离时间时间时差|object||
|&emsp;&emsp;&emsp;&emsp;realEndTimeISO|签离ISO时间|object||
|&emsp;&emsp;&emsp;&emsp;realEndTimeUTC|签离UTC时间|object||
|&emsp;&emsp;&emsp;&emsp;registerFlag|是否可提前登记标识|object||
|&emsp;&emsp;&emsp;&emsp;registerPlace||string||
|&emsp;&emsp;&emsp;&emsp;registerTime|登记时间|string||
|&emsp;&emsp;&emsp;&emsp;registerTimeDifference|登记时间时差|object||
|&emsp;&emsp;&emsp;&emsp;registerTimeISO|登记ISO时间|object||
|&emsp;&emsp;&emsp;&emsp;registerTimeUTC|登记UTC时间|object||
|&emsp;&emsp;&emsp;&emsp;scanningPhoto|证件扫描照片|object||
|&emsp;&emsp;&emsp;&emsp;sex|性别:1男,2女|object||
|&emsp;&emsp;&emsp;&emsp;startTime|预计来访时间|string||
|&emsp;&emsp;&emsp;&emsp;startTimeDifference|预计来访时间时差|object||
|&emsp;&emsp;&emsp;&emsp;startTimeISO|预计来访ISO时间|object||
|&emsp;&emsp;&emsp;&emsp;startTimeUTC|预计来访UTC时间|object||
|&emsp;&emsp;&emsp;&emsp;status|访客状态 ：0:审批中、1：正常、2：迟到、 3：超时 7：超期未签离、8：已到达|object||
|&emsp;&emsp;&emsp;&emsp;tempCard|访客卡号|object||
|&emsp;&emsp;&emsp;&emsp;temperatureStatus||integer||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;&emsp;&emsp;userType|创建者身份类型：1-平台用户，2-内部人员，3-来访人员|object||
|&emsp;&emsp;&emsp;&emsp;visitBatch|访客批次|object||
|&emsp;&emsp;&emsp;&emsp;visitorAddress|访客住址|object||
|&emsp;&emsp;&emsp;&emsp;visitorAllowTimes|访客进入次数|object||
|&emsp;&emsp;&emsp;&emsp;visitorCode|访客验证码|object||
|&emsp;&emsp;&emsp;&emsp;visitorId|访客Id|object||
|&emsp;&emsp;&emsp;&emsp;visitorPhoto|访客头像|object||
|&emsp;&emsp;&emsp;&emsp;visitorTemperature||string||
|&emsp;&emsp;&emsp;&emsp;visitorTypeId|访客类型id|object||
|&emsp;&emsp;&emsp;&emsp;visitorTypeName|访客类型名称|object||
|&emsp;&emsp;&emsp;&emsp;visitorWorkUnit|访客来访单位|object||
|&emsp;&emsp;pageNo|页码|integer(int32)||
|&emsp;&emsp;pageSize|页大小|integer(int32)||
|&emsp;&emsp;total|总条数|integer(int64)||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"list": [
			{
				"approvalResult": "审批通过",
				"barCode": "123456615",
				"beVisitGroupId": "ASDF454SDAF5656",
				"beVisitGroupName": "ASDF454SDAF5656",
				"beVisitOrgPathName": "123123sfsdfdf/ASDF454SDAF5656",
				"beVisitPersonId": "6546sdafse-we56adf",
				"beVisitPersonName": "小红",
				"beVisitPhoneNum": "15244445863",
				"birthplace": "杭州滨江",
				"carNumber": "浙A32216",
				"certAddr": "浙江省杭州市萧山区",
				"certIssuer": "杭州市公安局滨江分局",
				"certifyFlag": "",
				"createTime": "",
				"customf": "1253566554",
				"customg": "1253566554",
				"customh": "1253566554",
				"customi": "1253566554",
				"customj": "1253566554",
				"endTime": "",
				"endTimeDifference": "+08:00",
				"endTimeISO": "2018-10-29T16:33:07+08:00",
				"endTimeUTC": "2131231231231",
				"followFlag": 0,
				"groupId": "ASDF454SDAF5656",
				"identityId": "111",
				"identityNum": "32165165165161",
				"identityPhoto": "/visitor/1.jpg",
				"identityPid": "123456615",
				"name": "小红",
				"orderId": "6546sdafs56adf",
				"personNum": "1",
				"phoneNum": "1253566554",
				"pinyin": "xh",
				"privilegeGroupIds": "123123123,3434343434123123",
				"purpose": "参观",
				"qrCode": "casdvbdfhbtgdrt",
				"realEndTime": "",
				"realEndTimeDifference": "+08:00",
				"realEndTimeISO": "2018-10-29T16:33:07+08:00",
				"realEndTimeUTC": "2131231231231",
				"registerFlag": "1是可以 0 不可以",
				"registerPlace": "",
				"registerTime": "",
				"registerTimeDifference": "+08:00",
				"registerTimeISO": "2018-10-29T15:33:07+08:00",
				"registerTimeUTC": "2131231231231",
				"scanningPhoto": "http://...",
				"sex": "1",
				"startTime": "",
				"startTimeDifference": "+08:00",
				"startTimeISO": "2018-10-29T15:23:07+08:00",
				"startTimeUTC": "2131231231231",
				"status": "8",
				"tempCard": "123456615",
				"temperatureStatus": 0,
				"updateTime": "",
				"userType": "1",
				"visitBatch": "asdghasdgasd",
				"visitorAddress": "杭州滨江",
				"visitorAllowTimes": "0",
				"visitorCode": "1234",
				"visitorId": "ASDF454SDAF5656",
				"visitorPhoto": "/visitor/1.jpg",
				"visitorTemperature": "",
				"visitorTypeId": "访客所在公司",
				"visitorTypeName": "访客所在公司",
				"visitorWorkUnit": "某个公司"
			}
		],
		"pageNo": 1,
		"pageSize": 20,
		"total": 5
	},
	"msg": "success"
}
```


## 获取访客字段的配置信息


**接口地址**:`/webapi/visitorcs/api/v1/clientService/visitorInfo/configuration`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>获取访客字段的配置信息</p>



**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«Map«string,List«VisitorFieldBaseDto»»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|VisitorFieldBaseDto|VisitorFieldBaseDto|
|&emsp;&emsp;dataValue|取值范围|array|object|
|&emsp;&emsp;disOrder|排列顺序|object||
|&emsp;&emsp;display|是否可见|object||
|&emsp;&emsp;fieldType|接口对应参数类型|object||
|&emsp;&emsp;paraId|参数id,唯一标识|object||
|&emsp;&emsp;paraKey|参数名多语言key|object||
|&emsp;&emsp;paraName|参数名|object||
|&emsp;&emsp;readOnly|是否禁止修改|object||
|&emsp;&emsp;regular|参数校验正则|object||
|&emsp;&emsp;required|是否必填|object||
|&emsp;&emsp;showType|参数类型 文本框-1、下拉框-2 时间框-3  图片-6|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"additionalProperties1": {
			"dataValue": "[{\"text\":\"男\",\"value\":1,\"selected\":true},{\"text\":\"女\",\"value\":2}]",
			"disOrder": "1",
			"display": "true",
			"fieldType": "String",
			"paraId": "1123esasd2d-12dda2e-wds12edwd",
			"paraKey": "paraKey",
			"paraName": "name",
			"readOnly": "true",
			"regular": "String",
			"required": "true",
			"showType": "1"
		}
	},
	"msg": "success"
}
```


## 获取来访单位


**接口地址**:`/webapi/visitorcs/api/v1/clientService/workUnit`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:<p>获取访客来访单位</p>



**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|pageNo|当前页数|query|true|integer(int32)||
|pageSize|页面大小,限定大小不能超过1000,且记录起始数必须小于2147483647|query|true|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«PageResult«WorkUnitResponse»»|
|201|Created||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|PageResult«WorkUnitResponse»|PageResult«WorkUnitResponse»|
|&emsp;&emsp;list|数据信息|array|WorkUnitResponse|
|&emsp;&emsp;&emsp;&emsp;createTime|创建时间|string||
|&emsp;&emsp;&emsp;&emsp;projectId|项目编号|string||
|&emsp;&emsp;&emsp;&emsp;unitDesc|访客单位描述|string||
|&emsp;&emsp;&emsp;&emsp;unitId|访客单位ID|string||
|&emsp;&emsp;&emsp;&emsp;updateTime|更新时间|string||
|&emsp;&emsp;pageNo|页码|integer(int32)||
|&emsp;&emsp;pageSize|页大小|integer(int32)||
|&emsp;&emsp;total|总条数|integer(int64)||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"list": [
			{
				"createTime": "2021-07-01 12:00:00",
				"projectId": "aaa",
				"unitDesc": "拜访",
				"unitId": "ccc",
				"updateTime": "2021-07-11 12:00:00"
			}
		],
		"pageNo": 1,
		"pageSize": 20,
		"total": 5
	},
	"msg": "success"
}
```


# 18_图片上传等


## 18_上传图片


**接口地址**:`/webapi/visitorcs/ui/v1/base/image/upload`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:<p>1.上传图片
发布版本：V1.0.0</p>



**请求示例**:


```javascript
{
  "imageData": "dgfrgrttr",
  "productId": "bbb",
  "projectId": "aaa",
  "type": "passback"
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|pictureRequest|PictureRequest|body|true|PictureRequest|PictureRequest|
|&emsp;&emsp;imageData|图片数据，base64编码(不含data:image/jpg;base64)||true|object||
|&emsp;&emsp;productId|产品编号||false|string||
|&emsp;&emsp;projectId|项目编号||false|string||
|&emsp;&emsp;type|visitor/diy：预约字段||true|object||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«AcscImageUploadResponse»|
|201|Created|ActionErrorResult|
|204|No Content||
|401|Unauthorized|ActionErrorResult|
|403|Forbidden|ActionErrorResult|
|404|Not Found|ActionErrorResult|


**响应状态码-200**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|AcscImageUploadResponse|AcscImageUploadResponse|
|&emsp;&emsp;faceId|人脸专用：人脸图片编号|string||
|&emsp;&emsp;faceLevel|人脸专用：人脸质量级别(高>=80分，中>=70分 低>=60分 不合格<60)|string||
|&emsp;&emsp;faceScore|人脸专用：人脸评分值|integer(int32)||
|&emsp;&emsp;imageUrl|图片地址|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {
		"faceId": "1179524873320912",
		"faceLevel": "中",
		"faceScore": 20,
		"imageUrl": "http://aliyun.com/image/122ssss.jpg"
	},
	"msg": "success"
}
```


**响应状态码-201**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-401**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-403**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


**响应状态码-404**:


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|错误码返回码|string||
|data|返回数据(具体接口返回信息结构)|object||
|msg|错误提示信息(记录接口执行情况说明信息)|string||


**响应示例**:
```javascript
{
	"code": "201",
	"data": {},
	"msg": "success"
}
```


# basic-error-controller


## error


**接口地址**:`/webapi/visitorcs/error`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## error


**接口地址**:`/webapi/visitorcs/error`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## error


**接口地址**:`/webapi/visitorcs/error`


**请求方式**:`PUT`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## error


**接口地址**:`/webapi/visitorcs/error`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## error


**接口地址**:`/webapi/visitorcs/error`


**请求方式**:`PATCH`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## error


**接口地址**:`/webapi/visitorcs/error`


**请求方式**:`OPTIONS`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## error


**接口地址**:`/webapi/visitorcs/error`


**请求方式**:`TRACE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## error


**接口地址**:`/webapi/visitorcs/error`


**请求方式**:`HEAD`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


暂无


**响应示例**:
```javascript

```


# eits-login-controller


## getChallengeCode


**接口地址**:`/webapi/visitorcs/eits/login/challengeCode`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "name": "",
  "productCode": "",
  "type": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|challengeRequestCodeDTO|ChallengeRequestCodeDTO|body|true|ChallengeRequestCodeDTO|ChallengeRequestCodeDTO|
|&emsp;&emsp;name|||false|string||
|&emsp;&emsp;productCode|||false|string||
|&emsp;&emsp;type|||true|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|Mono«object»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript
null
```


## changePwd


**接口地址**:`/webapi/visitorcs/eits/login/changePwd`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "codeId": "",
  "password": "",
  "productCode": "",
  "salt": "",
  "type": 0,
  "verifyCode": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|changePwdRequestDTO|ChangePwdRequestDTO|body|true|ChangePwdRequestDTO|ChangePwdRequestDTO|
|&emsp;&emsp;codeId|||false|string||
|&emsp;&emsp;password|||false|string||
|&emsp;&emsp;productCode|||false|string||
|&emsp;&emsp;salt|||false|string||
|&emsp;&emsp;type|||false|integer(int32)||
|&emsp;&emsp;verifyCode|||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|Mono«object»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript
null
```


## checkCode


**接口地址**:`/webapi/visitorcs/eits/login/phone/checkCode`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "code": "",
  "phone": "",
  "productCode": "",
  "type": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|checkPhoneCodeRequestDTO|CheckPhoneCodeRequestDTO|body|true|CheckPhoneCodeRequestDTO|CheckPhoneCodeRequestDTO|
|&emsp;&emsp;code|||false|string||
|&emsp;&emsp;phone|||false|string||
|&emsp;&emsp;productCode|||false|string||
|&emsp;&emsp;type|||true|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|Mono«object»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript
null
```


## phoneStatus


**接口地址**:`/webapi/visitorcs/eits/login/phone/status`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "phoneNo": "",
  "productCode": "",
  "type": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|phoneStatusRequestDTO|PhoneStatusRequestDTO|body|true|PhoneStatusRequestDTO|PhoneStatusRequestDTO|
|&emsp;&emsp;phoneNo|||false|string||
|&emsp;&emsp;productCode|||false|string||
|&emsp;&emsp;type|||false|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|Mono«object»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript
null
```


## phoneCode


**接口地址**:`/webapi/visitorcs/eits/login/phone/verifyCode`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "phone": "",
  "productCode": "",
  "type": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|phoneCodeRequestDTO|PhoneCodeRequestDTO|body|true|PhoneCodeRequestDTO|PhoneCodeRequestDTO|
|&emsp;&emsp;phone|||false|string||
|&emsp;&emsp;productCode|||false|string||
|&emsp;&emsp;type|||true|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|Mono«object»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript
null
```


## userCheckCode


**接口地址**:`/webapi/visitorcs/eits/login/user/phone/checkCode`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "codeId": "",
  "oldPwd": "",
  "phoneNo": "",
  "verifyCode": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|userPhoneCheckCodeRequestDTO|UserPhoneCheckCodeRequestDTO|body|true|UserPhoneCheckCodeRequestDTO|UserPhoneCheckCodeRequestDTO|
|&emsp;&emsp;codeId|||false|string||
|&emsp;&emsp;oldPwd|||false|string||
|&emsp;&emsp;phoneNo|||false|string||
|&emsp;&emsp;verifyCode|||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|Mono«object»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript
null
```


## userPhoneCode


**接口地址**:`/webapi/visitorcs/eits/login/user/phone/verifyCode`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "phoneNo": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|userPhoneCodeRequestDTO|UserPhoneCodeRequestDTO|body|true|UserPhoneCodeRequestDTO|UserPhoneCodeRequestDTO|
|&emsp;&emsp;phoneNo|||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|Mono«object»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript
null
```


## userChangePwd


**接口地址**:`/webapi/visitorcs/eits/login/user/pwd/update`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "codeId": "",
  "newPwd": "",
  "oldPwd": "",
  "salt": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|userChangePwdRequestDTO|UserChangePwdRequestDTO|body|true|UserChangePwdRequestDTO|UserChangePwdRequestDTO|
|&emsp;&emsp;codeId|||false|string||
|&emsp;&emsp;newPwd|||false|string||
|&emsp;&emsp;oldPwd|||false|string||
|&emsp;&emsp;salt|||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|Mono«object»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript
null
```


## verifyCode


**接口地址**:`/webapi/visitorcs/eits/login/verifyCode`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "name": "",
  "productCode": "",
  "type": 0
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|baseRequestDTO|BaseRequestDTO|body|true|BaseRequestDTO|BaseRequestDTO|
|&emsp;&emsp;name|||false|string||
|&emsp;&emsp;productCode|||false|string||
|&emsp;&emsp;type|||true|integer(int32)||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|Mono«object»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript
null
```


# eits-specical-login-controller


## save


**接口地址**:`/webapi/visitorcs/eits/login`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "codeId": "",
  "expired": 0,
  "name": "",
  "password": "",
  "productCode": "",
  "type": 0,
  "verifyCodeId": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|loginRequestDTO|LoginRequestDTO|body|true|LoginRequestDTO|LoginRequestDTO|
|&emsp;&emsp;codeId|||false|string||
|&emsp;&emsp;expired|||false|integer(int64)||
|&emsp;&emsp;name|||false|string||
|&emsp;&emsp;password|||false|string||
|&emsp;&emsp;productCode|||false|string||
|&emsp;&emsp;type|||true|integer(int32)||
|&emsp;&emsp;verifyCodeId|||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|Mono«object»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript
null
```


## logout


**接口地址**:`/webapi/visitorcs/eits/logout`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|Mono«object»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript
null
```


## test


**接口地址**:`/webapi/visitorcs/eits/test`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript

```


# hello-world


## helloWorld


**接口地址**:`/webapi/visitorcs/hello/world`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript

```


# k8s测试类


## health


**接口地址**:`/webapi/visitorcs/application/health`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«string»|
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": "",
	"msg": "success"
}
```


## health


**接口地址**:`/webapi/visitorcs/application/health`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«string»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": "",
	"msg": "success"
}
```


## health


**接口地址**:`/webapi/visitorcs/application/health`


**请求方式**:`PUT`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«string»|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": "",
	"msg": "success"
}
```


## health


**接口地址**:`/webapi/visitorcs/application/health`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«string»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": "",
	"msg": "success"
}
```


## health


**接口地址**:`/webapi/visitorcs/application/health`


**请求方式**:`PATCH`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«string»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": "",
	"msg": "success"
}
```


## health


**接口地址**:`/webapi/visitorcs/application/health`


**请求方式**:`OPTIONS`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«string»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": "",
	"msg": "success"
}
```


## health


**接口地址**:`/webapi/visitorcs/application/health`


**请求方式**:`TRACE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«string»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": "",
	"msg": "success"
}
```


## health


**接口地址**:`/webapi/visitorcs/application/health`


**请求方式**:`HEAD`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult«string»|
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|string||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": "",
	"msg": "success"
}
```


## getServiceDetail


**接口地址**:`/webapi/visitorcs/getServiceDetail`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|serviceName|serviceName|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## getServiceDetail


**接口地址**:`/webapi/visitorcs/getServiceDetail`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|serviceName|serviceName|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## getServiceDetail


**接口地址**:`/webapi/visitorcs/getServiceDetail`


**请求方式**:`PUT`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|serviceName|serviceName|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## getServiceDetail


**接口地址**:`/webapi/visitorcs/getServiceDetail`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|serviceName|serviceName|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## getServiceDetail


**接口地址**:`/webapi/visitorcs/getServiceDetail`


**请求方式**:`PATCH`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|serviceName|serviceName|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## getServiceDetail


**接口地址**:`/webapi/visitorcs/getServiceDetail`


**请求方式**:`OPTIONS`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|serviceName|serviceName|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## getServiceDetail


**接口地址**:`/webapi/visitorcs/getServiceDetail`


**请求方式**:`TRACE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|serviceName|serviceName|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## getServiceDetail


**接口地址**:`/webapi/visitorcs/getServiceDetail`


**请求方式**:`HEAD`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|serviceName|serviceName|query|false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## services


**接口地址**:`/webapi/visitorcs/services`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## services


**接口地址**:`/webapi/visitorcs/services`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## services


**接口地址**:`/webapi/visitorcs/services`


**请求方式**:`PUT`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## services


**接口地址**:`/webapi/visitorcs/services`


**请求方式**:`DELETE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## services


**接口地址**:`/webapi/visitorcs/services`


**请求方式**:`PATCH`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## services


**接口地址**:`/webapi/visitorcs/services`


**请求方式**:`OPTIONS`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## services


**接口地址**:`/webapi/visitorcs/services`


**请求方式**:`TRACE`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## services


**接口地址**:`/webapi/visitorcs/services`


**请求方式**:`HEAD`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|204|No Content||
|401|Unauthorized||
|403|Forbidden||


**响应参数**:


暂无


**响应示例**:
```javascript

```


# operation-handler


## handle


**接口地址**:`/webapi/visitorcs/actuator/health`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## handle


**接口地址**:`/webapi/visitorcs/actuator/health/**`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript

```


## handle


**接口地址**:`/webapi/visitorcs/actuator/prometheus`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript

```


# test


## cal


**接口地址**:`/webapi/visitorcs/ui/v1/test/cal`


**请求方式**:`POST`


**请求数据类型**:`application/x-www-form-urlencoded,application/json`


**响应数据类型**:`*/*`


**接口描述**:


**请求示例**:


```javascript
{
  "openId": "",
  "personId": "",
  "productCode": "1612343543543556",
  "projectId": "1612343543543556",
  "registerType": "",
  "sessionKey": ""
}
```


**请求参数**:


| 参数名称 | 参数说明 | 请求类型    | 是否必须 | 数据类型 | schema |
| -------- | -------- | ----- | -------- | -------- | ------ |
|tokenDTO|对外接口项目参数信息|body|true|TokenDTO|TokenDTO|
|&emsp;&emsp;openId|||false|string||
|&emsp;&emsp;personId|||false|string||
|&emsp;&emsp;productCode|产品编号||true|string||
|&emsp;&emsp;projectId|租户编号||true|string||
|&emsp;&emsp;registerType|||false|string||
|&emsp;&emsp;sessionKey|||false|string||


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK|ActionResult|
|201|Created||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


| 参数名称 | 参数说明 | 类型 | schema |
| -------- | -------- | ----- |----- | 
|code|返回码|string||
|data|返回数据|object||
|msg|返回消息|string||


**响应示例**:
```javascript
{
	"code": "0",
	"data": {},
	"msg": "success"
}
```


# web-mvc-links-handler


## links


**接口地址**:`/webapi/visitorcs/actuator`


**请求方式**:`GET`


**请求数据类型**:`application/x-www-form-urlencoded`


**响应数据类型**:`*/*`


**接口描述**:


**请求参数**:


暂无


**响应状态**:


| 状态码 | 说明 | schema |
| -------- | -------- | ----- | 
|200|OK||
|401|Unauthorized||
|403|Forbidden||
|404|Not Found||


**响应参数**:


暂无


**响应示例**:
```javascript

```