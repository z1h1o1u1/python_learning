
字典是一系列的**键值对**，每一个健和每一个值一一对应
> 'key1':'value1'

就比如说上面的示例，'value1'是值，前面就是健

## 创建

字典使用花括号中的一系列键值对表示

```python
dct = {'key1':'value1', 'key2':'value2', 'key3':'value3', 'key4':'value4'}
print(dct)
```

键值对中的值可以是多种数据类型

### 访问字典中的值

可以通过引用键来访问字典里的值。

```python
dct = {'key1':'value1', 'key2':'value2', 'key3':'value3', 'key4':'value4'}
print(dct['key1'])
```
如果一个字典中所访问的键不存在，那么就会报错，这时我们可以使用get()
get方法第一个参数用于指定健，第二个用于指定健不存在时的值

```python
dct = {'key1':'value1', 'key2':'value2', 'key3':'value3', 'key4':'value4'}
print(dct.get('key5','none'))
```
## 添加键值对

字典是一种动态结构，可以通过指定字典名，健，值来添加
```python
dct = {'key1':'value1', 'key2':'value2', 'key3':'value3', 'key4':'value4'}
dct['key5'] = 'value5'
print(dct)
```

## 修改
修改可以理解为利用原来的健重新定义它的值

```python
dct = {'key1':'value1', 'key2':'value2', 'key3':'value3', 'key4':'value4'}
dct['key1'] = 'value'
print(dct)
```

## 删除
del():删除具有指定键名的项

```python
dct = {'key1':'value1', 'key2':'value2', 'key3':'value3', 'key4':'value4'}
del dct['key2']
print(dct)
```

还有两种方法：
- pop(key):删除具有指定键名的项。
- popitem():删除最后一项

## 删除字典

使用clear()方法可以删除整个字典

```python
dct = {'key1':'value1', 'key2':'value2', 'key3':'value3', 'key4':'value4'}
dct.clear()
```

## 字典与循环

对于字典来说，要是想遍历键值对，使用方法items()可以返回一个键值对列表，同时就需要同时定义两个变量，一个用于储存键，一个用于储存值

```python
dct = {
    'key1':'value1',
    'key2':'value2',
    'key3':'value3',
    'key4':'value4'
    }

for key, value in dct.items():
    print(key)
    print(value)
```

如果不需要使用值的时候，我们还可以使用方法keys()返回一个键的列表，这时就只需要定义一个变量

```python
dct = {
    'key1':'value1',
    'key2':'value2',
    'key3':'value3',
    'key4':'value4'
    }

  
for key in dct.keys():
    print(key)
```

如果想生成的列表按顺序排列还可以调用函数sorted()
```python
dct = {
    'key3':'value1',
    'key2':'value2',
    'key1':'value3',
    'key4':'value4'
    }

for key in sorted(dct.keys()):
    print(key)
```

## 嵌套

将一系列字典存储在列表中，或将列表作为值存储在字典中，这称为嵌套

### 将字典嵌套在列表里

```python
bob = {'address': 'Uganda','favorite_language': 'python'}
sarah ={'address': 'Brazil','favorite_language': 'C'}
phil = {'address': 'Prague','favorite_language': 'java'}

users = [bob, sarah, phil]
for user in users:
    print(user)

print(users)
```

### 将列表储存在字典里

```python
drink = {
    'cup': 'big',
    'kinds':['coffee','milk']
    }

print(drink['cup'])
print(drink['kinds'])

for kind in drink['kinds']:

    print(kind)
```

### 将字典储存在字典里

```python
users = {
    'aeinstein': {
        'first': 'albert',
        'last': 'einstein',
        'location': 'princeton',
        },
        
    'mcurie': {
        'first': 'marie',
        'last': 'curie',
        'location': 'paris',
        },

    }

for username, user_info in users.items():
    print(f"\nUsername: {username}")
    full_name = f"{user_info['first']} {user_info['last']}"
    location = user_info['location']

    print(f"\tFull name: {full_name.title()}")
    print(f"\tLocation: {location.title()}")
```