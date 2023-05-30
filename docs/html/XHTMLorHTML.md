XHTML（可扩展超文本标记语言）是 HTML 的一个更为严格的版本。XHTML 的目标是使 HTML 文档更加符合 XML 的语法规则，以便让浏览器和解析器更容易地处理和显示这些文档。与 HTML 相比，XHTML 有以下几个主要区别：

1. XHTML 强制使用小写标签和属性名，并要求每个元素和属性都有相应的关闭标签。
2. XHTML 规定所有标签和属性都必须正确嵌套。
3. XHTML 要求使用 XML 命名空间来区分不同的标记。
4. XHTML 将所有属性值都用引号包含起来。
5. XHTML 还包括了一些 HTML 中不支持的新标签和属性。
   下面是一个使用 HTML 和 XHTML 编写一个简单网页的例子。

HTML 示例代码：

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Website</title>
  </head>
  <body>
    <h1>Welcome to my website!</h1>
    <p>This is some example text.</p>
  </body>
</html>
```

XHTML 示例代码：

```xml
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
  <head>
    <title>My Website</title>
  </head>
  <body>
    <h1>Welcome to my website!</h1>
    <p>This is some example text.</p>
  </body>
</html>
```

可以看出，HTML 中标签和属性名大小写不敏感，而 XHTML 强制使用小写命名并添加命名空间；HTML 中省略封闭标签是合法的，而 XHTML 中必须完整使用封闭标签。

总体来说，XHTML 更加规范和严格，可以提高文档的可读性和可维护性，但也需要更多的注意和细节处理，而 HTML 则更加灵活和容错。
