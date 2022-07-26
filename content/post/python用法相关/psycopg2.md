---

title: Python psycopg2
date: 2022-05-05T12:22:45+08:00
draft: false

---
## **学习背景**
工作中常用到的数据库是PostgreSQL，在编写python脚本的时候免不了要连接数据库进行数据交换。需要一个第三方库来实现需求，于是发现了psycopg2...

## **安装方法**
```python
    pip install psycopg2
```
1. 使用pip进行安装，一般将pip升级到最新版本后，直接安装不会出现问题
2. 如果使用pycharm，也可以在interpre里面进行安装

```python
    import psycopg2
    -->>>
```
安装完成后试着import，出现-->>就是成功了

## **使用方法--查询**
```python
    import psycopg2
    ...
    # 创建一个连接，分别填上数据库的databases、user、password、host、port信息
    conn = psycopg2.connect(database=databases, user=users, password=passwords,
                        host=hosts, port=ports)
    # 创建一个cursor()方法
    opt = conn.cursor()
    # 创建一个或多个sql语句
    sqlTest = 'select * from Schemas.table'
    # 用execute执行sql语句
    opt.execute(sqlTest)
    # 使用fetchall将sql结果print出来
    [1] result = opt.fetchall()
    print(result)
    # 如果sql的结果仅一个，可以将fetchall改为fetchone
    [2] result = opt.fetchone()
    print(result)
    # 正常返回的数据类型为元组，tuple
    print(type(result))
-->> <'class'> :tuple
```
psycopg2自己暂时只用到查询方法，后面继续学习其他使用场景

## **待续。。。**