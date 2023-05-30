标准模式和兼容模式是指浏览器的渲染模式，它们区别如下：

1. 标准模式：浏览器按照 W3C 标准对网页进行渲染，包括 CSS、布局、盒模型等方面的实现。

2. 兼容模式：浏览器采用向后兼容的方式来渲染网页，保留了一些旧版本浏览器的渲染特性，以确保旧版网页的正确显示。

下面是示例代码，分别定义了标准模式和兼容模式：

标准模式：

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>Standard Mode</title>
    <style>
      div {
        width: 200px;
        height: 200px;
        background-color: red;
      }
    </style>
  </head>
  <body>
    <div></div>
  </body>
</html>
```

当使用标准模式时，div 元素将按照 CSS 盒模型的标准解析，即元素的 width 和 height 属性只包括内容区域，而不包括边框和内边距，因此宽度和高度为 200px。

兼容模式：

```html
<!DOCTYPE html>
<html>
  <head>
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <title>Compat Mode</title>
    <style>
      div {
        width: 200px;
        height: 200px;
        background-color: red;
      }
    </style>
  </head>
  <body>
    <div></div>
  </body>
</html>
```

当使用兼容模式时，div 元素将按照旧版的盒模型解析，即元素的 width 和 height 属性包括了边框和内边距，因此实际的宽度和高度会比指定的大。
