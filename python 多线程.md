# python 线程、进程

 多任务同时执行

实现方式：多线程、多进程、多进程+多线程

## 多线程

### 使用

```python
import threading

def shower():
    for i in range(10):
        print("你去洗澡啦")

def eat():
    for i in range(10):
        print("你去吃饭吧")

# target 需要一个函数，用来指定线程需要执行的任务
t1 =threading.Thread(target=shower) # 创建了一个线程1
t2 = threading.Thread(target=eat) # 创建了一个线程2
# 启动线程
t1.start()
t2.start()
```

### 多线程共享全局变量

 同时操作一个变量会出现线程安全问题；

解决方案是使用线程锁

```python
import threading
lock = threading.lock()
# 在使用到共享变量的前面 加锁
lock.acquire()
# 结束使用的后面 释放锁
lock.release()
```

# 多进程

