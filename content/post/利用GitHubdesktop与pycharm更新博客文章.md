---
title: "利用GitHubdesktop与pycharm更新博客文章"
date: 2020-06-11T12:22:45+08:00
draft: false
---



## 前言

​	之前分别介绍过如何在Windows和macos下搭建基于Hugo的静态博客，方法是部署到GitHub上实现的。这次来具体聊聊怎么用GitHub桌面客户端（GitHub desktop）配合python可视化工具（这边用的是pycharm）实现对博客进行修改，上传，删除。

### 1.安装GitHub desktop

用搜索引擎搜索github desktop即可，以下为网址

https://desktop.github.com/

可能需要用到科学上网才能顺利下载，这边不做科学上网的拓展，有兴趣的可以自己去了解。

### 2.安装python可视化工具

这边我用到的是pycharm这个软件，其他的软件也是可以的，根据个人喜好选择。

### 3.登录GitHub desktop并拷贝项目到本地

### 4.用pycharm打开拷贝回本地的目录文件



## 更新博客方法

一旦你对这个博客文章进行了修改，需要在pycharm的命令行中输入：

hugo -d docs

没提示报错的情况下，打开GitHub desktop，此时可以看见更改过的项目会出现在界面上，之后在下方输入：

update

然后点提交刷新即可。

过一会刷新你的博客主页，会发现之前对博客文章的修改已经生效~