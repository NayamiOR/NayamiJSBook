---
description: 函数是由事件驱动或者调用时执行的可重复使用的代码块
---

# 函数

## 定义

使用关键词function来定义函数，紧跟着的是函数名称，括号里写明需要的参数，多个参数用逗号分开。

```
function functionName(a,b){
    //doing sth.
    alert("your input:"+a+b);
}
```

## 调用

```
functionName(5,1);    //输出：your input: 5 1
```

## 返回值

在函数中使用return后加返回值结束函数并返回那个值。

带返回值的函数在调用时相当于它的返回值。
