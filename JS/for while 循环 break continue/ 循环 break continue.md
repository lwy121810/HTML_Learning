# While 循环
**只要指定条件为 true，循环就可以一直执行代码。**

### while 循环
While 循环会在指定条件为真时循环执行代码块。

语法

```
while (条件)
  {
  需要执行的代码
  }
  
```
  
实例

本例中的循环将继续运行，只要变量 i 小于 5：

```
while (i<5)
  {
  x=x + "The number is " + i + "<br>";
  i++;
  }
```

**提示：如果您忘记增加条件中所用变量的值，该循环永远不会结束。该可能导致浏览器崩溃。**


### do/while 循环
do/while 循环是 while 循环的变体。该循环会执行一次代码块，在检查条件是否为真之前，然后如果条件为真的话，就会重复这个循环。

语法

```
do
  {
  需要执行的代码
  }
while (条件);
```

实例

下面的例子使用 do/while 循环。该循环至少会执行一次，即使条件是 false，隐藏代码块会在条件被测试前执行：

```
do
  {
  x=x + "The number is " + i + "<br>";
  i++;
  }
while (i<5);
```

### 比较 for 和 while


本例中的循环使用 for 循环来显示 cars 数组中的所有值：

```
cars=["BMW","Volvo","Saab","Ford"];
var i=0;
for (;cars[i];)
{
document.write(cars[i] + "<br>");
i++;
}
```


本例中的循环使用使用 while 循环来显示 cars 数组中的所有值：

```
cars=["BMW","Volvo","Saab","Ford"];
var i=0;
while (cars[i])
{
document.write(cars[i] + "<br>");
i++;
}
```

# JavaScript Break 和 Continue 语句

**break 语句用于跳出循环。
continue 用于跳过循环中的一个迭代。**

***

###Break 语句

**break 语句可用于跳出循环。
break 语句跳出循环后，会继续执行该循环之后的代码（如果有的话）：**

```
for (i=0;i<10;i++)
  {
  if (i==3)
    {
    break;
    }
  x=x + "The number is " + i + "<br>";
  }
```

###Continue 语句

continue 语句中断循环中的迭代，如果出现了指定的条件，然后继续循环中的下一个迭代。

该例子跳过了值 3：

```
for (i=0;i<=10;i++)
 {
 if (i==3) continue;
  x=x + "The number is " + i + "<br>";
  }
```
# JavaScript 标签
可以对 JavaScript 语句进行标记。如需标记 JavaScript 语句，请在语句之前加上冒号：

```
label:
语句

```
break 和 continue 语句仅仅是能够跳出代码块的语句。

语法

```
break labelname;

continue labelname;
```

**continue 语句（带有或不带标签引用）只能用在循环中。
break 语句（不带标签引用），只能用在循环或 switch 中。
通过标签引用，break 语句可用于跳出任何 JavaScript 代码块：**


实例

```
<script>
cars=["BMW","Volvo","Saab","Ford"];
list:
{
document.write(cars[0] + "<br>"); 
document.write(cars[1] + "<br>"); 
document.write(cars[2] + "<br>"); 
break list;
document.write(cars[3] + "<br>"); 
document.write(cars[4] + "<br>"); 
document.write(cars[5] + "<br>"); 
}
</script>

```

结果：

```
BMW
Volvo
Saab
```
