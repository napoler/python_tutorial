# try except 捕获所有异常

```text
try:
    a=1
except Exception as e:

    print (e)


import traceback
import sys
try:
    a = 1
except:
    traceback.print_exc()
    #sys.exc_info() 

```

