# 变量和数据类型

## 变量

用var声明，没有强制类型：

```javascript
var a;    //声明变量，默认值是undefined
var b=5;    //声明变量并赋值
//声明变量可以跨多行
var c=4,
d=6,
e=8;
//可以用如下方式在声明时指定变量类型
var carname=new String;
var x=      new Number;
var y=      new Boolean;
```

此外，重新声明一个变量不会改变这个变量已有的值。

每个变量有自己的生命周期，从被声明时开始，到它所在的函数结束时结束。生命周期结束后就被删除了。

## 数据类型

**值类型(基本类型)**：字符串（String）、数字(Number)、布尔(Boolean)、空（Null）、未定义（Undefined）、Symbol。

**引用数据类型（对象类型）**：对象(Object)、数组(Array)、函数(Function)，还有两个特殊的对象：正则（RegExp）和日期（Date）。

<figure><img src="../../.gitbook/assets/Javascript-DataType.png" alt=""><figcaption></figcaption></figure>

JavaScript采用动态类型，也就是一个变量不会限制存储的值的类型，刚存储数字的变量也可以赋值字符串。

查看变量类型：

```
var a=5;
typeof a;    //返回number
```

* 字符串：单引号或双引号中的任意文本
* 数字：不区分整数浮点数等，全部合并为数字
* 布尔：只有true和false两个值
* 数组：用new Array()创建，或者new Array(用逗号分开的值)
* 对象：对象由花括号分隔。在括号内部，对象的属性以名称和值对的形式 (name : value) 来定义。属性由逗号分隔
