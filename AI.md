
# 基于百度PaddleOCR文字识别

## paddle.ocrText(img, cpuThreadNum, useSlim);

识别结果为字符串数组

## paddle.ocr(img, cpuThreadNum, useSlim);

识别结果为包含字符串，坐标，置信度等的JSON数组

* img {图片对象} 需要识别的图片，可以是`images.captureScreen()`、`images.read(path)`等等
* cpuThreadNum {number} 识别使用的CPU核心数量，可选参数，默认为4
* useSlim {布尔} 可选参数，加载的模型，默认true (slim)

两种模型：ocr_v2_for_cpu与ocr_v2_for_cpu(slim)，，前者更快后者更精准

以上均为全局函数。
