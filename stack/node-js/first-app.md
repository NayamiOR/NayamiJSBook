---
Description:
---

# 第一个应用

## 创建应用

用require指令载入http模块，并将实例化的HTTP赋值：

```js
var http = require("http");
```

用http.createServer()方法创建服务器，并使用listen方法绑定8888端口。函数通过request,response参数来接收和响应数据。

在根目录下创建server.js文件：

```js
