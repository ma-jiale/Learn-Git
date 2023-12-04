# 学习Git笔记

## 什么是Git? 

Git是一个免费开源的分布式**版本控制系统**，它使用**仓库**（数据库类型）来记录文件。仓库中的文件有完整的版本历史记录。

## 安装和初始化

使用powershell

~~~
git -v
~~~

确认是否安装好git

配置用户名和邮箱，目的是识别出是谁提交的内容

--global:全局配置

--system:系统配置

## 新建仓库

~~~
git init
~~~

~~~
git clone <url>
~~~

## git工作区域和工作状态

工作区，暂存区，本地仓库

文件的状态：未跟踪，未修改，已修改，已暂存

~~~
git status //查看仓库状态
git add //添加到暂存区
git add. //可以提交当前文件夹
git commit -m "" //提交，只提交暂存区内容，不会提交工作区内容
git log //查看仓库提交记录
git log --oneline
~~~

## git reset 回退版本

~~~
git reset --soft
git reset --hard
git reset --mixed
git ls-files //查看暂存区内容
git reflog //查看操作的历史记录
~~~

## git diff 查看差异

~~~
git diff //查看工作区和暂存区的差异
git diff HEAD //比较工作区和版本库之间的差异
git diff --cached //比较暂存区和版本库之间的差异
git diff <commit_hash><commit_hash> //比较提交之间的差异
~~~

HEAD指的是某一分支的最新节点

## 使用git rm删除文件

~~~
git rm <file> //把文件从工作区和暂存区同时删除
git rm --cached <file> 把文件从暂存区删除，但保留在当前工作区中
~~~

删除后提交，版本库中的文件才能一并被删除。

## .gitingore忽略文件/文件夹

将想要忽略的文件名（包括后缀）添加到.gitingore文件中

*.log忽略所有log文件。

.gitingore忽略规则和模板

[github/gitignore: A collection of useful .gitignore templates](https://github.com/github/gitignore)

## Github

**GitHub**是一个在线软件[源代码](https://zh.wikipedia.org/wiki/源代码)托管服务平台，使用[Git](https://zh.wikipedia.org/wiki/Git)作为[版本控制](https://zh.wikipedia.org/wiki/版本控制)软件

注册github账号

## SSH KEY

**安全外壳协议**（Secure Shell Protocol，简称**SSH**）是一种加密的[网络传输协议](https://zh.wikipedia.org/wiki/网络传输协议)，可在不安全的网络中为网络服务提供安全的传输环境。

SSH以[非对称加密](https://zh.wikipedia.org/wiki/非对称加密)实现[身份验证](https://zh.wikipedia.org/wiki/身份验证)[[2\]](https://zh.wikipedia.org/zh-cn/Secure_Shell#cite_note-rfc4252-2)。身份验证有多种途径，例如其中一种方法是使用自动生成的公钥-私钥对来简单地加密网络连接，随后使用密码认证进行登录；

