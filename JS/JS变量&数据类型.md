#JavaScript 语句
JavaScript 语句向浏览器发出的命令。语句的作用是告诉浏览器该做什么。

下面的 JavaScript 语句向 id="demo" 的 HTML 元素输出文本 "Hello World"：

```
document.getElementById("demo").innerHTML="Hello World";

```

###分号 ;
分号用于分隔 JavaScript 语句。
通常我们在每条可执行的语句结尾添加分号。
使用分号的另一用处是在一行中编写多条语句。

提示：您也可能看到不带有分号的案例。
在 JavaScript 中，用分号来结束语句是可选的。

***

###JavaScript 代码块

JavaScript 语句通过代码块的形式进行组合。
块由左花括号开始，由右花括号结束。
块的作用是使语句序列一起执行。

JavaScript 函数是将语句组合在块中的典型例子。
下面的例子将运行可操作两个 HTML 元素的函数：

实例

```
function myFunction()
{
document.getElementById("demo").innerHTML="Hello World";
document.getElementById("myDIV").innerHTML="How are you?";
}
```
***

### JavaScript 对大小写敏感。
JavaScript 对大小写是敏感的。
当编写 JavaScript 语句时，请留意是否关闭大小写切换键。
函数 getElementById 与 getElementbyID 是不同的。
同样，变量 myVariable 与 MyVariable 也是不同的。

***

###空格
JavaScript 会忽略多余的空格。您可以向脚本添加空格，来提高其可读性。下面的两行代码是等效的：

```
var name="Hello";
var name = "Hello";
```

***

###对代码行进行折行
您可以在文本字符串中使用反斜杠对代码行进行换行。下面的例子会正确地显示：

```
document.write("Hello \
World!");
不过，您不能像这样折行：
document.write \
("Hello World!");
```

***

**提示：JavaScript 是脚本语言。浏览器会在读取代码时，逐行地执行脚本代码。而对于传统编程来说，会在执行前对所有代码进行编译。**


# JS变量
**变量是存储信息的容器。**

实例

```
var x=2;
var y=3;
var z=x+y;
```

就像代数那样

```
x=2
y=3
z=x+y
```

在代数中，我们使用字母（比如 x）来保存值（比如 2）。
通过上面的表达式 z=x+y，我们能够计算出 z 的值为 5。
在 JavaScript 中，这些字母被称为变量。

**提示：可以把变量看做存储数据的容器。**

###JavaScript 变量
与代数一样，JavaScript 变量可用于存放值（比如 x=2）和表达式（比如 z=x+y）。

变量可以使用短名称（比如 x 和 y），也可以使用描述性更好的名称（比如 age, sum, totalvolume）。

* 变量必须以字母开头
* 变量也能以 $ 和 _ 符号开头（不过不推荐这么做）
* 变量名称对大小写敏感（y 和 Y 是不同的变量）

**提示：JavaScript 语句和 JavaScript 变量都对大小写敏感。**

***

###JavaScript 数据类型
JavaScript 变量还能保存其他数据类型，比如文本值 (name="Bill Gates")。

在 JavaScript 中，类似 "Bill Gates" 这样一条文本被称为字符串。

JavaScript 变量有很多种类型，当向变量分配文本值时，应该用双引号或单引号包围这个值。当向变量赋的值是数值时，不要使用引号。如果用引号包围数值，该值会被作为文本来处理。

例子

```
var pi=3.14;
var name="Bill Gates";
var answer='Yes I am!';
```
***


###声明（创建） JavaScript 变量

在 JavaScript 中创建变量通常称为“声明”变量。
我们使用 var 关键词来声明变量：

`var carname;`

变量声明之后，该变量是空的（它没有值）。
如需向变量赋值，请使用等号：

`carname="Volvo";`

不过，您也可以在声明变量时对其赋值：

`var carname="Volvo";`

例子
在下面的例子中，我们创建了名为 carname 的变量，并向其赋值 "Volvo"，然后把它放入 id="demo" 的 HTML 段落中：

```
<p id="demo"></p>
var carname="Volvo";
document.getElementById("demo").innerHTML=carname;
```
***

###一条语句，多个变量
可以在一条语句中声明很多变量。该语句以 var 开头，并使用逗号分隔变量即可：

`var name="Gates", age=56, job="CEO";`

声明也可横跨多行：

```
var name="Gates",
age=56,
job="CEO";
```


**Value = undefined**
在计算机程序中，经常会声明无值的变量。未使用值来声明的变量，其值实际上是 undefined。

在执行过以下语句后，变量 carname 的值将是 undefined：

`var carname;`

***

###重新声明 JavaScript 变量

如果重新声明 JavaScript 变量，该变量的值不会丢失：

在以下两条语句执行后，变量 carname 的值依然是 "Volvo"：

```
var carname="Volvo";
var carname;
```

###JavaScript 算数
可以通过 JavaScript 变量来做算数，使用的是 = 和 + 这类运算符：

例子

```
y=5;
x=y+2;
```

# JS数据类型
**字符串、数字、布尔、数组、对象、Null、Undefined**

###JavaScript 拥有动态类型
JavaScript 拥有动态类型。这意味着相同的变量可用作不同的类型：
实例

```
var x                // x 为 undefined
var x = 6;           // x 为数字
var x = "Bill";      // x 为字符串
```

***
###JavaScript 字符串
字符串是存储字符（比如 "Bill Gates"）的变量。

字符串可以是引号中的任意文本。可以使用单引号或双引号：

实例

```
var carname="Bill Gates";
var carname='Bill Gates';
```

可以在字符串中使用引号，只要不匹配包围字符串的引号即可：
实例

```
var answer="Nice to meet you!";
var answer="He is called 'Bill'";
var answer='He is called "Bill"';
```

```
<!DOCTYPE html>
<html>
<body>

<script>
var carname1="Bill Gates";
var carname2='Bill Gates';
var answer1="Nice to meet you!";
var answer2="He is called 'Bill'";
var answer3='He is called "Bill"';

document.write(carname1 + "<br>")
document.write(carname2 + "<br>")
document.write(answer1 + "<br>")
document.write(answer2 + "<br>")
document.write(answer3 + "<br>")
</script>

</body>
</html>
```
***


###JavaScript 数字

JavaScript 只有一种数字类型。数字可以带小数点，也可以不带：

实例

```
var x1=34.00;      //使用小数点来写
var x2=34;         //不使用小数点来写
```

极大或极小的数字可以通过科学（指数）计数法来书写：

实例

```
var y=123e5;      // 12300000
var z=123e-5;     // 0.00123
```

###JavaScript 布尔
布尔（逻辑）只能有两个值：true 或 false。

```
var x=true
var y=false
```
***

###JavaScript 数组

下面的代码创建名为 cars 的数组：

```
var cars=new Array();
cars[0]="Audi";
cars[1]="BMW";
cars[2]="Volvo";
```

或者 (condensed array):

```
var cars=new Array("Audi","BMW","Volvo");
```

或者 (literal array):

```
var cars=["Audi","BMW","Volvo"];
```

***

###JavaScript 对象
对象由花括号分隔。在括号内部，对象的属性以名称和值对的形式 (name : value) 来定义。属性由逗号分隔：

```
var person={firstname:"Bill", lastname:"Gates", id:5566};
```

上面例子中的对象 (person) 有三个属性：`firstname`、`lastname `以及 `id`。


空格和折行无关紧要。声明可横跨多行：

```
var person={
firstname : "Bill",
lastname  : "Gates",
id        :  5566
};
```

对象属性有两种寻址方式：

实例

```
name=person.lastname;
name=person["lastname"];
```

***

### Undefined 和 Null
Undefined 这个值表示变量不含有值。
可以通过将变量的值设置为 null 来清空变量。

```
cars=null;
person=null;
```

###声明变量类型
当声明新变量时，可以使用关键词 "new" 来声明其类型：

```
var carname=new String;
var x=      new Number;
var y=      new Boolean;
var cars=   new Array;
var person= new Object;
```

**JavaScript 变量均为对象。当声明一个变量时，就创建了一个新的对象。**