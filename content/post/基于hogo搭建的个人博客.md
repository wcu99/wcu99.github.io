---
title: "MACOS环境基于hugo搭建的个人博客"
date: 2020-09-07T12:22:45+08:00
draft: false
---

## 概述

Hugo 是基于go语言搭建起来的一个静态博客



## 搭建前的准备：

#### 一、Mac os下推荐使用brew这个工具进行安装，下文使用到的也是brew命令安装Hugo。



#### 二、安装Hugo

打开终端，使用命令：brew install Hugo，等待进度条结束即可。



#### 三、检查是否安装成功

终端下输入：hugo version

返回：Hugo static site generator v：xxx   表示安装成功。



## 开始搭建博客

#### 一、生成博客

终端输入：hugo new 博客所在主文件名

例如：hugo new myblog



#### 二、下载并设置主题

主题下载地址：themes.hugo.io

安装主题：两种方法

1⃣️终端切到博客根目录，输入命令git clone 你所选用的主题的github地址

2⃣️主题页面提供的安装命令

下载完成后主题在themes文件夹下

 

#### 三、本地启动博客

终端输入：hugo server -t 主题名 –buildDrafts

使用返回的地址在浏览器上预览博客主页。



#### 四、创建博客文章

可以在终端博客跟目录输入：hugo new 文章目录/文章名.md

例如：hugo new post/test.md

创建完成后可用vim命令修改文章内容也可以用适配md格式的软件进行编辑。



## 将个人博客部署到远端服务器，以GitHub为例

#### 一、GitHub 新建repository

#### 二、将个人博客部署到GitHub仓库

1⃣️终端输入：hugo --theme=主题名 --baseurl=“仓库地址” --buildDrafts

完成后会生成一个public文件夹。

2⃣️切换到public文件下，输入：

git init

git add .

git commit -m "提交的描述"

3⃣️本地public文件和远程GitHub关联

git remote add origin 仓库地址.git

4⃣️推送到仓库

git push 如果这个命令提示失败也可以尝试下面的命令

git push -u origin master 然后按照提示输入GitHub的账户密码



## 至此个人静态博客部署完成






