---
description: 用JS做网络爬虫有相当的优势，且语法比Python优雅
---

# JavaScript 爬虫

> 相比Python，JavaScript才是更适合写爬虫的语言。原因有如下三个方面：
>
> * JavaScript异步IO机制适用于爬虫这种IO密集型任务。JavaScript中的回调非常自然，使用异步网络请求能够充分利用CPU。
> * JavaScript中的jQuery毫无疑问是最强悍的HTML解析工具，使用JavaScript写爬虫能够减少学习负担和记忆负担。虽然Python中有PyQuery，但终究还是比不上jQuery自然。
> * 爬取结果多为JSON，JavaScript是最适合处理JSON的语言。

## 工具

### 请求

ajax库

request库（支持node）

axios（支持react native，Node，浏览器），vue2推荐

fly.js

### 解析提取

jQuery有强大的html解析功能，但是在node里需要利用jsdom模拟Windows对象，效率太低太笨重但是稳妥。

cheerio实现了jq的dom部分，相当于子集，在解析html方面比jq易用。

### 储存

node内置了fs模块，可以操作文件系统。
