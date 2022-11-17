---
Description:
---

# 数组

## 构造函数

```js
var arr = new Array();
var arr = new Array(20);
var arr = new Array(1, 2, 3, 4);
const map = new Map([['foo', 3], ['bar', {}]]);
const set = new Set([1, 2, 3, 4, 4]);
var arr = Array.from(map);
var arr = Array.from(set);
var arr = Array.from(another Array);

```

## API方法

### 监测包含

```js
arr.includes(value);
```

### 排序

```js
arr.sort();
arr.reverse();
```

### 长度

```js
arr.length;
```

### 判断是不是数组
    
```js
if(value instanceof Array){

}
```

### 迭代器

```js
const a = ['foo','bar','baz','qux'];
console.log(Array.from(a.key()));       // [0,1,2,3]
console.log(Array.from(a.values()));    // ['foo','bar','baz','qux']
console.log(Array.from(a.entries()));   // [[0,'foo'],[1,'bar'],[2,'baz'],[3,'qux']]
```

用ES6规定的解构快速获取键值对

```js
const a = ['foo','bar','baz','qux'];
for (let [key, value] of a.entries()) {
    console.log(key, value);
}
```

### 填充

fill:

```js
//将value填充到arr的start到end位置，越界的部分不填充，不传end则填充到最后，不传start则从0开始填充，不传value则填充undefined
arr.fill(value, start, end);
```

copyWithin:

```js
//将start到end位置的值复制到target位置，越界的部分不复制，不传end则复制到最后，不传start则从0开始复制，不传target则从0开始覆盖
arr.copyWithin(target, start, end);
```

### 转换

- toString: 将数组转换为字符串，元素之间用逗号分隔
- toLocaleString: 将数组转换为字符串，元素之间用逗号分隔，元素调用toLocaleString方法
- valueOf: 返回数组本身

### 栈方法&队列方法

- push
- pop
- shift
- unshift

```js
var arr = [1, 2, 3];
//压栈
arr.push(4);    // [1, 2, 3, 4]
//出栈
arr.pop();      // [1, 2, 3]
//出队
arr.shift();    // [2, 3]
//从头部入队
arr.unshift(1); // [1, 2, 3]
```

### 搜索&定位

- indexOf
- lastIndexOf
- includes

```js
var arr = [1, 2, 3, 4, 5];
arr.indexOf(3);         // 2
arr.lastIndexOf(3);     // 2
//搜索第二个3
arr.indexOf(3, 3);      // -1
//搜索从后往前第二个3
arr.lastIndexOf(3, 3);  // 2
arr.includes(3);        // true
//包含两个3
arr.includes(3, 3);     // false
```

### 操作方法

- concat：传入多个值或者数组，返回一个按顺序包含所有值的新数组
- slice：传入开始位置和结束位置，返回一个在原数组从开始位置到结束位置-1的切片（一个新数组）
- splice：可以删除可以插入可以替换

#### splice

- 删除：传入开始位置和删除个数，返回一个包含被删除元素的新数组
- 插入：传入开始位置和要插入的值，返回一个空数组
- 替换：传入开始位置、删除个数和要插入的值，返回一个包含被删除元素的新数组

```js
var arr = ["a", "b", "c", "d", "e"];
//删除
arr.splice(1, 2);   // ["a", "d", "e"]
//插入
arr.splice(2, 0, "f");    // ["a", "b", "f", "c", "d", "e"]
//替换
arr.splice(1, 2, "g","h");    // ["a", "g", "h", "d", "e"]
```

### 迭代方法

- every：对数组中的每个元素执行一次传入的函数，如果所有元素都返回true，则返回true，否则返回false
- filter：对数组中的每个元素执行一次传入的函数，返回一个新数组，新数组中的元素是传入函数返回true的元素
- forEach：对数组中的每个元素执行一次传入的函数，没有返回值
- map：对数组中的每个元素执行一次传入的函数，返回一个新数组
- some：对数组中的每个元素执行一次传入的函数，如果有一个元素返回true，则返回true，否则返回false

### 归并方法

- reduce：对数组中的每个元素执行一次传入的函数，返回一个值
- reduceRight：对数组中的每个元素执行一次传入的函数，返回一个值，从右到左执行