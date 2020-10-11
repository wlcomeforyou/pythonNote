# python eval、json、pickle

序列化 

​	dumps ：将python数据转换成二进制

​	dump：将python数据转换成二进制并保存到指定文件

反序列化 

​	loads：将二进制加载成python数据 

​	load：读取文件，将文件的二进制内容加载成python数 据 

## eval

内置函数：可以执行字符串里的代码

```python
a = 'print("zs")'
print(eval(a)) # zs
```

## json

把列表、元组、字典等转换为JSON字符串

```python
import json
m = json.dumps({"name": "zs", "age": 18}) # dumps 转化成JSON字符串
print(m) # {"name": "zs", "age": 18}

n = '{"name": "zs", "age": 18}'
s = json.loads(n) # loads json字符串转换成python对象 
```

## pickle

将任意对象转换成二进制

```python
import pickle
names = ['张三', '李四', '王二']
b_names = pickle.dumps(names) # 转换成二进制
file = open('names.txt', 'wb') # 写入的是二进制 不是纯文本
file.close()

file1 = open('names.txt', 'rb') # 以二进制读取
b_content = file1.read()
content = pickle.loads(b_content) # 转换成
file1.close()

```

