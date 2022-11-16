# sublime text 安装

## 介绍

sublime是功能类似vscode的代码编辑器，主要的功能是编辑，支持代码高亮和代码提示，并不直接提供运行代码的功能。

官网网址：[https://www.sublimetext.com](https://www.sublimetext.com/)

实际上必应就可以在第一条的位置轻松搜索到：

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

## 安装

官网可以一键下到安装包，下载后打开exe程序（exe是Windows通用的运行程序，常见于各类程序软件的启动和安装包）

第一个问题是是否将sublime添加到右键菜单，一般来说可以在文件管理器里选择文件和文件夹直接用sublime打开，推荐勾选，不是很重要。

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

然后程序会自动进行安装，安装目录建议选择Program Files文件夹，可以自己选择。最后点击Finish按钮后安装就完成了。

## 配置

因为sublime只是一个编辑器，刚安装完成时只有很有限的功能，所以需要另外配置和插件来实现更丰富的功能，其中最重要的功能主要是这两个：

1. 代码高亮
2. 代码提示

sublime自带代码高亮所以我们只需要把代码提示插件安装一下就好了。

## 代码提示

{% hint style="info" %}
施工中，下面不用看，看了也没用
{% endhint %}

安装官方的package control（包控制）功能，使用Ctrl+Shift+P打开一个窗口，输入Install Package Control，选中对应的选项然后回车确认。

{% embed url="https://packagecontrol.io/packages/SublimeCodeIntel" %}

代码提示使用了这个插件，安装和使用在上面的链接里都写了，这里也说一下。

需要先安装python，用pip安装一个库，代码如下：

```
pip3 install --upgrade --pre CodeIntel
```

然后在sublime的菜单里选择Preferences -> Browse Packages...，会打开一个文件夹，在这个文件夹里打开git bash，

