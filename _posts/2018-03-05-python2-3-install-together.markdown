---
title:      "Python2与python3兼容于pip同时兼容"
date:       2018-03-05 12:00:00
categories:
- 工具
tags:
    - 学习
---

> "python安装问题"

##  问题

安装python2于python3的pip在同一系统。

环境：
* **系统** windows

##  实现(命令)
~~~python
#python2
> py -2 -m pip install bs4
#python3
> py -3 -m pip install bs4
# 启用python2(3)
> py -2 (-3)
~~~

## 后记
快速积累

