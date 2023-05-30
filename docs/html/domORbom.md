DOM 和 BOM 是两种不同的浏览器技术。

DOM（Document Object Model，文档对象模型）是一种用来表示 HTML 页面内容的树形结构模型，它将整个 HTML 页面转化成由节点（Node）和对象（Object）组成的树形结构，可以通过 JavaScript 和模拟用户操作来修改 HTML 页面中的内容和样式。

BOM（Browser Object Model，浏览器对象模型）是一种用来描述浏览器窗口和浏览器本身的对象模型，它为 JavaScript 提供了访问浏览器窗口和浏览器本身的接口，包括访问浏览器属性（如 URL、history）和浏览器窗口属性（如大小、位置）等。

下面是一些简单的 DOM 和 BOM 操作的示例：

DOM 操作示例：

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      .red {
        color: red;
      }
    </style>
  </head>
  <body>
    <p>This is a paragraph.</p>

    <script>
      // 选中并修改元素内容
      var para = document.querySelector("p");
      para.textContent = "This is a new paragraph.";

      // 给元素添加类名
      para.classList.add("red");

      // 创建新元素
      var newPara = document.createElement("p");
      newPara.textContent = "This is another new paragraph.";
      document.body.appendChild(newPara);
    </script>
  </body>
</html>
```

BOM 操作示例：

```html
<!DOCTYPE html>
<html>
  <head>
    <script>
      // 弹出提示框
      alert("Welcome to my website!");

      // 重定向页面
      window.location = "https://www.example.com";

      // 更新页面标题
      document.title = "My Website";

      // 打开一个新窗口
      var win = window.open("https://www.example.com", "_blank");
      win.focus();
    </script>
  </head>
  <body></body>
</html>
```

这些示例只是对 DOM 和 BOM 操作做出了一些简单的说明，DOM 和 BOM 是非常庞大复杂的技术，需要深入学习和应用才能掌握。
