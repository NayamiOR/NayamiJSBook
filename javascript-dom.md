---
description: DOM：Document Object Model，文档对象模型
---

# JavaScript DOM

网页被加载时，浏览器会创建页面的DOM，DOM模型被构造为（HTML）对象的树。

<figure><img src=".gitbook/assets/image (4) (2).png" alt=""><figcaption><p>DOM的结构，帮助理解</p></figcaption></figure>

## 查找元素

### 通过ID查找

如，查找id="intro"元素：

```
var x=document.getElementById("intro");
```

