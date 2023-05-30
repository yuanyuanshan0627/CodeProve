水平垂直居中一个元素可以使用 CSS 中的 `display:flex` 和 `justify-content:center` 以及 `align-items:center` 或者 `position`+`transform` 属性来实现。以下是两种方法的示例代码：

1. 使用 `display:flex` 和 `justify-content:center` 以及 `align-items:center` 的方法

```html
<style>
  .container {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100vw;
    height: 100vh;
  }
  .box {
    width: 100px;
    height: 100px;
    background-color: red;
  }
</style>
<div class="container">
  <div class="box"></div>
</div>
```

2. 使用 `position`+`transform` 属性的方法

```html
<style>
  .container {
    position: relative;
    width: 100vw;
    height: 100vh;
  }
  .box {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 100px;
    height: 100px;
    background-color: red;
  }
</style>
<div class="container">
  <div class="box"></div>
</div>
```

以上两种方法都可以实现元素在父元素中水平垂直居中的效果。第一种方法适用于大多数情况下，而第二种方法在某些情况下，例如一个父元素中有多个元素都需要居中，且它们的大小不同，就比较适用。
