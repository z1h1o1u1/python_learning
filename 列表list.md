
## 列表

在python中，有四种集合数据类型，分别为：

- list：列表是一个集合，有序，可修改的，允许有重复的成员。
- tuple：元组，是一个有序，不可修改的集合，允许有重复的成员。
- set：是一个无序，无所有、不可修改的集合，可以添加新成员，不允许有重复的成员。
- dictionary：是一个无序的、可修改和可索引的集合，没有重复的成员

### 创建列表

列表由一系列按特定顺序排列的**元素**组成。
列表是**有序集合**，因此要访问列表的任何元素，只需将该元素的索引告诉Python
当然列表内可以是**不同数据类型的元素**

```python
language = ['c','c++','java','python']
print(language)
print(language[0])
print(language[2].title())
#注意索引是从零开始而不是从一开始
print(language[-1])#-1表示倒数第一个，-2表示倒数第二个

dream = f"my favurite language is {language[-1].title()}"
print(dream)

lst = ['Asabeneh', 250, True, {'country':'Finland','city':'Helsinki'}]
print(lst)
```
索引-2返回倒数第二个列表元素，索引-3返回倒数第三个列表元素，以此类推。

### 切片

切片就是指处理列表的部分元素组成的新列表,
在[:]的两边可以是正索引也可以是负索引，返回值将是一个新的列表。

```python
players = ['zhou','xue','zhang','hua']
print(players[0:3])
print(players[:3])
```

### 修改、添加和删除元素

#### 修改

要修改列表元素，可指定列表名和要修改的元素的索引，再指定该元素的新值
```python
language = ['c','c++','java','python']
language[0] = 'go'
print(language)
```

#### 添加

1. **添加元素**
简单的方式是将元素附加到列表末尾，方法**append()** 将元素'ducati'添加到了列表末尾
```python
language = ['c','c++','java','python']
language.append('ruby')
print(language)
```
方法append()可以动态地创建列表，可以先创建一个空列表，再使用一系列的append()语句添加元素。
2. **插入元素**
使用方法insert()可在列表的任何位置添加新元素，需要指定新元素的索引和值
```python
magicians = ['alice','david','charon']
magicians.insert(0,'zhou')
print(magicians)
```

#### 删除

1. **del语句**
```python
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)

del motorcycles[0]
print(motorcycles)
```
使用del可删除任何位置处的列表元素，条件是知道其索引
使用del语句将值从列表中删除后，你就无法再访问了,为永久性删除

2. **方法pop()**
术语弹出（pop）源自这样的类比：列表就像一个栈，而删除列表末尾的元素相当于弹出栈顶元素。
```python
language = ['c','c++','java','python']
print(language)
name = language.pop(2)#弹出任意值
print(name)
print(language)
```
可以使用pop()来删除列表中任何位置的元素，只需在括号中指定要删除的元素的索引即可。
如果没填则默认删除末尾元素
使用pop()时，被弹出的元素就不再在列表中了。还能继续使用它

3. **方法remove()**
只知道要删除的元素的值，可使用方法remove()。
```python
motorcycles = ['honda', 'yamaha', 'suzuki', 'ducati']
print(motorcycles)

too_expensive = 'ducati'
motorcycles.remove('ducati')
print(motorcycles)
```
如果还想使用元素，只需要将要删除的元素储存在变量中
如果要删除的值可能在列表中出现多次，就需要使用循环来判断是否删除了所有这样的值

4. 清除列表中的元素

```python
motorcycles = ['honda', 'yamaha', 'suzuki', 'ducati']
motorcycles.clear()
print(motorcycles)
```

### 组织列表

#### 排序
1. **sort()/sorted()**
方法sort()能够对列表进行永久性按字母顺序排序
```python
list = ['a','b','s','i']
list.sort()
print(list)
```
向sort()方法传递参数reverse=True。列表按与字母顺序相反的顺序排列：

2. 使用**函数 sorted()** 对列表进行**临时排序**
函数sorted()让你能够按特定顺序显示列表元素，同时不影响它们在列表中的原始排列顺序。
```python
list = ['a','b','s','i']
print(sorted(list))
print(list)
```
调用函数sorted()后，列表元素的排列顺序并没有变
要按与字母顺序相反的顺序显示列表，也可向函数sorted()传递参数reverse=True。

3. 可使用**方法reverse()使列表成反转元素的排列顺序，**
```python
list = ['a','b','s','i']
list.reverse()
print(list)
```
方法reverse()永久性地修改列表元素的排列顺序，随时恢复到原来的排列顺序，只需对列表再次调用reverse()

4. 函数len()可快速**获悉列表的长度**也就是列表由几个组成
```python
list = ['a','b','s','i']
print(len(list))
```


### 复制列表

这里有两个方法来复制列表
方法一：将motorcycles内的所有元素复制到motorcycles_copy
方法二：使用 copy() 
这两种方法都可以避免list2 = list1这种方法对 list2 所做的任何修改也会修改原始的 list1的问题

```python
motorcycles = ['honda', 'yamaha', 'suzuki', 'ducati']
motorcycles_copy = motorcycles[:]
motorcycles_c = motorcycles.copy()
print(motorcycles
print(motorcycles_copy)#方法一
print(motorcycles_c)#方法二
```

### 列表解析

```python
squares = [val ** 2 for val in range(1,11)]
print(squares)
```



