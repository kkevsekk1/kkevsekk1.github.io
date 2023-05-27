# event-stream
v6.4.0新增
> 稳定性: 稳定

来自npm模块event-stream，如需使用，请用
```js
const es = require('event-stream')
```
该模块用于便捷的创建流
```js
es.readable(function (count, callback) {
  if(streamHasEnded)
    return this.emit('end')
  
  //...
  
  this.emit('data', data) //use this way to emit multiple chunks per call.
      
  callback() // you MUST always call the callback eventually.
             // the function will not be called again until you do this.
})
```
