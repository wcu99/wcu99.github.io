---

title: "Python中比较日期"
date: 2021-12-08T12:22:45+08:00
draft: false

---

## datetime 方法
ex：
    star_time = 2021-10
    end_time = 2022-12

import datetime
import time

star_time = time.strptime(star_time, ''%Y-%m')
end_time = time.strptime(end_time, ""%Y-%m")

if start_time <= end_time:
    print(" ")
else:
    print(" ")

## replace 方法
ex：
    star_time = 2021-10
    end_time = 2022-12
star_time = star_time.replace("-", " " )
end_time = end_time.replace("-", " ")