# 比较运算

## 连续比较

```python
x < y > z
等效于： x < y and y > z
```

## 是否相等

```python
l1 = [1, ['a', 'b']]
l2 = [1, ['a', 'b']]
print l1 == l2  # True
print l1 is l2  # False
```

`==` 递归地比较所有内嵌对象

`is` 判断是否是同一内存

另外 `<` `>` 也会递归地比较内嵌对象。



# 位运算

```python
x << 2  # 左移
x | 2   # 或
x & 2   # 与
```





# if-else

* 以冒号结尾
* 括号是可选的
* python中没有switch-case语句

```python
if <test1>:
	<statements1>
elif <test2>:
	<statements2>
else:
	<statements3>
```

```python
>>> if 1:
...     print('true')
...
true
>>>
>>> if not 1:
...     print('true')
... else:
...     print('false')
...
false
```

## if-else三元表达式

```python
A = Y if X else Z
```

等同于：

```python
if X:
	A = Y
else:
	A = Z
```

这是短路运算，只有X为真才会执行Y,同样X为假才会执行Z