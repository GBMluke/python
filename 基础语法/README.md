`注：本文部分内容如有需要，请至链接处查看`

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
