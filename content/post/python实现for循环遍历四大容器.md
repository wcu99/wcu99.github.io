---

title: "python中实现for循环遍历四大容器"
date: 2020-03-25T12:22:45+08:00
draft: false

---

## 实现for循环遍历四大容器

#### #for循环

#作用：可以让指定的代码重复执行，可以循环遍历容器中的数据（从容器中把数据一个一个取出）

#格式：for 临时变量 in 容器：

​				对临时变量的处理

#特点：临时变量从容器中一个一个获取到

#注意：for循环中可以添加条件判断
#注意：for循环不能遍历数字，浮点数，布尔类型这样不可遍历的类型

#### #定义列表

```python
info_list = [100,'hello',true,12.5,(10,20)]

for value in info_list:

		print(value) 
结果：
100
hello
true
12.5
(10，20)

```

#### #定义元组

```python
info_tuple = (10,20,30,40,50)

for value in info_tuple:

				print(value)
结果：
10
20
30
40
50
```

#### #定义字符串

```python
info_str = "hello"

for value info_str:

			print(value)
结果：
h
e
l
l
o
```

#### #定义字典 (获取键值对的“键”)

```python
info_dict = {"name":"张三","age":30,"high":175}

for i in info_dict:

			print(i)

结果:

name

age

high

同时获取键值方法
info_dict = {"name":"张三","age":30,"high":175}

for i in info_dict:

			print(i,info_dict[i])

```

