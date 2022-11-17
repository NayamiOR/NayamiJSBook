---
description: 函数是由事件驱动或者调用时执行的可重复使用的代码块
---

# 函数

## 定义/声明

使用关键词function来定义函数，紧跟着的是函数名称，括号里写明需要的参数（paremeters），多个参数用逗号分开。

```
function functionName(a,b){
    //doing sth.
    alert("your input:"+a+b);
}
```

### 函数提升

一般来说变量和函数等，不可以在声明前调用。但是Js可以自动函数提升和变量提升，所以支持在声明前调用的行为。

## 调用

```javascript
let temp = functionName(5,1);    //输出：your input: 5 1
```

### 自调用

写法：

在定义函数时用括号包裹整个函数并在后面加上一对空括号(和分号)。

还有一种写法是在function前加“+”号并在后面后面加上一对空括号(和分号)。

```javascript
(function() {
  // function body...
}());
// or
(function() {
  // function body...
})();

//another method
+function(){

}();
```

自调用函数会在定义后自动调用。

### this关键字

this指向函数执行时的当前对象，当函数没有被自身的对象调用时this的值就会变成全局对象。

### 作为方法调用

```javascript
var myObject = {
    firstName:"John",
    lastName: "Doe",
    fullName: function () {
        return this.firstName + " " + this.lastName;
    }
}
myObject.fullName();         // 返回 "John Doe"
```

### 作为函数方法调用函数

（这部分我是真的快看不懂）

call() 和 apply() 是预定义的函数方法。 两个方法可用于调用函数，两个方法的第一个参数必须是对象本身。

```javascript
function myFunction(a, b) {
    return a * b;
}
myObject = myFunction.call(myObject, 10, 2);     // 返回 20
```

## 返回值

在函数中使用return后加返回值结束函数并返回那个值。

带返回值的函数在调用时的值等于它的返回值。

## 箭头函数

看起来这是一个类似其它语言中lambda表达式的功能。

在只有一个参数时，可以省略包括参数的圆括号；在没有参数时，只需要写一对空的圆括号。

```javascript
(参数1, 参数2, …, 参数N) => { 函数声明 }

(参数1, 参数2, …, 参数N) => 表达式(单一)
// 相当于：(参数1, 参数2, …, 参数N) =>{ return 表达式; }
```

## 参数

参数分为显式参数(parameters)和隐式参数(arguments)，Js调用函数时不检查参数类型，也不会检测隐式参数的个数。

### 默认参数

如何设置默认参数：

1. 未定义时自行定义：

```javascript
function myFunction(x, y) {
    if (y === undefined) {
          y = 0;
    } 
}
```

2. 更简洁的方式：

```javascript
function myFunction(x, y) {
    y = y || 0;
}
```

ES6以后支持默认参数，如下：
```javascript
function myFunction(x, y = 10) {
    // y=默认值，没给的话就默认为10
    return x + y;
}
```

### arguments

函数都有内置的arguments对象。

用例如下：

```javascript
x = findMax(1, 123, 500, 115, 44, 88);
 
function findMax() {
    var i, max = arguments[0];
    
    if(arguments.length < 2) return max;
 
    for (i = 0; i < arguments.length; i++) {
        if (arguments[i] > max) {
            max = arguments[i];
        }
    }
    return max;
}
```

## 闭包

{% hint style="info" %}
施工中，这部分暂时看不下去了有点晕。
{% endhint %}