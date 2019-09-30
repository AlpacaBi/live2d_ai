

# 项目简介
本项目是我git服务器[Alpaca Bi的代码库](https://git.alpaca.run)右下角小人的源代码，基于live2d.js开发，我单独把她抽离了出来，你们可以嵌入到你们自己的网站里，演示demo地址如下：https://live2d.alpaca.run

# 安装与使用方法

### 关于聊天功能和图片识别功能
如果你不想加入聊天功能和图片识别功能，只是想单纯的加入个小人，可以跳过此步骤直接看下面安装教程，如果想，请往下看，巴拉巴拉巴拉巴拉（有空再更新）


### 安装过程
1. 直接把本项目下载下来
2. 下载完成后，复制`assets`文件夹，到你的项目跟目录下
3. 之后嵌入如下代码在你的index.html的body标签里面，放在最后body标签最后
```html

<input placeholder="和她聊天" id="talk"/>
<form id="uploadForm">
    <input type="file" name="file"/>
</form>
<div class="waifu">
    <div class="waifu-tips"></div>
    <canvas id="live2d" width="320" height="280" class="live2d"></canvas>
</div>
<script src="assets/waifu-tips.js"></script>
<script src="assets/live2d.js"></script>
<script type="text/javascript">initModel("assets/")</script>
```
4. 当然了也别忘记在你的index.html的head标签里，加入以下代码

```html
<link rel="manifest" href="%PUBLIC_URL%/manifest.json">
    <link rel="stylesheet" type="text/css" href="assets/waifu.css"/>
    <script src="https://cdn.bootcss.com/jquery/3.2.1/jquery.min.js"></script>
```

### 自定义交互功能
她可以监听到你的鼠标移动到或者点击某个元素，并给出相应的反应，实现这个功能你可以去`assets/waifu-tips.json`文件里配置，很简单的你一看demo源码就秒懂了