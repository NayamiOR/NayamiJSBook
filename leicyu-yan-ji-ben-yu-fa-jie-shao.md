---
description: 所有类C语言大都有的通用的语法要素，纯概念但是对于了解编程的要素很通用很好用。
---

# 类C语言基本语法介绍

JavaScript是一门类C语言，实际上现在热门的语言里类C语言占了相当大的一部分，Java/C#等OOP（面对对象编程）语言都可以算。特点就是语法和C语言有一定的接近。

## 变量

宏观来说，电脑中的内存是一整条连续的存储空间，程序中的变量会在内存中占几个位置。每个变量都有自己的存储内容和自己在内存上的空间。

具体到程序中，变量可以粗略的理解为一个装特定数据的盒子，可以往里拿东西放东西（数据），并且有自己的编号（地址）。

### 声明和赋值

声明可以理解为创建变量，赋值就是把数据放进变量里。不同语言中的声明和赋值有不同的写法，比如C语言中写法如下

```c
int a;    //a是一个变量，只能放整数，默认没有赋值
int b=0;    //b是一个变量，只能放整数，默认是0
int c,d;    //同时声明c和d，只能放整数，没赋值
bool e=1;    //e是一个放布尔值的变量，值可以是true或者false，c语言中用1和0代替
float f=1.34;    //f是一个浮点数，也就是数学中的小数
```

变量有不同的类型，常见的有：

* 整型：整数
* 浮点型：浮点数（小数）
* 布尔型：对或错，有或无
* 字符串：一段字符
* 单个字符

除此之外还有很多，具体情况随语言变化。

此外，在对变量类型的处理中，众多语言的表现往往都不一样，所以人们经常用这方面的区别来分类语言，如下：

> * 动态类型语言：在运行期进行类型检查的语言，也就是在编写代码的时候可以不指定变量的数据类型，比如Python和Ruby&#x20;
> * 静态类型语言：它的数据类型是在编译期进行检查的，也就是说变量在使用前要声明变量的数据类型，这样的好处是把类型检查放在编译期，提前检查可能出现的类型错误，典型代表C/C++和Java&#x20;
> * 强类型语言，一个变量不经过强制转换，它永远是这个数据类型，不允许隐式的类型转换。举个例子：如果你定义了一个double类型变量a,不经过强制类型转换那么程序int b = a无法通过编译。典型代表是Java。&#x20;
> * 弱类型语言：它与强类型语言定义相反,允许编译器进行隐式的类型转换，典型代表C/C++。

{% hint style="info" %}
根据我的经验得出的感想就是，动态类型语言在很多时候用来写脚本很合适，更加灵活，比如我前两天做python爬虫就感觉很方便，但是用go实现一样的功能，还要多写一个很长的结构体。Python因为是动态类型语言所以不用那么复杂的结构体来让程序进行一个萝卜一个坑。

但是不好的地方就是，在开发中因为类型不是很明确所以有些不熟悉的变量和函数的作用，输入和返回值的具体意义不大好判断。（不大好描述，但是以后会自然而然的在过程中体验到真意的）
{% endhint %}

## 数组

是极其常用的数据结构。

本质上是一堆连续的变量的集合，如果变量是档案袋，那数组就是档案柜。变量是纸张，数组就是一沓纸。

```clike
// C语言中数组声明
int[5] hello = [1,2,3,4,5]

//数组元素访问
int a = hello[0]
```

访问数组的方式就是在数组变量名后加中括号，中括号里面的数字叫索引（index），

## 循环

循环一般来说分两种，可能可以继续细分。循环的作用就是操作程序在指定的情况中指定同一段程序重复执行指定次数。

### while循环

```c
while(/*条件*/){
    //程序代码
}
```

while循环的效果是在括号中条件成立的情况下执行程序代码，直到括号中条件不成立，或者就一直运行下去。

### for循环

程序中最常用的循环，for循环由几个部分组成。

括号中有三条表达式，如下代码中，先声明了一个变量，名叫i，在i小于9时执行代码，每执行一次代码就把i的值加1（i++就是i=i+1的意思）。

```c
for(int i=0;i<9;i++){
    
}
```

### foreach循环

是部分语言才具备的功能（java，js，python等等都有，还是属于很广泛的功能）。

本质上只是for循环的加强版，用途狭窄一点，但是在对应的情况中使用体验会比for循环好。

**用途：**

一般用来遍历数组，可以自动按顺序读取数组里的数据并作出操作，当然，还有很多其他的用法。

## 注释

每个主流编程语言都有注释功能，用途是在程序中做笔记，说明代码功能，方便程序员阅读、理解、修改别人的代码。同时是在编写过程中捋顺逻辑的重要工具。注释本身不会被程序识别或者有任何的影响。（曾经有人发现注释对程序本身产生了影响，那个问题吸引了极大的注意力和关注。一般来说完全不用担心这种情况因为实在破天荒）

注释一般分两种：

1. 单行注释
2. 多行注释

### 单行注释

大多数主流类C语言中用符号"//"表示，python中的符号是"#"。

该符号后所有内容会被忽略，不影响下一行，仅限本行内。

### 多行注释

大多数语言中用"/\*"和"\*/"表示开始和结束。在这两个符号中夹着的一切内容都会被忽略，可以跨行。

## 函数

又叫方法，一般来说这两个名词说的是同一种东西。

在数学中的函数是类似$$f(x) = x * e^{2 pi i \xi x}$$的东西，本质上来说，就是输入x，返回和x有关的值。同理，编程中的函数是，输入变量，然后可以利用变量做出指定的操作以及返回数据的功能，最简单的栗子如下：

```go
//本程序用Go语言做例子
func main(){
    var a,b = 1,2
    var c = add(a,b)
}

func add(a,b int) int {    //输入两个整数，输出一个整数
    return a+b    //return是用来结束函数的操作，return的值就是返回的值
}
```

上面的栗子中add(a,b)本身是一个表达式，值就是它的返回值，本身等于a+b的值，也就是说变量c被赋值成a+b的值，所以c=3。

同时函数不只是用来返回值，中间可以做很多操作。比如输入一个数组，可以操作函数把数组里的所有内容输出一遍，同时可以没有返回值。总之函数能起到各种作用。

具体应用中一般会选择复用性强，重复性高的代码做成函数，方便以后的重复使用。

## 结构体和类

结构体和类是面向对象编程中一个非常核心的概念。

类是可以包含多个数据结构的集合，日常使用中本质上也是变量。结构体同上，但是类可以包含方法，但是结构体一般没有这类功能。

{% hint style="info" %}
实际上go语言的结构体功能可以通过函数的绑定结构体的功能来实现和类包含函数差不多的效果，就是写法和一般面向对象编程中的写法不大一样。
{% endhint %}