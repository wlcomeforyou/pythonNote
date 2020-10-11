# python 集合

集合（set）是一个无序的不重复元素序列，可以使用{}或者set()函数创建集合

注意：创建一个空集合，必须用set()

## 操作

### 增

```python
a = set()
a.add('a')
print(a) # a
a.update({'b'})
print(a) # {'a','b'} 合并集合
a.union({'c'})
print(a) # {'a','b'} union 合并集合 对原集合不操作；返回一个新集合
```

### 删

```python
names = {'a', 'b', 'v'}
names.clear() # 结果 set()  清空
names.pop() # 删除一个 不确定
names.remove('b') # 删除指定元素 没有会报错
```

### 高级使用

set不支持 + 运算

set支持  -  运算 求差集

set支持 & 运算 求交集

set支持 | 运算 求并集

set支持 ^ 运算 求差集的并集