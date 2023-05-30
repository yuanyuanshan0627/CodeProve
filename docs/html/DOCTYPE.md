DOCTYPE（文档类型）是一种用来告诉浏览器当前 HTML 文档类型的声明。DOCTYPE 的作用主要有以下两点：

1. 通知浏览器当前文档使用的 HTML 版本

DOCTYPE 的主要作用是告诉浏览器当前文档使用的 HTML 版本，以便浏览器能够正确解析文档并且按照规定的方式显示内容。如果没有正确指定 DOCTYPE，浏览器就会默认使用几乎没有任何规则限制的近似标准模式，这会导致不同浏览器对同一 HTML 页面的解析结果存在差异，严重影响网站的兼容性。

2. 规定浏览器文档解析的工作模式

DOCTYPE 还可以规定浏览器在解析文档时使用哪种解析模式，主要包括两种模式：

标准模式（Standards Mode，或 Strict Mode）：这种模式会尽可能地使文档在不同浏览器之间呈现一致。在此模式下，浏览器会忽略所有未知的 HTML 标签和属性，并根据规范严格执行内容布局和渲染。在 HTML5 中，标准模式是默认的模式。

怪异模式（Quirks Mode）：这种模式会在某些网页的旧版设计中扮演着重要角色，它会让浏览器采用一些旧式的渲染方式来解析页面内容，以便实现更好的向后兼容性。在怪异模式下，浏览器会忽略部分 HTML 标签和属性，同时也会忽略实现 CSS 的部分属性和属性值。

以下是 DOCTYPE 的一些常见示例：

- HTML 4.01 Strict DTD：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
```

- HTML 4.01 Transitional DTD：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
```

- HTML 4.01 Frameset DTD：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN" "http://www.w3.org/TR/html4/frameset.dtd">
```

- HTML5 DTD：

```html
<!DOCTYPE html>
```
