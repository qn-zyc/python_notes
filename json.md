# 编码

```py
import json

data = {"a":"hello", "b":123, "c":[2,5,0]}
jsonStr = json.dumps(data)
print jsonStr  # {"a": "hello", "c": [2, 5, 0], "b": 123}
```

# 解码

```py
import json

jsonStr = '{"a": "hello", "c": [2, 5, 0], "b": 123}'
data = json.loads(jsonStr)
print data  # {u'a': u'hello', u'c': [2, 5, 0], u'b': 123}
print data["a"]  # hello
print data["c"]  # [2, 5, 0]
```

