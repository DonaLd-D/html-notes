## HTML可以将元素分类方式分为`行内元素`、`块状元素`和`行内块状`元素三种。
- display:inline;转换为行内元素
- display:block;转换为块状元素
- display:inline-block;转换为行内块状元素

### 块级元素(典型：div，很多标签可以看作div的衍生标签)
- 能够识别宽高
- margin和padding的上下左右均对其有效
- 可以自动换行
- 多个块状元素标签写在一起，默认排列方式为从上至下

### 行内块元素（典型：span,很多标签可以看作span的衍生标签）
- 不自动换行
- 能够识别宽高
- 默认排列方式为从左到右

### 行内元素
- 设置宽高无效
- 对margin仅设置左右方向有效，上下无效；
- padding设置上下左右都有效，即会撑大空间
- 不会自动进行换行

### 头部（head标签，不会渲染成dom树）
- title
    - 定义了浏览器工具栏的标题
    - 当网页添加到收藏夹时，显示在收藏夹中的标题
    - `显示在搜索引擎结果页面的标题`
- 网页标题图片:`<link rel="shortcut icon" href="图片url">`
- 为搜索引擎定义关键词:`<meta name="keywords" content="HTML, CSS, XML, XHTML, JavaScript">`
- 为网页定义描述内容: `<meta name="description" content="免费 Web & 编程 教程">`

***
## `HTML标签`
|  基础       |          |
|  :----  | :----  |
| `<!DOCTYPE>` | 定义文档类型 |
| `<html>`  | 定义一个HTML文档 |
| `<title>`| 为文档定义一个标题|
| `<body>`| 定义文档的主体|
| `<h1>` to `<h6>`|定义html标题|
| `<p>` |定义一个段落|
| `<br>`|定义简单的折行|
| `<hr>`|定义水平线|
|`<!--...-->`|定义一个注释|

|   链接  |       |
|   :----|  :----|
|   `<a>`|  定义一个链接  |
|   `<link>`|   定义文档与外部资源的关系    |
|   `<main>`|   定义文档的主体部分   |
|   `<nav>`|    定义导航链接  |

|   元信息|        |
|   :----|  :----|
|   `<head>`|   定义关于文档的信息|
|   `<meta>`|   定义关于html文档的元信息|
|   `<base>`|   定义页面中所以链接的默认地址或默认目标|

|   程序|     |
|   :---|   :---|
|   `<script>`| 定义客户端脚本|
|   `<noscript>`|   定义针对不支持客户端脚本的用户的替代内容|
|   `<embed>`|  定义了一个容器，用来嵌入外部应用或者互动程序|
|   `<object>`| 定义 嵌入的对象|
|   `<param>`|  定义对象的参数|
***
    
## `HTML5`
```
最新的修订版本，2014年10月由万维网联盟（W3C）完成标准制定。
```
#### HTML5新元素
- `<canvas>` 新元素
- 新多媒体元素
  - audio
  - video
  - source
  - embed
  - track
- 新表单元素
  - datalist
  - keygen
  - output
- 新的语义和结构元素
  - HTML5提供了新的元素来创建更好的页面结构

#### HTML5 Canvas
- `<canvas>` 标签定义图形，比如图表和其他图像，您必须使用脚本来绘制图形

#### SVG
- SVG 指可伸缩矢量图形 (Scalable Vector Graphics)
- SVG 用于定义用于网络的基于矢量的图形
- SVG 使用 XML 格式定义图形
- SVG 图像在放大或改变尺寸的情况下其图形质量不会有损失
- SVG 是万维网联盟的标准
#### HTML5 拖放（Drag 和 Drop）
```html
<script>
function allowDrop(ev){
    ev.preventDefault();
}
function drag(ev){
    ev.dataTransfer.setData("Text",ev.target.id);
}
 
function drop(ev){
    ev.preventDefault();
    var data=ev.dataTransfer.getData("Text");
    ev.target.appendChild(document.getElementById(data));
}
</script>
</head>
<body>
<p>拖动图片到矩形框中:</p>
<div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)"></div>
<br>
<img loading="lazy" id="drag1" src="/images/logo.png" draggable="true" ondragstart="drag(event)" width="336" height="69">
</body>
```
#### HTML5 Geolocation（地理定位）
```js
var dom=document.getElementById("demo");
function getLocation(){
    if (navigator.geolocation){
        navigator.geolocation.getCurrentPosition(showPosition,showError);
    }else{
        dom.innerHTML="该浏览器不支持获取地理位置。";
    }
}
function showPosition(position){
    dom.innerHTML="纬度: " + position.coords.latitude + 
    "<br>经度: " + position.coords.longitude;    
}
function showError(error){
    switch(error.code) {
        case error.PERMISSION_DENIED:
            dom.innerHTML="用户拒绝对获取地理位置的请求。"
            break;
        case error.POSITION_UNAVAILABLE:
            dom.innerHTML="位置信息是不可用的。"
            break;
        case error.TIMEOUT:
            dom.innerHTML="请求用户地理位置超时。"
            break;
        case error.UNKNOWN_ERROR:
            dom.innerHTML="未知错误。"
            break;
    }
}
```
#### HTML5 Video(视频)
- [网页的视频是如何工作的](https://baijiahao.baidu.com/s?id=1677080286604476353&wfr=spider&for=pc)
#### HTML5 Audio(音频)
- HTML5 提供了播放音频文件的标准。
#### HTML5 新的 Input 类型
- color
- date
- datetime `chrome不支持`
- datetime-local `无时区`
- email
- month
- number
- range
- search
- tel
- time
- url
- week
#### HTML5 表单元素
- `<datalist>`
- `<keygen>`
- `<output>`

#### HTML5 语义元素
- 无语义 元素实例: `<div>` 和 `<span>` - 无需考虑内容
- 语义元素实例: `<form>`, `<table>`, and `<img>` 清楚的定义了它的内容

#### HTML5 Web 存储
- localStorage - 用于长久保存整个网站的数据，保存的数据没有过期时间，直到手动去除
- sessionStorage - 用于临时保存同一窗口(或标签页)的数据，在关闭窗口或标签页之后将会删除这些数据
```js
// 存储
localStorage.sitename = "早鸟教程";
// 查找
document.getElementById("result").innerHTML = localStorage.sitename;
//删除
localStorage.removeItem("sitename");

// 保存数据：localStorage.setItem(key,value);
// 读取数据：localStorage.getItem(key);
// 删除单个数据：localStorage.removeItem(key);
// 删除所有数据：localStorage.clear();
// 得到某个索引的key：localStorage.key(index);
```

#### HTML5 应用程序缓存
- 使用 HTML5，通过创建 cache manifest 文件，可以轻松地创建 web 应用的离线版本

#### HTML5 `Web Workers`
- 由于 web worker 位于外部文件中，它们无法访问下列 JavaScript 对象：
  - window 对象
  - document 对象
  - parent 对象
```html
<body>
<p>计数： <output id="result"></output></p>
<button onclick="startWorker()">开始工作</button> 
<button onclick="stopWorker()">停止工作</button>
<p><strong>注意：</strong> Internet Explorer 9 及更早 IE 版本浏览器不支持 Web Workers.</p>
<script>
var w;
function startWorker() {
    if(typeof(Worker) !== "undefined") {
        if(typeof(w) == "undefined") {
            w = new Worker("demo_workers.js");
        }
        w.onmessage = function(event) {
            document.getElementById("result").innerHTML = event.data;
        };
    } else {
        document.getElementById("result").innerHTML = "抱歉，你的浏览器不支持 Web Workers...";
    }
}
function stopWorker() { 
    w.terminate();
    w = undefined;
}
</script>
</body>
```
```js
//demo_workers.js
var i=0;
function timedCount(){
    i=i+1;
    postMessage(i);
    setTimeout("timedCount()",500);
}
timedCount();
```
#### HTML5 `WebSocket`
- 在 WebSocket API 中，浏览器和服务器只需要做一个握手的动作，然后，浏览器和服务器之间就形成了一条快速通道
- HTML5 定义的 WebSocket 协议，能更好的节省服务器资源和带宽，并且能够更实时地进行通讯

***
## HTML DOM `Document` 对象
- 当浏览器载入 HTML 文档, 它就会成为 Document 对象。
- Document 对象是 HTML 文档的根节点。
- Document 对象使我们可以从脚本中对 HTML 页面中的所有元素进行访问。
- 提示：Document 对象是 Window 对象的一部分，可通过 window.document 属性对其进行访问。

|   属性/方法   |   描述  |
|   :----|  :----   |
|   document.activeEvent    |   返回当前获取焦点元素  |
|   document.addEventListener|  向文档添加句柄 |
|   document.adoptNode(node)|   从另外一个文档返回adapded节点到当前文档 |
|   document.anchors    |   返回对文档中所有Anchor对象的引用 |
|   document.baseURI    |   返回文档的绝对基础URI        |
|   document.body|  返回文档的body元素 |
|   document.close()|   关闭用document.open()方法打开的输出流，并显示选定的数据 |
|   document.cookie|    设置或返回与当前文档有关的所有cookie   |
|   document.createAttribute()| 创建一个属性节点    |
|   document.createComment()|   createComment()方法可创建注释节点    |
|   document.createDocumentFragment()|  创建空的DocumentFragment对象，并返回此对象|
|   document.createElement()|   创建元素节点|
|   document.createTextNode()|  创建文本节点|
|   document.doctype|   返回与文档相关的文档类型声明（DTD）|
|   document.documentElement|   返回文档的根节点|
|   document.documentMode|  返回用于通过浏览器渲染文档的模式|
|   document.documentURI|   设置或返回文档的位置|
|   document.domain|    返回当前文档的域名|
|   document.embeds|    返回文档中所有嵌入的内容集合|
|   document.forms| 返回对文档中所有Form对象引用|
|   document.getElementsByClassName()|  返回文档中所有制定类名的元素集合，作为NodeList对象|
|   document.getElementById()|  返回对拥有指定id的第一个对象的引用|
|   document.getElementsByName()|   返回带有指定名称的对象集合|
|   document.getElementsByTagName()|    返回带有指定标签名的对象集合|
|   document.images||
|   document.implementation||
|   document.importNode()||
|   document.inputEncoding||
|   document.lastModified||
|   document.links||
|   document.normalize()||
|   document.normalizeDocument()||
|   document.open()||
|   document.querySelector()||
|   document.querySelectorAll()||
|   document.readyState||
|   document.referrer||
|   document.removeEventListener()||
|   document.renameNode()||
|   document.scripts||
|   document.stricErrorChecking||
|   document.title||
|   document.URL||
|   document.write()||
|   document.writeIn()||

***

## 自定义一个hello标签。(造原始轮子的思路)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>hello</title>
</head>
<body>
    <hello>hello</hello>
</body>
<script>
    function customTag(tagName, fn){
        Array
            .from(document.getElementsByTagName(tagName))
            .forEach(fn);
    }
    function greetingHandler(element) {
        element.style.width='100px';
        element.style.height='50px';
        element.style.border='1px solid red';
        element.style.position='absolute';
        element.style.top='50%';
        element.style.left='50%';
        element.style.transform='translateX(-50px) translateY(-25px)';
    }   
    customTag('hello', greetingHandler);
</script>
</html>
```
