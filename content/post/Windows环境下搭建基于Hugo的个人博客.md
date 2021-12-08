---
title: "Windows环境下搭建Hugo的个人博客"
date: 2020-02-06T12:22:45+08:00
draft: false
---



## 概述

之前写的一篇博客搭建是基于MacOS系统的，考虑到windows的受众面比较广泛，这里开一篇如何在windows上搭建博客，其中用到的方法和MacOS上大同小异，如若没看懂可以移步之前那篇，下文中会给出链接

## 一、（下载hugo）

1、hugo官方下载地址https://github.com/gohugoio/hugo/releases

2、创建文件夹。此处举例：F盘创建 **`hugo/bin`**，将解压后的**`hugo.exe`**放到**`bin`**目录下。

3、配置系统环境变量。将**`F:\hugo\bin`**加到**path**变量中，以上设置好后，就可以在cmd中查看是否安装成功。执行命令：

> $ **`hugo version`**

没返回报错即代表配置成功

## 二、生成站点

> 进入`F:\hugo`下，打开命令窗口,输入

> $ **`hugo new site`** 文件名称 (如`blog`)

执行后，在hugo目录下就会生成一个 名叫`myblog`的站点文件夹

进入`myblog`，显示以下目录结构：

- archetypes　(存放default.md，头文件格式，每次新建文章默认显示的头部信息在此修改)
- content 　　 (存放博客文章，markdown格式文件)
- data (存放自定义或者导入的模板)
- layouts (存放网站的数据模板)
- static (存放图片、css、js等静态资源)
- themes (存放主题文件，每个主题都是一个独立的文件夹)
- config.toml (网站配置文件)

## 三、创建文章

进入**站点根目录**`myblog`下，执行命令：

> $ **`hugo new post/test.md`**

执行后，会自动在content/post下生成 test.md文件，打开可编辑内容(markdown编辑器推荐Typora

**注意：文件头部的draft要改为false，这样部署后才能看到文章。**

当前网站是没有任何内容的，需要下载个主题。

## 四、下载主题

> $ **`git clone`** https://github.com/vaga/hugo-theme-m10c.git themes/m10c
>
> 也可以直接下载压缩包解压到themes目录

这样themes下就多了一个文件夹，文件夹名即为主题名称。此时可回到站点目录下打开`config.tom
配置指定主题，如theme = “m10c” 没有theme参数就自己写上

**站点根目录**下，执行命令：

> hugo server --theme=m10c --buildDrafts

其中 --theme 选项可以指定主题，–buildDrafts 包括标记为草稿

执行后会显示

> Web Server is available at http://localhost:1313/ (bind address 127.0.0.1) Press Ctrl+C to stop

可访问：http://localhost:1313/ 查看效果

## 五、部署到原创GitHub上

这一部分可以查看我之前写的在macos上的操作，大同小异，这里就不做赘述了。

贴上地址：https://wcu99.github.io/post/%E5%9F%BA%E4%BA%8Ehogo%E6%90%AD%E5%BB%BA%E7%9A%84%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/

