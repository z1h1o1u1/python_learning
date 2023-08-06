
## 读取文件

```python
with open("0.txt") as object:
    file = object.read()

print(file)

```

利用关键字with就可以不需要访问文件后将其关闭，运用函数open()打开一个文件并将其赋予给一个变量object，方法read()可以读取文件。

### 文件路径

对于读取文件而言。文件的路径一定是至关重要的，路径也分为绝对路径和相对路径
一个文件在计算机中的准确位置就是绝对路径
在文件路径中使用反斜杠会引发错误，而windows使用的就是反斜杠，这时可以将反斜杠改为斜杠，或者对反斜杠进行转义。


## 使用文件

```python
with open("0.txt") as object:
    files = object.readlines()

for file in files:
    print(file)

pi = ''
for file in files:
    pi += file.strip()

print(pi)
```
常用方法：
- readline():只读取第一行
- readlines():逐行读取所有的文本，并返回一个行的列表
- splitlines()来获得所有行的列表

## 写入文件

在使用Open函数中可以定义两个实参，第一个就是要打开的文件，第二个就是打开的模式
而对于文件有一下几种打开模式
> 'r'读取模式,'w'写入模式,'a'附加模式,'r+'读写模式

```python
with open("0.txt",'w') as object:
    files = object.write("i'm charon")
```
在python中只能写入字符串。

