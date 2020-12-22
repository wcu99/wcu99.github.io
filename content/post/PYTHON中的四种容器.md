---

title: "PYTHON中的四种容器"
date: 2020-10-02T12:22:45+08:00
draft: false

---

## PYTHON中的四种容器

列表list

元组Tuple

字典Ddict

集合set

## **四种数据类型的比较**

1. 元组Tuple是存放固定的数据
2. 集合set中的数据插入和遍历的时间，随数据的增多而变慢
3. 列表List中的数据插入和查询的时间，随数据的增多而变慢
4. 字典Ddict中的数据插入和查询的速度非常快，不会因为数据太多而变慢

​     元组、集合和列表占用内存较少，字典占用内存较多，字典是一种通过占用空间来换取操作速度的一种数据类型。

## 列表（list）

定义：列表是一种线性表，由大量的节点组成，每一个 节点都可以存放大量的数据。
创建：列表名=[节点，节点，节点，节点] 例如：ls=[1,2,3,4,]
访问：列表是有序的可以通过下标来访问，从0开始
常用方法：

```python
列表名.append() 添加一个节点
     .clear()  删除列表
     .copy()  开辟了一块新的内存，把原来的复制
     .count()  在数组中的重复次数
     .index()  查询元素在列表中第一次出现的下标。
     .insert()指定要插入位置和元素。xxx.insert(1,"xx")
     .remove()移除列表中对应的元素
     .pop()通过下标进行移除，若不添加下标则删除最后一位
     .reverse()倒序
     .sort()按照数字大小进行排序。
     .extend 合并列表 xx.extend(yy) 对xx列表进行添加yy
     
123456789101112
list=[1,7,6,4]
print(list)
list.append(5) #添加
print(list)
ls=list.copy()#浅拷贝
print(ls)
list.insert(0,1)#在list[0]处添加1
print(list)
print(list.count(1))#重复次数
print(list.index(1))#第一次出现的位置的下标
list.sort() #排序
print(list)
list.reverse()#倒序
print(list)
list.extend(ls)#将两个表合并
print(list)
list.remove(7)#移除节点7，仅移除第一个
print(list)
list.pop(0) #移除下标为0的元素
print(list)
list.clear()#删除该列表
print(list)
12345678910111213141516171819202122
```



## 集合（set）

定义：元素唯一，不能重复，无序的，不能通过下标去访问
创建：集合名=set（{元素，元素，元素}）例如：ss = set({1,3,4,5,6,})
访问，由于是无序的只能通过元素名来访问
常用方法：

```python
集合名.add() 添加一个元素
     .difference() 差集
     .intersection() 交集
     .union() 并集
     .pop()随机移除一个元素
     .remove() 通过元素名移除，不存在会报错
     .discard()移除一个元素，不存在也不报错
1234567
s1=set({1,3,4,5,7})
s2=set({2,4,6,8})
print(s1,s2)
s1.add(9)#添加
print(s1)
s3=s1.copy()#浅拷贝
print(s3)
print(s1.difference(s2))#差集
print(s1.intersection(s2))#交集
print(s1.union(s2))#并集
print(s1)
s1.pop()#随机删除一个元素
print(s1)
s1.remove(3)#移除元素3
print(s1)
s1.discard(3) #移除元素3，没有该元素也不报错
12345678910111213141516
```



## 元组（tuple）

定义：元组表示固定，不可变的值，不可变的类型,可以通过下标访问，**如果某元素的是可变类型，那么该元组可以发生改变。比如添加了一个list。在定义元组是若只有一个元素需要在后面加上一个“，”否则会将()认为是数学中的提高优先级。**
创建：元组名=tuple((元素，))例如：a=tuple(1,) a=tuple((1,2,3,4,5,6))
访问：元组可以通过下标来访问
常用方法：

```python
元组名 .count()  在数组中的重复次数
      .index()  查询元素在列表中第一次出现的下标
    
123
t1=tuple((1,2,3,3,4,4,4,4,55,))
print(t1)
print(t1.count(3))#查看3重复的次数
print(t1.count(4))
print(t1.index(55))#查看55所在位置的下标
12345
```



## 字典（dict）

定义：字典一个二维表分为key，value。key必须是字符串，key和value之间使用“:”分隔
创建：字典名={“key“：”value“,“key“：”value“}例如a={“name”:“xxx” “age”:“160”}
访问：字典的访问主要通过key来访问
常见方法：

```python
字典名.get通过key返回对应的value
	 .items成对返回对应的
for k,v in xx.items：
    print(k,v)
	 .keys返回所有的keys
	 .values返回所有的values
	 .pop 通过key来删除对应的value
	 .popitem 移除一对key,value遵循后进先出的规则。
	 
123456789
a={"郭靖":"黄蓉","杨康":"穆念慈","东邪":"冯蘅"}
print(a.get("东邪"))
for k,v in a.items():
    print(k,v)
print(a.keys())
print(a.values())
print(a.pop("郭靖"))
print(a)
print(a.popitem())
print(a)
```