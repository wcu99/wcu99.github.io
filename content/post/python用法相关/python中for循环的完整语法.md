---

title: "python中for循环的完整语法"
date: 2020-03-27T12:22:45+08:00
draft: false

---

### python中for循环的完整语法

#### #for循环的完整语法,for...else语法

#### #1.作用：

遍历数据时，使用的语法格式，满足条件时执行break语句提前终止循环，不执行break语句，则会执行else部分

#### #2.格式：

for 临时变量 in 容器:

​	对临时变量的处理

​	满足条件时，执行break语句

else:

​	在上面for循环中没有执行break语句，容器遍历完，一定会执行else部分

#### 例子

```
#定义列表

info_list = [10,20,30,40,50,60]

#使用for循环完整语法格式遍历列表

​	查找数据30

​	如果找到30，停止遍历

​	如果容器遍历完成也没有找到，结束

find_data = 30

for value in info_list:

​	print(value)

​	if value==find_data:

​	print(value)

  #已经找到数据，停止遍历

​	break

else:

​	print(“没有找到需要的数据”)
```

