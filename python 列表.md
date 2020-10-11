# python-列表

## 列表的基本使用

### 列表的表示

1. 使用 [ ] 表示一个列表

2. 可以使用 list(可迭代对象) 将可迭代对象转换

   ```python
    names = list(('zhangsan', 'lisi', 'wanger'))
    print(names) // ['zhangsan', 'lisi', 'wanger']
   ```

### 列表的操作

​	可以通过下标获取元素和对元素进行切片；还可以修改元素

​	切片与字符串用法一致

#### 	增

##### append

```python
list.append('sth') // 在列表的最后面追加
```

##### insert

```python
list.insert(index, 'sth') // 在索引之前插入数据
```

##### extend

```python
list.extend(iterable) // 将一个可迭代对象追加到list 
```

#### 删

##### pop

```python
list.pop() // 删除list的最后一个， 返回被删除的元素
list.pop(index) // 删除指定位置的元素
```

##### remove

```python
list.remove(obj) // 删除指定元素， 若元素不存在会抛出异常
```

##### clear

```python
list.clear() // 清空list
```

##### del

```python
del list[i]
```

#### 改

##### 下标修改

#### 查

##### index

```python
list.index(obj) // 返回下标，若无会抛出异常
```

##### count

```
list.count(obj) // 计数
```

### 列表的遍历

```python
for iter in iterable:
	print(iter)
    
while i < len(iterable):
    print(iterable[i])
```

### 列表的排序

```python
list.sort(reverse=False) // 升序排序 reverse=True 降序
new_list = sorted(list) // 内置排序函数 生成新的有序list 不会改变原list
```

### 列表的反转

```python
list.revers() // new_list = list[::-1] 反转list
```

### ※列表的复制

pyhton里的数据分为可变类型和不可变类型

可变类型：列表、字典、集合

不可变类型：字符串、数字、元祖

![](.\images\可变与不可变数据类型.png)

![](.\images\列表的copy.png)

### ※浅拷贝、深拷贝

```python
# 浅拷贝
list = ['hi', 'yes', [10, 20, 30], 'ok']
list_1 = copy.copy(list)
list[0] = 'hello'
print(list_1)  # ['hi', 'yes', [10, 20, 30], 'ok']
list[2][1] = 2
print(list_1)  # ['hi', 'yes', [10, 2, 30], 'ok']
#浅拷贝 只拷贝一层 list里面的list实际上指向同一list
#所以当浅拷贝后 改变里层的list 拷贝与被拷贝的都会改变
```

```python
import copy
list = ['hi', 'yes', [10, 20, 30], 'ok']
list_2 = copy.deepcopy(list)
list[0] = 'hello'
print(list_2)  # ['hi', 'yes', [10, 20, 30], 'ok']
list[2][1] = 2
print(list_2)  # ['hi', 'yes', [10, 20, 30], 'ok']
#深拷贝 完全复制 两者没有任何关联
```

