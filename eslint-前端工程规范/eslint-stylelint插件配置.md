## 配置指南

配置的插件，基于云曜的脚手架的配置基础上进行配置

1. 修改**eslint-loade**r 插件 为 **eslint-webpack-plugin ，并且需要 安装`eslint >= 7.x`**
   释掉配置：
   ![公共空间 > 前端编码插件配置 > image_1.png](https://wiki.hikvision.com.cn/download/attachments/176951428/image_1.png?version=1&modificationDate=1650270663059&api=v2)

   插件配置如下：**
   **![公共空间 > 前端编码插件配置 > image_2.png](https://wiki.hikvision.com.cn/download/attachments/176951428/image_2.png?version=2&modificationDate=1654589437706&api=v2)

2.  安装eslint-friendly-formatter
   使用配置同上图，安装之前的效果如下图：
   ![公共空间 > 前端编码插件配置 > image-9.png](https://wiki.hikvision.com.cn/download/attachments/176951428/image-9.png?version=1&modificationDate=1650270861701&api=v2)
   安装之后的提示如下：
   ![公共空间 > 前端编码插件配置 > image-8.png](https://wiki.hikvision.com.cn/download/attachments/176951428/image-8.png?version=1&modificationDate=1650270920613&api=v2)

3.  安装 **eslint-plugin-vue**
   全量配置如下：
   ![img](https://wiki.hikvision.com.cn/plugins/servlet/view-file-macro/placeholder?type=JavaScript+File&name=.eslintrc.js&attachmentId=176952086&version=2&mimeType=text%2Fjavascript&height=250)

4.  安装 **vue-eslint-parser**
   配置如下：
   ![公共空间 > 前端编码插件配置 > image.png](https://wiki.hikvision.com.cn/download/attachments/176951428/image.png?version=1&modificationDate=1653273742619&api=v2)

   注：ecmaVersion这版本号与js的ECMA版本号匹配，例如： ***this.arr[0]?.name\*** 这种?.语法糖需要2020版本的ECMA规范js, ecmaVersion:2020

   

5.  安装 **stylelint-order**
   配置如下：
   ![img](https://wiki.hikvision.com.cn/plugins/servlet/view-file-macro/placeholder?type=JavaScript+File&name=.stylelintrc.js&attachmentId=176952126&version=1&mimeType=text%2Fjavascript&height=250)

   

6. 参考链接：
   eslint 中文文档：https://cloud.tencent.com/developer/doc/1078
   eslint 官方文档: https://eslint.vuejs.org/rules/
   stylelint 中文文档：https://cloud.tencent.com/developer/chapter/18030
   stylelint 官方文档： [stylelint](http://stylelint.cn/) [stylelint (docschina.org)](https://stylelint.docschina.org/)

   

7. 实例工程： 

   ![img](https://wiki.hikvision.com.cn/plugins/servlet/view-file-macro/placeholder?type=Zip+Archive&name=eslint-test.zip&attachmentId=176952234&version=1&mimeType=application%2Fzip&height=250)