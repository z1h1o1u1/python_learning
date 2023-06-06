## 字符串-一系列字符

任何单引号、双引号或三引号下的数据都是字符串，有不同的字符串方法和内置函数来处理字符串。
```python
"this is python"
'this is python'
```

### 使用以及转义字符
使用字符串时只需赋予变量一个字符串
```python
name = "charon"
print(name)
```
转义的意思就是：**采用某些方式暂时取消该字符本来的含义**

| 转义字符 | 说明            |
| -------- | --------------- |
| \'       | 单引号          |
| \\       | 反斜杠          |
| \n       | 换行            |
| \r       | 回车            |
| \t       | Tab             |
| \b       | 退格(Backspace) |
| \f       | 换页            |
| \ooo     | 八进制值        |
| \xhh     | 十六进制值      |       

```python
print("python")
print("\tpython")
print("language:\npython\nc++")
```

为什么要怎么做？可以试着运行下面的示例
```python
message  = 'this is charon's computer'
print(message)
```

### 运算字符

| 运算字符 | 说明                                               |
| -------- | -------------------------------------------------- |
| +        | 字符串连接                                         |
| *        | 重复输出字符串                                     |
| []       | 通过索引获取字符串中字符                           |
| [:]      | 截取字符串中的一部分，遵循**左闭右开**原则         |
| in       | 成员运算符 - 如果字符串中包含给定的字符返回 True   |
| not in   | 成员运算符 - 如果字符串中不包含给定的字符返回 True |

示例
```python

language = 'python'
first_three = language[0:3] # pyt
print(first_three)

name = "charon"
if "c" in name:
    print(name)
```

### 字符串中的方法
**方法是python可对数据执行的操作（类中的函数）**
示例
```python
name = "charon"
print(name.title())
name = "CHARON"
print(name.upper())
print(name.lower())
```
**比如name后的点（.）让python执行方法title()，而后面的括号内可选填额外的信息来完成工作**

| 方法         | 说明                                                                |
| ------------ | ------------------------------------------------------------------- |
| capitalize() | 将字符串的第一个字符转换为大写                                      |
| len()        | 返回字符串长度                                                      |
| lower()      | 转换字符串中所有大写字符为小写.                                     |
| lstrip()     | 截掉字符串左边的空格或指定字符。                                    |
| max()        | 返回字符串 str 中最大的字母。                                       |
| min()        | 返回字符串 str 中最小的字母。                                       |
| rstrip()     | 删除字符串末尾的空格或指定字符。                                    |
| title()      | 返回"标题化"的字符串,就是说所有单词都是以大写开始，其余字母均为小写 |
| upper()      | 转换字符串中的小写字母为大写                                        |
| strip()      | 在字符串上执行 lstrip()和 rstrip()                                  |
**注意：strip为暂时性删除，若想完全删除需将新值关联到原来的变量**

### 在字符串中使用变量
```python
first_name = "charon"
last_name = "zhou"
full_name = f"{first_name} {last_name}"#变量所用符号为花括号
print(full_name)
```
这种字符串名为f字符串。f为format（设置格式）的缩写