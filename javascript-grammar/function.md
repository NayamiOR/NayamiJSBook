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

```
functionName(5,1);    //输出：your input: 5 1
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

## 返回值

在函数中使用return后加返回值结束函数并返回那个值。

带返回值的函数在调用时的值等于它的返回值。
