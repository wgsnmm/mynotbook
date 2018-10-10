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

## python中主要存在四种命名方式：

1、object #公用方法

2、_object #半保护

​                 \#被看作是“protect”，意思是只有类对象和子类对象自己能访问到这些变量，

​                  在模块或类外不可以使用，不能用’from module import *’导入。

​                \#__object 是为了避免与子类的方法名称冲突， 对于该标识符描述的方法，父

​                  类的方法不能轻易地被子类的方法覆盖，他们的名字实际上是

​                  _classname__methodname。

3、_ _ object  #全私有，全保护

​                       \#私有成员“private”，意思是只有类对象自己能访问，连子类对象也不能访

​                          问到这个数据，不能用’from module import *’导入。

4、_ _ object_ _     #**内建方法，用户不要这样定义**

## 关于from sys import argv

```
sys.argv是传递给python脚本的命令行参数【字符串】列表
argv[0]为该脚本自身路径，其余为命令行参数
```

  