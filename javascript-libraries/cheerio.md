# cheerio

{% embed url="https://cheerio.js.org/#note" %}
官方文档
{% endembed %}

{% embed url="https://github.com/cheeriojs/cheerio/wiki/Chinese-README" %}
中文wiki
{% endembed %}

## 安装&使用

安装：

`npm install cheerio`

使用：

```javascript
const cheerio = require('cheerio');
const $ = cheerio.load('<h2 class="title">Hello world</h2>');

$('h2.title').text('Hello there!');
$('h2').addClass('welcome');

$.html();
//=> <html><head></head><body><h2 class="title welcome">Hello there!</h2></body></html>
```

## 加载

