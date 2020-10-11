#  python 字典

适用场景：列表一般存储同一数据类型 或者 含义相同的数据集合

​					字典可以保存不同含义；并且元素已键值对存在，键对

​					值进行描述

## 使用

```python
person = {
    'name': 'zs',
    'age': 18
}
# 1、key不予许重复; 若存在重复的key;后一个keyd的值会替代前一个的key的值
# 2、key只允许为不可变数据类型
# 3、字典存储是无序的
```

## 操作

### 增

```python
person = {
    'name': 'xiaoming',
    'age': 18
}
person['gender'] = 'female'
```

### 删

```python
person = {
    'name': 'xiaoming',
    'age': 18
}
person.pop('name') # 删除 name 若没有name则抛出异常 返回值为被删除的 value
person.popitem() # 删除 返回值为被删除的键值对
person.clear() # 清空一个字典
del person['age'] # 删除age 没有回报错
```

### 改

```python
person = {
    'name': 'xiaoming',
    'age': 18
}
person['age'] = 19 
```



### 查

```python
person = {
    'name': 'xiaoming',
    'age': 18
}
person['age'] # 18
person['book'] # 会报错
person.get('book') # None 不会报错
person.get('book', 'chinese') # chinese 如果没找到则返回chinese 不会往字典增加
```

### update

```python
p_1 = {
    'name': 'xiaoming'
}
p_2 = {
    'age': 18
}
p_1.update(p_2) # p_1=> {'name': 'xiaoming', 'age': 18}
# 拓展
s1 = ('yes', 'ok')
s2 = ('no', 'hi')
s1 + s2 # => ('yes', 'ok', 'no', 'hi')    s1、s2本身没有变
# 字典之间不可以 + 运算
```

### 遍历

```python
person = {
    'name': 'xiaoming',
    'age': 18,
    'height': '180'
}
for x in person:
    print(x, person[x]) # x为key

for x in person.keys(): # 获取所有的key  是一个list
    print(x, person[x]) # x为key
    
for x in person.values(): # 获取所有的value 是一个list
    print(x) # x为value
    
for x in person.items(): # 获取所有的键值对 是一个list里面是元组 [()]
    print(x) # x 为(key, value)
for k,v in person.items(): # 获取所有的键值对 是一个list里面是元组 [()]
    print(k,v) # k 为key,v 为 value
```

### 推导式

```python
dict1 = {"a":100, "b":200 }
dict2 = {v,k for k,v in dict1.items()}
print(dict2) # {100:"a", 200:"b" }
```

