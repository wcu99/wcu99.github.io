---

title: Python multiprocessing库 多进程
date: 2022-06-08T12:22:45+08:00
draft: false

---

进程与线程的区别：
1. 进程使用的是本机CPU的核心数，因此进程的最大数量与本机CPU核心数相关
2. 线程使用的是某个CPU核心，在此核心下创建线程，线程数理论上可以是任意数
3. 线程中如果这个CPU核心挂了，那么下面的线程也会受到影响；进程相互独立

运用的场景：
数据量较大时，依靠单线程效果不理想，建议加入多线程处理，以提高速度

## **multiprocessing库与thread**
1. 实际项目中尝试用过一次thread，但效果不理想，转而学习multiprocessing的使用
2. 若一份list原数据需要切分后分别传入相应的线程，使用thread时需要指定分配；multiprocessing可自己读取
```python
    multiprocessing.thread1 ----->list1
    multiprocessing.thread2 ----->list2
    ....
    multiprocessing.thread3 ----->list3

    thread.threading1 ----->list1
    thread.threading2 ----->list1
    thread.threading3 ----->list2
```
## **一、多进程简易用法**
### **1.首先导入库**
```python
​	import multiprocessing
```
## ***2.定义将要丢入multiprocessing的函数***
```python
   def test(arg):
    return
```
## ***3.调用***
```python
   if __name__ == '__main__'
    jobs = []
    for i in range(5):
        i+=1
        p = multiprocessing.Process(target=test, args=(arg,))
# jobs 进程池
# for i in range(num) 启动
# i+=num 进程池的数量
# jobs.append(p) 把进程p放进进程池，进程池的数量为i+=num
# start 启动程序
```

## **二、多线程简易用法**
### **1.首先导入库**
```python
    from multiprocessing.dummy import Pool as ThreadPool
    #从multiprocessing的dummy导入Pool方法  as 后面是别名，可任意取
```
### **2.定义将要丢入Pool的函数**
```python
   def test(arg):
    return
```

### **3.调用**
```python
   if __name__ == '__main__':
    p = ThreadPool(processes=5)
    p.map(proce, sqlResult)
    p.close()
    p.join()
# processes=num  num为线程数量
# map方法放入函数及函数的参数，如入参有多个的情况。可将map换为apply
# 关闭进程池（pool），使其不再接受新的任务
# 主进程阻塞等待子进程的退出， join方法要在close或terminate之后使用