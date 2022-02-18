
# 基于百度PaddleOCR文字识别

## paddle.ocrText(img, cpuThreadNum, useSlim);

识别结果为字符串数组

## paddle.ocr(img, cpuThreadNum, useSlim);

识别结果为包含字符串，坐标，置信度等的数组

* img {图片对象} 需要识别的图片
* cpuThreadNum {number} 识别使用的CPU核心数量，可选参数，默认为4
* useSlim {布尔} 两种模型：ocr_v2_for_cpu与ocr_v2_for_cpu(slim)，可选参数，此选项用于选择加载的模型,默认true使用v2的slim版(速度更快)，false使用v2的普通版(准确率更高）
