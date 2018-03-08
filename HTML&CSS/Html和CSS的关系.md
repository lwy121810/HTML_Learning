## Html和CSS的关系

1. **HTML是网页内容的载体。** 内容就是用户浏览的信息，可以是文字，图片，视频等
2. **CSS样式是表现**。就像网页的外衣。比如标题的字体 颜色变化，背景图片 边框等。所有改变内容外观的东西称之为表现
3. **JavaScript是用来实现网页上的特效效果**。 比如：鼠标滑过表格的背景颜色改变。有动画的 有交互的一般都是用javaScript来实现的

* 个人理解： HTML就像是数据 CSS就是UI， JavaScript是交互 动画等


###  Html的标签
1. 标签由英文尖括号`<`和`>`括起来，如`<html>`就是一个标签。
2. html中的标签一般都是成对出现的，分开始标签和结束标签。结束标签比开始标签多了一个`/`。
3. 标签与标签之间是可以嵌套的，但先后顺序必须保持一致，如：`<div>`里嵌套`<p>`，那么`</p>`必须放在`</div>`的前面。
4. HTML标签不区分大小写，`<h1>`和`<H1>`是一样的，但建议小写，因为大部分程序员都以小写为准。

###  认识html文件基本结构
一个HTML文件是有自己固定的结构的

```
<html>
    <head>...</head>
    <body>...</body>
</html>

```
1. `<html></html>`称为根标签，所有的网页标签都在其中
2. `<head>`标签用于定义文档的头部，它是所有头部元素的容器， 头部元素有`<title>``<script>``<style>``<link>``<meta>`等
3. 在`<body>``</body>`标签之间的内容是网页的主要内容。如`<h1>``<p>``<a>``<img>`等网页内容标签


### 认识head标签
文档的头部描述了文档的各种属性和信息，包括文档的标题等。绝大多数文档头部包涵的数据都不会真正作为内容展示给读者。

`<title>`:在`<title>`和`</title>`标签之间的文字内容是网页的标题信息，它会出现在浏览器的标题栏中。网页的title标签用于告诉用户和搜索引擎这个网页的主要内容是什么，搜索引擎可以通过网页标题，迅速的判断出网页的主题。每个网页的内容都是不同的，每个网页都应该有一个独一无二的`title`。

HTML代码注释语法：

`<!--注释文字 -->`

### body标签
#### 1.	`<p>`标签 添加段落

 **语法：** `<p>段落文本</p>`
>  一段文字一个`<p>` 标签。

#### 2. <hx>标签 为网页添加标题
标题标签一共有6个，h1、h2、h3、h4、h5、h6分别为一级标题、二级标题、三级标题、四级标题、五级标题、六级标题。并且依据重要性递减。`<h1>`是最高的等级。

**语法:**  `<hx>`标题文本`</hx>` (x为1-6)

>  因为h1标签在网页中比较重要，所以一般h1标签被用在网站名称上

#### 3. `<strong>` `<em>`标签
`<em>`默认使用斜体表示 `<strong>`用粗体表示

**语法：**

`<em>`需要强调的文本`</em>  `

`<strong>`需要强调的文本`</strong>` 

#### 使用`<span>`标签为文字设置单独样式
`<span>`标签是没有语义的，它的作用就是为了**设置单独的样式用的**

**语法：**
`<span>`文本`</span>`


#### `<q>`标签，短文本引用
**语法：**

`<q>`引用文本`</q>`
> 要引用的文本不用加双引号，浏览器会对q标签自动添加双引号。
> 
> 这里用<q>标签的真正关键点不是它的默认样式双引号（如果这样我们不如自己在键盘上输入双引号就行了），而是它的语义：引用别人的话。

#### `<blockquote>`标签，长文本引用
`<blockquote>`的作用也是引用别人的文本。但它是对长文本的引用，如在文章中引入大段某知名作家的文字，这时需要这个标签。

**语法:**

`<blockquote>`引用文本`</blockquote>`

#### 使用`<br>`标签分行显示文本
在需要加回车换行的地方加入`<br />`，`<br />`标签作用相当于word文档中的回车。

> `<br />`标签是一个空标签，没有HTML内容的标签就是空标签，空标签只需要写一个开始标签，这样的标签有`<br />`、`<hr />`和`<img />`。
> 在 html 代码中输入回车、空格都是没有作用的。在html文本中想输入回车换行，就必须输入`<br />`。

**空格语法：**

`&nbsp;`

```
来源：作文网&nbsp;&nbsp;作者：为梦想而飞 
```
#### `<hr>`标签，添加水平横线
**语法：**

> html4.01版本 `<hr>`
> 
> xhtml1.0版本 `<hr />`

* `<hr />`标签和`<br />`标签一样也是一个空标签，所以只有一个开始标签，没有结束标签。

#### `<address>`标签，为网页加入地址信息
```
语法：

<address>联系地址信息</address>
```

#### 使用`<code>`标签 添加代码 使用`<pre>`标签为你的网页加入大段代码
```

语法：

<code>代码语言</code>

<pre>语言代码段</pre>
```
> 在文章中一般如果要插入多行代码时不能使用`<code>`标签了。如果是多行代码，可以使用`<pre>`标签。


#### 使用ul，ol添加新闻信息列表
`ul-li`是没有前后顺序的信息列表

```
语法：

<ul>
  <li>信息</li>
  <li>信息</li>
   ......
</ul>
```

`ol-li`是有前后顺序的信息列表

```
<ol>
   <li>信息</li>
   <li>信息</li>
   ......
</ol>

```
#### div 在排版中的作用
在网页制作中 可以把一些独立的逻辑部分划分出来，放在`<div>`标签中

```
语法：

<div>…</div>
```

为了使逻辑更清晰，可以为一个独立的逻辑部分设置一个名称，用`id`属性来为`<div>`提供唯一的名称。

```
语法：

<div  id="版块名称">…</div>

```

#### table标签 网页上的表格
创建表格的四个元素：table、tbody、tr、td、th

1. `<table>...</table>`:整个表格以`<table>`标记开始，`</table>`标记结束
2. `<tbody>...</tbody>`:如果不加`<tbody>``<thead>``<tfooter>`，table表格加载完毕之后才显示，加上这些表格结构，tbody包含航的内容下载完优先显示，不必等表格结束之后再显示。如果表格很长，使用tbody可以一部分一部分的显示
3. `<tr>...</tr>`:表格的一行，所以有几对tr 表格就有几行
4. `<td>...</td>`:表格的一个单元格，所以一行有几对td 表格就有几列
5. `<th>...</th`:表格头部的一个单元格，表格表头
6. 表格中列的个数 取决于一行中数据单元格的个数。即`<tr>...</tr>`中包含的`<td>...</td>`的个数

> 
1、table表格在没有添加css样式之前，在浏览器中显示是没有表格线的
>
2、表头，也就是th标签中的文本默认为粗体并且居中显示

#### caption标签 为标签添加标题和摘要
#####摘要：

>摘要的内容不会在浏览器中显示出来，作用是增加表格的可读性（语义化），使搜索引擎更好的读懂表格内容

**语法：** `<table summary="表格摘要内容">`

#####标题
> 用以描述表格内容，标题的显示位置：表格上方
**语法：**

```
<table>
	<caption>表格标题</caption>
	<tr>
		<td>...</td>
		...
	</tr>
</table>

```

#### 使用`<a>`标签 链接到另一个页面
使用`<a>`标签可以实现超链接，只要有链接的地方都会有该标签

**语法：**	`<a href="目标网址" title="鼠标滑过显示的文本">链接显示的文本</a>`

示例：

```
 <a href="www.baidu.com" title="点击跳转到百度">百度</a>
```
显示：  <a href="www.baidu.com" title="点击跳转到百度">百度</a>

`<a>`标签默认是在当前窗口打开网页，如果需要在新窗口打开的话，

```
<a href="www.baidu.com" target="_blank">在新窗口打开百度</a>

```


#### `<img>`标签 为网页插入图片
**语法：**
`<img src="图片地址" alt="图片下载失败时的替换文本" title="提示文本">`

> 1. src: 图像的地址
> 2. alt: 指定图片的描述性文本，当图片不可见（下载不成功时）可以看到该文本
> 3. title: 对图片的描述 （当鼠标滑过图片时显示该文本）
> 4. 图片可以是GIF PNG JPEG格式

#### 使用form表单 与用户交互
使用HTML表单（form）可以把用户输入的数据传送给服务器
**语法：**

```
<form method="传送方式" action="服务器文件">
```
> 1. **`<form>`**: form标签是成对出现的 以`<form>`开始 以`</form>`结束
> 2. action:数据被传送到的地方 比如一个php页面（save.php）
> 3. method: 数据传送的方式（get/post）

```
<form    method="post"   action="save.php">
        <label for="username">用户名:</label>
        <input type="text" name="username" />
        <label for="pass">密码:</label>
        <input type="password" name="pass" />
</form>
```
**注意**
> 所有表单控件（文本框、文本域、按钮、单选框、复选框等）都必须放在 `<form></form>` 标签之间（否则用户输入的信息可提交不到服务器上哦！）。


#### 文本输入框 密码输入框 (类似textField)
**语法：**

```
<form>
	<input type="text/password" name="名称" value="文本"/>

</form>
```

> 1. type: 等于text时 是文本输入框 为password时是密码输入框
> 2. name： 文本框名称
> 3. value: 为文本框设置默认值（起提示作用）

```
<form>
  姓名：
  <input type="text" name="myName">
  <br/>
  密码：
  <input type="password" name="pass">
</form>

```
<form>
  姓名：
  <input type="text" name="myName">
  <br/>
  密码：
  <input type="password" name="pass">
</form>


#### 文本域 支持多行文本输入 (类似textView)

**语法：**
`<textarea rows="行数" cols="列数">文本</textarea>`
> 1、`<textarea>`标签是成对出现的，以`<textarea>`开始，以`</textarea>`结束。
> 
> 2、cols ：多行输入域的列数。

> 3、rows ：多行输入域的行数。

>4、在`<textarea></textarea>`标签之间可以输入默认值。

```
<form  method="post" action="save.php">
        <label>联系我们</label>
        <textarea cols="50" rows="3" >在这里输入内容...</textarea>
</form>
```
<form  method="post" action="save.php">
        <label>联系我们</label>
        <textarea cols="50" rows="3" >在这里输入内容...</textarea>
</form>


#### 单选框 复选框
html有两种选择框： 单选框 复选框

**语法：**
`<input type="radio/checkbox" value="值" name="名称" checked="checked" />`

> 1. type: radio为单选框 checkbox为复选框
> 2. value: 提交到服务器的值
> 3. name: 为控件命名 **同一组**的单选按钮 name的值**一定要一致**
> 4. checked：当设置checked="checked"时 该选项被选中


```
<form name="iForm" method="post" action="save.php">
你是否喜欢旅游？<br />
<input type="radio" name="radioLove" value="喜欢" checked="checked"> 喜欢
<input type="radio" name="radioLove" value="不喜欢" > 不喜欢
<br/><br/>
你对那些运动感兴趣？<br/>
<input type="checkbox" name="checkbox1" value="run"> 跑步
<input type="checkbox" name="checkbox2" value="basketball"> 篮球

<input type="checkbox" name="checkbox3" value="sleep" checked="checked"> 睡觉

</form>
```
<form name="iForm" method="post" action="save.php">
你是否喜欢旅游？<br />
<input type="radio" name="radioLove" value="喜欢" checked="checked"> 喜欢
<input type="radio" name="radioLove" value="不喜欢" > 不喜欢
<br/><br/>
你对那些运动感兴趣？<br/>
<input type="checkbox" name="checkbox1" value="run"> 跑步
<input type="checkbox" name="checkbox2" value="basketball"> 篮球

<input type="checkbox" name="checkbox3" value="sleep" checked="checked"> 睡觉

</form>

#### 下拉列表框
用法：

```
<select>
<option value="reading">读书</option>
<option value="run" selected="selected">跑步</option>

</select>
```

<select>
<option value="reading">读书</option>
<option value="run" selected="selected">跑步</option>

</select>


#### 提交按钮
表单中有两种按钮：提交按钮 重置按钮

**语法：**
`<input type="submit" value="提交">`
> 1. type:只有当type等于submit时 按钮才有提交作用
> 2. value: 按钮上显示的文字

<input type="submit" value="提交">

#### 重置按钮
当用户需要重置表单信息到初始时的状态时，比如用户输入“用户名”后，发现书写有误，可以使用重置按钮使输入框恢复到初始状态。只需要把type设置为"reset"就可以。

**语法：**
`<input type="reset" value="重置">`

<input type="reset" value="重置">

#### form表单的label标签
label标签不会向用户呈现任何特殊效果，它的作用是为鼠标用户改进了可用性。如果你在 label 标签内点击文本，就会触发此控件。就是说，当用户单击选中该label标签时，浏览器就会自动将焦点转到和标签相关的表单控件上（就自动选中和该label标签相关连的表单控件上）。

**语法：**

`<label for="控件id名称">`

> 注意：标签的 for 属性中的值应当与相关控件的 id 属性值一定要相同。

```
<form>
  <label for="male">男</label>
  <input type="radio" name="gender" id="male" />
  <br />
  <label for="female">女</label>
  <input type="radio" name="gender" id="female" />
  <label for="email">输入你的邮箱地址</label>
  <input type="email" id="email" placeholder="Enter email">
</form>
```
<form>
  <label for="male">男</label>
  <input type="radio" name="gender" id="male" />
  <br />
  <label for="female">女</label>
  <input type="radio" name="gender" id="female" />
  <label for="email">输入你的邮箱地址</label>
  <input type="email" id="email" placeholder="Enter email">
</form>