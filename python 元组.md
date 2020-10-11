# python-元组

使用一对小括号() 表示一个元组

元组和列表的区别在于，列表是可变的，而元组是不可变数据类型；不能增加、修改、删除

## 表示

只有一个元素时：

```python
ages = (18,) #加一个 ，
```

多个元素时：

```python
ages = (18, 20, 21)
```

## 用法

```python
ages.index(20)
ages.count(20)
```

## 转换

```python
#将列表转换成元组
words = ['ok', 'yes', 'no']
tuple_words = tuple(words) # ('ok', 'yes', 'no')
# tuple list set都是这样使用 
```

