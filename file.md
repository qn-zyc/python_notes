# 创建

## 创建一个可写的文件

```py
>>> f = open('data.txt', 'w')
>>> f.write('hello\n')
>>> f.write('world\n')
>>> f.close()  # close to flush output buffers to disk
```

# 读取

## 读取文件

```py
try:
	f = open("data.txt", 'r')
	print f.read()  # 会读取所有内容
finally:
	if f:
		f.close()
```

如果文件不存在，open()函数就会抛出一个IOError的错误。

下面是简洁形式：

```py
with open("data.txt", "r") as f:
	print f.read()
```

```py
with open("data.txt", "r") as f:
	for line in f:
		print line
```


不需要调用close关闭。

### 分批读取

- read(size)方法，每次最多读取size个字节的内容
- readline()可以每次读取一行内容
- readlines()一次读取所有内容并按行返回list

```py
with open("data.txt", "r") as f:
	while True:
		line = f.readline()
		if not line:
			break
		print line
```

