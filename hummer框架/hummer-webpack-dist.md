```javascript
__webpack_require__.r(__webpack_exports__);
/* harmony import */ var _hummer_tenon_vue__WEBPACK_IMPORTED_MODULE_0__ = __webpack_require__(/*! @hummer/tenon-vue */ "./node_modules/@hummer/tenon-vue/dist/tenon-vue.es.js");
/* harmony import */ var _app__WEBPACK_IMPORTED_MODULE_1__ = __webpack_require__(/*! ./app */ "./src/pages/index/app.vue");
/* harmony import */ var _hummer_vue_plugin_list__WEBPACK_IMPORTED_MODULE_2__ = __webpack_require__(/*! @hummer/vue-plugin-list */ "./node_modules/@hummer/vue-plugin-list/dist/index.js");



_hummer_tenon_vue__WEBPACK_IMPORTED_MODULE_0__.register(_hummer_vue_plugin_list__WEBPACK_IMPORTED_MODULE_2__["default"]);
_hummer_tenon_vue__WEBPACK_IMPORTED_MODULE_0__.render(_app__WEBPACK_IMPORTED_MODULE_1__["default"]);
```

```javascript
register->registerComponent->components.set("ex-".concat(name), component);

if (components) instance.components = components;


applyOptions->finishComponentSetup-> handleSetupResult -> setupStatefulComponent

applyOptions->finishComponentSetup->handleSetupResult->setupStatefulComponent->registerDep->createSuspenseBoundary->hydrateSuspense

applyOptions->finishComponentSetup->handleSetupResult->setupStatefulComponent->registerDep->createSuspenseBoundary->SuspenseImpl

applyOptions->finishComponentSetup->handleSetupResult->setupStatefulComponent->registerDep->createSuspenseBoundary->SuspenseImpl

applyOptions->finishComponentSetup-> setupStatefulComponent -> setupComponent


render

超出预期：积极讨论推进插件版本功能设计，完成版本功能开发/自测/发布并完善插件使用教程文档，积极响应插件在项目中对接，将发布的新版本落地到实际项目中，收到实际项目应用良好的反馈，无重大缺陷回滚版本或是出现版本补丁
达到预期：积极讨论完成插件版本功能设计，6月30号前完成插件版本开发、测试、开发功能，完善使用的教程文档，文档教程清晰完整且无误
未达到预期：插件版本未能完成质量较差，测试中出现反复修改，导致插件版本延迟发布，同时未能及时完善教程文档，文档出现重大错误

超出预期（分数高于等于权重分的80%（含））：
工作任务按时录入海客平台，且正确无误，4月30日前完成3个hikyun-ui组件、editorjs插件3个的开发，并发布上线；6月15日前完成软件技术部前端组《移动APP混合开发探索与实践》主题分享，让其他业务小组组内前端开发者了解移动混合APP开发，收到良好反馈。
达到预期（分数等于权重分的70%（含）-80%（不含））：
工作任务按时录入海客平台，且正确无误，5月31日前完成1个hikyun-ui组件、editorjs插件1个的开发，并发布上线；6月30日前完成软件技术部前端组《移动APP混合开发探索与实践》主题分享，让其他业务小组组内前端开发者了解移动混合APP开发，收到良好反馈。
未达预期（分数低于权重分的70%（不含））：
工作任务未按时、按要求录入海客平台；5月31日前未完成hikyun-ui组件、editorjs插件的开发，或未发布上线；未完成或推迟软件技术部前端组《移动APP混合开发探索与实践》主题分享会

    
```

