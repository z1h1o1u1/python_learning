
默认情况下，python脚本中的语句都是从上到下依次执行，可以通过两种方式改变执行的顺序流程：

- 条件执行：如果某个表达式为真，将执行一个或多个语句块。
- 重复语句：只要某个表达式为真，一个或多个语句块就会被重复执行。


## 条件测试

**两个等号为相等运算符**，检查两边值是否相等。当然还有!=表示不相等符

```python
player = 'xue'
print(player == 'xue')
print(player == 'zhou')
```

### 数值比较

数值比较很简单，除了相等运算符之外，python还支持<,>.<=,>=号

```python
age = 22
print(age == "24")
print(age > 20)
print(age < 40)
print(age <= 6)
print(age >= 63)
```

还可以用and 和or判断多个条件,**and需要两边同时满足,or至少一个满足，一个及以上**

```python
age = 22
answer = 42
print((age > 20) and (answer< 60))  
print((age>10)and(answer>60))
print((age > 40) or (answer< 40))
```


### 判断元素是否在列表内

使用**关键词in**可以判断元素是否在列表内

```python
car = ['a','b','c','d','e']
print('c' in car)
print('f' in car)
```

## if 语句

if用于检查条件是否为真，如果为真，则执行里面的代码块。

语法：

```python
if conditional_test:
	do something	
```

示例
```python
answer = 42
if answer != '24':
    print("you are wrong")
```

### if-else结构

```python
ages= 17
if ages < 18:
    print("you are ennough toget in ")
else:
    print("you are not enough ,get out")
```

如果条件符合将执行第一个代码块，否则执行else里的内容，无论如何总会执行两个操作中的一个

### if-elif-else结构

如果判断的条件超过两个，python就提供了if-elif-else结构，这其中elif代码块可以任意数量使用

```python
a = 20
if a < 4:
    cost = 0
elif a < 18:
    cost =  25
else:
    cost = 40
print(f"you will cost {cost}")
```


### and & or
if也可以和and,or逻辑运算符一起使用
示例：

```python
a = 0
if a > 0 and a % 0 == 0:
    print('A is  a positive and even integer')
    print('A is a positive number')
elif a > 0 and a % 2 != 0:
    print('A is a positive number')
elif a == 0:
    print('A is zero')
else:
    print('A is a negative number')
```







