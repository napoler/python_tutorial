# Python 编程中使用 time 模块可以让程序休眠

Python 编程中使用 time 模块可以让程序休眠，具体方法是time.sleep\(秒数\)，其中“秒数”以秒为单位，可以是小数，0.1秒则代表休眠100毫秒。

## 例1：循环输出休眠1秒



`import time`

`i = 1` 

`while i <= 3:` 

`print(i) # 输出i` 

`i += 1` 

`time.sleep(1) # 休眠1秒`



## 例1：循环输出休眠100毫秒

import time

 i = 1 

while i &lt;= 3: 

print i \# 输出i 

i += 1 

time.sleep\(0.1\) \# 休眠0.1秒

