# git安装

{% embed url="https://git-scm.com/downloads" %}
git官网下载链接
{% endembed %}

## 安装

点击自己的系统，如Windows。一般来说可以直接选择Standalone Installer，同样这里也有32和64两个版本供选择。

先会让你选择安装位置，一般还是建议Program Files文件夹，也可以自己怎么顺手怎么来，不过养成好的使用习惯很有必要。

<figure><img src="../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

接着会让你选择安装组件，可以自己决定也可以照搬下面的选项。

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

方框内 Git 可改为其他名字，也可点击 “`Browse...`” 选择其他文件夹或者给"`Don't create a Start Menu folder`" 打勾不要文件夹，点击 \[next] 到第五步。\


<figure><img src="https://img-blog.csdnimg.cn/6414569159a044d1944bd0a1a023bbfa.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBAbXVrZXM=,size_20,color_FFFFFF,t_70,g_se,x_16" alt=""><figcaption></figcaption></figure>

安装成功后在开始菜单里的图如下：\
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210417142055838.png?x-oss-process=image/watermark,type\_ZmFuZ3poZW5naGVpdGk,shadow\_10,text\_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L211a2Vz,size\_16,color\_FFFFFF,t\_70)

决定初始化新项目(仓库)的主干名字，第一种是让 Git 自己选择，名字是 master ，但是未来也有可能会改为其他名字；第二种是我们自行决定，默认是 main，当然，你也可以改为其他的名字。一般默认第一种，点击 \[next] 到第七步。

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

调整你的 path 环境变量，这里可以盲选第二个

<figure><img src="../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

选择执行文件，这个默认

<figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

选择HTTPS后端传输，可以直接默认

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

**（对不起我写不下去了，下面所有选项全部默认就好了）**

## 配置GitHub的SSH

> 一 、\
> 设置Git的user name和email：\
> $ git config --global user.name "xuhaiyan"\
> $ git config --global user.email "haiyan.xu.vip@gmail.com"
>
>
>
> 二、生成SSH密钥过程：\
> 1.查看是否已经有了ssh密钥：cd \~/.ssh\
> 如果没有密钥则不会有此文件夹，有则备份删除\
> 2.生存密钥：\
> $ ssh-keygen -t rsa -C “haiyan.xu.vip@gmail.com”
>
> 如果提示  ssh-keygen 不是内部命令或者。。。
>
> 这时候要配置环境变量，具体操作如下：
>
> 1.找到Git/usr/bin目录下的ssh-keygen.exe(如果找不到，可以在计算机全局搜索)
>
> 2.属性-->高级系统设置-->环境变量-->系统变量,找到Path变量，进行编辑，End到最后，输入分号，粘贴复制的ssh-keygen所在的路径，保存；
>
> &#x20;\
> 按3个回车，密码为空。
>
> Your identification has been saved in /home/tekkub/.ssh/id\_rsa.\
> Your public key has been saved in /home/tekkub/.ssh/id\_rsa.pub.\
> The key fingerprint is:\
> ………………
>
> 最后得到了两个文件：id\_rsa和id\_rsa.pub
>
> 3.添加密钥到ssh：ssh-add 文件名\
> 需要之前输入密码。\
> cd \~/.ssh 文件夹在：C:\Users\kingdee\\.ssh 有一个文件名为id\_rsa.pub，把里面的内容复制到git库的我的SSHKEYs中
>
> 4.在github上添加ssh密钥，这要添加的是“id\_rsa.pub”里面的公钥。\
> 打开https://github.com/ ，登陆xuhaiyan825，然后添加ssh。

## 使用

git bash是用的最多的git命令行程序

git gui有图形界面，但是功能相对简陋，该用bash还得用bash

#### 命令

* git push：把所有提交上传
* git pull
* git add
  * git add .：往暂存区添加所有更改
* git commit -m "some text"：提交
* git branch sth：创建分支
* git checkout：切换分支
* git branch -d sth：删除分支
