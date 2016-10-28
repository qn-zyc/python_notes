# First Class

定义：

```python
class FirstClass:
	def setData(self, value):
		self.data = value

	def display(self):
		print(self.data)
```

创建：

```python
x = FirstClass()
x.setData("hello")
x.display()
```

可以对未定义的字段赋值：

```python
x.data2 = "未定义的字段"
```


# 继承

```python
class FirstClass:
	def setData(self, value):
		self.data = value

	def display(self):
		print(self.data)


class SecondClass(FirstClass):
	def display(self):  # 重载
		FirstClass.display(self)  # 注意需要传递self
		print('current value = "%s"' % self.data)


x = SecondClass()
x.setData("second")
x.display()
```

通过 `FirstClass.display(self)` 的方法来调用父类的方法，调用父类的构造方法可以用 `FirstClass.__init__(self, 其余参数)`


# 特殊方法

```python
class ThirdClass(SecondClass):
	def __init__(self, value):
		self.data = value

	def __add__(self, other):
		return ThirdClass(self.data + other)

	def __str__(self):
		return "[ThirdClass: %s]" % self.data

x = ThirdClass('abc')
y = x + 'def'
print(y)
```

`__init__` 是构造方法。

`__add__` 是加法运算。

`__str__` 是返回字符串。


# 最简单的类

```python
class rec: pass


rec.name = "test"
rec.age = 13
```

name 和 age 是类rec的属性，对于rec的实例来说(比如x=rec())所有的实例都继承这些属性（像是java中的静态属性），当`x.name=""`时x才拥有自己的属性，此时x和其他实例就不再共享相同的name属性。

```python
def upperName(self):
	return self.name.upper()


print(upperName(rec))

rec.method = upperName

x = rec()
x.name = 'x'
print(x.method())
print(rec.method(x))  # 通过类调用时需要传实例
```

在类定义之外的方法`upperName`可以当做普通函数使用，也可以赋值成类的方法。


```python
rec = {}
rec['name'] = "test"
rec['age'] = 12
print(rec)  # {'age': 12, 'name': 'test'}


class rec: pass


pers = rec()
pers.name = 'test'
pers.age = 12
print(pers)  # <__main__.rec instance at 0x110022200>
```

实现字典的功能。（打印的话还是需要定义`__str__`方法）




