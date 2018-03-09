# JS 对象
**JavaScript 中的所有事物都是对象：字符串、数字、数组
日期，等等。在JavaScript中，对象是拥有属性和方法的数据。**

### 属性和方法
属性是与对象相关的值。 方法是能够在对象上执行的动作。


举例：汽车就是现实生活中的对象。

汽车的属性：

```
car.name=Fiat

car.model=500

car.weight=850kg

car.color=white 
```

汽车的方法：

```
car.start()

car.drive()

car.brake()
```

汽车的属性包括名称、型号、重量、颜色等。
所有汽车都有这些属性，但是每款车的属性都不尽相同。
汽车的方法可以是启动、驾驶、刹车等。

###JavaScript 中的对象
在JavaScript中，对象是数据（变量），拥有属性和方法。

当声明一个 JavaScript 变量时：

```
var txt = "Hello";
```

实际上已经创建了一个 JavaScript 字符串对象。字符串对象拥有内建的属性 length。对于上面的字符串来说，length 的值是 5。字符串对象同时拥有若干个内建的方法。

属性：

`txt.length=5`

方法：

```
txt.indexOf()

txt.replace()

txt.search()
```

提示：在面向对象的语言中，属性和方法常被称为对象的成员。
***

### 创建JavaScript对象

JavaScript几乎所有的事物都是对象：字符串、数字、日期、函数等。

创建名为 "person" 的对象，并为其添加了四个属性：

```
person=new Object();
person.firstname="Bill";
person.lastname="Gates";
person.age=56;
person.eyecolor="blue";
```
***

### 访问对象的属性

访问对象属性的语法是：

```
objectName.propertyName
```

本例使用 String 对象的 length 属性来查找字符串的长度：

```
var message="Hello World!";
var x=message.length;
```

在以上代码执行后，x 的值是：

```
12
```

***

### 访问对象的方法

可以通过下面的语法调用方法：

```
objectName.methodName()
```

这个例子使用 String 对象的 `toUpperCase()` 方法来把文本转换为大写：

```
var message="Hello world!";
var x=message.toUpperCase();
```
在以上代码执行后，x 的值是：

```
HELLO WORLD!
```
***

# JS 函数
函数是由事件驱动的或者当它被调用时执行的可重复使用的代码块。

### JS 函数语法

函数就是包裹在花括号中的代码块，前面使用了关键词 `function`：

```
function functionname()
{
这里是要执行的代码
}
```

当调用该函数时，会执行函数内的代码。

可以在某事件发生时直接调用函数（比如当用户点击按钮时），并且可由 JavaScript 在任何位置进行调用。


**提示：JavaScript 对大小写敏感。关键词 function 必须是小写的，并且必须以与函数名称相同的大小写来调用函数。**

***

### 调用带参数的函数
在调用函数时，可以向其传递值，这些值被称为参数。

这些参数可以在函数中使用。

可以发送任意多的参数，由逗号（,）分开;

```
myFunction(argument1,argument2)
```

当声明函数时，请把参数作为变量来声明：

```
function myFunction(var1,var2)
{
这里是要执行的代码
}
```

变量和参数必须以一致的顺序出现。第一个变量就是第一个被传递的参数的给定的值，以此类推。

实例

```
<button onclick="myFunction('Bill Gates','CEO')">点击这里</button>

<script>
function myFunction(name,job)
{
alert("Welcome " + name + ", the " + job);
}
</script>

```
***

###带有返回值的函数
有时，我们会希望函数将值返回调用它的地方。
通过使用 return 语句就可以实现。

在使用 return 语句时，函数会停止执行，并返回指定的值。

语法

```
function myFunction()
{
var x=5;
return x;
}
```

函数调用将被返回值取代：

```
var myVar=myFunction();
```

myVar 变量的值是 5，也就是函数 "myFunction()" 所返回的值。

即使不把它保存为变量，也可以使用返回值：

```
document.getElementById("demo").innerHTML=myFunction();
```

"demo" 元素的 innerHTML 将成为 5，也就是函数 "myFunction()" 所返回的值。

***

### 局部JavaScript变量

在JavaScript函数内部声明的变量（使用var）是**局部变量**，只能在函数内部使用它。（该变量的作用域是局部的）。我们可以在不同的函数中使用名字相同的局部变量，因为只有声明过该变量的函数才能识别出该变量。

**只要函数运行完毕，本地变量就会被删除**
***


###全局变量
在函数外部声明的变量就是全局变量，网页上的所有脚本和函数都能访问它。
***


###JavaScript变量的生命周期
JS变量的生命周期从它们被声明的时间开始。

**局部变量会在函数运行以后被删除。**

**全局变量会在页面被关闭之后删除**

***

### 向未声明的Javascript变量来分配值
如果把值赋给尚未声明的变量，该变量会自动作为全局变量声明。

这条语句：

```
carname="Volvo";
```

将声明一个全局变量 carname，即使它在函数内执行。
***

# JS 运算符

运算符 = 用于赋值。

运算符 + 用于加值。

运算符 = 用于给 JavaScript 变量赋值。

算术运算符 + 用于把值加起来。

```
y=5;
z=2;
x=y+z; 
```

在以上语句执行后，x 的值是 7。

### JavaScript 算术运算符

算术运算符用于执行变量与/或值之间的算术运算。

给定 y=5，下面的表格解释了这些算术运算符：

<table>
	<thead>
		<th>运算符</th>
		<th>描述</th>
		<th>例子</th>
		<th>结果</th>
	</thead>
	
	<tbody>
		<tr>
		<td> + </td>
		<td> 加 </td>
		<td> x=y+2 </td>
		<td> x=7 </td>
		</tr>
		
		<tr>
		<td> - </td>
		<td> 减 </td>
		<td> x=y-2 </td>
		<td> x=3 </td>
		</tr>
		
		
		<tr>
		<td> * </td>
		<td> 乘 </td>
		<td> x=y*2 </td>
		<td> x=10 </td>
		</tr>
		
		
		<tr>
		<td> / </td>
		<td> 除 </td>
		<td> x=y/2 </td>
		<td> x=2.5 </td>
		</tr>
		
		<tr>
		<td> %	</td>
		<td> 求余数 (保留整数)	 </td>
		<td> x=y%2 </td>
		<td> x=1  </td>
		</tr>
		
		<tr>
		<td> ++ </td>
		<td> 累加 </td>
		<td> x=++y </td>
		<td> x=6   </td>
		</tr>
	
	
		<tr>
		<td> -- </td>
		<td> 递减 </td>
		<td> x=--y </td>
		<td> x=4   </td>
		</tr>
	</tbody>
	
</table>

***

###JavaScript 赋值运算符
赋值运算符用于给 JavaScript 变量赋值。
给定 x=10 和 y=5，下面的表格解释了赋值运算符：


<table>
	<thead>
		<th>运算符</th>
		<th>例子</th>
		<th>等价于</th>
		<th>结果</th>
	</thead>
	
	<tbody>
		<tr>
		<td> =	</td>
		<td> x=y</td>
		<td>  </td>
		<td> x=5</td>
		</tr>
		
		<tr>
		<td> +=
 </td>
		<td> 	x+=y</td>
		<td> 	x=x+y	 </td>
		<td> x=15</td>
		</tr>
		
		
		<tr>
		<td> -= </td>
		<td> x-=y</td>
		<td> 	x=x-y </td>
		<td> 	x=5   </td>
		</tr>
		
		
		<tr>
		<td> *= </td>
		<td> 	x*=y</td>
		<td> 	x=x*y </td>
		<td> 	x=50 </td>
		</tr>
		
		<tr>
		<td> /=</td>
		<td> 	x/=y</td>
		<td> 	x=x/y	</td>
		<td> x=2	  </td>
		</tr>
		
		<tr>
		<td> %=</td>
		<td> 	x%=y	 </td>
		<td> x=x%y </td>
		<td> 	x=0   </td>
		</tr>

	</tbody>
	
</table>

***

###用于字符串的 + 运算符
`+` 运算符用于把文本值或字符串变量加起来（连接起来）。

如需把两个或多个字符串变量连接起来，请使用 + 运算符。

```
txt1="What a very";
txt2="nice day";
txt3=txt1+txt2;
```

在以上语句执行后，变量 txt3 包含的值是 "What a verynice day"。

要想在两个字符串之间增加空格，需要把空格插入一个字符串之中：

```
txt1="What a very ";
txt2="nice day";
txt3=txt1+txt2;
```

或者把空格插入表达式中：

```
txt1="What a very";
txt2="nice day";
txt3=txt1+" "+txt2;
```

在以上语句执行后，变量 txt3 包含的值是：

"What a very nice day"

***

### 对字符串和数字进行加法运算
请看这些例子：

```
x=5+5;
document.write(x);

x="5"+"5";
document.write(x);

x=5+"5";
document.write(x);

x="5"+5;
document.write(x);
```

**如果把数字与字符串相加，结果将成为字符串。**
