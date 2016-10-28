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


