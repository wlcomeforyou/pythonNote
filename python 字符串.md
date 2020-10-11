# python 字符串

 **<u>字符串是不可变数据类型；对于字符串的任何操作，都不会改变原有的字符串</u>**

 ## 转义字符

在字符串前面加 r 表示 原声字符创；不对里面的含义字符转义

## 下标和切片

### 切片：[start : end : step]

- 包含start;不包含end
- 如果只有start，会取到最后
- 如果只有end，会从头开始
- 如果start和end都为负数；表示从右边数
- start和end都没有，从头到尾复制
- start和end都没有，并且step为-1，表示倒序
- step：步长为每个step-1
  - 默认为1
  - 不能为0
  - 为负数时，表示从右往左

## 字符串的常见操作

### len()

​		获取字符串长度

### find/index/rfind/rindex([start,end])

​		查找内容相关

- find/index

  区别: find找不到 返回-1；index找不到 报错

- rfind/rindex

  区别: rfind找不到 返回-1；rindex找不到 报错

### startswith,endswith,isalpha,isdigit,isalnum,isspace

- startswith,endswith: 以什么开始，结尾
- isalpha：是不是字母
- isdigit： 是不是只有数字组成，有符号 也不行
- isalnum：是不是有字母或者数字组成，有符号 也不行
- isspace：是否全部由空格组成

### count([start,end])

​		返回在start,end之间字符出现的次数

### replace

​		替换字符串的内容

### split,rsplit,splitlines,partition,rpartition

- split,rsplit('split_str',maxsplit)：将字符串以 split_str分割maxsplit次
- splitlines：以换行符分割
- partition,rpartition('split_str')：将一个字符串 分成 3部分=> 前面 分隔符 后面

### capitalize,title

​		让第一个单词/每个单词的首字母大写

### upper,lower

​		全大写/小写

### ljust,rjust,center(length，fillchar='')

​		让字符串以指定长度显示,如果长度不够使用fillchar补齐；str长度够了,直接显示

### lstrip,rstrip,strip(strip_str)

​		将字符串中的 strip_str去掉

### join(iterable_object)

​		将可迭代对象拼接成字符串

### in,not in

​		判断字符串有无某个字符

## 格式化输出字符串

1.  %占位符

   -  %s ==> 表示字符串占位符
   -  %d ==> 表示整数占位符
   -  %nd ==> 表示显示n位，如果不够，在前面空格补齐
   -  %f ==> 表示浮点数占位符

2.  format

   ```python
   x = '大家好，我是{}，今年{}岁'.format('张三', 18)
   print(x) // 大家好，我是张三，今年18岁
   y = '大家好，我是{0}，今年{1}岁'.format('张三', 18)
   print(y) // 大家好，我是张三，今年18岁
   z = '大家好，我是{name}，今年{age}岁'.format(name='张三', age=18)
   print(z) // 大家好，我是张三，今年18岁
   ```

   

​		



