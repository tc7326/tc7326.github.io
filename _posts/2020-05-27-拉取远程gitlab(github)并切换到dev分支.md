引言：
[https://gitlab.com/](https://gitlab.com/)
若注册 无法访问 可以使用 **github** 账号登录，然后在**Settings**里设置账号和密码。

[https://www.git-scm.com/downloads](https://www.git-scm.com/downloads)
在这里下载git.exe

# 创建本地账户和邮箱账户

```java
git config –global user.name “随便起”

git config –global user.email “你的gitlab邮箱地址”
```
# 创建SSH key
```java
ssh-keygen -t rsa -C 你的gitlab邮箱地址	//PS:无双引号

然后一路回车即可
```
创建完成后

一般会在 **C : \ Users \ 你电脑用户名 \ .ssh** 目录下 生成一个 **id_rsa.pub**

复制里面的内容

# 创建SSH key

然后到 **gitlab** 右上角 头像 **Settings**

然后 左边栏 **SSH keys**

将 复制的 **id_rsa.pub** 里的内容粘贴到

**Add an SSH key **里 也就是最大的那个输入框

然后点击 **Add** 即可

# 克隆项目到本地并切换分支
```java

//克隆到本地
git clone 项目地址.git

//查看远端分支
git branch -r

//创建本地dev分支 并切换到dev分支
git checkout -b dev origin/dev

//拉取dev分支的代码
git pull origin dev

```
然后就OK了

PS：这里的dev分支只是举例，具体看公司项目是什么分支。

# HTTP 和 SSH 协议切换
## 查看
```java
//查看你项目的当前协议
git remote -v
```

## 修改
```java
//http 协议 一般长这样
https://github.com/user/project.git

//ssh 协议 一般长这样
git@github.user/project.git

//切换到SSH协议
git remote set-url origin git@github.user/project.git
```
