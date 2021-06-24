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
