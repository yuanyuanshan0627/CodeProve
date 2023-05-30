CSS 中的 `position` 属性用于指定元素在文档流中的定位方式。一般情况下，一个元素的定位方式可以设置为以下四种：

1. static（默认值）：元素在正常的文档流中（即没有设置 `position`)，并且忽略后续的 top, bottom, left, right 和 z-index 属性设置。在绝大多数情况下，不需要设置 static。

2. relative：元素相对于其原来的位置进行定位，不会脱离文档流。为元素本身预留了位置，并不会改变其他元素的位置。

3. absolute：元素相对于其最近的非 static（即 relative、absolute、fixed）定位祖先元素进行定位，会脱离文档流，并与其他元素重叠。如果最近的祖先元素不存在，则相对于 `viewport` 定位元素。

4. fixed：元素相对于 `viewport` 进行定位，与其他元素重叠。它始终会脱离文档流，并可以通过设置 top, right, bottom 和 left 属性来控制位置。

以下是 `position` 常用属性的详细解释：

- `top`：用于设置元素相对于它的父元素或者最近非 static 定位祖先元素顶部的偏移。
- `right`：用于设置元素相对于它的父元素或者最近非 static 定位祖先元素右侧的偏移。
- `bottom`：用于设置元素相对于它的父元素或者最近非 static 定位祖先元素底部的偏移。
- `left`：用于设置元素相对于它的父元素或者最近非 static 定位祖先元素左侧的偏移。
- `z-index`：用于改变元素的层级关系。元素的 z-index 值越大，其显示在顶部的概率就越高。

下面是一个元素用 `position` 属性实现相对定位的例子：

```html
<style>
  .container {
    position: relative;
    width: 300px;
    height: 200px;
  }
  .box {
    position: relative;
    top: 50px;
    left: 50px;
    width: 100px;
    height: 100px;
    background-color: red;
  }
</style>
<div class="container">
  <div class="box"></div>
</div>
```

下面是一个元素用 `position` 属性实现绝对定位的例子：

```html
<style>
  .container {
    position: relative;
    width: 300px;
    height: 200px;
  }
  .box {
    position: absolute;
    top: 50px;
    left: 50px;
    width: 100px;
    height: 100px;
    background-color: red;
  }
</style>
<div class="container">
  <div class="box"></div>
</div>
```

注意，在设置定位属性时，务必要清楚地知道自己想要实现的效果，同时还要注意不要将元素的相对和绝对定位混用，否则会产生不可预料的结果。
