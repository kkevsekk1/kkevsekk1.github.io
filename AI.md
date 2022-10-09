
# 基于百度PaddleOCR文字识别

## paddle.ocrText(img, cpuThreadNum, useSlim);

识别结果为字符串数组

## paddle.ocr(img, cpuThreadNum, useSlim);

识别结果为包含字符串，坐标，置信度等的JSON数组

* img {图片对象} 需要识别的图片，可以是`images.captureScreen()`、`images.read(path)`等等
* cpuThreadNum {number} 识别使用的CPU核心数量，可选参数，默认为4
* useSlim {布尔} 可选参数，加载的模型，默认true (slim)

PaddleOCR 移动端提供了两种模型：ocr_v2_for_cpu与ocr_v2_for_cpu(slim)，此选项用于选择加载的模型,默认true使用v2的slim版(速度更快)，false使用v2的普通版(准确率更高）

以上均为全局函数。
