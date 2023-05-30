CSS 选择器用于选择需要应用样式的元素，CSS 中常见的选择器包括以下几种：

1. 标签选择器

通过标签名选择元素，应用相应样式。

```css
p {
  color: red;
}
```

2. 类选择器

通过类名选择元素，应用相应样式。

```css
.warning {
  color: yellow;
}
```

3. ID 选择器

通过元素的唯一标识选择元素，应用相应样式。

```css
#myDiv {
  background-color: blue;
}
```

4. 属性选择器

通过元素的属性选择元素，应用相应样式。

```css
input[type="text"] {
  border: 1px solid green;
}
```

5. 伪类选择器

通过元素的状态或位置选择元素，应用相应样式。

```css
a:hover {
  color: purple;
}
```

常见的伪类选择器还包括:visited、active、focus 等。

6. 伪元素选择器

通过元素的某些部分选择元素，应用相应样式。

```css
p::before {
  content: "Chapter: ";
  font-weight: bold;
}
```

常见的伪元素选择器还包括::after 等。

7. 组合选择器

通过不同的方式组合选择器，选择满足要求的元素，应用相应样式。

```css
p.warning {
  color: yellow;
}
```

在上面的例子中，p 和.warning 共同组成了一个组合选择器，选中具有.warning 类的 p 元素。

这些是 CSS 中最常用的选择器，但不是全部。选择器在 CSS 中起着非常重要的作用，掌握不同类型的选择器使用方法是 CSS 开发的基础。
