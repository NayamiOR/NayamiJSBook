---
desripion: 
---

# 类

> class只是ES6中增加的语法糖，本质上还是object。

## 创建类

使用class关键词来创建一个类，类体在大括号中。

每个类包含了一个特殊的方法叫constructor，这是类的构造函数，用于创建和初始化一个由class创建的对象。

```js
class Runoob {
  constructor(name, url) {
    this.name = name;
    this.url = url;
  }
}
```

## 使用类

定义后可以用new关键字创建对象：
    
```js
var obj = new Runoob("菜鸟教程", "www.runoob.com");
```

## 类表达式

类表达式是定义类的另一种方法。