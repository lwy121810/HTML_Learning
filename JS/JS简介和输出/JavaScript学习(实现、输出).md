# JavaScript学习

HTML中的脚本必须位于`<script></script>`标签之间。
脚本可以被放置在HTML页面中的`<body>`和`<head>`部分中。

***

### `<script>`标签
如需在HTML页面中插入JavaScript，请使用`<script>`标签。

`<script>` 和 `</script>` 会告诉 JavaScript 在何处开始和结束。
`<script>` 和 `</script>` 之间的代码行包含了 JavaScript：

```
<script>
alert("My First JavaScript");
</script>
```

您无需理解上面的代码。只需明白，浏览器会解释并执行位于 `<script> `和 `</script>` 之间的 JavaScript。

那些老旧的实例可能会在 `<script>` 标签中使用 `type="text/javascript"`。现在已经不必这样做了。JavaScript 是所有现代浏览器以及 HTML5 中的默认脚本语言。

### `<body>` 中的 JavaScript
在本例中，JavaScript 会在页面加载时向 HTML 的 `<body>` 写文本：

实例

```
<!DOCTYPE html>
<html>
<body>
.
.
<script>
document.write("<h1>This is a heading</h1>");
document.write("<p>This is a paragraph</p>");
</script>
.
.
</body>
</html>
```
***
### JavaScript 函数和事件
上面例子中的 JavaScript 语句，会在页面加载时执行。
通常，我们需要在某个事件发生时执行代码，比如当用户点击按钮时。
如果我们把 JavaScript 代码放入函数中，就可以在事件发生时调用该函数。
***
###`<head>` 或 `<body>` 中的 JavaScript
您可以在 HTML 文档中放入不限数量的脚本。
脚本可位于 HTML 的 `<body>` 或 `<head>` 部分中，或者同时存在于两个部分中。

通常的做法是把函数放入 `<head>` 部分中，或者放在页面底部。这样就可以把它们安置到同一处位置，不会干扰页面的内容。

***

###`<head>` 中的 JavaScript 函数
在本例中，我们把一个 JavaScript 函数放置到 HTML 页面的 `<head>` 部分。

该函数会在点击按钮时被调用：

实例

```
<!DOCTYPE html>
<html>

<head>
<script>
function myFunction()
{
document.getElementById("demo").innerHTML="My First JavaScript Function";
}
</script>
</head>

<body>

<h1>My Web Page</h1>

<p id="demo">A Paragraph</p>

<button type="button" onclick="myFunction()">Try it</button>

</body>
</html>
```

***

### `<body>` 中的 JavaScript 函数
在本例中，我们把一个 JavaScript 函数放置到 HTML 页面的 `<body>` 部分。

该函数会在点击按钮时被调用：

实例

```
<!DOCTYPE html>
<html>
<body>

<h1>My Web Page</h1>

<p id="demo">A Paragraph</p>

<button type="button" onclick="myFunction()">Try it</button>

<script>
function myFunction()
{
document.getElementById("demo").innerHTML="My First JavaScript Function";
}
</script>

</body>
</html>
```

**提示：**我们把 JavaScript 放到了页面代码的底部，这样就可以确保在 <p> 元素创建之后再执行脚本。

***

###外部的 JavaScript
也可以把脚本保存到外部文件中。外部文件通常包含被多个网页使用的代码。
外部 JavaScript 文件的文件扩展名是 .js。
如需使用外部文件，请在 `<script>` 标签的 "src" 属性中设置该 .js 文件：

实例

```
<!DOCTYPE html>
<html>
<body>
<script src="myScript.js"></script>
</body>
</html>
```

在 `<head>` 或 `<body>` 中引用脚本文件都是可以的。实际运行效果与在 `<script>` 标签中编写脚本完全一致。\

**提示：外部脚本不能包含 `<script> `标签。**

***

### 操作HTML元素
如需从JavaScript访问某个HTML元素，可以使用document.getElementById(id)方法。 使用id属性来标识HTML元素；

例子

通过指定的 id 来访问 HTML 元素，并改变其内容：

```
<!DOCTYPE html>
<html>
<body>

<h1>我的第一张网页</h1>

<p id="demo">我的第一个段落</p>

<script>
document.getElementById("demo").innerHTML="我的第一段 JavaScript";
</script>

</body>
</html>
```

JavaScript 由 web 浏览器来执行。在这种情况下，浏览器将访问 id="demo" 的 HTML 元素，并把它的内容（innerHTML）替换为 "My First JavaScript"。

***

### 写到文档输出

下面的例子直接把 <p> 元素写到 HTML 文档输出中：

实例

```
<!DOCTYPE html>
<html>
<body>

<h1>我的第一张网页</h1>

<script>
document.write("<p>我的第一段 JavaScript</p>");
</script>

</body>
</html>
```

####警告
请使用 document.write() 仅仅向文档输出写内容。
如果在文档已完成加载后执行 document.write，整个 HTML 页面将被覆盖：