# python 文件操作

##  使用

使用内置函数open打开并操作一个文件

open 参数介绍

- file：用来指定打开的文件（不是文件的名字，而是文件路径）

- mode：打开文件的模式

  - r：只读

    - 默认 打开文件后，只能读取，不能写入

      ```python
      file = open('xxx.txt',  'r')
      file.read()
      file.write('hello') # 报错
      file.close()
      ```

  - w：只写

    - 只能写入，不能读取；如果文件存在会覆盖；不存在会新建

      ```python
      file = open('yyy.txt',  'w')
      file.read() # 报错
      file.write('hello')
      file.close()
      ```

  - rb：只读二进制

  - wb：只写二进制

    ```python
    file = open('yyy.txt',  'wb')
    file.write('hello') # 报错
    file.write('hello'.encode('utf8'))
    file.close()
    ```

    

  - a：追加； 文件最后追加内容

- encoding：打开文件时的编码（注意读写时的编码一致）

## 文件的读取

```python
file = open('xxx.txt', encoding='utf8')
file.read() # 将所有的数据都读出来
file.read(10) # 在r模式下 读取10个长度以避免一次读取内容太多
file.readline() # 只读一行
file.readlines() # 读取出每一行内容放到一个数组里
```

## with关键字的使用

with 称之为上下文管理器 

```python
with open('xxx.txt', 'r') as file:
	file.read()
# file自动close()
```

