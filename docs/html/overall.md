常见的布局方式有以下几种：

1. 块级布局（Block Layout）

块级布局指的是让元素按照块的形式垂直排列，每个元素会单独占用一行。主要用于构建网页中的主体结构。

```html
<style>
  div {
    width: 100px;
    height: 100px;
    background-color: red;
    margin-bottom: 10px;
  }
</style>

<div></div>
<div></div>
<div></div>
```

2. 行内布局（Inline Layout）

行内布局指的是元素按照内联的形式水平排列，每个元素之间没有换行，如果超过了容器的宽度则会自动折行。主要用于构建网页中的文本、链接和按钮等内容。

```html
<style>
  a {
    display: inline-block;
    padding: 10px;
    background-color: blue;
    color: white;
    text-align: center;
    text-decoration: none;
  }
</style>

<a href="#">Link 1</a>
<a href="#">Link 2</a>
<a href="#">Link 3</a>
```

3. 行内块级布局（Inline-Block Layout）

行内块级布局是行内和块级布局的结合体，具有内联元素的特点，同时也可以设置宽度、高度和 margin/padding 等样式属性。主要用于构建网页中的图标、图片和输入框等内容。

```html
<style>
  img {
    display: inline-block;
    width: 100px;
    height: 100px;
    margin-right: 10px;
  }
</style>

<img src="example.png" alt="An example image" />
<img src="example.png" alt="An example image" />
<img src="example.png" alt="An example image" />
```

4. 弹性布局（Flex Layout）

弹性布局是一种基于 CSS3 的布局方式，它可以自适应容器的大小和内容的大小，实现了在不同设备上的自适应布局。主要用于构建网页中复杂和多样化的布局。

```html
<style>
  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .item {
    width: 100px;
    height: 100px;
    background-color: red;
    margin-right: 10px;
  }
</style>

<div class="container">
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
</div>
```

除了以上四种基本布局方式，实际上还有很多其他的高级布局方式，例如栅格布局（Grid Layout）、多列布局（Multi-Column Layout）和流式布局（Responsive Layout）等，它们可以更加精细和灵活地控制网页中的布局效果。
