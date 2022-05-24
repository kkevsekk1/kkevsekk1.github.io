# AI

## OCR(基于百度PaddleOCR文字识别)

### result = paddle.ocr(img, cpuThreadNum, useSlim)
* img {image object} 需要识别的图片
* cpuThreadNum {number} 识别使用的CPU核心数量，可选参数，默认为4
* useSlim {boolean} 两种模型：ocr_v2_for_cpu与ocr_v2_for_cpu(slim)，可选参数，此选项用于选择加载的模型,默认true使用v2的slim版(速度更快)，false使用v2的普通版(准确率更高）
* result {JSON object} 返回完整识别信息，识别结果为包含字符串，坐标，置信度等的JSON对象（兼容百度OCR格式）。列表中的文字默认按图像位置从左到右、从上到下排序。


### result = paddle.ocrText(img, cpuThreadNum, useSlim)
* img {image object} 需要识别的图片
* cpuThreadNum {number} 识别使用的CPU核心数量，可选参数，默认为4
* useSlim {boolean} 两种模型：ocr_v2_for_cpu与ocr_v2_for_cpu(slim)，可选参数，此选项用于选择加载的模型,默认true使用v2的slim版(速度更快)，false使用v2的普通版(准确率更高）
* result {string list} 只返回文本识别信息。列表中的文字默认按图像位置从左到右、从上到下排序。

### result = paddle.ocr(img)
### result = paddle.ocrText(img)
* 简化的调用命令，默认参数：cpuThreadNum = 4, useSlim = true


### paddle.release()
* 手动释放OCR占用的native内存，非必要，供万一出现内存泄露时使用


### 示例
```javascript
let img = images.read("./0.jpg")
let cpuThreadNum = 4
let useSlim = true
let start = new Date()
const result = paddle.ocr(img, cpuThreadNum, useSlim)
log('OCR完整识别耗时：' + (new Date() - start) + 'ms')
toastLog("完整识别信息: " + JSON.stringify(result))
start = new Date()
const stringList = paddle.ocrText(img, cpuThreadNum, useSlim)
log('OCR纯文本识别耗时：' + (new Date() - start) + 'ms')
toastLog("文本识别信息: " + JSON.stringify(stringList))
img.recycle() // 回收图片
```
