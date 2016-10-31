# 注释

## 中文注释

在开头加上 `# -*- coding: utf-8 -*`



# 在命令行加载文件

假设当前文件有一个trees.py

```py
import sys
sys.path.append("./")

import trees

# 修改文件后重新加载
reload(trees)
```


# 启动参数

```py
import sys

print sys.argv
```

执行 `python test.py hello ad ds "dd"`
输出: `['test.py', 'hello', 'ad', 'ds', 'dd']`



# 模块

## import & from

被导入的模块 const.py

```python
A = "hello"
B = "world"
```

hello.py

```python
import const

print(const.A, const.B)
```

输出：`('hello', 'world')`

只导入特定属性

```python
from const import A

print(A)  # hello
```

## 列举模块的属性

```python
import const

print(dir(const))
```

```python
['A', 'B', '__builtins__', '__doc__', '__file__', '__name__', '__package__']
```



# 检测变量类型

```python
>>> type(f)
<type 'file'>
```

```python
L = []
if type(L) == type([]):
	print('yes')

if type(L) == list:
	print('yes')

if isinstance(L, list):
	print('yes')
```

