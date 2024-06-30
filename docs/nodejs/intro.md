# 概述

> <font color="red">注意：V7 版本目前处于开发中，本文档描述的功能模块在 V6 版本不可用</font>

## 启用 nodejs 引擎

默认情况下 js 文件由第一代引擎(Rhino)运行，当文件名由 mjs,cjs,node.js 结尾时使用 nodejs 引擎运行，以 mjs 结尾还会启用 esm 模块特性，这是推荐的运行方式

## 从全局变量改为导入模块

在第 2 代 api，所有模块都需要先导入才能使用，如

```js
import { showToast } from "toast";
```

........待补充

## autox v7 开发进度

- [x] **分离脚本引擎运行的进程（进行中）**
      使脚本运行在与 app 不同的进程，彻底解决脚本崩溃连同 app 一起崩溃的问题
- [ ] **迁移 app 界面至 m3 风格**
- [ ] **完善的插件扩展功能**
      使用一个独立的页面显示已安装和可下载的插件，采用激活/禁用的方式在每次运行脚本时自动加载插件，无需在代码中显式加载
- [x] **集成基于[Javet](https://github.com/caoccao/Javet)的 v8/nodejs 引擎**
- [ ] **nodejs 引擎功能模块适配**
- [ ] **全新的 ui 设计框架，采用 vue3 的[vue-core](https://github.com/vuejs/core)框架与[htm](https://github.com/developit/htm)模板引擎**
      基于新的引擎设计，支持组件和 vue 一样的响应式状态

## 参与开发基本操作

V7 版本开发目前由开发者【[aiselp](https://github.com/aiselp)】组成，如有兴趣共同参与开发和测试可加入本人创建的[tg 开发群](https://t.me/+bkx23tdbM6U3N2M1)交流

1. 首先确保你已经 fork 了此仓库，并且已拉取到本地并能够完成构建
2. 打开一个终端切换到项目目录输入

```shell
git remote add aiselp git@github.com:aiselp/AutoX.git
#更新远程仓库
git fetch --all
```

3. 创建并拉取 v7 分支
   ```shell
   git checkout -b setup-v7 aiselp/setup-v7
   ```
4. 推送到你的远程仓库并设置为默认
   `git push -u origin setup-v7`
   其中 origin 表示你的远程仓库名，可能并非为 origin
