```json
DeepSeek-R1（671B满血版本）: LanzOpenAI_194d45ba-50e0-4bff-beeb-931dc297526a

DeepSeek-V3-0324: LanzOpenAI_7b5e32ea-bca7-401d-8635-4e1fdc40366f

Lanz-Code:  LanzOpenAI_9807b89c-ad51-4aab-80c8-0d7d0e441858
```

https://www.framelink.ai/docs/quickstart?utm_source=github&utm_medium=readme&utm_campaign=readme

npx figma-developer-mcp --\figma-api-key=$FIGMA_API_KEY

// [Figma API Key loaded from environment variable]

```json
{
  "mcpServers": {
    "mastergo-magic-mcp": {
      "disabled": true,
      "timeout": 60,
      "command": "cmd",
      "args": [
        "/c",
        "npx",
        "-y",
        "@mastergo/magic-mcp",
        "--token=$FIGMA_API_TOKEN",
        "--url=https://mastergo.com"
      ],
      "env": {
        "NPM_CONFIG_REGISTRY": "https://registry.npmjs.org/"
      },
      "transportType": "stdio"
    },
    "Framelink Figma MCP": {
      "disabled": false,
      "timeout": 60,
      "url": "http://localhost:3333/sse",
      "transportType": "sse"
    }
  }
}
```



https://pb.hik-cloud.com/lite-miniapp-h5/index.html#/inspect/todo/myTodo/checkProcess?activeTab=rectify&recordId=1639226847e54827ac897bb7a00cd8a0&taskStatusName=%E5%BE%85%E6%95%B4%E6%94%B9&taskStatus=1&nextLevel=0&rectifyStatus=1&questionIds=%5B%2251c7fb6382384f3a9986095adad7a0aa%22%5D&token=b6e38bd7-7fe8-42f8-a817-9237df7109e4



%NVM_SYMLINK%

%NVM_HOME%

### 简析AI模型能力在开发中的体验

#### 前言

​		2022年11月30，openAI发布的chatGPT是打响了人们迈向AI大模型开始的第一枪，继3年后2025年1月15日deepseek的发布，则意味着正式吹响了所有人冲向AI智能模型能力的冲锋号。就像蒸汽机出现在20世纪初，带来的第一次工业革命，当代人开始体验了又一次革命浪潮，包括各个社会组织或公司，各行各业的从业者，都不得不开始拥抱大模型，拥抱AI智能，体验AI模型能力在工作生活中带来的一些变化。

#### 思考

最近随着市场行情严峻挑战，公司面临的压力也一步步的开始传递给每一个人，同时AI模型的出现，也给公司带来了机遇。公司各个部门领导组织负责人，都在积极寻找进一步的方向和机遇。不仅仅是公司领导，作为公司生产一线的开发者，也必须开始思考怎么利用AI模型提高生产效率：一、首先认识AI模型，学习并掌握怎么向AI模型描述清楚自己的需求，二、接着结合自己日常的工作场景，给自己的日常工作做一个问题分类，三、根据问题的分类将需求输入给AI模型

#### 梳理

根据最近在自己开发工作中遇到的最常见的问题分为以下几个场景，分别是开发中的编码设计、版本迭代中的代码维护、质量检测中代码缺陷维护。

#### 场景一 、

开发中的代码设计，怎么向AI提问或是怎么向AI描述我的需求，我这边根据AI模型的回答知道以下几个点

```json
1、页面的基本功能和目标：页面的主要功能是什么？用户通过这个页面可以完成哪些操作？
2、页面的结构和布局：页面的主要区域和组件有哪些？例如，头部、导航栏、主要内容区、底部等。
3、屏幕方向：页面是否需要支持横屏和竖屏？如果有，具体的设计需求是什么？
4、样式和主题：页面的整体风格和颜色方案是什么？是否有特定的设计规范或品牌指南？
5、交互设计：用户在页面上的主要交互行为有哪些？例如，点击、滑动、输入等。
6、技术栈：你打算使用哪些技术栈来实现这个页面？例如，HTML、CSS、JavaScript、React、Vue等。
7、其他特殊需求：是否有其他特殊需求或功能，例如响应式设计、动画效果、适配不同设备等？
```

##### 新建功能代码试一下：

![image-20250327195200263](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250327195200263.png)

得到如下部分代码生成截图

![image-20250327195249565](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250327195249565.png)

![image-20250327195414099](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250327195414099.png)

点击代码右上角

![image-20250327195611085](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250327195611085.png)

![image-20250327195625962](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250327195625962.png)

可以将生成的代码复制，插入，或是新建文件到你的代码工程目录中，省去了编码过程中新建文件，写一些基础的代码。

##### 根据进一步追问，修正代码样式

![image-20250327200103978](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250327200103978.png)

能进一步优化的代码样式，尽管没有达到直接使用的完美效果，但是会省略很多手写的代码，进一步调试代码样式的步骤。

##### 新增一些代码工具函数

![image-20250327202051349](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250327202051349.png)



#### 场景二

##### 功能迭代中，不同语法框架的转换

丢入一段vue3+ts的代码，让AI模型将代码转换成vue2+vant2的代码

![image-20250327200552999](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250327200552999.png)

![image-20250327200621968](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250327200621968.png)





##### 对于不熟悉的代码，怎么去理解阅读他的逻辑

经常会遇到一些业务比较复杂的代码逻辑，维护者需要去阅读代码，去理解业务，可以通过AI模型去提高这个效率，例如，丢入一段代码

![image-20250327200843362](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250327200843362.png)

![image-20250327200854992](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250327200854992.png)

![image-20250327200907092](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250327200907092.png)

居然还会有代码的流程图给你生成，在实际的学习开发中，阅读源码，维护一些老代码给我们带来了很大的便利性。

#### 场景三

##### 代码逻辑自检

对于一些复杂的逻辑代码，通常会有一些考虑不全代码的缺陷风险，在开发中，同样利用模型的能录可以给我们带来一些代码质量的自检，如下

![image-20250327201344089](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250327201344089.png)

![image-20250327201353343](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250327201353343.png)

##### 缺陷自查分析

遇到一些场景的代码缺陷报错

![image-20250327201809658](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250327201809658.png)

![image-20250327201846145](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250327201846145.png)

##### 代码缺陷修复

我在使用van-popup组件开发业务组件的时候，在web浏览器端能否实现滚动一切正常，但是在真机运行的时候却发现滚动失效了

经过大模型分析处理

![image-20250327202517264](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250327202517264.png)

![image-20250327202529856](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250327202529856.png)

不但给出了问题分析，给出了解决方法，同时还给出了验证步骤。



#### 模型工具的错误

模型使用过程中，要注意一些模型导致的明显错误

![image-20250327203142350](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250327203142350.png)

![image-20250327203147355](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20250327203147355.png)

在开发工作中，使用模型是一个大趋势，前期我们许需要耐心，掌握一些模型提示词提测技巧，才能更好的驾驭AI模型的能力。希望AI大模型响应速度会越来越快，同时，自己也需要更加关注AI模型的新技能，快速熟悉一些工具的使用，将AI模型能力能更加高效的运用到自己的工作中，以上是我使用AI模型能力在开发中的一些体验分享

