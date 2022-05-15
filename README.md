`注：本文部分内容如有需要，请至链接处查看`

# 预备知识

## 简介
[传送门](https://edu.csdn.net/skill/python/python-3-0?category=1)

### 简介
PYthon是一个高层次的结合了解释性、编译性、互动性和面向对象的脚本语言

Python的设计具有很强的可读性，相比其他语言经常使用英文关键字，其他语言的一些标点符号，它具有比其他语言更有特色语法结构

- Python是一种解释型语言
> 这意味着开发过程中没有了编译这个环节
> 
> 类似于PHP和Perl语言

- Python是交互式语言
> 这意味着，您可以在一个Python提示符>>>后直接执行代码

- Python是面向对象语言
> 这意味着Python支持面向对象的风格或代码封装在对象的编程技术

- Python是初学者的语言
> Python对初级程序员而言，是一种伟大的语言
> 
> 它支持广泛的应用程序开发，从简单的文字处理到浏览器再到游戏

## 程序设计思想
[传送门](https://edu.csdn.net/skill/python/python-3-1?category=1)

## 安装
[传送门](https://edu.csdn.net/skill/python/python-3-2?category=1)

## 运行方式
[传送门](https://edu.csdn.net/skill/python/python-3-3?category=1)

## 常用开发工具
[传送门](https://edu.csdn.net/skill/python/python-3-4?category=1)

## 编码规范
[传送门](https://edu.csdn.net/skill/python/python-3-5?category=1)

## 模块管理
[传送门](https://edu.csdn.net/skill/python/python-3-6?category=1)

# 基础语法

## 缩进规则
[传送门](https://edu.csdn.net/skill/python/python-3-7?category=2)

## 函数
[传送门](https://edu.csdn.net/skill/python/python-3-9?category=2)

### 概念
- 函数
> 把重复利用的代码块进行整合，可以提升代码的运行效率

- 内置函数
> 如print()、len()等，都是python为我们提供的内置函数，可以直接进行调用

- 自定义函数
> 自己定义一段可重复使用代码的函数，简单理解就是自己创建的函数

### 语法
```python
# 定义函数
def <函数名称>(<参数列表>):
	<函数主体>
	return

# 调用函数
<函数名称>(<参数值>)
```
```text
函数名称 = 函数的名称，区分大小写
参数列表 = 小括号中的参数，如没有，可以不写，如有多个，用逗号分隔
函数主体 = 本函数将实现的功能
return = 函数的返回值，可以省略
```
注意：函数调用不能放在定义函数之前

### 无参函数
1. 无返回值
```python
def a(): # 定义函数a()
	print("my idol is hackjacking") # 显示字符串my idol is hackjacking

a() # 调用函数a()
```
结果为
```text
my idol is hackjacking
```

2. 有返回值
```
def a():
	b = int(input("请输入b的值 ")) # 获取b的值
	c = int(input("请输入c的值 ")) # 获取c的值
	return b + c # 返回 b + c 的值

print(a())
```
结果为
```text
请输入b的值 3
请输入c的值 4
7
```

### 含参函数
1. 无返回值
```python
def a(b,c): # b和c为形参
	print(b + c)

a(3,4) # 实参
```
结果为
```text
7
```

2. 有返回值
```python
def a(b,c):
	return b + c

print(a(3,4))
```
结果为
```
7
```

3. 形参和实参
> 形式参数
> 
>    在定义函数求过程的时候命名的参数，告诉这里需要一个参数，你不传就用不了这个方法，定义函数的参数都是形参
> 
> 实参
> 
>    实际参与运算，那么通过方法名使用这个方法的时候传的参数都是实参
> 
> 关系
> 
>    两者是在调用的时候进行结合的，通常实参会将取值传递给形参，形参之后进行函数过程运算，然后可能将某些值经过参数或函数符号返回给调用者

4. 参数位置关系
```python
def a(b,c,d):
	print((b - c) * d)

b_num = 3 # b的值
c_num = 4 # c的值
d_num = 5 # d的值

print(a(b_num,c_num,d_num))
# 正确写法，结果为-5

print(a(d_num,c_num,b_num)) 
# 错误写法_1，结果为3

print(a(b_num,c_num))
# 错误写法_2，结果为TypeError: a() missing 1 required positional argument: 'd'
```

5. 关键词参数
```python
def a(b,c,d):
	print((b - c) * d)

b_num = 3 # b的值
c_num = 4 # c的值
d_num = 5 # d的值

print(a(d = d_num,c = c_num,b = b_num)) # 可以通过等号，改变各个参数对应的位置 
```

6. 默认值参数
```python
def a(b,c,d=3):
	return b + c + d

# 当有一个默认值已确定时，只需要写出没默认值的参数即可
print(a(4,5)) # 结果为12
```

7. 不定长参数

- 加一个*号(tuple)
```python
def a(b,*c): # 此处b为正常参数，c为元组
	print("b = ",b)
	print("*c = ",c)

a(1,2,3,4,5,6) # 调用函数
```
结果为
```text
b = 1
*c = (2,3,4,5,6)
```

- 加两个*号(dict)
```python
def a(b,**c): # 此处b为正常参数，c为字典
	print("b = ",b)
	print("**c = ",c)

a(1,c = 2,d = 3)
```
结果为
```text
ab = 1
**c = {'c':2,'d':3}
```

## 类
[传送门](https://edu.csdn.net/skill/python/python-3-10?category=2)

## 顺序语句结构
[传送门](https://edu.csdn.net/skill/python/python-3-11?category=2)

## 条件分支语句
[传送门](https://edu.csdn.net/skill/python/python-3-12?category=2)

## 循环语句
[传送门](https://edu.csdn.net/skill/python/python-3-13?category=2)

## 数据类型
[传送门](https://edu.csdn.net/skill/python/python-3-14?category=2)

## 内置类
[传送门](https://edu.csdn.net/skill/python/python-3-15?category=2)

## 常用内置函数
[传送门](https://edu.csdn.net/skill/python/python-3-16?category=2)

# 进阶语法

## 列表推导式
[传送门](https://edu.csdn.net/skill/python/python-3-17?category=3)

## 三元表达式
[传送门](https://edu.csdn.net/skill/python/python-3-18?category=3)

## 断言
[传送门](https://edu.csdn.net/skill/python/python-3-19?category=3)

## with-as
[传送门](https://edu.csdn.net/skill/python/python-3-20?category=3)

## 异常捕获预处理
[传送门](https://edu.csdn.net/skill/python/python-3-21?category=3)

-------------------------------------------------------------------------

### 常见异常类型

## 字符串方法
[传送门](https://edu.csdn.net/skill/python/python-3-22?category=3)

## lambda函数
[传送门](https://edu.csdn.net/skill/python/python-3-23?category=3)

## 文件
[传送门](https://edu.csdn.net/skill/python/python-3-24?category=3)

## 常用标准库
[传送门](https://edu.csdn.net/skill/python/python-3-25?category=3)

## 自负编码与解码
[传送门](https://edu.csdn.net/skill/python/python-3-26?category=3)

# 面向对象编程

## 类核对象的概念
[传送门](https://edu.csdn.net/skill/python/python-3-27?category=4)

## 类成员
[传送门](https://edu.csdn.net/skill/python/python-3-28?category=4)

## 面向对象三要素
[传送门](https://edu.csdn.net/skill/python/python-3-29?category=4)

## 创建类
[传送门](https://edu.csdn.net/skill/python/python-3-30?category=4)

## 抽象类
[传送门](https://edu.csdn.net/skill/python/python-3-31?category=4)

## 访问限制
[传送门](https://edu.csdn.net/skill/python/python-3-32?category=4)

## 获取对象信息
[传送门](https://edu.csdn.net/skill/python/python-3-33?category=4)

# 基本技能

## 解析命令行参数
[传送门](https://edu.csdn.net/skill/python/python-insert-4?category=6)

## 时间日期处理
[传送门](https://edu.csdn.net/skill/python/python-3-128?category=6)

## 数据文件读写
[传送门](https://edu.csdn.net/skill/python/python-3-129?category=6)

## 数据库操作
[传送门](https://edu.csdn.net/skill/python/python-3-130?category=6)

## 操作系统和环境
[传送门](https://edu.csdn.net/skill/python/python-3-131?category=6)

## 源码打包
[传送门](https://edu.csdn.net/skill/python/python-3-133?category=6)

## 网络编程
[传送门](https://edu.csdn.net/skill/python/python-3-134?category=6)

## 发送邮件
[传送门](https://edu.csdn.net/skill/python/python-3-135?category=6)

# Web应用开发

## Web开发基础知识
[传送门](https://edu.csdn.net/skill/python/python-3-136?category=7)
`如有更多需要，请参考www.github.com/GBMluke/Web`

## Django
[传送门](https://edu.csdn.net/skill/python/python-3-137?category=7)

## Tornado
[传送门](https://edu.csdn.net/skill/python/python-3-138?category=7)

## Flask
[传送门](https://edu.csdn.net/skill/python/python-3-139?category=7)

# 网络爬虫

## urllib
[传送门](https://edu.csdn.net/skill/python/python-3-147?category=8)

## 正则表达式
[传送门](https://edu.csdn.net/skill/python/python-3-148?category=8)

## Beautiful Soup
[传送门](https://edu.csdn.net/skill/python/python-3-149?category=8)

## lxml
[传送门](https://edu.csdn.net/skill/python/python-3-150?category=8)

## requests
[传送门](https://edu.csdn.net/skill/python/python-3-151?category=8)

## Selenium
[传送门](https://edu.csdn.net/skill/python/python-3-152?category=8)

## Scrapy框架
[传送门](https://edu.csdn.net/skill/python/python-3-153?category=8)

## pyspider框架的使用
[传送门](https://edu.csdn.net/skill/python/python-3-171?category=8)

## 验证码处理
[传送门](https://edu.csdn.net/skill/python/python-3-158?category=8)

## 动态渲染页面爬取
[传送门](https://edu.csdn.net/skill/python/python-3-166?category=8)

## 模拟登录
[传送门](https://edu.csdn.net/skill/python/python-3-169?category=8)

## autoscraper
[传送门](https://edu.csdn.net/skill/python/python-7330398a1359430c9b02244f689203c7?category=8)

## selectolax
[传送门](https://edu.csdn.net/skill/python/python-113824a228cf45f9b4f6e854a992c2f9?category=8)

## requests-html
[传送门](https://edu.csdn.net/skill/python/python-7d8a025ed5434ecc84708407e3db6d17?category=8)

# 桌面应用开发

## Tkinter
[传送门](https://edu.csdn.net/skill/python/python-3-174?category=9)

## PyQT
[传送门](https://edu.csdn.net/skill/python/python-3-175?category=9)

## WxPython
[传送门](https://edu.csdn.net/skill/python/python-3-176?category=9)
