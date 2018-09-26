## 1.线程与进程

对于操作系统来说，一个任务就是一个进程（Process），比如打开一个浏览器就是启动一个浏览器进程，打开一个记事本就启动了一个记事本进程，打开两个记事本就启动了两个记事本进程，打开一个Word就启动了一个Word进程。

有些进程还不止同时干一件事，比如Word，它可以同时进行打字、拼写检查、打印等事情。在一个进程内部，要同时干多件事，就需要同时运行多个“子任务”，我们把进程内的这些“子任务”称为线程（Thread）。

## 2.常用内建模块

datetime是Python处理日期和时间的标准库

```python
from datetime import datetime
now = datetime.now() # 获取当前datetime
```

```python
from datetime import datetime
dt = datetime(2015, 4, 19, 12, 20) # 用指定日期时间创建datetime
print(dt)
2015-04-19 12:20:00
```

```python
>>> from datetime import datetime #绝对秒数
>>> dt = datetime(2015, 4, 19, 12, 20) # 用指定日期时间创建datetime
>>> dt.timestamp() # 把datetime转换为timestamp
1429417200.0
```

