# 定义和调用

```python
# -*- coding: utf-8 -*

def funcName(p1, p2):
    print p1, p2
    return 123


print funcName(1, 2)
```

调用时指定参数名:

```python
# -*- coding: utf-8 -*

def funcName(p):
    print p
    return


funcName(p="hello")
```

## 默认参数

```python
# -*- coding: utf-8 -*

def funcName(p=23):
    print p
    return


funcName()
```

## 不定参数(参数前加*)

```python
# -*- coding: utf-8 -*

def funcName(*p):
    print p  # (1, 2, 3)
    return


funcName(1, 2, 3)

# 把列表或元组当做可变参数传递
nums = [1, 2, 3]
funcName(*nums)  # 在nums前加*
```

## 关键字参数(参数前加**)

```python
def person(name, age, **kw):
	print 'name:', name, 'age:', age, 'other:', kw


if __name__ == '__main__':
	person('Michael', 30)  # name: Michael age: 30 other: {}
	person('Bob', 35, city='Beijing')  # name: Bob age: 35 other: {'city': 'Beijing'}
	person('Adam', 45, gender='M', job='Engineer')  # name: Adam age: 45 other: {'gender': 'M', 'job': 'Engineer'}

	# 传递一个字典
	kw = {'city': 'Beijing', 'job': 'Engineer'}
	person('Jack', 24, **kw)  # name: Jack age: 24 other: {'city': 'Beijing', 'job': 'Engineer'}
```


## 参数组合

参数定义的顺序必须是：必选参数、默认参数、可变参数和关键字参数

```python
def func(a, b, c=0, *args, **kw):
    print 'a =', a, 'b =', b, 'c =', c, 'args =', args, 'kw =', kw
```


## 返回多个值

```python
def move(x, y, step, angle=0):
    nx = x + step * math.cos(angle)
    ny = y - step * math.sin(angle)
    return nx, ny


# 调用
x, y = move(100, 100, 60, math.pi / 6)
```

其实返回的是元组

```python
>>> r = move(100, 100, 60, math.pi / 6)
>>> print r
(151.96152422706632, 70.0)
```


# 匿名函数

```python
# -*- coding: utf-8 -*

sum = lambda a1, a2: a1 + a2

print sum(1, 2)
```


# 变量作用域

```python
# -*- coding: utf-8 -*

total = 1


def sum(a1, a2):
    total = a1 + a2
    return total


print sum(2, 3)  # 5
print total  # 1
```

函数内的变量属于局部变量。

函数内访问全局变量:

```python
# -*- coding: utf-8 -*

total = 1


def sum(a1, a2):
    global total
    total = a1 + a2
    return total


print sum(2, 3)  # 5
print total  # 5
```

