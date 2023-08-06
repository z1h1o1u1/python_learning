
元组是有序且不可修改的不同数据类型的集合，换一种解释就是不可变的列表

## 定义

元组通过()来定义，
同样的，和列表一样，使用正索引和负索引访问元组中的元素。

```python
dimensions = (200,30,50)
print(dimensions)
print(dimensions[0])
```

还可以使用len()方法确定元组长度

```python
dimensions = (200,30,50)
len(dimensions)
```


## 切片

在[:]的两边可以是正索引也可以是负索引，返回值将是一个新的元组。

```python
tpl = ('item1', 'item2', 'item3', 'item4')
print(tpl[0:2])
tpls = tpl[0:3]
print(tpls)
```

## 转换&删除

元组可以转换为列表，之后就可以进行修改了

```python
tpl = ('item1', 'item2', 'item3', 'item4')
lst = list(tpl)
del tpl
```

## 修改

刚才可以先将元组转换成列表再修改，另一种方法是直接重新定义元组变量

```python
dimensions = (200,30,50)
print(dimensions)
dimensions = (4006,0,50)
print(dimensions)
```















