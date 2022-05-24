# Zips(基于P7zip实现的的压缩解压功能)

## 压缩

### result = zips.A(type, filePath, dirPath, password)
* filePath {string} 压缩后的文件路径(必须是完整路径)
* dirPath {string} 要压缩的目录路径(必须是完整路径)
* type {string} 压缩类型，支持的压缩类型包括:zip 7z bz2 bzip2 tbz2 tbz gz gzip tgz tar wim swm xz txz等。
* password {string} 压缩密码
* result {number} 返回值，P7zip默认的退出代码。

### result = zips.A(type, filePath, dirPath)
* filePath {string} 压缩后的文件路径(必须是完整路径)
* dirPath {string} 要压缩的目录路径(必须是完整路径)
* type {string} 压缩类型，支持的压缩类型包括:zip 7z bz2 bzip2 tbz2 tbz gz gzip tgz tar wim swm xz txz等。
* result {number} 返回值，P7zip默认的退出代码。

### 示例
```javascript
var filePath = "/sdcard/脚本.7z";
var dirPath = "/sdcard/脚本";
var type = "7z";
var password = "password"
switch (zips.A(type, filePath, dirPath)) {
    case 0:
        toastLog("压缩成功！文件已保存为： " + filePath)
        break;
    case 1:
        toastLog("压缩结束，存在非致命错误（例如某些文件正在被使用，没有被压缩）")
        break;
    case 2:
        toastLog("致命错误")
        break;
    case 7:
        toastLog("命令行错误")
        break;
    case 8:
        toastLog("没有足够内存")
        break;
    case 255:
        toastLog("用户中止操作")
        break;
    default: toastLog("未知错误")
}
```

## 解压(若文件已存在则跳过)
### result = zips.X(filePath, dirPath, password)
* filePath {string} 要解压的文件路径(必须是完整路径)。支持的解压缩类型包括：zip、7z、bz2、bzip2、tbz2、tbz、gz、gzip、tgz、tar、wim、swm、xz、txz以及rar、chm、iso、msi等众多格式。
* dirPath {string} 解压后的目录路径(必须是完整路径)
* password {string} 压缩密码
* result {number} 返回值，P7zip默认的退出代码。

### result = zips.X(filePath, dirPath)
* filePath {string} 压缩文件路径(必须是完整路径)
* dirPath {string} 目录路径(必须是完整路径)
* result {number} 返回值，P7zip默认的退出代码。

### 示例
```javascript
var filePath = "/sdcard/脚本.7z";
var dirPath = "/sdcard/脚本";
var type = "7z";
var password = "password"
switch (zips.X(filePath, dirPath, password)) {
    case 0:
        toastLog("解压缩成功！请到 " + dirPath + " 目录下查看。")
        break;
    case 1:
        toastLog("压缩结束，存在非致命错误（例如某些文件正在被使用，没有被压缩）")
        break;
    case 2:
        toastLog("致命错误")
        break;
    case 7:
        toastLog("命令行错误")
        break;
    case 8:
        toastLog("没有足够内存")
        break;
    case 255:
        toastLog("用户中止操作")
        break;
    default: toastLog("未知错误")
}
```

## 7zip命令行使用参考

### 7z|7za 子命令 [参数开关] 压缩包  [<文件名称>|<@列表文件...>]
在方括号内的表达式(“[” 和 “]”之间的字符)是可选的。在书名号内的表达式(“<” 和 “>”之间的字符)是必须替换的表达式(而且要去掉括号)。
7-Zip 支持和 Windows 相类似的通配符：
“*”可以使用星号代替零个或多个字符。
“?”可以用问号代替名称中的单个字符。
如果只用 `*`，7-Zip 会将其视为任何扩展名的全部文件。
#### 子命令
* a: 添加到压缩文件
* b: 基准测试
* d: 从档案中删除文件
* e: 解压档案文件 (无目录名称)
* l: 列出压缩文件内容
* t: 测试压缩文件的完整性
* u: 更新文件到压缩文件中
* x: 完整路径下解压文件
#### 参数开关
* -ai[r[-|0]]{@列表文件|!通配符}: 包括 压缩文件
* -ax[r[-|0]]{@列表文件|!通配符}: 排除 压缩文件
* -bd: 禁用百分比显示功能
* -i[r[-|0]]{@列表文件|!通配符}: 包括 文件名称
* -m<参数>，关于它有许多参数及指令，这里仅介绍简单且常用的用法。
  -m0=<压缩算法> 默认使用 lzma
  -md=<字典大小> 设置字典大小,例如 -md=32m
  -mfb=64 number of fast bytes for LZMA = 64
  -ms=<on|off> 是否固实压缩
  -mx=<1~9> 压缩级别-m0=压缩算法    默认使用 lzma
  -mx=数字    1~9 压缩级别
* -o{目录}: 设置输出目录
* -p{密码}: 设置密码
* -r[数字]: 递归子目录，使用数字定义递归子目录的深度
* -scs{UTF-8 | WIN | DOS}: 设置列表文件的编码格式
* -sfx[{名称}]: 创建 SFX 自解压文件
* -si[{名称}]: 从stdin(标准输入设备)读取数据
* -slt: 为 l (列表) 命令显示技术信息
* -so: 将数据写入stdout(标准输出设备)
* -ssc[-]: 设置大小写区分模式
* -ssw: 压缩共享文件
* -t{类型}: 设置压缩文件格式，(7z, zip, gzip, bzip2 or tar. 7z是默认的格式)
* -v{大小}[b|k|m|g]: 分卷压缩
* -u[-][p#][q#][r#][x#][y#][z#][!新建档案_名称]: 更新选项
* -w[{路径}]: 指定工作目录，路径为空时代表临时文件夹目录
* -x[r[-|0]]]{@列表文件|!通配符}: 排除 文件名称
* -y: 所有询问选是


#### 退出代码
* 0 ：正常，没有错误
* 1 ：警告，没有致命的错误，例如某些文件正在被使用，* 没有被压缩
* 2 ：致命错误
* 7 ：命令行错误
* 8 ：没有足够的内存
* 255 ：用户中止了操作

