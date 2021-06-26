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
