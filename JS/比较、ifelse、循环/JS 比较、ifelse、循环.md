# JS 比较
**比较和逻辑运算符用于测试 true 或 false。**

### 比较运算符
比较运算符在逻辑语句中使用，以测定变量或值是否相等。

给定 x=5，下面的表格解释了比较运算符：

|运算符| 描述 |例子 |
|---|---|---|
|==|等于|x==8 为 false|
|===|	全等（值和类型）|	x===5 为 true；x==="5" 为 false|
|!=	|不等于	|x!=8 为 true|
|>	|大于|	x>8 为 false|
|<	|小于	|x<8 为 true|
|>=|	大于或等于	|x>=8 为 false|
|<=	|小于或等于	|x<=8 为 true|

**如何使用**

可以在条件语句中使用比较运算符对值进行比较，然后根据结果来采取行动：

```
if (age<18) document.write("Too young");
```

### 逻辑运算符
逻辑运算符用于测定变量或值之间的逻辑。

给定 x=6 以及 y=3，下表解释了逻辑运算符：


|运算符| 描述 |例子 |
|---|---|---|
|&&	|and	|(x < 10 && y > 1) 为 true|
| \|\|	|or	|(x==5 \|\| y==5) 为 false|
|!	|not	|!(x==y) 为 true|


### 条件运算符
JavaScript 还包含了基于某些条件对变量进行赋值的条件运算符。类似于三目运算符

语法

```
variablename=(condition)?value1:value2 
```

例子

```
greeting=(visitor=="PRES")?"Dear President ":"Dear ";
```

如果变量 visitor 中的值是 "PRES"，则向变量 greeting 赋值 "Dear President "，否则赋值 "Dear"。

***

# JS if else

条件语句用于基于不同的条件来执行不同的动作。

### 条件语句
通常在写代码时，您总是需要为不同的决定来执行不同的动作。您可以在代码中使用条件语句来完成该任务。

在 JavaScript 中，我们可使用以下条件语句：

* if 语句 - 只有当指定条件为 true 时，使用该语句来执行代码
* if...else 语句 - 当条件为 true 时执行代码，当条件为 false 时执行其他代码
* if...else if....else 语句 - 使用该语句来选择多个代码块之一来执行
* switch 语句 - 使用该语句来选择多个代码块之一来执行

***

### If 语句
只有当指定条件为 true 时，该语句才会执行代码。

语法

```
if (条件)
  {
  只有当条件为 true 时执行的代码
  }

```
注意：请使用小写的 if。使用大写字母（IF）会生成 JavaScript 错误！

###If...else 语句
请使用 if....else 语句在条件为 true 时执行代码，在条件为 false 时执行其他代码。

语法

```
if (条件)
  {
  当条件为 true 时执行的代码
  }
else
  {
  当条件不为 true 时执行的代码
  }
```

***

###If...else if...else 语句

使用 if....else if...else 语句来选择多个代码块之一来执行。

语法

```
if (条件 1)
  {
  当条件 1 为 true 时执行的代码
  }
else if (条件 2)
  {
  当条件 2 为 true 时执行的代码
  }
else
  {
  当条件 1 和 条件 2 都不为 true 时执行的代码
  }
  
```

# Switch 语句
switch 语句用于基于不同的条件来执行不同的动作。

###JavaScript Switch 语句

请使用 switch 语句来选择要执行的多个代码块之一。

**语法**

```
switch(n)
{
case 1:
  执行代码块 1
  break;
case 2:
  执行代码块 2
  break;
default:
  n 与 case 1 和 case 2 不同时执行的代码
}
```

工作原理：首先设置表达式 n（通常是一个变量）。随后表达式的值会与结构中的每个 case 的值做比较。如果存在匹配，则与该 case 关联的代码块会被执行。请使用 break 来阻止代码自动地向下一个 case 运行。

**实例**

显示今日的周名称。请注意 Sunday=0, Monday=1, Tuesday=2, 等等：

```
var day=new Date().getDay();
switch (day)
{
case 0:
  x="Today it's Sunday";
  break;
case 1:
  x="Today it's Monday";
  break;
case 2:
  x="Today it's Tuesday";
  break;
case 3:
  x="Today it's Wednesday";
  break;
case 4:
  x="Today it's Thursday";
  break;
case 5:
  x="Today it's Friday";
  break;
case 6:
  x="Today it's Saturday";
  break;
}
```

x 的结果：

```
Today it's Friday
```

###default 关键词
请使用 default 关键词来规定匹配不存在时做的事情：

**实例**

如果今天不是周六或周日，则会输出默认的消息：

```
var day=new Date().getDay();
switch (day)
{
case 6:
  x="Today it's Saturday";
  break;
case 0:
  x="Today it's Sunday";
  break;
default:
  x="Looking forward to the Weekend";
}
```

x 的结果：

```
Looking forward to the Weekend
```
***

# for循环

###JavaScript 循环
如果您希望一遍又一遍地运行相同的代码，并且每次的值都不同，那么使用循环是很方便的。

我们可以这样输出数组的值：

```
document.write(cars[0] + "<br>");
document.write(cars[1] + "<br>");
document.write(cars[2] + "<br>");
document.write(cars[3] + "<br>");
document.write(cars[4] + "<br>");
document.write(cars[5] + "<br>");
```

不过通常我们这样写：

```
for (var i=0;i<cars.length;i++)
{
document.write(cars[i] + "<br>");
}
```

###不同类型的循环
JavaScript 支持不同类型的循环：

* **for** - 循环代码块一定的次数
* **for/in** - 循环遍历对象的属性
* **while** - 当指定的条件为 true 时循环指定的代码块
* **do/while** - 同样当指定的条件为 true 时循环指定的代码块

###For 循环

下面是 for 循环的语法：

```
for (语句 1; 语句 2; 语句 3)
  {
  被执行的代码块
  }
```

**语句 1** 在循环（代码块）开始前执行

**语句 2** 定义运行循环（代码块）的条件

**语句 3** 在循环（代码块）已被执行之后执行

```
for (var i=0; i<5; i++)
  {
  x=x + "The number is " + i + "<br>";
  }
```

**语句 1**

通常我们会使用语句 1 初始化循环中所用的变量 (var i=0)。

**语句 1** 是可选的，也就是说不使用语句 1 也可以。

可以在语句 1 中初始化任意（或者多个）值：

实例:

```
for (var i=0,len=cars.length; i<len; i++)
{
document.write(cars[i] + "<br>");
}

```

同时还可以省略语句 1（比如在循环开始前已经设置了值时）：

实例:

```
var i=2,len=cars.length;
for (; i<len; i++)
{
document.write(cars[i] + "<br>");
}

```

**语句 2**

通常语句 2 用于评估初始变量的条件。

语句 2 同样是可选的。

如果语句 2 返回 true，则循环再次开始，如果返回 false，则循环将结束。

**提示：**如果您省略了语句 2，那么必须在循环内提供 break。否则循环就无法停下来。这样有可能令浏览器崩溃。

**语句 3**

通常语句 3 会增加初始变量的值。

语句 3 也是可选的。

语句 3 有多种用法。增量可以是负数 (i--)，或者更大 (i=i+15)。
语句 3 也可以省略（比如当循环内部有相应的代码时）：

实例:

```
var i=0,len=cars.length;
for (; i<len; )
{
document.write(cars[i] + "<br>");
i++;
}
```

###For/In 循环
JavaScript for/in 语句循环遍历对象的属性：

实例

```
var person={fname:"John",lname:"Doe",age:25};

for (x in person)
  {
  txt=txt + person[x];
  }

```

