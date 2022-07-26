---

title: "Python multiprocessing库 多进程"
date: 2022-06-08T12:22:45+08:00
draft: false

---

1.首先导入库

​	`Import multiprocessing`

2.定义将要丢入multiprocessing的函数

​	`def test():`

3.调用

`if __name__=='__main__':`

​    `jobs=[]`

​    `for i in range(5):`

​        	`i+=1`

​        	`p = multiprocessing.Process(target=函数,args=(函数的入参))`

​        	`jobs.append(p)`

​        	`p.start()`

"jobs" 进程池

"for i in range(num)" 启动

"i+=num" 进程池的数量

"jobs.append(p)" 把进程p放进进程池，进程池的数量为i+=num

"start" 启动程序