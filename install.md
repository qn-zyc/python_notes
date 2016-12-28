# MySQLdb

- 下载 <https://pypi.python.org/pypi/MySQL-python/1.2.5#downloads>
- 查找 `mysql_config` : `whereis mysql_config`
- - 如果没有的话可能是没有安装 `mysql-devel` : `yum install mysql-devel`, 之后在 `/usr/bin` 应该存在 mysql_config 了。
- 修改 site.cfg
  - 修改mysql_config为mysql配置文件的路径 /usr/bin/mysql_config
  - threadsafe = False
- `python setup.py build`
- `sudo python setup.py install`



## centos

`yum install mysql-python`



# pip

## centos

下载 [get-pip.py](https://pip.pypa.io/en/stable/installing/)

执行: `python get-pip.py`



