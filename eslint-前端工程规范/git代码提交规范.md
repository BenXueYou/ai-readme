1、太鲁阁脚本需要扫描git commit 的提交日志，对我们的代码仓库进行更进一步的管理，代码仓库中的提交格式需要统一规范一下

2、仓库代码工程应该都配置了husky插件配置了hook脚本，校验git commit 命令的提交规则，大家代码仓库的配置可以自查一下，是不是配置了脚本

3、QA质量组那边要求，我们commit -m 信息的填写 统一的格式，如下：

``` <type> (<scope>): <subject>```

- （1）type （必须）：英文，小写，用于说明commit内容变更的类型。必须是这些规定标识中的一个或多个： [feat](https://sys-gitlab.hikvision.com.cn/PBG/components/special/xres/-/commit/671db2d60bc4025755afecc9aff5e33b78b5cc84)、fix、perf、impr、ci、docs、style、test、refactor、chore、jvm、pom、apm、conf、typo、wip。

- （2）subject （必须）：是commit的简短描述，建议不超过50字符避免换行影响美观。

- （3）scope（可选）：scope用于说明commit影响的范围，比如数据层、控制层、视图层等等，视项目不同而不同。如果你的修改影响了不止一 个scope,你可以使用*代替。

  > 示例1：git commit -m " feat(controller)：新增用户查询接口"
  >
  > 示例2：git commit -m " fix(ui): 修复展位高度
  >
  > 示例3：git commit -m " impr：优化资源刷入es逻辑，提高刷入效率"
  >
  > 示例4：git commit -m " chore：删除多余的重复功能的类 "

（1）因为脚本可能是字符串全匹配，所以注意type字段的格式，可能在其他规范里面习惯 【fix】、[feat]加一些符号进行强调，规范里面特别做了说明 **一定不要加**特殊字符 **【】[ ]**

（2）包含多个type的提交，日志书写举例：fix：xxxxx；feat：xxxxxx。（fix类型的提交尽量纯粹完整，方便后期做缺陷分析和回归修复）

| type                                                         | 含义                          | 备注                                                         |
| :----------------------------------------------------------- | :---------------------------- | :----------------------------------------------------------- |
| [feat](https://sys-gitlab.hikvision.com.cn/PBG/components/special/xres/-/commit/671db2d60bc4025755afecc9aff5e33b78b5cc84) | feature，新功能               | feature是新功能的统称，不特指项目需求清单里的需求。如果按小功能点分批提交，也可用function。 |
| fix                                                          | fix bug，修复缺陷             | 包括编码过程中的逻辑修复，不特指线上bug修复。                |
| perf                                                         | performance ，性能优化        |                                                              |
| impr                                                         | improvement，小的代码设计改进 |                                                              |
| ci                                                           | 构建过程或辅助工具的变动      |                                                              |
| docs                                                         | 仅文档变更                    |                                                              |
| style                                                        | 代码格式调整                  | 如 import 清理，代码格式化。                                 |
| test                                                         | 单测和自动化 case 相关        |                                                              |
| refactor                                                     | 重构代码                      | 非bug修复和性能优化，包括编码过程中的代码结构调整，不特指重构项目。 |
| chore                                                        | 无关紧要的改动                | 如删除用不到的注解、调整日志内容等。                         |
| jvm                                                          | 仅 JVM 参数变更               |                                                              |
| pom                                                          | 仅依赖和版本变化              |                                                              |
| apm                                                          | 仅监控打点、异常日志处理相关  |                                                              |
| conf                                                         | 仅配置变化                    | 如Spring 配置、properties 文件                               |
| typo                                                         | 修复小的拼写错误              |                                                              |
| wip                                                          | work in progress              | 少用，用于开发中的不完整提交，新工程开始时偶尔使用           |

## 

4、subject 中message的描述

- **iscan、敏感词、合规性、安全扫描、缺陷单、研发子单**

> fix：iscan缺陷修复
>
> fix：敏感词修改

- 关联缺陷单

  > fix：[构架2.3.0][B4][sdmc]萤石协议接入设备，编辑时，缺少“设备验证码”字段；
  >
  > 缺陷来源：缺陷单，[BGA230460220](http://defect.hikvision.com.cn/approve/document?flowInstId=262756852)

- 定制需求单

  > fix：paf异常，巡检不到设备在线状态；
  >
  > 缺陷来源：研发子单，QUK202308030097