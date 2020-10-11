# python xpath

## 语法

### 基础语法

| 表达式   | 描述                                   |
| -------- | -------------------------------------- |
| nodename | 选取改元素                             |
| /        | 从根节点选取、或者是元素与元素间的过渡 |
| //       | 匹配选择的当前节点中选取节点           |
| .        | 选取当前节点                           |
| ..       | 选取当前节点的父节点                   |
| @        | 选取节点的属性值                       |
| text()   | 选取文本                               |

### 修饰语法

| 路径表达式                          | 结果                                                         |
| ----------------------------------- | ------------------------------------------------------------ |
| //title[@lang="eng"]                | 选取lang属性值为eng的所有title元素                           |
| /bookstore/book[1]                  | 选取bookstore下第一个book元素                                |
| /bookstore/book[last()]             | 选取bookstore下最后一个book元素                              |
| /bookstore/book[last()-1]           | 选取bookstore下倒数第二个book元素                            |
| /bookstore/book[position()>1]       | 选取bookstore下book元素，从第二个开始                        |
| //book/title[text()='Harry Potter'] | 选取所有book下的title元素，且文本仅为Harry Potter的title元素 |
| /bookstore/book[price>35.00]/title  | 选取bookstore中的book元素的所有title元素，且其中price元素值大于35.00 |

