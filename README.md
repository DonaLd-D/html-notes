## HTML可以将元素分类方式分为`行内元素`、`块状元素`和`行内块状`元素三种。
- display:inline;转换为行内元素
- display:block;转换为块状元素
- display:inline-block;转换为行内块状元素

### 块级元素
- 能够识别宽高
- margin和padding的上下左右均对其有效
- 可以自动换行
- 多个块状元素标签写在一起，默认排列方式为从上至下

### 行内块元素
- 不自动换行
- 能够识别宽高
- 默认排列方式为从左到右

### 行内元素
- 设置宽高无效
- 对margin仅设置左右方向有效，上下无效；
- padding设置上下左右都有效，即会撑大空间
- 不会自动进行换行

***
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

| 格式 |          |
|   :----|  :----|
| `<abbr>`  | 定义一个缩写|
| `<address>` | 定义文档作者或拥有者的联系信息|
| `<b>`|    定义粗体文本|
| `<bdi>`|  允许您设置一段文本，使其脱离父元素的文本方向设置|
| `<bdo>`|  定义文本的方向|
| `<blockquote>`|   定义块引用|
| `<cite>`| 定义引用|
| `<code>`| 定义计算机代码|
| `<del>`|  定义被删除的文本|
| `<dfn>`|  定义项目|
|   `<em>`| 定义强调文本|
|   `<i>`|  定义斜体文本 |
|   `<ins>`|    定义被插入文本|
|   `<kbd>`|    定义键盘文本|
|   `<mark>`|   定义带有记号的文本|
|   `<meter>`|  定义度量衡，仅用于已知最大和最小值的度量|
|   `<pre>`|    定义预格式文本|
|   `<progress>`|   定义运行中的任务进度|
|   `<q>`|  定义短的引用|
|   `<rp>`| 定义不支持ruby元素的浏览器所显示的内容|
|   `<rt>`| 定义字符的解释或发音|
|   `<ruby>`|   定义ruby注释|
|   `<s>`|  定义加删除线的文本|
|   `<samp>`|   定义计算机代码样本|
|   `<small>`|  定义小号文本|
|   `<strong>`| 定义语气更为强烈的强调文本|
|   `<sub>`|    定义下标文本|
|   `<sup>`|    定义上标文本|
|   `<time>`|   定义一个日期/时间|
|   `<u>`|  定义下划线文本|
|   `<var>`|    定义文本的变量部分|
|   `<wbr>`|    规定在文本中的何处适合添加换行符|

|   表单  |     |
|   :----|:----|
|   `<form>`|   定义一个html表单，用于用户输入|
|   `<input>`|  定义一个输入控件|
|   `<textarea>`|   定义多行的文本输入控件|
|   `<button>`| 定义按钮|
|   `<select>`| 定义选择列表|
|   `<optgroup>`|   定义选择列表中相关选项的组合|
|   `<option>`| 定义选择列表中的的选项|
|   `<label>`|  定义input元素的标注|
|   `<fieldset>`|   定义围绕表单中的元素的边框|
|   `<legend>`| 定义fieldset元素的标题|
|   `<datalist>`|   规定了input元素可能的选项列表|
|   `<keygen>`| 规定用于表单的密钥对生成器字段|
|   `<output>`| 定义一个计算的结果|

|   框架|     |
|   :----|  :----   |
|   `<iframe>`| 定义内联框架  |

|   图像  |       |
|   :----   |   :----   |
|   `<img>`|    定义图像|
|   `<map>`|    定义图像映射|
|   `<area>`|   定义图像地图内部的区域|
|   `<canvas>`| 通过脚本来绘制图形|
|   `<figcaption>`| 定义一个captioon for a `<figure>` element|
|   `<figure>`| figure标签用于对元素进行组合|
    
|   audio/video|        |
|   :----   |  :----    |
|   `<audio>`|  定义声音，比如音乐或其他音频流|
|   `<source>`| 定义media元素的媒体资源  |
|   `<track>`|  为媒体元素定义外部文本轨道   |
|   `<video>`|  定义一个音频活着视频|

|   链接  |       |
|   :----|  :----|
|   `<a>`|  定义一个链接  |
|   `<link>`|   定义文档与外部资源的关系    |
|   `<main>`|   定义文档的主体部分   |
|   `<nav>`|    定义导航链接  |

|   列表  |       |
|   :----   |  :----    |
|   `<ul>`| 定义一个无序列表    |
|   `<ol>`| 定义一个有序列表    |
|   `<li>`| 定义一个列表项 |
|   `<dl>`| 定义一个定义列表|
|   `<dt>`| 定义一个定义列表中的项目    |
|   `<dd>`| 定义列表中项目的描述  |
|   `<menu>`|   定义菜单列表  |
|   `<command>`|    定义可能调用的命令|

|   表格  |       |
|   :----   |   :----   |
|   `<table>`|  定义一个表格  |
|   `<caption>`|    定义表格标题  |
|   `<th>`| 定义表格中的表头单元格 |
|   `<tr>`| 定义表格中的行 |
|   `<td>`| 定义表格中的单元|
|   `<thead>`|  定义表格中的表头内容  |
|   `<tbody>`|  定义表格中的主体内容  |
|   `<tfoot>`|  定义表格中的表注内容  |
|   `<col>`|    定义表格中的一个或多个列的属性值  |
|   `<colgroup>`|  定义表格中供格式化的列组 |

|   样式/节    |       |
|   :----   |   :----   |
|   `<style>`|  定义文档的样式信息|
|   `<div>`|    定义文档中的节|
|   `<span>`|   定义文档中的节|
|   `<header>`| 定义一个文档头部部分|
|   `<footer>`| 定义一个底部|
|   `<section>`|   定义文档中的某个区域 |
|   `<article>`|    定义一个文章内容|
|   `<aside>`|  定义其所处内容之外的内容|
|   `<details>`|    定义了用户可见的或隐藏的需求的补充细节|
|   `<dialog>`| 定义了一个对话框或者窗口|
|   `<summary>`|    定义了一个可见的标题。当用户点击标题时会显示出详细信息|

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

```
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
