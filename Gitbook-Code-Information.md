---
description: 用于给本地编辑提供部分Gitbook语法参照
---

# Gitbook代码参考

## 一级标题

#### 三级标题（最多三级）

图片：

<figure><img src=".gitbook/assets/image (4) (2).png" alt=""><figcaption></figcaption></figure>

* [ ] task list
* [x] task list ticked

{% hint style="info" %}
Hint
{% endhint %}

> quota

```
// Some code
```

file:

{% file src=".gitbook/assets/image (1) (1).png" %}

table:

|   |   |   |
| - | - | - |
|   |   |   |
|   |   |   |
|   |   |   |

$$
f(x) = x * e^{2 pi i \xi x}
$$

page link:

{% content-ref url="prepare/pre/" %}
[pre](prepare/pre/)
{% endcontent-ref %}

api:

{% swagger method="get" path="" baseUrl="" summary="" %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}
