---
title: Python数学求和
date: 2020-6-25 00:27:38
categories: Python
---



以下实例为通过用户输入两个数字，并计算两个数字之和：

##### 实例1

```python
# -*- coding: UTF-8 -*-  
# Filename : test.py 
# author by : www.runoob.com  
# 用户输入数字 num1 = input('输入第一个数字：') num2 = input('输入第二个数字：')  
# 求和 sum = float(num1) + float(num2)  
# 显示计算结果 print('数字 {0} 和 {1} 相加结果为： {2}'.format(num1, num2, sum))
```

<!-- more -->

执行以上代码输出结果为：

```python
输入第一个数字：1.5
输入第二个数字：2.5
数字 1.5 和 2.5 相加结果为： 4.0
```

在该实例中，我们通过用户输入两个数字来求和。使用了内置函数 input() 来获取用户的输入，input() 返回一个字符串，所以我们需要使用 float() 方法将字符串转换为数字。

两数字运算，求和我们使用了加号 (+)运算符，除此外，还有 减号 (-), 乘号 (*), 除号 (/), 地板除 (//) 或 取余 (%)。更多数字运算可以查看我们的Python 数字运算。

我们还可以将以上运算，合并为一行代码：

##### 实例2

```python
# -*- coding: UTF-8 -*-  
# Filename : test.py 
# author by : www.runoob.com  
print('两数之和为 %.1f' %(float(input('输入第一个数字：'))+float(input('输入第二个数字：'))))
```

执行以上代码输出结果为：

```python
$ python test.py 
输入第一个数字：1.5
输入第二个数字：2.5
两数之和为 4.0
```