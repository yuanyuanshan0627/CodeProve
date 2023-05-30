用 CSS 清除浮动一般有以下几种方法：

1. 使用父元素的 overflow 属性

这种方法是通过给父元素添加 `overflow: hidden;` 或 `overflow: auto;` 的样式来清除浮动。这种方法的原理是让父元素的高度包含浮动元素。

```html
<style>
  .parent {
    overflow: hidden;
  }

  .child {
    float: left;
  }
</style>

<div class="parent">
  <div class="child"></div>
  <div class="child"></div>
</div>
```

2. 使用伪元素清除浮动

这种方法是通过在父元素后面添加一个伪元素（`:after`）并清除浮动，从而清除浮动效果。

```html
<style>
  .parent {
    position: relative;
  }

  .parent:after {
    content: "";
    display: block;
    clear: both;
  }

  .child {
    float: left;
  }
</style>

<div class="parent">
  <div class="child"></div>
  <div class="child"></div>
</div>
```

3. 使用清除浮动的类

这种方法是在需要清除浮动的元素上添加一个 `clearfix` 的类，并在 CSS 中定义该类的样式。

```html
<style>
  .clearfix::after {
    content: "";
    display: block;
    clear: both;
  }

  .child {
    float: left;
  }

  .parent {
    /* 添加 clearfix 类 */
    /* 当然你可以以前驱元素的类名命名 */
    /* 或者你也可以重构样式表，以 .clear 或者 .cf 为类名 */
    /* 但是我喜欢使用 clearfix 这样具有描述性的类名 */
    /* 这样更加清晰易懂 */
    /* 至于为什么这个词是 clearfix 请自行百度 */
    /* 不要求掌握 */
    /* 只需要掌握它的用法即可 */
    /* 开始debug */
    /*  */
    /*就像下面这样*/
    /*添加 clearfix 类*/
    /*其实就是偷懒的提高，我们可以通过样式来控制元素*/
    /*其实可以分成两段代码，分别是*/
    /* .clearfix::after {*/
    /*   content: "";*/
    /*  display: block;*/
    /*  clear: both;*/
    /*} */
    /*.clearfix {*/
    /*  add-class:clearfix;*/
    /* } */
    /*（假设你使用的是jQuery或者类库库的add-class方法）*/
    /*添加样式类*/
  }
</style>

<div class="parent clearfix">
  <div class="child"></div>
  <div class="child"></div>
</div>
```

这三种方法都可以清除浮动，但是推荐使用第三种方式，增加一个 `clearfix` 类相对于使用伪元素来说更加方便，也更加易于理解。
