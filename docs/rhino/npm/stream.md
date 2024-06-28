# stream

v6.4.0 新增

> 稳定性: 稳定

注意: <font color="#ef5952">这个模块是异步的，使用此模块请勿阻塞线程</font>
该模块不会自动加载，如需使用，请用

```
const stream = require('stream');
```

使用方法参考 node 文档中 stream，下方是一些 autox 中特有的内容

## stream.fromInputStream(inputStream[,options])

- inputStream \{InputStream} java 输入流
- options \{object} 选项,详细见 node 文档

将 java 流转为 Readable 可读流，为提高处理速度，默认的缓冲区大小被设为 64kb，io 操作由内部 io 线程处理

## stream.fromOutputStream(outputStream[,options])

- outputStream \{OutputStream} java 输出流
- options \{object} 选项,详细见 node 文档

将 java 流转为 Writable 可写流，为提高处理速度，默认的缓冲区大小被设为 64kb，io 操作由内部 io 线程处理

## stream.createFileReadStream(path[,bufferSize])

- path \{String} 文件路径
- bufferSize \{Number} 缓冲区大小，默认 256k

从文件创建一个可读流

## stream.createFileWriteStream(path[,bufferSize])

- path \{String} 文件路径
- bufferSize \{Number} 缓冲区大小，默认 256k

从文件创建一个可写流
