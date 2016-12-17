# 随机数

```python
import random
```

生成0-1之间的随机浮点数

```python
In [2]: random.random()
Out[2]: 0.40649275346907676
```

指定范围的浮点数

```python
In [3]: random.uniform(10,20)
Out[3]: 18.27338366045023

In [4]: random.uniform(0,20)
Out[4]: 5.720987757429256
```

生成随机整数,结果可能包含20

```python
In [7]: random.randint(10, 20)
Out[7]: 18
```

指定步长的整数

```python
In [9]: random.randrange(10, 20)
Out[9]: 14

In [10]: random.randrange(10, 20, 2) # 从[10,12,14,16,18]中随机选，不包含20
Out[10]: 16
```

从序列中随机选

```python
In [12]: random.choice([1, 2, 5, 7])
Out[12]: 2
```

从序列中随机选n个：

```python
In [17]: a = [1, 2, 3, 4, 5]

In [18]: random.sample(a, 3)
Out[18]: [2, 3, 5]
```



将列表中的元素随机打乱

```python
In [14]: a = [1, 2, 3, 4, 5]

In [15]: random.shuffle(a)

In [16]: a
Out[16]: [2, 5, 3, 4, 1]
```

