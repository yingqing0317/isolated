# Git

## 常用指令

### 本地仓库

* 暂存`git add`

* 取消暂存`git reset HEAD <file>即文件名`

* 撤销修改`git checkout -- <file>`（须谨慎使用，因为它会删除在本地进行的所有修改）

* 检查状态`git status`

* 提交`git commit`

  ![image-20220226001944109](C:\Users\青\AppData\Roaming\Typora\typora-user-images\image-20220226001944109.png)

  ![image-20220226001957669](C:\Users\青\AppData\Roaming\Typora\typora-user-images\image-20220226001957669.png)

  

* 克隆`git clone 网址`

* 查看修改历史`git log`

### 远程仓库

* 查看远程仓库`git clone 网址`
* 读取远程仓库的简称和URL`git remote -v`
* 自行添加远程仓库`git remote add 简称 网址`
* 拉取远程仓库中有但本地没有的信息`git fetch 简称`（只会将数据下载到本地仓库，不会直接修改和更新，后续操作需要自己实现）
* 查看远程仓库信息`git remote show 简称`
* 远程仓库重命名`git remote rename 原名 新名`
* 移除远程仓库`git remote remove/rm 简称`（与其相关的远程跟踪分支和配置信息都会被删除）

### 打标签

* 查看所有标签`git tag (-l "v1.8*")`
* 创建轻量标签`git tag -a 标签名`
* 创建附注标签`git tag -a 标签名 -m 注释`
* 查看标签信息`git show 标签名`
* 补打标签`git tag -a 标签名 校验和/部分校验和`
* 查看校验和`git log --pretty=online`
* 共享标签`git push origin 标签名/--tags（很多标签）`
* 删除本地标签`git tag -d 标签名`（不会影响远程仓库，后续须手动更新）
* 更新远程仓库标签`git push 远程仓库名 :refs/tags/v1.4-lw`
* 删除远程仓库标签`git push 远程仓库名 --delete 标签名`
* 检出标签`git checkout 版本号`

### 分支

* 创建分支`git branch 分支名`（仅仅是创建新分支，不会自动跳到新分支）
* 查看各个分支当前所指的对象`git log --online --decorate (--graph --all)`
* 切换到已存在的分支`git checkout 分支名`（这样HEAD就指向该分支了）
* 创建并切换到新分支`git checkout -b 分支名`
* 合并分支`git merge 待合并分支名`（合并当前分支和待合并分支）![image-20220226235334197](C:\Users\青\AppData\Roaming\Typora\typora-user-images\image-20220226235334197.png)
* 删除分支`git branch -d 分支名`

![image-20220226235527613](C:\Users\青\AppData\Roaming\Typora\typora-user-images\image-20220226235527613.png)

* 查看状态`git status`

![image-20220227000737911](C:\Users\青\AppData\Roaming\Typora\typora-user-images\image-20220227000737911.png)

* 使用图形化工具解决冲突`git mergetool`
* 查看分支情况`git branch`

![image-20220227001155763](C:\Users\青\AppData\Roaming\Typora\typora-user-images\image-20220227001155763.png)

* 查看分支合并情况`git branch --merged/--no-merged`（注：已合并到当前分支的可以直接删掉，未合并到当前分支的则须强制删除-如果需要的话）

## 思维导图

![img](https://pic2.zhimg.com/80/v2-31a3f3d822e9c7cd2264054b0808ab61_720w.jpg)

## bug

* `fatal: unable to access 'https://github.com/yingqing0317/learn_git/': OpenSSL SSL_read: Connection was reset, errno 10054`

反复`git push 远程分支名 本地分支名`









# Markdown

![image-20220226130549560](C:\Users\青\AppData\Roaming\Typora\typora-user-images\image-20220226130549560.png)

**加粗**

> 引用

[here][(41条消息) 本地git和远程github连接完整教程_一树荼蘼的博客-CSDN博客_连接github](https://blog.csdn.net/dgreh/article/details/83302358)

- [ ] 待办

```长代码/代码段```

`短代码`

:joy:表情（:<表情名称>:）

![image-20220226133419799](C:\Users\青\AppData\Roaming\Typora\typora-user-images\image-20220226133419799.png)



# GUI

图形用户界面（Graphical User Interface，简称 GUI，又称图形用户接口）是指采用图形方式显示的计算机操作用户界面。



# Webhook

Webhook 就是一个接收 HTTP POST（或GET，PUT，DELETE）的URL，一个实现了 Webhook 的 API 提供商就是在当事件发生的时候会向这个配置好的 URL 发送一条信息，与请求-响应式不同，使用 Webhook 你可以实时接受到变化。

这又是一种对 `客户机-服务器` 模式的逆转，在传统方法中，客户端从服务器请求数据，然后服务器提供给客户端数据（客户端是在拉数据），在 Webhook 范式下，服务器更新所需提供的资源，然后自动将其作为更新发送到客户端（服务器是在推数据），客户端不是请求者，而是被动接收方；这种控制关系的反转可以用来促进许多原本需要在远程服务器上进行更复杂的请求和不断的轮询的通信请求；通过简单地接收资源而不是直接发送请求，我们可以更新远程代码库，轻松地分配资源，甚至将其集成到现有系统中来根据 API 的需要来更新端点和相关数据，唯一的缺点是初始建立困难。

## URL

统一资源定位系统（uniform resource locator;URL）是因特网的万维网服务程序上用于指定信息位置的表示方法。HTTP URL 方案是用来标志因特网上使用HTTP(HyperText Transfer Protocol，超文本传输协议)的可达资源。![image-20220226140422122](C:\Users\青\AppData\Roaming\Typora\typora-user-images\image-20220226140422122.png)

## HTTP请求

[(41条消息) HTTP请求的完全过程_ailunlee的博客-CSDN博客_http请求](https://blog.csdn.net/ailunlee/article/details/90600174)

## API

API（Application Programming Interface，应用程序接口）是一些预先定义的接口（如函数、HTTP接口），或指软件系统不同组成部分衔接的约定。用来提供应用程序与开发人员基于某软件或硬件得以访问的一组[例程](https://baike.baidu.com/item/例程/2390628)，而又无需访问源码，或理解内部工作机制的细节。



# 快照

快照指照相馆的一种冲洗过程短的照片·如：证件快照。基于硬件编程技术的一种，针对内存进行的快速读取技术，常用于硬件开发。





# BN、ReLU与Conv融合

[神经网络量化入门--Folding BN ReLU - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/176982058)

* 如果使用 ReLU 之后的 scale 和 zp，那我们就可以用量化本身的截断功能来实现 ReLU 的作用。

注：ReLU 前后应该使用同一个 scale 和 zeropoint。这是因为 ReLU 本身没有做任何的数学运算，只是一个截断函数，如果使用不同的 scale 和 zeropoint，会导致无法量化回 float 域。

注：ReLU 本身就是在做 clip。所以，我们才能用量化的截断功能来模拟 ReLU 的功能。



