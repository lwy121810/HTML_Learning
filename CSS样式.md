##CSS
CSS全称为“层叠样式表 (Cascading Style Sheets)”，它主要是用于定义HTML内容在浏览器内的显示样式，如文字大小、颜色、字体加粗等。

如下列代码：
```
p{
   font-size:12px;
   color:red;
   font-weight:bold;
}
```

使用CSS样式的一个好处是通过定义某个样式，可以让不同网页位置的文字有着统一的字体、字号或者颜色等。

css样式由**选择符**（又称选择器）和**声明**组成，声明又由**属性**和**值**组成

<img src="http://img.mukewang.com/52fde5c30001b0fe03030117.jpg">

> **选择符：**又称选择器，指明网页中要应用样式规则的元素。
> 
> **声明：**在英文大括号{}中的就是声明，属性和值之间用英文分号:隔开，多个声明用英文分号隔开。
>
>  p{font-size:12px;color:red;}
> 


css代码注释为`/*注释语句*/`

### CSS样式
CSS样式可以写在哪些地方呢？从CSS 样式代码插入的形式来看基本可以分为以下3种：内联式、嵌入式和外部式三种。

**内联式：**就是把css代码直接写在HTML标签中
比如：`<p style="color:red">这里是红色的文本</p>`
> 要写在开始标签里，不能是结束标签里，并且css样式代码要写在style=""双引号中，如果有多个，可以用分号隔开


**嵌入式：** 写在当前文件内 就是把css代码写在`<style type="text/css"></style>`标签之间

比如

```
<style type="text/css">
span{
color:red;
}
</style>


```

嵌入式css样式必须写在`<style></style>`之间，并且一般在`<head></head>`之间

**外部式：**也称为外联式，写在一个单独的一个文件中，这个css样式文件以`.css`为扩展名，在head标签中（不实在style标签中），使用link标签链接到HTML文件内
`<link href="base.css" rel="stylesheet" type="text/css">`

> 1、css样式文件名称以有意义的英文字母命名，如 main.css。

> 2、rel="stylesheet" type="text/css" 是固定写法不可修改。

> 3、<link>标签位置一般写在<head>标签之内。


三种css样式的优先级：**就近原则**（离被设置的元素越近优先级越高）

### 选择器
每一条css样式声明（定义）由两部分组成，形式如下

```
选择器{
	样式;
}
```
在{}之前的就是选择器，选择器指明了{}中的样式的作用对象，也就是样式作用于网页中的哪些元素

####标签选择器
标签选择器其实就是html代码中的标签。如右侧代码编辑器中的`<html>、<body>、<h1>、<p>、<img>`。

例如下面代码：

`p{font-size:12px;line-height:1.6em;}`

####类选择器
**语法：**
`.类选择器名称{css样式代码;}`
> 1. 以英文圆点开头
> 2. 名称可以随便取（不要取中文）

使用方法：

1. 使用合适的标签把内容标记
	`<span>胆小如鼠</span>`
2. 使用 `class="类选择器名称"`为标签设置一个类
	`<span class="stress">胆小如鼠</span>`
3. 设置类选器css样式 `.stress{color:red;}`

#### ID选择器
ID选择器跟类选择器的区别

1. 为标签设置id="ID名称"，而不是class="类名称"。
2. ID选择器前面是井号（#），而不是英文圆点（.）;

#### 类选器和ID选择器的异同点
**相同点：**可以应用于任何元素

**不同点：**
	
1. ID选择器在文档中只能使用一次，类选择器可以使用多次
2. 可以使用类选择器词列表方法为一个元素同时设置多个样式。我们可以为一个元素同时设多个样式，但只可以用类选择器的方法实现，ID选择器是不可以的（不能使用 ID 词列表）


下面的代码是正确的

```
.stress{
    color:red;
}
.bigsize{
    font-size:25px;
}
<p>到了<span class="stress bigsize">三年级</span>下学期时，我们班上了一节公开课...</p>

```

下面的代码是不正确的

```
#stressid{
    color:red;
}
#bigsizeid{
    font-size:25px;
}
<p>到了<span id="stressid bigsizeid">三年级</span>下学期时，我们班上了一节公开课...</p>
```

####子选择器

还有一个比较有用的选择器子选择器，即大于符号(>),用于选择指定标签元素的第一代子元素

`.名称>标签{css样式}`

比如
`.food>li{border:1px solid red;}`

#### 包含(后代)选择器
包含选择器，即加入空格,用于选择指定标签元素下的后辈元素。
比如：`.first  span{color:red;}`

请注意这个选择器与子选择器的区别，子选择器（child selector）仅是指它的**直接后代**，或者你可以理解为作用于子元素的第一代后代。而后代选择器是作用于**所有子后代元素**。后代选择器通过`空格`来进行选择，而子选择器是通过`>`进行选择。

总结：`>`作用于元素的第一代后代，`空格`作用于元素的所有后代

#### 通用选择器
通用选择器是功能最强大的选择器，它使用一个（*）号指定，它的作用是匹配html中所有标签元素，如下使用下面代码使用html中任意标签元素字体颜色全部设置为红色：

`* {color:red;}`

#### 伪类选择符
伪类选择符可以给html不存在的标签（标签的某种状态）设置样式，比如可以给html中的一个标签元素的鼠标滑过的状态来设置字体颜色

比如
`a:hover{color:red}` 就是为a标签鼠标滑过的状态设置字体颜色。

> 关于伪类选择符，到目前为止，可以兼容所有浏鉴器的“伪类选择符”就是 a 标签上使用 :hover 了（其实伪类选择符还有很多，尤其是 css3 中，但是因为不能兼容所有浏览器，本教程只是讲了这一种最常用的）。其实 :hover 可以放在任意的标签上，比如说 p:hover，但是它们的兼容性也是很不好的，所以现在比较常用的还是 a:hover 的组合。


#### 分组选择符
当想要为html中的多个标签设置同一个样式时，可以使用分组选择符(,)
比如 `h1,span{color:red}`,就相当于

```
h1{color:red}
span{color:red}
```

### 继承
CSS的**某些标签**是具有继承性的，继承是一种规则，它允许样式不仅作用于某个特定的html标签元素，而且应用于其后代。

比如：

```
p{color:red;}

<p>三年级时，我还是一个<span>胆小如鼠</span>的小女孩。</p>
```
这里颜色设置不仅作用于`<p>`标签，还作用于其后代标签，这里是`<span>`标签。

但有些css样式不具备继承性，比如`border:1px solid red;`

### 特殊性 （权值）
有时候我们会为同一元素设置不同的css样式，比如

```
p{color:red;}
.first{color:green;}
<p class="first">三年级时，我还是一个<span>胆小如鼠</span>的小女孩。</p>
```
p和.first都匹配到了p这个标签上，那么会显示哪种颜色呢？green是正确的颜色，那么为什么呢？是因为浏览器是根据权值来判断使用哪种css样式的，权值高的就使用哪种css样式。

**权值的规则：**

> **标签的权值为1 类选择器的权值为10 ID选择符的权值最高为100.**

```
p{color:red;} /*权值为1*/
p span{color:green;} /*权值为1+1=2*/
.warning{color:white;} /*权值为10*/
p span.warning{color:purple;} /*权值为1+1+10=12*/
#footer .note p{color:yellow;} /*权值为100+10+1=111*/
```
注意：还有一个权值比较特殊--继承也有权值但很低，有的文献提出它只有0.1，所以可以理解为继承的权值最低。

### 层叠
如果在html文件中对于同一个元素可以有多个css样式存在并且这多个css样式具有相同权重值怎么办？

**层叠**就是在html文件中对于同一个元素可以有多个css样式存在，当有相同权重的样式存在时，会根据这些css样式的前后顺序来决定，处于最后面的css样式会被应用。

```
p{color:red;}
p{color:green;}
<p class="first">三年级时，我还是一个<span>胆小如鼠</span>的小女孩。</p>
```
最后 p 中的文本会设置为green，这个层叠很好理解，理解为后面的样式会覆盖前面的样式。

所以前面的css样式优先级就不难理解了：

**内联样式表（标签内部）> 嵌入样式表（当前文件中）> 外部样式表（外部文件中）。***

### 重要性
我们在做网页代码的时，有些特殊的情况需要为某些样式设置具有最高权值，怎么办？这时候我们可以使用`!important`来解决。

```
p{color:red!important;}
p{color:green;}
<p class="first">三年级时，我还是一个<span>胆小如鼠</span>的小女孩。</p>
```
这时 p 段落中的文本会显示的red红色。

**注意：!important要写在分号的前面**

这里注意当网页制作者不设置css样式时，浏览器会按照自己的一套样式来显示网页。并且用户也可以在浏览器中设置自己习惯的样式，比如有的用户习惯把字号设置为大一些，使其查看网页的文本更加清楚。这时注意样式优先级为：**浏览器默认的样式 < 网页制作者样式 < 用户自己设置的样式**，但记住!important优先级样式是个例外，权值高于用户自己设置的样式。

### 文字排版--字体
我们可以使用css样式为网页中的文字设置字体、字号、颜色等样式属性。下面我们来看一个例子，下面代码实现：为网页中的文字设置字体为宋体。

`body{font-family:"宋体";}`

这里注意不要设置不常用的字体，因为如果用户本地电脑上如果没有安装你设置的字体，就会显示浏览器默认的字体。（因为用户是否可以看到你设置的字体样式取决于用户本地电脑上是否安装你设置的字体。）
现在一般网页喜欢设置“微软雅黑”，如下代码：

```
body{font-family:"Microsoft Yahei";}

```
或

```
body{font-family:"微软雅黑";}
```
注意：第一种方法比第二种方法兼容性更好一些。

因为这种字体即美观又可以在客户端安全的显示出来（用户本地一般都是默认安装的）。

### 段落排版--中文字间距、字母间距
中文字间隔、字母间隔设置：

如果想在网页排版中设置文字间隔或者字母间隔就可以使用    letter-spacing 来实现，如下面代码：

```
h1{
    letter-spacing:50px;
}
...
<h1>了不起的盖茨比</h1>
```

注意：这个样式使用在英文单词时，是设置字母与字母之间的间距。

单词间距设置：

如果我想设置英文单词之间的间距呢？可以使用 word-spacing 来实现。如下代码

```
h1{
    word-spacing:50px;
}
...
<h1>hellow world!</h1>
```
## 盒模型
### 元素分类
在讲解CSS布局之前，我们需要提前知道一些知识，在CSS中，html中的标签元素大体被分为三种不同的类型：块状元素、内联元素(又叫行内元素)和内联块状元素。

常用的块状元素有：

```
<div>、<p>、<h1>...<h6>、<ol>、<ul>、<dl>、<table>、<address>、<blockquote> 、<form>
```

常用的内联元素有：

```
<a>、<span>、<br>、<i>、<em>、<strong>、<label>、<q>、<var>、<cite>、<code>

```

常用的内联块状元素有：

`<img>、<input>`

#### 块级元素
什么是块级元素？在html中`<div>、 <p>、<h1>、<form>、<ul> 和 <li>`就是块级元素。设置`display:block`就是将元素显示为块级元素。如下代码就是将内联元素a转换为块状元素，从而使a元素具有块状元素特点。

`a{display:block;}`

**块级元素特点：**

> 1、每个块级元素都从新的一行开始，并且其后的元素也另起一行。（真霸道，一个块级元素独占一行）

> 2、元素的高度、宽度、行高以及顶和底边距都可设置。

> 3、元素宽度在不设置的情况下，是它本身父容器的100%（和父元素的宽度一致），除非设定一个宽度。

#### 内联元素
在html中，`<span>、<a>、<label>、 <strong> 和<em>`就是典型的内联元素（行内元素）（inline）元素。当然块状元素也可以通过代码`display:inline`将元素设置为内联元素。如下代码就是将块状元素div转换为内联元素，从而使 div 元素具有内联元素特点。

```
 div{
     display:inline;
 }

......

<div>我要变成内联元素</div>
```

**内联元素特点：**

> 1、和其他元素都在一行上；

> 2、元素的高度、宽度及顶部和底部边距不可设置；

> 3、元素的宽度就是它包含的文字或图片的宽度，不可改变。


#### 内联块状元素
内联块状元素（inline-block）就是同时具备内联元素、块状元素的特点，代码`display:inline-block`就是将元素设置为内联块状元素。(css2.1新增)，`<img>、<input>`标签就是这种内联块状标签。

**`inline-block` 元素特点：**

> 1、和其他元素都在一行上；

> 2、元素的高度、宽度、行高以及顶和底边距都可设置。

```
<style type="text/css">
a{
    
	width:20px;/*在默认情况下宽度不起作用*/
	height:20px;/*在默认情况下高度不起作用*/
	background:pink;/*设置背景颜色为粉色*/
	text-align:center; /*设置文本居中显示*/
}
</style>
```
我们为 a 元素设置了宽和高，但都没有起到作用，原因是a在默认的时候是内联元素，内联元素是不可以设置宽和高的。

修改如下：

```
<style type="text/css">
a{
    display:inline-block;
	width:20px;/*在默认情况下宽度不起作用*/
	height:20px;/*在默认情况下高度不起作用*/
	background:pink;/*设置背景颜色为粉色*/
	text-align:center; /*设置文本居中显示*/
}
</style>

```

修改之后

<style type="text/css">
a{
    display:inline-block;
	width:20px;/*在默认情况下宽度不起作用*/
	height:20px;/*在默认情况下高度不起作用*/
	background:pink;/*设置背景颜色为粉色*/
	text-align:center; /*设置文本居中显示*/
}
</style>

<a>1</a>
<a>2</a>
<a>3</a>
<a>4</a>


### 盒模型 - 边框
盒子模型的边框就是围绕着内容及补白的线，这条线你可以设置它的粗细、样式和颜色(边框三个属性)。

如下面代码为 div 来设置边框粗细为 2px、样式为实心的、颜色为红色的边框：

```
div{
    border:2px  solid  red;
}

```
上面是 border 代码的缩写形式，可以分开写：

```
div{
    border-width:2px;
    border-style:solid;
    border-color:red;
}
```

**注意：**

> 1、border-style（边框样式）常见样式有
dashed（虚线）| dotted（点线）| solid（实线）。

> 2、border-color（边框颜色）中的颜色可设置为十六进制颜色，如:
`border-color:#888;`//前面的井号不要忘掉。

> 3、border-width（边框宽度）中的宽度也可以设置为：
thin | medium | thick（但不是很常用），最常还是用象素（px）。


如果有想为 p 标签单独设置下边框，而其它三边都不设置边框样式怎么办呢？css 样式中允许只为一个方向的边框设置样式：

`div{border-bottom:1px solid red;}`

同样可以使用下面代码实现其它三边(上、右、左)边框的设置：

```
border-top:1px solid red;
border-right:1px solid red; 
border-left:1px solid red;
```

### 盒模型 宽度和高度
盒模型的宽度和高度和我们平常所说的物体的宽度和宽度不一样。css定义的宽(width)和高（height） 指的是填充里的内容范围

因此一个**元素实际宽度**（盒子的宽度）=左边界+左边框+左填充+内容宽度+右填充+右边框+右边界。

<img src="http://img.mukewang.com/539fbb3a0001304305570259.jpg">

元素的高度也是同理。
比如：

css代码：

```
div{
    width:200px;
    padding:20px;
    border:1px solid red;
    margin:10px;    
}
```

html代码：

```
<body>
   <div>文本内容</div>
</body>
```
元素的实际长度为：10px+1px+20px+200px+20px+1px+10px=262px。在chrome浏览器下可查看元素盒模型，如下图：
<img src="http://img.mukewang.com/543b4cae0001b34304300350.jpg">

#### 盒模型--填充 (padding)
元素内容与边框之间是可以设置距离的，称之为“填充”。填充也可分为上、右、下、左(顺时针)。如下代码：

```
div{padding:20px 10px 15px 30px;}
```

顺序一定不要搞混。可以分开写上面代码：

```
div{
   padding-top:20px;
   padding-right:10px;
   padding-bottom:15px;
   padding-left:30px;
}
```

如果上、右、下、左的填充都为10px;可以这么写

`div{padding:10px;}`

如果上下填充一样为10px，左右一样为20px，可以这么写：

`div{padding:10px 20px;}`


####盒模型--边界

元素与其它元素之间的距离可以使用边界（`margin`）来设置。边界也是可分为上、右、下、左。如下代码：

`div{margin:20px 10px 15px 30px;}`

也可以分开写：

```
div{
   margin-top:20px;
   margin-right:10px;
   margin-bottom:15px;
   margin-left:30px;
}
```

如果上右下左的边界都为10px;可以这么写：

`div{ margin:10px;}`

如果上下边界一样为10px，左右一样为20px，可以这么写：

`div{ margin:10px 20px;}`

总结一下：**padding和margin的区别，padding在边框里，margin在边框外。**


###css布局模型
清楚了CSS 盒模型的基本概念、 盒模型类型， 我们就可以深入探讨网页布局的基本模型了。布局模型与盒模型一样都是 CSS 最基本、 最核心的概念。 但布局模型是建立在盒模型基础之上，又不同于我们常说的 CSS 布局样式或 CSS 布局模板。如果说布局模型是本，那么 CSS 布局模板就是末了，是外在的表现形式。 

CSS包含3种基本的布局模型，用英文概括为：Flow、Layer 和 Float。
在网页中，元素有三种布局模型：

> 1 流动模型（Flow）
> 
> 2 浮动模型 (Float)
> 
> 3 层模型（Layer）

#### 流动模型
先来说一说流动模型，流动（Flow）是默认的网页布局模式。也就是说网页在默认状态下的 HTML 网页元素都是根据流动模型来分布网页内容的。



流动布局模型具有2个比较典型的特征：

> 第一点，块状元素都会在所处的包含元素内自上而下按顺序垂直延伸分布，因为在默认状态下，块状元素的宽度都为100%。实际上，块状元素都会以行的形式占据位置。

> 第二点，在流动模型下，内联元素都会在所处的包含元素内从左到右水平分布显示。（内联元素可不像块状元素这么霸道独占一行）

#### 浮动模型
块状元素这么霸道都是独占一行，如果现在我们想让两个块状元素并排显示，怎么办呢？不要着急，设置元素浮动就可以实现这一愿望。

任何元素在默认情况下是不能浮动的，但可以用 CSS 定义为浮动，如 div、p、table、img 等元素都可以被定义为浮动。如下代码可以实现两个 div 元素一行显示。

```
div{
    width:200px;
    height:200px;
    border:2px red solid;
    float:left;
}
<div id="div1"></div>
<div id="div2"></div>

```

div{
    width:200px;
    height:200px;
    border:2px red solid;
    float:left;
}
<div id="div1"></div>
<div id="div2"></div>

效果图:
<img src="http://img.mukewang.com/540e62c60001c56a06760417.jpg">

当然你也可以同时设置两个元素右浮动也可以实现一行显示。

```
div{
    width:200px;
    height:200px;
    border:2px red solid;
    float:right;
}

```
效果图

<img src="http://img.mukewang.com/540e632b0001f5f506760417.jpg">

又有小伙伴问了，设置两个元素一左一右可以实现一行显示吗？当然可以：

```
div{
    width:200px;
    height:200px;
    border:2px red solid;
}
#div1{float:left;}
#div2{float:right;}
```

<img src="http://img.mukewang.com/540e63b50001f6a206760417.jpg">


#### 层模型

层模型有三种形式：

1、绝对定位(position: absolute)

2、相对定位(position: relative)

3、固定定位(position: fixed)


##### 层模型--绝对定位

如果想为元素设置层模型中的绝对定位，需要设置position:absolute(表示绝对定位)，这条语句的作用将元素从文档流中拖出来，然后使用left、right、top、bottom属性相对于其最接近的一个具有定位属性的父包含块进行绝对定位。如果不存在这样的包含块，则相对于body元素，即相对于浏览器窗口。

如下面代码可以实现div元素相对于浏览器窗口向右移动100px，向下移动50px。

```
div{
    width:200px;
    height:200px;
    border:2px red solid;
    position:absolute;
    left:100px;
    top:50px;
}
<div id="div1"></div>
```

<img src="http://img.mukewang.com/53a00b130001e86707360547.jpg">


##### 层模型--相对定位

如果想为元素设置层模型中的相对定位，需要设置position:relative（表示相对定位），它通过left、right、top、bottom属性确定元素在正常文档流中的偏移位置。相对定位完成的过程是首先按static(float)方式生成一个元素(并且元素像层一样浮动了起来)，然后相对于**以前的位置**移动，移动的方向和幅度由left、right、top、bottom属性确定，偏移前的位置保留不动。

如下代码实现相对于以前位置向下移动50px，向右移动100px;

```
#div1{
    width:200px;
    height:200px;
    border:2px red solid;
    position:relative;
    left:100px;
    top:50px;
}

<div id="div1"></div>
```

效果图：
<img src="http://img.mukewang.com/53a00d2b00015c4b06190509.jpg">

什么叫做“偏移前的位置保留不动”呢？

大家可以做一个实验，在div标签的后面加入一个span标签，在标并在span标签中写入一些文字。如下代码：

```
<body>
    <div id="div1"></div><span>偏移前的位置还保留不动，覆盖不了前面的div没有偏移前的位置</span>
</body>
```

<img src="http://img.mukewang.com/541a4bfc0001abef05940489.jpg">

从效果图中可以明显的看出，虽然div元素相对于以前的位置产生了偏移，但是div元素以前的位置还是保留着，所以后面的span元素是显示在了div元素以前位置的后面。

##### 固定定位
**fixed：**表示固定定位，与absolute定位类型类似，但它的相对移动的坐标是视图（屏幕内的网页窗口）本身。由于视图本身是固定的，它不会随浏览器窗口的滚动条滚动而变化，除非你在屏幕中移动浏览器窗口的屏幕位置，或改变浏览器窗口的显示大小，因此固定定位的元素会始终位于浏览器窗口内视图的某个位置，不会受文档流动影响，这与background-attachment:fixed;属性功能相同。以下代码可以实现相对于浏览器视图向右移动100px，向下移动50px。并且拖动滚动条时位置固定不变。

```
#div1{
    width:200px;
    height:200px;
    border:2px red solid;
    position:fixed;
    left:100px;
    top:50px;
}
<p>文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本。</p>
....
```

##### Relative和 Absolute的组合使用
使用`position:absolute`可以实现被设置元素相对于浏览器(body)设置定位，我们也可以设置相对于其他元素进行定位，使用position:absolute来帮忙就行
	
1. 参照定位的元素必须是相对定位的前辈元素：

```
<div id="box1"><!--参照定位的元素-->
    <div id="box2">相对参照元素进行定位</div><!--相对定位元素-->
</div>
```
从上面代码可以看出box1是box2的父元素（父元素当然也是前辈元素了）。

2、参照定位的元素必须加入position:relative;

```
#box1{
    width:200px;
    height:200px;
    position:relative;        
}
```

3、定位元素加入position:absolute，便可以使用top、bottom、left、right来进行偏移定位了。

```
#box2{
    position:absolute;
    top:20px;
    left:30px;         
}
```

这样box2就可以相对于父元素box1定位了（这里注意参照物就可以不是浏览器了，而可以自由设置了）。

```
#box3{
    width:200px;
    height:200px;
    position:relative;       
}
#box4{
    width:99%;
 	position:absolute;	
	bottom:0;
	left:0;
	right:0;
    
}


<div id="box3">
    <img src="http://img.mukewang.com/541a7d8a00018cf102000200.jpg">
    <div id="box4">当我还是三年级的学生时是一个害羞的小女生。</div>
</div>

```

## CSS代码缩写 占用更少的带宽

###  盒模型代码简写
还记得在讲盒模型时外边距(margin)、内边距(padding)和边框(border)设置上下左右四个方向的边距是按照顺时针方向设置的：上右下左。具体应用在margin和padding的例子如下

```
margin:10px 15px 12px 14px;/*上设置为10px、右设置为15px、下设置为12px、左设置为14px*/

```

通常有下面三种缩写方法:

1、 如果top、right、bottom、left的值相同，如下面代码：

`margin:10px 10px 10px 10px;`
可缩写为：

`margin:10px;`

2、如果top和bottom值相同、left和 right的值相同，如下面代码：

`margin:10px 20px 10px 20px;`
可缩写为：

`margin:10px 20px;`


3、如果left和right的值相同，如下面代码：

`margin:10px 20px 30px 20px;`
可缩写为：

`margin:10px 20px 30px;`

注意：padding、border的缩写方法和margin是一致的。

### 颜色值缩写
颜色的css样式也是可以缩写的，当你设置的是16进制的色彩值是，如果每两位的值相同，可以缩写一半。

例子1：

`p{color:#000000;}`

可以缩写为：

`p{color: #000;}`

例子2：

`p{color: #336699;}`

可以缩写为：

`p{color: #369;}`

### 字体缩写

网页中的字体css样式代码也有他自己的缩写方式，下面是给网页设置字体的代码：

```
body{
    font-style:italic;
    font-variant:small-caps; 
    font-weight:bold; 
    font-size:12px; 
    line-height:1.5em; 
    font-family:"宋体",sans-serif;
}
```

这么多行的代码其实可以缩写为一句：

```
body{
    font:italic  small-caps  bold  12px/1.5em  "宋体",sans-serif;
}
```

注意：

 1、使用这一简写方式你至少要指定 font-size 和 font-family 属性，其他的属性(如 font-weight、font-style、font-variant、line-height)如未指定将自动使用默认值。

 2、在缩写时 font-size 与 line-height 中间要加入“/”斜扛。

一般情况下因为对于中文网站，英文还是比较少的，所以下面缩写代码比较常用：

```
body{
    font:12px/1.5em  "宋体",sans-serif;
}
```

只是有字号、行间距、中文字体、英文字体设置。

## 单位和值
### 颜色值
在网页中的颜色设置是非常重要，有字体颜色（color）、背景颜色（background-color）、边框颜色（border）等，设置颜色的方法也有很多种：

1、英文命令颜色

前面几个小节中经常用到的就是这种设置方法：
`p{color:red;}`

2、RGB颜色

这个与 photoshop 中的 RGB 颜色是一致的，由 R(red)、G(green)、B(blue) 三种颜色的比例来配色。

`p{color:rgb(133,45,200);}`

每一项的值可以是 0~255 之间的整数，也可以是 0%~100% 的百分数。如：

`p{color:rgb(20%,33%,25%);}`

3、十六进制颜色

这种颜色设置方法是现在比较普遍使用的方法，其原理其实也是 RGB 设置，但是其每一项的值由 0-255 变成了十六进制 00-ff。

`p{color:#00ffff;}`

### 长度值
长度单位目前比较常用到`px（像素）em、 %百分比`，这三个单位都是相对单位

**1、 像素**
	
像素为什么是相对单位呢？ 因为像素指的是显示器上的小点（css规范中假设“90像素=1英寸”）。实际情况是浏览器会使用显示器的实际像素值，在目前大多数的设计者都倾向于使用像素（px）作为单位。

**2、 em**

如果元素的font-size为14px，那么 1em = 14px， 如果font-size为18px， 那么 1em = 18px;

`p{font-size:12px;text-indent:2em;}`

上面代码就是可以实现段落首行缩进 24px（也就是两个字体大小的距离）。

有一个特殊情况：
当给一个font-size设置单位为 em 时，此时的计算标准是以 p 的父元素的 font-size为基础。

html:

`<p>以这个<span>例子</span>为例。</p>`

css:

```
p{font-size:14px}
span{font-size:0.8em;}
```

结果 span 中的字体“例子”字体大小就为 11.2px（14 * 0.8 = 11.2px）。

**3. 百分比**

`p{font-size:12px;line-height:130%}`

设置行高（行间距）为字体的130%（12 * 1.3 = 15.6px）。


## CSS样式设置小技巧
### 水平居中设置-行内元素

我们在实际工作中常会遇到需要设置水平居中的场景，比如为了美观，文章的标题一般都是水平居中显示的。

这里我们又得分两种情况：行内元素 还是 块状元素 ，块状元素里面又分为定宽块状元素，以及不定宽块状元素。今天我们先来了解一下行内元素怎么进行水平居中？

如果被设置元素为文本、图片等行内元素时，水平居中是通过给父元素设置 `text-align:center` 来实现的。(父元素和子元素：如下面的html代码中，div是“我想要在父容器中水平居中显示”这个文本的父元素。反之这个文本是div的子元素 )如下代码：

html代码：

```
<body>
  <div class="txtCenter">我想要在父容器中水平居中显示。</div>
</body>
```

css代码：

```
<style>
  .txtCenter{
    text-align:center;
  }
</style>
```

### 水平居中设置-定宽块状元素
当被设置的元素是 **块状元素**的时候，设置`text-align:center`就不起作用了，这时也分为两种情况：**定宽块状元素**和**不定宽块状元素。**

**定宽块状元素：**块状元素的宽度width为固定值。

满足**定宽**和**块状**两个条件的元素是可以通过设置“左右margin”值为“auto”来实现剧中的。

html代码

```
<body>
  <div>我是定宽块状元素，哈哈，我要水平居中显示。</div>
</body>

```

css代码：

```
<style>
div{
    border:1px solid red;/*为了显示居中效果明显为 div 设置了边框*/
    
    width:200px;/*定宽*/
    margin:20px auto;/* margin-left 与 margin-right 设置为 auto */
}

</style>
```

也可以写成：

```
margin-left:auto;
margin-right:auto;
```
注意：元素的“上下 margin” 是可以随意设置的。


### 水平居中总结-不定宽块状元素方法（一）
在实际工作中我们会遇到需要为“不定宽度的块状元素”设置居中，比如网页上的分页导航，因为分页的数量是不确定的，所以我们不能通过设置宽度来限制它的弹性。

**不定宽块状元素：**块状元素的宽度width不固定。


不定宽度的块状元素有三种方法居中（这三种方法目前使用的都很多）：

1. 加入 table 标签

2. 设置 display: inline 方法：与第一种类似，显示类型设为 行内元素，进行不定宽元素的属性设置
3. 设置 position:relative 和 left:50%：利用 相对定位 的方式，将元素向左偏移 50% ，即达到居中的目的

**加入table标签**
加入table标签是利用table标签的**长度自适应**--即不定义其长度也不默认父元素body的长度（table其长度根据其内文本长度决定），因此可以看作一个**定宽度块元素**，然后在利用定宽度块状居中的margin方法，使其水平居中。

**第一步：**为需要居中的元素外面加入一个table标签（包括`<tbody><tr><td>`）.

**第二步：** 为这个table 设置“左右margin 居中”（这个和定宽块状元素的方法一样）。

举例：

html代码：

```
<div>
 <table>
  <tbody>
    <tr><td>
    <ul>
        <li>我是第一行文本</li>
        <li>我是第二行文本</li>
        <li>我是第三行文本</li>
    </ul>
    </td></tr>
  </tbody>
 </table>
</div>
```
css代码：

```
<style>
table{
    border:1px solid;
    margin:0 auto;
}
</style>

```

### 水平居中总结-不定宽块状元素方法（二）
除了上一节讲到的插入table标签，可以使不定宽块状元素水平居中之外，本节介绍第2种实现这种效果的方法，改变元素的display类型为行内元素，利用其属性直接设置。

第二种方法：改变块级元素的 display 为 inline 类型（设置为 行内元素 显示），然后使用 text-align:center 来实现居中效果。如下例子：

html代码：

```
<body>
<div class="container">
    <ul>
        <li><a href="#">1</a></li>
        <li><a href="#">2</a></li>
        <li><a href="#">3</a></li>
    </ul>
</div>
</body>
```
css代码：

```
<style>
.container{
    text-align:center;
}
/* margin:0;padding:0（消除文本与div边框之间的间隙）*/
.container ul{
    list-style:none;
    margin:0;
    padding:0;
    display:inline;
}
/* margin-right:8px（设置li文本之间的间隔）*/
.container li{
    margin-right:8px;
    display:inline;
}
</style>

```
这种方法相比第一种方法的优势是不用增加无语义标签，但也存在着一些问题：它将块状元素的 display 类型改为 inline，变成了行内元素，所以少了一些功能，比如设定长度值。
