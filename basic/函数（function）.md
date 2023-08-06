
## 定义函数

使用关键字def，来定义一个函数

```python
def hello():
    """say hello"""
    print("hello,world!")

hello()
```

当创建一个函数时，称之为**声明一个函数**，当开始使用时，称之为**调用函数.**

### 带参函数

```python
def hello(user):
    print(f"hello,{user.title()}")

hello('charon')
```

我们在定义函数时，在括号内添加了一个参数（一个变量），在调用函数时我们也就需要给函数指定一个参数

所以，user就是形参，函数**完成工作需要的信息**，"charon"就是实参，是调用函数时**我们给函数的信息**

## 实参

实参分为**位置实参和关键词实参**

### 位置实参

基于参数位置实现关联。所以在调用时要实参与形参位置对应

```python
def hello(user,age):
    print(f"hello,{user.title()}")
    print(f"I am {age} years old")

hello('charon','18')
```

### 关键词实参

在调用时，**在实参中直接和形参关联起来**

```python
def hello(user,age):
    print(f"hello,{user.title()}")
    print(f"I am {age} years old")

hello(user='charon',age='18')
```

### 默认值

当我们定义一个函数时，可以在形参后面**指定一个值作为默认值**

```python
def hello(user= 'charon',age= '18'):
    print(f"hello,{user.title()}")
    print(f"I am {age} years old")

hello()
```

#### 空默认值

可给实参address指定一个默认值——空字符串，让address变成可选的，并将其移到形参列表的末尾
```python
def hello(user,age,address=''):
    if address:
        full = f"i am {user},{age} year old,live in {address}"
    else:
        full = f"i am {user},{age} year old"
    return full

  
say_hello = hello('charon','18')
print(say_hello)
say_hello2 = hello('charon','18', 'china')
print(say_hello2)
```

## 返回值

用return语句将值返回到调用函数的代码行。函数返回的值被称为返回值。

```python
def hello(user):
    return user

say_hello = hello('charon')
print(say_hello)
```

+ 返回字典

```python
def build_person(first_name, last_name, age=None):
    person = {'first': first_name, 'last': last_name}
    if age:
        person['age'] = age
    return person

musician = build_person('jimi', 'hendrix', age=27)
print(musician)
```


## 传递列表


```python
def greet_users(names):
    for name in names:
        msg = f"Hello, {name.title()}!"
        print(msg)

usernames = ['hannah', 'ty', 'margot']
greet_users(usernames)
```

用函数来解决实际问题通常会更加高效

在函数中如果对于列表想要禁止修改（保留）就需要用切片[:]来创建列表副本
```python
def print_models(unprinted_designs, completed_models):
    while unprinted_designs:
        current_design = unprinted_designs.pop()
        print(f"Printing model: {current_design}")
        completed_models.append(current_design)

def show_completed_models(completed_models):
    print("\nThe following models have been printed:")
    for completed_model in completed_models:
        print(completed_model)

unprinted_designs = ['phone case', 'robot pendant', 'dodecahedron']
completed_models = []

print_models(unprinted_designs[:], completed_models)
show_completed_models(completed_models)
print(unprinted_designs)
```

## 任意数量的实参

参数名前添加*号来创建一个可以接受任何参数的函数。

```python
def number(*args):
    print(args)

number('1','2','3','4')
```

当然这种接纳任意数量的实参的形参要在定义一个函数是放在最后一个

当然，如果不知道传递给函数的会是什么信息，**号来创建一个空字典来接受任意数量的键值对

```python
def build_profile(first, last, **user_info):
    user_info['first_name'] = first
    user_info['last_name'] = last
    return user_info

user_profile = build_profile('albert', 'einstein',
                             location='princeton',
                             field='physics')

print(user_profile)

#{'location': 'princeton', 'field': 'physics', 'first_name': 'albert', 'last_name': 'einstein'}
```







