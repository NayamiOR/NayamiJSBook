---
description: 在JavaScript中，几乎所有事物都是对象
---

# 对象

## 概念

对象是变量的容器，通过键值对（类似字典里一个单词对应一个释义的匹配方式）将多个小变量合并到一个大变量中。

## 对象定义

```
var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
```

## 对象属性

对象里的键值对一般成为对象的属性。

对象属性的访问有两种方法：

```javascript
// 最常见的访问方式
person.firstName;

//用类似数组的方式访问
person['firstName'];
```

## 对象方法

{% hint style="info" %}
关于方法，具体请看函数篇
{% endhint %}

对象方法定义了一个函数，并作为对象属性存储。具体

```javascript
person.run()    //调用person对象里定义了的run函数
```

