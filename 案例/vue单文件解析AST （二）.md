## 通过AST遍历vue单文件

### 简介

**AST**（**abstract syntax tree**）抽象语法树，通常都只说到了概念以及一些常见工具类使用的例子，没有说到AST具体的使用场景以及实际案例。这次做一个简单单文件遍历工具类，体验一下他的功能。现阶段经典的开发框架中Angular、React、Vue中的共同点就是，各种开发框架工具都有自己的指令/语法词以及各种hook函数钩子。同时各种不同的语法文件后缀``` .ts、.jsx、.vue```，最终都要通过编译解释打包后转换成`.js`文件，在同一个环境中js引擎中运行。其中转换的过程中的遍历，就体现了AST的作用。

### 思路

梳理下知识点，基于打包编译工具的思路，首先需要装载器loaders，将文件内容读取成string字符串，分别通过插件parser的方法parse转为AST，如下：

![image-20231127143453329](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20231127143453329.png)

​																								*图1 vue模板文件编译步骤*

接着将AST以及自定义迭代器，传入traverse遍历器内， 获取每个遍历的节点，其中根据各个parser的迭代器，进行自定义规则，大致的规则如下

![image-20231127150223214](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20231127150223214.png)

​																									*图2  traverse步骤*

示例源码：

```javascript
// template标签
function templateCompile(code) {
    const {ast} = vueCompiler.compile(code);
    const dfs = (node, path) => {
        for (let index in node.children) {
            let child = node.children[index];
            if ('img' === child.tag) {
                child.attrsList.forEach(attr => {
                    if (attr.name === ':src' || attr.name === 'src') {
                        console.log('这是一个img', attr.value, ` path= ${ path }`);
                    }
                })
            }
            dfs(child, path.concat(child.tag))
        }
    }
    dfs(ast, []);
}
// script 标签解析
function scriptCompile(code) {
    const ast = parser.parse(code, { sourceType: 'module' });
    const visitor = {
        ImportDeclaration(path) {
            const {specifiers, source} = path.node;
            console.log('这是一个import', specifiers[0].local.name, source.value);
        }        
    }
    traverse(ast, visitor);
}
// style 标签
function traverseStyleAstByCode(ast) {
  let imageArr = [];
  let importArr = [];
  const dfs = (node, _path) => {
    if (isEmpty(node) || isEmpty(node.nodes)) {
      return [];
    }
    for (let index in node.nodes) {
      let child = node.nodes[index];
      // TODO  
      dfs(child, [])
    }
  }
  dfs(ast, []);
}
```



### loader自定义

关于loader，通常我们接触较多的是vue-loader，它通常是搭配webpack打包器使用，使用起来比较复杂，我这边自定义了一个loader，如下：

```javascript
const fs = require("fs");
const readline = require('readline');

module.exports = class vueFileLoader {
  constructor(filePath) {
    this.file = null;
    this.filePath = filePath;
    this.templateCode = "";
    this.scriptCode = "";
    this.styleCode = "";
    this.isReadTemplate = false;
    this.isReadScript = false;
    this.isReadStyle = false;
  }
  /**
   * 同步读取文件内容
   * @param {string} filePath 
   * @returns 
   */
  async readFileLineSync (filePath) {
    this.file = readline.createInterface({
      input: fs.createReadStream(filePath),
      output: process.stdout,
      terminal: false
    });
    for await (const line of this.file) {
      // 读取 template 标签
      if (line.includes("<template>") && !this.isReadTemplate) {
        this.isReadTemplate = true;
      }
      if (line.includes("</template>")) {
        this.isReadTemplate = false;
      }
      if (this.isReadTemplate && !line.includes("<template>") && !line.includes("</template>")) {
        this.templateCode += line;
      }
      // 读取 script 标签
      if (line.includes("<script")) {
        this.isReadScript = true;
      }
      if (line.includes("</script>")) {
        this.isReadScript = false;
      }
      if (this.isReadScript && !line.includes("<script") && !line.includes("</script>")) {
        this.scriptCode += line;
      }
      // 读取 style 标签
      if (line.includes("<style")) {
        this.isReadStyle = true;
      }
      if (line.includes("</style>")) {
        this.isReadStyle = false;
      }
      if (this.isReadStyle && !line.includes("<style") && !line.includes("</style>")) {
        this.styleCode += `\n${line}\t`;
      }
    }
    return {
      templateCode: this.templateCode,
      scriptCode: this.scriptCode,
      styleCode: this.styleCode,
    }
  }
  /**
   * 异步读取文件
   * @param {string} filePath  文件路径 
   * @returns 
   */
  async readFileLineAsync (filePath) {
    this.file = readline.createInterface({
      input: fs.createReadStream(filePath),
      output: process.stdout,
      terminal: false
    });

    return new Promise((resolve, reject) => {
      this.file.on('line', (line) => {
        // 读取 template 标签
        if (line.includes("<template>") && !this.isReadTemplate) {
          this.isReadTemplate = true;
        }
        if (line.includes("</template>")) {
          this.isReadTemplate = false;
        }
        if (this.isReadTemplate && !line.includes("<template>") && !line.includes("</template>")) {
          this.templateCode += line;
        }
        // 读取 script 标签
        if (line.includes("<script")) {
          this.isReadScript = true;
        }
        if (line.includes("</script>")) {
          this.isReadScript = false;
        }
        if (this.isReadScript && !line.includes("<script") && !line.includes("</script>")) {
          this.scriptCode += line;
        }
        // 读取 style 标签
        if (line.includes("<style")) {
          this.isReadStyle = true;
        }
        if (line.includes("</style>")) {
          this.isReadStyle = false;
        }
        if (this.isReadStyle && !line.includes("<style") && !line.includes("</style>")) {
          // this.styleCode += line;
           this.styleCode += `\n${line}\t`;
        }
        resolve({
          fileLoader: this,
          styleCode: this.styleCode,
          scriptCode: this.scriptCode,
          templateCode: this.templateCode,
        })
      })
    })
  }
}
```

以上VueFileLoader类是基于node的fs 以及 readline 插件库，编写的简单vue单文件loader，测试代码如下：

函数执行测试如下：

```javascript
const path = require('path');
const VueFileLoader = require("./loader-vue");

async function getFileContent(pagePath) {
  const vueFileLoader = new VueFileLoader(pagePath);
  const fileContent = await vueFileLoader.readFileLineSync(pagePath);
  return {
    fileName: pagePath.split(path.sep).pop(),
    filePath: pagePath,
    templateCode: fileContent.templateCode,
    styleCode: fileContent.styleCode,
    scriptCode: fileContent.scriptCode
  }
}
getFileContent('./dest-file/app.vue').then((ret)=>{
  console.log("-----------", ret);
});
```

执行结果如下：

![image-20231127211647435](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20231127211647435.png)

以上的loader只针对单个标签，不存在多个style标签以及script、template标签，若是存在多个，可以采用正则表达式，如下：

```javascript
const readFileScript = async (_path) => {
  const _content = await readFile(_path);
  let rets = _content.match(/<script\s*\S*>[\s\S]*<\/script>/g);
  if (rets) {
    return rets[0].replace("<script>", "").replace("</script>", "");
  }
  return _content
}

const readFileScriptSync = (_path) => {
  const _content = readFileSync(_path);
  let rets = _content.match(/<script\s*\S*>[\s\S]*<\/script>/g);
  if (rets) {
    return rets[0].replace("<script>", "").replace("</script>", "");
  }
  return _content
}
```

使用@babel/parse、@babel/traverse进行转换js、遍历ast， 收集代码中依赖的import 文件路径、以及静态的图片jpg/png/jpeg/svg等图片资源

```javascript
function scriptCompile (code, pagepath) {
    let _import_path_list = [];
    try {
        const ast = parser.parse(code, {
            sourceType: 'module',
            plugins: [
                'decorators',
                'decoratorAutoAccessors',
                'doExpressions',
                'exportDefaultFrom',
                'flow',
                'functionBind',
                'importAssertions',
                'jsx',
                'regexpUnicodeSets',
            ],
        });
        const visitor = {
            ImportDeclaration (p) {
                const { source } = p.node;
                if (source.value !== undefined) {
                    let _value = source.value;
                    let _ret = _value.match(/\@\//g);
                    if (_ret !== undefined && _ret !== null && _ret.length > 0) {
                        let PROROOTPATH = pagepath.slice(0, pagepath.indexOf("src"));
                        _value = path.join(PROROOTPATH, "./src", _value.slice(_value.indexOf("@") + 1)); // 转化 @/ 相对路径为全路径;
                    }
                    _ret = _value.match(/\.\//g);
                    if (_ret !== undefined && _ret !== null && _ret.length > 0) {
                        _value = path.resolve(pagepath, "../", _value); /// 转化 ..等相对路径为全路径
                    }
                    _import_path_list.push(_value);
                }
            },
            ObjectProperty (path) {
                const node = path.node;
                if (node.value.type === 'StringLiteral') {
                    if (node.value.value !== undefined &&
                        (node.value.value.endsWith('.png') ||
                            node.value.value.endsWith('.jpeg') ||
                            node.value.value.endsWith('.jpg') ||
                            node.value.value.endsWith('.svg'))) {
                        let _value = node.value.value;
                        if (_value.startsWith('https://') === false && _value.startsWith('http://') === false) {
                            let _ret = _value.match(/\@\//g);
                            if (_ret !== undefined && _ret !== null && _ret.length > 0) {
                                let PROROOTPATH = pagepath.slice(0, pagepath.indexOf("src"));
                                _value = _value.replace(/\@/g, `${PROROOTPATH}`);
                            }
                            _ret = _value.match(/\.\//g);
                            if (_repatht !== undefined && _ret !== null && _ret.length > 0) {
                                _value = path.resolve(pagepath, "../", _value); /// 转化 ..等相对路径为全路径
                            }
                            _import_path_list.push(_value);
                        }

                    }
                }
            }
        }
        traverse(ast, visitor);
        return {
            ast,
            importFiles: uniqueArray(_import_path_list) // 去重
        };
    } catch (error) {
        console.log("======出错了=====， 文件格式不规范，出现特殊字符>>>>>>>", error);
    }
}
```

收集到的依赖有文件测试有，如下结果：

![image-20231127214220296](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20231127214220296.png)

### 遍历转换AST

其中css转换的工具类有[cssom](https://www.npmjs.com/package/cssom)、[postcss](https://github.com/postcss/postcss)，以postcss为例，遍历ast方法如下：

```javascript
/** 遍历 template ast 节点中 图片依赖 */
function traverseTemplateAstByCode(ast, filepath) {
  let imageArr = [];
  const dfs = (node, _path) => {
    if (isEmpty(node.children)) {
      return [];
    }
    for (let index in node.children) {
      let child = node.children[index];
      if ('image' === child.tag) {
        child.attrsList.forEach(attr => {
          if (attr.name === ':src' || attr.name === 'src') {
            // 排除 远程链接的图片
            if (!attr.value.includes("http")) {
              IMAGEEXT.some((ext) => attr.value.endsWith(ext)) && imageArr.push(attr.value);
            }
          }
        })
      }
      if (child.staticStyle && child.staticStyle.includes("url")) {
        const urlArr = child.staticStyle.match(/url\([\s\S]*\)/g).map((uriStr) => {
          const str = uriStr.match(/\([\s\S]*\)/g)[0];
          const end = str.length - 4;
          return str.substr(2, end)
        });
        imageArr = [...imageArr, ...urlArr].filter((url) => !url.includes("http"))
      }
      dfs(child, _path.concat(child.tag))
    }

  }
  if (ast) {
    dfs(ast, []);
  }
  return imageArr;
}
/** 遍历 style ast 节点中 css 文件 与  图片依赖 */
function traverseStyleAstByCode(ast) {
  let imageArr = [];
  let importArr = [];
  const dfs = (node, _path) => {
    if (isEmpty(node) || isEmpty(node.nodes)) {
      return [];
    }
    for (let index in node.nodes) {
      let child = node.nodes[index];
      if ('atrule' === child.type && 'import' === child.name) {
        const { params } = child
        // console.log("===>", __filename, params);
        // importArr.push(params.slice(1, params.length - 1)); /// 不兼容 @import url("/components/gaoyia-parse/parse.css")
        if (params.startsWith("'") || params.startsWith('"')) {
          importArr.push(params.slice(1, params.length - 1)); // 常规inport
        }
        else if (params.startsWith("url(")) {
          const img = params.slice(5, params.length - 2);
          if (!img.startsWith('http')) {
            importArr.push(img); // import url('xxx')
          }
        }
      }
      if ('decl' === child.type && 'background' === child.prop && child.value.includes("url")) {
        const urlArr = child.value.match(/url\([\s\S]*\)/g).map((matchStr) => {
          const str = matchStr.match(/\([\s\S]*\)/g)[0];
          if (!str.includes('http') && !str.includes('data:')) {
            const end = str.length - 4;
            return str.substr(2, end)
          }
          else {
            if (str.includes('data:')) {
              return '';
            }
            return str.substr(1, str.length - 2);
          }
        });
        imageArr = [...imageArr, ...urlArr]
      }
      if ('decl' === child.type && 'background-image' === child.prop && child.value.includes("url")) {
        const urlArr = child.value.match(/url\([\s\S]*\)/g).map((matchStr) => {
          const str = matchStr.match(/\([\s\S]*\)/g)[0];
          if (!str.includes('http') && !str.includes('data:')) {
            const end = str.length - 4;
            return str.substr(2, end)
          }
          else {
            if (str.includes('data:')) {
              return '';
            }
            return str.substr(1, str.length - 2);
          }
        });
        imageArr = [...imageArr, ...urlArr]
      }
      dfs(child, [])
    }
  }
  dfs(ast, []);
  return {
    imageArr: (imageArr || []).filter((url) => !url.includes("http")), // 筛除 远程链接
    importArr: (importArr || []).filter((url) => !url.includes("http"))
  };
}
```

执行遍历 ```bash node test.js```，结果如下：

![image-20231128093814347](C:\Users\pengxueyou\AppData\Roaming\Typora\typora-user-images\image-20231128093814347.png)



### 总结

以上就是本人对vue文件解析的示例，联想到在vue编译的使用场景，通过自定义的vue单文件的loade，了解到AST转换工具类；遍历ast节点，搜索到节点的分析语法词，进行收集依赖代码分析，其中关于AST的进一步使用场景，需要进一步进行探究，大家可以在线上[astexplorer](https://astexplorer.net/) 训练场进行尝试。
