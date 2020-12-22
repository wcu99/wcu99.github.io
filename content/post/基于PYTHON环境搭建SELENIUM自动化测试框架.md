---
title: "基于python环境搭建selenium自动化测试框架"
date: 2020-09-07T12:22:45+08:00
draft: false
---



# 1.环境搭建

#### 基于python环境搭建

1.python开发环境

2.安装selenium

3.安装浏览器

4.安装浏览器驱动



# 1.1安装selenium

注意：python3安装完毕并且能够正常运行

### pip工具

pip是一个通用的python包管理工具，提供了对python包的查找、下载、安装、卸载功能。

#### 安装

pip install selenium

#### 卸载

pip uninstall selenium

# 1.2安装浏览器

常见的火狐、谷歌、microsoft edge等都可以

# 1.3安装浏览器驱动driver

方法：可以去GitHub上面找对应版本的浏览器驱动，也可以用搜索引擎搜索对应驱动

# 2.尝试使用selenium

1.导包

​	from selenium import webdriver

2.创建浏览器驱动对象

​	Firefox浏览器：driver = webdriver.Firefox()

​	Chrome浏览器：driver = webdriver.Chrome()

​	Edge浏览器：driver = webdriver.Edge()

3.打开web页面

​	driver.get("http://www.baidu.com")

4.暂停

​	time.sleep(3)

5.关闭驱动对象

​	driver.quite()

#### 例子：调用Firefox浏览器打开百度，停止三秒后退出浏览器

代码：

from selenium import webdriver

driver = webdriver.Firefox()

driver.get("http://www.baidu.com")

time.sleep(3)

driver.quite()



上述例子成功之后，表明selenium环境已搭建好~