### 人员管理组件API

```js
/** 公共接口 (12) */
  GET_GROUP: "fdcs/fdcs/web/v1/personGroup/page", // 获取人员分组
  SEARCH_PERSON: "/fdcs/fdcs/web/v1/person/page", // 人员远程搜索
  SEARCH_PERSON_BY_PERMISSION: "/fdcs/fdcs/web/v1/person/page/byPermission", // 人员远程搜索
  SEARCH_PERSON_BY_ORG: "/fdcs/fdcs/web/v1/person/page/byOrgId", // 根据组织id查询人员
  SEARCH_PERSON_BY_GROUP: "/fdcs/fdcs/web/v1/person/page/byGroupId", // 根据分组id查询人员
  UPLOAD_PERSON: "/fdcs/fdcs/web/v1/person/import", // 批量上传人员
  UPLOAD_PHOTO: "/fdcs/fdcs/web/v1/person/upload/photo", // 批量上传照片
  UPLOAD_UPDATE_PERSON: "/fdcs/fdcs/web/v1/person/batch/update", // 批量上传更新人员
  GET_LABEL: "/fdcs/fdcs/web/v1/person/query/personLabel", // 获取人员标签
  ADD_LABEL: "/fdcs/fdcs/web/v1/person/add/personLabel", // 添加人员标签
  DELETE_LABEL: "/fdcs/fdcs/web/v1/person/delete/personLabel", // 删除人员标签
  GET_OPERATION_RECORD: "/fdcs/fdcs/web/v1/imex/page", // 分页查询导入导出记录
  /** 人员信息 (35) */
  SEARCH_ORG_ROOT: '/fdcs/fdcs/web/v1/personOrg/search/root', // 查询组织树根节点
  SEARCH_ORG_TREE: '/fdcs/fdcs/web/v1/personOrg/search/tree', // 查询组织树
  SEARCH_ORG_NAME_TREE: '/fdcs/fdcs/web/v1/personOrg/search/name/tree', // 根据节点名称查询组织树
  DEPT_MOVE: '/fdcs/fdcs/web/v1/personOrg/move', // 组织树节点移动
  PERSON_PAGE: '/fdcs/fdcs/web/v1/person/page', // 人员信息分页
  PERSON_PAGE_DETAIL: "/fdcs/fdcs/web/v1/person/queryDetail", // 获取详情页数据
  QUERY_EDIT_DETAIL: '/fdcs/fdcs/web/v1/person/queryEditDetail', // 查询人员详细信息
  PERSON_EXPORT: '/fdcs/fdcs/web/v1/person/export', // 人员信息导出
  SEARCH_DEPT_PAGE: '/fdcs/fdcs/web/v1/personOrg/page', // 查询部门列表
  PERSON_CHANGE_ORG: '/fdcs/fdcs/web/v1/person/batchUpdate/changeOrg', // 人员换组织
  PERSON_CHANGE_ORG_CHECK: '/fdcs/fdcs/web/v1/person/changeOrg/checkGroup', // 人员更换组织前检查此次更换组织会删除该人员的分组信息
  PERSON_AUTH_DATE_TIME: '/fdcs/fdcs/web/v1/person/batchUpdate/personAuthDateTime', // 批量更新权限日期
  PERSON_GROUP_PAGE: '/fdcs/fdcs/web/v1/personGroup/page', // 人员分组分页查询
  PERSON_GROUP_ADD: '/fdcs/fdcs/web/v1/personGroup/person/add', // 人员加入分组
  PERSON_AUTH_CHANGE: '/fdcs/fdcs/web/v1/person/batchUpdate/black', // 标记重点人员
  PERSON_DELETE: '/fdcs/fdcs/web/v1/person/delete', // 删除人员
  ADD_PERSON_ORG: '/fdcs/fdcs/web/v1/personOrg/add', // 新增组织树节点
  UPDATE_PERSON_ORG: '/fdcs/fdcs/web/v1/personOrg/update', // 更新组织树节点
  DELETE_PERSON_ORG: '/fdcs/fdcs/web/v1/personOrg/delete', // 删除组织树节点
  GET_ORG_PERSON_COUNT: '/fdcs/fdcs/web/v1/personOrg/search/personCount', // 根据组织id获取当前组织下的人员总数
  SYNC_PERSON_ORG: '/fdcs/fdcs/web/v1/personOrg/sync', // 同步组织树节点
  PERSON_FACE_UPLOAD: '/fdcs/fdcs/web/v1/person/face/upload', // 人脸图片上传
  PERSON_FACE_DELETE: '/fdcs/fdcs/web/v1/person/face/delete', // 人脸图片删除
  PERSON_FACE_PAGE: '/fdcs/fdcs/web/v1/person/face/search', // 获取人脸分页
  FINGER_PRINT_DELETE: '/fdcs/fdcs/web/v1/person/fingerprint/delete', // 指纹删除
  FINGER_PRINT_PAGE: '/fdcs/fdcs/web/v1/person/fingerprint/page', // 获取指纹分页
  ADD_PERSON: '/fdcs/fdcs/web/v1/person/add', // 新增人员
  UPDATE_PERSON: '/fdcs/fdcs/web/v1/person/update', // 修改人员
  GET_GROUP_BY_ORG: '/fdcs/fdcs/web/v1/personGroup/queryPageByOrgId', // 根据组织id获取分组（祖先组织的分组，新增人员时组织与分组联动使用）
  GET_STS_INFO: '/fdcs/fdcs/web/v1/security/query/stsOssInfo', // 获取sts和加密信息
  GET_DECODE_URL: '/fdcs/fdcs/web/v1/person/face/uploadUrl', // 用图片加密地址换解密地址及其他信息
  QUERY_AVAILABLE_FILED: '/fdcs/fdcs/web/v1/field/queryAvailableFiled', // 查询可用自定义字段
  REPORT_OR_RELIEVE_LOSS: '/fdcs/fdcs/web/v1/person/cardNum/reportOrRelieveLoss', // 卡号挂失/解挂
  QUERY_CERT_NUM_PHONE: '/fdcs/fdcs/web/v1/person/queryCertNumAndPhone', // 根据人员ID查询未脱敏卡号电话号码数据
  QUERY_FIELD: '/fdcs/fdcs/web/v1/field/query', // 查看人员信息字段列表

  /** 人员分组 (2) */
  PERSON_GROUP_ADD_FULL: '/fdcs/fdcs/web/v1/personGroup/add/full', // 添加人员分组
  PERSON_GROUP_UPDATE_FULL: '/fdcs/fdcs/web/v1/personGroup/update/full', // 修改人员分组

  /** 参数配置 (2) */
  SET_PERMISSION_CONFIG: "/fdcs/fdcs/web/v1/project/config", // 设置用户权限配置和短信配置
  GET_PERMISSION_CONFIG: "/fdcs/fdcs/web/v1/project/queryConfig", // 获取用户权限配置和短信配置

  /** 人员信息字段配置 (4) */
  GET_FIELD_QUERY: "/fdcs/fdcs/web/v1/field/query", // 查询自定义字段
  ADD_FIELD: '/fdcs/fdcs/web/v1/field/add', // 自定义字段新增
  DELETE_FIELD: '/fdcs/fdcs/web/v1/field/delete', // 删除自定义字段
  EDIT_FIELD: '/fdcs/fdcs/web/v1/field/edit', // 编辑自定义字段

  /** 人员录入审核 (12) */
  GET_TEMPLATE: "/fdcs/fdcs/web/v1/template/getTemplate", // 获取二维码模板配置信息
  SAVE_TEMPLATE: "/fdcs/fdcs/web/v1/template/save", // 保存二维码模板配置信息
  GET_EDIT_TEMPLATE: "/fdcs/fdcs/web/v1/template/getEditTemplate", // 获取二维码模板配置信息
  QUERY_PERSON_PAGE: "/fdcs/fdcs/web/v1/audit/queryPersonPage", // 获取人员录入列表
  QUERY_PERSON: '/fdcs/fdcs/web/v1/audit/queryPerson', // 获取待审核人员详情
  VERIFY_PERSON: '/fdcs/fdcs/web/v1/audit/auditPerson', // 审核人员
  QUERY_PERSON_FACE: '/fdcs/fdcs/web/v1/person/face/queryToAuditFace', // 获取人员人脸信息，区别是此接口会返回faceId
  BATCH_AUDIT: '/fdcs/fdcs/web/v1/audit/personAuditBatch', // 批量审批
  GET_QR_CONTENT: '/fdcs/fdcs/web/v1/template/getQr/content', // 获取二维码内容
  CHANGE_CONFIG_STATUS: '/fdcs/fdcs/web/v1/template/configStatus', // 启用/禁用组织二维码
  QUERY_AUDIT_NUM: '/fdcs/fdcs/web/v1/audit/queryAuditCertNumAndPhone', // 获取未脱敏数据
  GET_AVAILABLE_DATA: '/fdcs/fdcs/web/v1/field/queryAvailableFiled' // 获取自定义字段


```

