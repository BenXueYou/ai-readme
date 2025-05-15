## eslint 源码阅读笔记



### 初始化

```bash
npm init @eslint/config  // 执行过程中 安装有插件模块 @eslint/create-config
```

### node 进程检测脚本

处理进程异常，抛出的错误信息， 与```try{}catch(){}```类似，具体的文档需要查阅开发文档

```bash
process.on("uncaughtException", (error)=>{});
process.on("unhandledRejection", (error)=>{});
```

示例：

```javascript
(async function main () {
    process.on("uncaughtException", onFatalError);
    process.on("unhandledRejection", onFatalError);
    // TODO
    
}).catch(onFatalError)
```



### node基础知识

#### 命令行参数

命令行参数指的是 2 个方面：

- 传给 node 的参数。例如 `node --harmony script.js --version` 中，`--harmony` 就是传给 node 的参数

- 传给进程的参数。例如 `node script.js --version --help` 中，`--version --help` 就是传给进程的参数

分别通过 `process.argv` 和 `process.execArgv` 来获得

#### process.argv 

包含启动 Node.js 进程时传入的命令行参数， 返回值 []

- 第一个元素将是 [`process.execPath`](https://nodejs.cn/api/process.html#processexecpath)。 如果需要访问 `argv[0]` 的原始值，请参阅 `process.argv0`。当前进程的根目录，暂理解为  环境 上下文 目录

- 第二个元素将是正在执行的 JavaScript 文件的路径。 执行的脚本文件目录/路径

- 其余元素将是任何其他命令行参数。 其他 后缀的 参数

  

#### process.exitCode

官方解释为：当进程正常退出或通过 [`process.exit()`](https://nodejs.cn/api/process.html#processexitcode) 退出而不指定代码时，将作为进程退出码的数字。

个人理解为：即进程退出时，可自定义的返回

> 将代码指定为 [`process.exit(code)`](https://nodejs.cn/api/process.html#processexitcode) 将覆盖 `process.exitCode` 的任何先前设置。

#### process.stdin

属性返回连接到 `stdin` (文件描述符 `0`) 的流。 它是 [`net.Socket`](http://url.nodejs.cn/hcpLVK)（也就是 [Duplex](http://url.nodejs.cn/cJa2Cm) 流），除非文件描述符 `0` 指向文件，在这种情况下它是 [Readable](http://url.nodejs.cn/uGwSta) 流。

有关如何从 `stdin` 读取的详细信息，请参阅 [`readable.read()`](http://url.nodejs.cn/a2T71f)。

作为 [Duplex](http://url.nodejs.cn/cJa2Cm) 流，`process.stdin` 还可以在为 Node.js v0.10 之前编写的脚本兼容的“旧”模式下使用。 有关更多信息，请参阅[流的兼容](http://url.nodejs.cn/gwr7PL)。

在“旧”流模式下，`stdin` 流默认是暂停的，所以必须调用 `process.stdin.resume()` 来读取它。 另请注意，调用 `process.stdin.resume()` 本身会将流切换到“旧”模式。

> - [`process.stdin`](https://link.juejin.cn/?target=https%3A%2F%2Fnodejs.org%2Fapi%2Fprocess.html%23processstdin)(0):标准输入流，它是程序的输入源。
> - [`process.stdout`](https://link.juejin.cn/?target=https%3A%2F%2Fnodejs.org%2Fapi%2Fprocess.html%23processstdout)(1):标准输出流，它是程序的输出源。
> - [`process.stderr`](https://link.juejin.cn/?target=https%3A%2F%2Fnodejs.org%2Fapi%2Fprocess.html%23processstderr)(2):标准错误流，用于由程序发出的错误信息和诊断。

*暂时不太理解以下：*

```
process.stdin.setEncoding("utf8").on("readable", ()=>{
	// 这里的readable 流的 源是 什么
})
```



