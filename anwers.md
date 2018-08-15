<!-- markdown-toc start - Don't edit this section. Run M-x markdown-toc-generate-toc again -->
**Table of Contents**


   * [Python语言特性](#python语言特性)
      * [1 对Python的理解(对比其他语言)](#1-对Python的理解(对比其他语言))
      * [2 什么是Python的命名空间 ](#2-什么是Python的命名空间)
      * [3 Python中的pass语句](#3-Python中的pass语句)
      * [4 Python异常处理的用法和作用](#4-Python异常处理的用法和作用)
      * [5 Python的函数参数传递](#5-python的函数参数传递)
      * [6 函数的参数用法和注意事项](#6-函数的参数用法和注意事项)
      * [7 可变对象和不可变对象](#7-可变对象和不可变对象)
      * [8 def是运行时执行语句,并且是赋值语句](#8-def是运行时执行语句,并且是赋值语句)
      * [9 Python是否能以可变对象做函数默认参数](#9-Python是否能以可变对象做函数默认参数)
      * [10 企图在函数中修改全局变量,没有使用global,而创建了本地变量](#10-企图在函数中修改全局变量,没有使用global,而创建了本地变量)
      * [11 对象的dir属性和dict属性](#11-对象的dir属性和dict属性)
      * [12 @staticmethod和@classmethod](#12-staticmethod和classmethod)
      * [13 使用property创建可管理的对象属性](#13-使用property创建可管理的对象属性)
      * [14 类属性和实例属性](#14-类属性和实例属性)
      * [15 Python自省](#15-python自省)
      * [16 字典解析、列表解析、集合解析](#16-字典解析、列表解析、集合解析)
      * [17 Python中单下划线和双下划线](#17-python中单下划线和双下划线)
      * [18 字符串格式化:\x和.format](#18-字符串格式化和format)
      * [19 正则表达式相关知识及字符串操作](#19-正则表达式相关知识及字符串操作)
      * [20 迭代器和生成器](#20-迭代器和生成器)
      * [21 *args and <code>**kwargs</code>](#21-args-and-kwargs)
      * [22 装饰器](#22-装饰器)
      * [23 Python中重载](#23-python中重载)
      * [24 __new__和<code>__init__</code>的区别](#24-__new__和__init__的区别)
      * [25 单例模式](#25-单例模式)
         * [1 使用__new__方法](#1-使用__new__方法)
         * [2 共享属性](#2-共享属性)
         * [3 装饰器版本](#3-装饰器版本)
         * [4 import方法](#4-import方法)
      * [26 Python中的作用域](#26-python中的作用域)
      * [27 GIL线程全局锁](#27-gil线程全局锁)
      * [28 协程](#28-协程)
      * [29 闭包](#29-闭包)
      * [30 lambda函数](#30-lambda函数)
      * [31 Python函数式编程](#31-python函数式编程)
      * [32 Python里的拷贝](#32-python里的拷贝)
      * [33 Python是如何进行内存管理的](#33-Python是如何进行内存管理的)
         * [1 对象的引用计数机制](#1-对象的引用计数机制)
         * [2 垃圾回收](#2-垃圾回收)
         * [3 内存池机制](#3-内存池机制)
      * [34 Python的List和Dict的实现原理](#34-Python的List和Dict的实现原理)
      * [35 Python的is](#35-python的is)
      * [36 read,readline和readlines](#36-readreadline和readlines)
      * [37 Python2和3的区别](#37-python2和3的区别)
      * [38 Python的编码问题](#38-Python的编码问题)

   * [数据库](#数据库)
      * [1 事务](#1-事务)
      * [2 数据库索引](#2-数据库索引)
      * [3 Redis原理](#3-redis原理)
         * [Redis是什么？](#redis是什么)
         * [Redis数据库](#redis数据库)
         * [Redis缺点](#redis缺点)
      * [4 MyISAM和InnoDB](#4-myisam和innodb)
   * [网络](#网络)
      * [1 三次握手](#1-三次握手)
      * [2 四次挥手](#2-四次挥手)
      * [3 ARP协议](#3-arp协议)
      * [4 urllib和urllib2的区别](#4-urllib和urllib2的区别)
      * [5 Post和Get](#5-post和get)
      * [6 Cookie和Session](#6-cookie和session)
      * [7 apache和nginx的区别](#7-apache和nginx的区别)
      * [8 网站用户密码保存](#8-网站用户密码保存)
      * [9 HTTP和HTTPS](#9-http和https)
      * [10 XSRF和XSS](#10-xsrf和xss)
      * [12 RESTful架构(SOAP,RPC)](#12-restful架构soaprpc)
      * [15 CGI和WSGI](#15-cgi和wsgi)
      * [18 socket](#18-socket)
      * [19 浏览器缓存](#19-浏览器缓存)
      * [20 HTTP1.0和HTTP1.1](#20-http10和http11)
      * [21 Ajax](#21-ajax)
   * [编程题](#编程题)
      * [1 列表复制问题](#1-列表复制问题)
      * [2 求列表第三大的那个值](#2-求列表第三大的那个值)
      * [3 实现一个队列](#3-实现一个队列)
      * [4 实现一个堆栈](#4-实现一个堆栈)
      * [5 用Python实现一个单向链表](#5-用Python实现一个单向链表)
      * [6 用Python实现一个双向链表 ](#6-用Python实现一个双向链表)
      * [7 台阶问题/斐波那契](#7-台阶问题斐波那契)
      * [8 变态台阶问题](#8-变态台阶问题)
      * [9 去除列表中的重复元素](#9-去除列表中的重复元素)
      * [10 创建字典的方法](#10-创建字典的方法)
         * [1 直接创建](#1-直接创建)
         * [2 工厂方法](#2-工厂方法)
         * [3 fromkeys()方法](#3-fromkeys方法)
      * [11 合并两个有序列表](#11-合并两个有序列表)
      * [12 归并排序](#12-归并排序)
      * [13 质数和日期问题](#13-质数和日期问题)
      * [14 二分查找](#14-二分查找)
      * [15 打印文件夹](#15-打印文件夹)
      * [16 找零问题](#16-找零问题)
      * [17 前中后序遍历](#17-前中后序遍历)
      * [18 求最大树深](#18-求最大树深)
      * [19 求两棵树是否相同](#19-求两棵树是否相同)
      * [20 前序中序求后序](#20-前序中序求后序)
      * [21 广度遍历和深度遍历二叉树](#21-广度遍历和深度遍历二叉树)
      * [22 快排](#22-快排)
      * [23 层次遍历](#23-层次遍历)
      * [24 深度遍历](#24-深度遍历)



<!-- markdown-toc end -->





# Python语言特性

## 1 对Python的理解(对比其他语言)
下面是一些关键点：

* Python是一种解释型语言。这就是说，与C语言和C的衍生语言不同，Python代码在运行之前不需要编译。
* Python是动态类型语言，指的是你在声明变量时，不需要说明变量的类型。
* Python非常适合面向对象的编程（OOP），因为它支持通过组合（composition）与继承（inheritance）的方式定义类（class）。
* Python中没有访问说明符（access specifier，类似C++中的public和private），这么设计的依据是“大家都是成年人了”。

在Python语言中，函数是第一类对象（first-class objects）。这指的是它们可以被指定给变量，函数既能返回函数类型，也可以接受函数作为输入。类（class）也是第一类对象。
Python代码编写快，但是运行速度比编译语言通常要慢。好在Python允许加入基于C语言编写的扩展，因此我们能够优化代码，消除瓶颈，这点通常是可以实现的。numpy就是一个很好地例子，它的运行速度真的非常快，因为很多算术运算其实并不是通过Python实现的。

Python用途非常广泛——网络应用，自动化，科学建模，大数据应用，等等。它也常被用作“胶水语言”，帮助其他语言和组件改善运行状况。
Python让困难的事情变得容易，因此程序员可以专注于算法和数据结构的设计，而不用处理底层的细节。
### 补充
* Python彩蛋

````Python
import this

The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!

import __hello__

Hello world!
````

## 2 什么是Python的命名空间

在Python中，所有的名字都存在于一个空间中，它们在该空间中存在和被操作——这就是命名空间。

它就好像一个盒子，每一个变量名字都对应装着一个对象。当查询变量的时候，会从该盒子里面寻找相应的对象。

## 3 Python中的pass语句

Pass是一个在Python中不会被执行的语句。在复杂语句中，如果一个地方需要暂时被留白，它常常被用于占位符。


## 4　Python异常处理的用法和作用

[参考廖雪峰](https://www.liaoxuefeng.com/wiki/0014316089557264a6b348958f449949df42a6d3a2e542c000/00143191375461417a222c54b7e4d65b258f491c093a515000]
答：try…except…except…[else…][finally…)

* 执行try下的语句，如果引发异常，则执行过程会跳到except语句。对每个except分支顺序尝试执行，如果引发的异常与except中的异常组匹配，执行相应的语句。

* 如果所有的except都不匹配，则异常会传递到下一个调用本代码的最高层try代码中。

* try下的语句正常执行，则执行else块代码。如果发生异常，就不会执行

* 如果存在finally语句，最后总是会执行。
```
try:
    print('try...')
    r = 10 / int('2')
    print('result:', r)
except ValueError as e:
    print('ValueError:', e)
except ZeroDivisionError as e:
    print('ZeroDivisionError:', e)
else:
    print('no error!')
finally:
    print('finally...')
print('END')
```

## 5 Python的函数参数传递

看两个例子:

```python
a = 1
def fun(a):
    a = 2
fun(a)
print a  # 1
```

```python
a = []
def fun(a):
    a.append(1)
fun(a)
print a  # [1]
```

所有的变量都可以理解是内存中一个对象的“引用”

通过`id`来看引用`a`的内存地址可以比较理解：

```python
a = 1
def fun(a):
    print "func_in",id(a)   # func_in 41322472
    a = 2
    print "re-point",id(a), id(2)   # re-point 41322448 41322448
print "func_out",id(a), id(1)  # func_out 41322472 41322472
fun(a)
print a  # 1
```

注：具体的值在不同电脑上运行时可能不同。

可以看到，在执行完`a = 2`之后，`a`引用中保存的值，即内存地址发生变化，由原来`1`对象的所在的地址变成了`2`这个实体对象的内存地址。

而第2个例子`a`引用保存的内存值就不会发生变化：

```python
a = []
def fun(a):
    print "func_in",id(a)  # func_in 53629256
    a.append(1)
print "func_out",id(a)     # func_out 53629256
fun(a)
print a  # [1]
```

这里记住的是类型是属于对象的，而不是变量。而对象有两种,“可变”（mutable）与“不可变”（immutable）对象。在python中，string, tuple, 和number是不可更改的对象，而 list, dict, set 等则是可以修改的对象。(这就是这个问题的重点)

当一个引用传递给函数的时候,函数自动复制一份引用,这个函数里的引用和外边的引用没有半毛关系了.所以第一个例子里函数把引用指向了一个不可变对象,当函数返回的时候,外面的引用没半毛感觉.而第二个例子就不一样了,函数内的引用指向的是可变对象,对它的操作就和定位了指针地址一样,在内存里进行修改.

如果还不明白的话,这里有更好的解释: http://stackoverflow.com/questions/986006/how-do-i-pass-a-variable-by-reference

## 6 函数的参数用法和注意事项
(参考廖雪峰课程)[https://www.liaoxuefeng.com/wiki/0014316089557264a6b348958f449949df42a6d3a2e542c000/001431752945034eb82ac80a3e64b9bb4929b16eeed1eb9000]
函数参数分为位置参数、默认参数、可变参数、关键字参数、命名关键字参数（定义和调用必须按顺序传入）
```
numbers=[1,2,3,4,5]
def sum(*args):
    sum=0
    for i in args:
        sum = sum+i*i
    return sum  
sum(*numbers)

dict1={'a':1,'b':2}
def f(**kwargs):
    for k,v in kwargs.items():
        print('{0}:{1}'.format(k,v))
f(**dict1)

# 如果需要约束传入的关键字参数的名称，可以用命名关键字参数
# 命名关键字参数必须传入参数名，这和位置参数不同。
def person(name, age, *, city, job):
    print(name, age, city, job)

def person(name, age, *args, city, job):
    print(name, age, args, city, job)

# 命名关键字参数可以有缺省值，从而简化调用：
def person(name, age, *, city='Beijing', job):
    print(name, age, city, job)
```
## 7 可变对象和不可变对象
* python所有数字类型(布尔树,整数,浮点数,复数)均为不可变对象,
* 可变对象:file,dict,set,list,bytesarray,range
* 不可变对象:boolean,int,float,complex,tuple,str,bytes,frozenset
* 有序sequence:str,list,tuple,OrderedDict,
* 无序:dict,set,
* 不可重复:set,tuple
* 可变对象(mutable object)has no hash value
* 不可变对象可哈希,hashable

## 8 def是运行时执行语句,并且是赋值语句
类和对象均为第一类对象，调用的时候才会运行
## 9 Python是否能以可变对象做函数默认参数
不可以,字典,集合,列表等可变对象不适合作为函数默认值
要不然第二次调用时,一次调用的默认参数的值会影响二次调用.
```
def f(l=[]):
    for i in range(3):
        l.append(i)
    return l
f(l=[2]),---- l=[2,0,1,2]
f(),     ---- l=[0,1,2]
f(),     ---- l=[0,1,2,0,1,2]
```

## 10 企图在函数中修改全局变量,没有使用global,而创建了本地变量
修改全局变量需要global声明,要不然会创建同名的本地变量.

## 11 对象的dir属性和dict属性
Python一切皆对象，每个对象都有自己独特的属性和方法
dir()函数会自动寻找一个对象的所有属性，包括dict中的属性。
dict是dir()的子集，dir()包含dict中的属性。

## 12 @staticmethod和@classmethod

Python其实有3个方法,即静态方法(staticmethod),类方法(classmethod)和实例方法,如下:

```python
def foo(x):
    print "executing foo(%s)"%(x)

class A(object):
    def foo(self,x):
        print "executing foo(%s,%s)"%(self,x)

    @classmethod
    def class_foo(cls,x):
        print "executing class_foo(%s,%s)"%(cls,x)

    @staticmethod
    def static_foo(x):
        print "executing static_foo(%s)"%x

a=A()

```

这里先理解下函数参数里面的self和cls.这个self和cls是对类或者实例的绑定,对于一般的函数来说我们可以这么调用`foo(x)`,这个函数就是最常用的,它的工作跟任何东西(类,实例)无关.对于实例方法,我们知道在类里每次定义方法的时候都需要绑定这个实例,就是`foo(self, x)`,为什么要这么做呢?因为实例方法的调用离不开实例,我们需要把实例自己传给函数,调用的时候是这样的`a.foo(x)`(其实是`foo(a, x)`).类方法一样,只不过它传递的是类而不是实例,`A.class_foo(x)`.注意这里的self和cls可以替换别的参数,但是python的约定是这俩,还是不要改的好.

对于静态方法其实和普通的方法一样,不需要对谁进行绑定,唯一的区别是调用的时候需要使用`a.static_foo(x)`或者`A.static_foo(x)`来调用.

| \\      | 实例方法     | 类方法            | 静态方法            |
| :------ | :------- | :------------- | :-------------- |
| a = A() | a.foo(x) | a.class_foo(x) | a.static_foo(x) |
| A       | 不可用      | A.class_foo(x) | A.static_foo(x) |

更多关于这个问题:
1. http://stackoverflow.com/questions/136097/what-is-the-difference-between-staticmethod-and-classmethod-in-python
2. https://realpython.com/blog/python/instance-class-and-static-methods-demystified/

## 13 使用property创建可管理的对象属性
property可以让实例在形式上是属性访问,但实际上调用方法
```
class Circle2(object):
    def __init__(self, radius):
        self.radius = radius

    def getRadius(self):
        # return self.radius
        return round(self.radius, 2)  # 表示四舍五入后保留小数点后两位

    def setRadius(self, value):
        if not isinstance(value, (int, long, float)):
            raise valueError('wrong type .')
        self.radius = float(value)

    def getArea(self):
        return self.radius * 2 * pi

    R = property(getRadius, setRadius)

r = Circle2(3.2)
print(r.R)  # 自动调用getRadius
r.R = 5.4  # 自动调用setRadius
print(r.R)  # 自动调用getRadius
```


## 14 类属性和实例属性

**：**

> ​	是可在类的所有实例之间共享的值（也就是说，它们不是单独分配给每个实例的）。例如下例中，num_of_instance 就是类属性，用于跟踪存在着多少个Test 的实例。

**实例属性：**

> 实例化之后，每个实例单独拥有的变量。

```python
class Test(object):  
    num_of_instance = 0  
    def __init__(self, name):  
        self.name = name  
        Test.num_of_instance += 1  

if __name__ == '__main__':  
    print Test.num_of_instance   # 0
    t1 = Test('jack')  
    print Test.num_of_instance   # 1
    t2 = Test('lucy')  
    print t1.name , t1.num_of_instance  # jack 2
    print t2.name , t2.num_of_instance  # lucy 2
```

> 补充的例子

```python
class Person:
    name="aaa"

p1=Person()
p2=Person()
p1.name="bbb"
print p1.name  # bbb
print p2.name  # aaa
print Person.name  # aaa
```

这里`p1.name="bbb"`是实例调用了类属性,这其实和上面第一个问题一样,就是函数传参的问题,`p1.name`一开始是指向的类属性`name="aaa"`,但是在实例的作用域里把类属性的引用改变了,就变成了一个实例属性,self.name不再引用Person的类属性name了.

可以看看下面的例子:

```python
class Person:
    name=[]

p1=Person()
p2=Person()
p1.name.append(1)
print p1.name  # [1]
print p2.name  # [1]
print Person.name  # [1]
```

参考:http://stackoverflow.com/questions/6470428/catch-multiple-exceptions-in-one-line-except-block

## 15 Python自省

这个也是python彪悍的特性.

自省就是面向对象的语言所写的程序在运行时,所能知道对象的类型.简单一句就是运行时能够获得对象的类型.比如type(),dir(),getattr(),hasattr(),isinstance().

```python
a = [1,2,3]
b = {'a':1,'b':2,'c':3}
c = True
print type(a),type(b),type(c) # <type 'list'> <type 'dict'> <type 'bool'>
print isinstance(a,list)  # True
```



## 16 字典解析、列表解析、集合解析
代码示例如下：

```python
list1=[x for x in range(100) if x%2==0] #或 [x for x in range(0,100,2)]
L = list(map(lambda x: x * x, [1, 2, 3, 4, 5, 6, 7, 8, 9])
L2 = list(filter(lambda x: x > 0, [1. - 1, -3, -4, 3, 3, 45, 34]))
#集合的列表生成式
s={1,34,5,-7,6,87,-8,-9,11}
print({x for x in s if x%3==0})
#补充：集合的交集并集等操作
A=set([randint(1,20) for _ in range(10)])
B=set([randint(1,20) for _ in range(10)])
print(A&B,A|B,A-B,A^B) #交，并，差，补

d = {key: value for (key, value) in iterable if key**}
#补充 如何根据字典中值的大小,对字典中的项排序
#方案1 使用zip将字典数据转化为元组
score = {
    'LiLei': 79,
    'Jim': 88,
    'Lucy': 92
}
score4 = tuple(zip(score.values(),score.keys()))
score5 = sorted(score4)
##直接用sorted,
print(sorted(score.items(),key=lambda x:x[1])) #表示对生成的列表的元组索引第二位进行排序
#补充 k,v交换
score2={v:k for k,v in score.items()}
score3=dict(zip(score2.values(),score2.keys()))
```
#### 补充1 如何为元组的每个元素命名,提高程序可读性
```
from collections import namedtuple
Student = namedtuple('Student', ['name', 'age', 'sex', 'email'])
Jim = Student('Jim', 16, 'male', 'jim8721@gamil.com')
print(Jim.name)
print(Jim.age)
print(Jim.sex)
print(Jim.email)
```

#### 补充2 如何统计序列中元素的出现频度
```
from collections import Counter, OrderedDict
from random import randint
import re

data = [randint(0, 20) for _ in range(30)] #产生30个0到20的随机整数
print(Counter(data))
print(Counter(data).most_common(3))
```

#### 补充3 如何快速找到多个字典中的公共键(key)
```
from functools import reduce

N1 = {
    '苏亚雷斯': 1,
    '梅西': 2,
    '本泽马': 1,
    'C罗': 3
}

N2 = {
    '苏亚雷斯': 2,
    'C罗': 1,
    '格里子曼': 2,
    '贝尔': 1
}

N3 = {
    '苏亚雷斯': 1,
    '托雷斯': 2,
    '内马尔': 1,
    '贝尔': 1
}

# 统计出每轮比赛都有进球的球员
res = []
for k in N1:
    if k in N2 and k in N3:
        res.append(k)

print(res)
#解决方案:
'''
利用set集合的交集操作
1.使用dict的viewkeys()方法,返回一个dict.keys()的集合
2.使用map函数,得到所有字典的keys的集合
3.使用reduce函数,取所有字典的keys的集合的交集
'''
print(reduce(lambda x,y:x &y,list(map(dict.keys,[N1,N2,N3]))))
```
#### 补充4 创建有序的字典
```
from functools import OrderedDict
od = OrderedDict([('a', 1), ('b', 2), ('c', 3)])
# 字典输出可以按插入的顺序排序并输出
```

#### 补充5 元组和列表的同异
同：列表与元组都是容器，是一系列的对象。二者都可以包含任意类型的元素甚至可以是一个序列，还可以包含元素的顺序（不像集合和字典）。
元组属于不可变对象，列表属于可变对象，列表的很多方法不适用于元组；元组可哈希而列表不可哈希；元组占用空间更小，代码的语义更好理解再函数式编程较常用。





## 17 Python中单下划线和双下划线

```python
>>> class MyClass():
...     def __init__(self):
...             self.__superprivate = "Hello"
...             self._semiprivate = ", world!"
...
>>> mc = MyClass()
>>> print mc.__superprivate
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: myClass instance has no attribute '__superprivate'
>>> print mc._semiprivate
, world!
>>> print mc.__dict__
{'_MyClass__superprivate': 'Hello', '_semiprivate': ', world!'}
```

`__foo__`:一种约定,Python内部的名字,用来区别其他用户自定义的命名,以防冲突，就是例如`__init__()`,`__del__()`,`__call__()`这些特殊方法

`_foo`:一种约定,用来指定变量私有.程序员用来指定私有变量的一种方式.不能用from module import * 导入，其他方面和公有一样访问；

`__foo`:这个有真正的意义:解析器用`_classname__foo`来代替这个名字,以区别和其他类相同的命名,它无法直接像公有成员一样随便访问,通过对象名._类名__xxx这样的方式可以访问.

详情见:http://stackoverflow.com/questions/1301346/the-meaning-of-a-single-and-a-double-underscore-before-an-object-name-in-python

或者: http://www.zhihu.com/question/19754941

## 18 字符串格式化:%和.format

.format在许多方面看起来更便利.对于`%`最烦人的是它无法同时传递一个变量和元组.你可能会想下面的代码不会有什么问题:

```
"hi there %s" % name
```

但是,如果name恰好是(1,2,3),它将会抛出一个TypeError异常.为了保证它总是正确的,你必须这样做:

```
"hi there %s" % (name,)   # 提供一个单元素的数组而不是一个参数
```

但是有点丑..format就没有这些问题.你给的第二个问题也是这样,.format好看多了.

你为什么不用它?

* 不知道它(在读这个之前)
* 为了和Python2.5兼容(譬如logging库建议使用`%`([issue #4](https://github.com/taizilongxu/interview_python/issues/4)))

http://stackoverflow.com/questions/5082452/python-string-formatting-vs-format

## 19 正则表达式相关知识及字符串操作
[参考廖雪峰](https://www.liaoxuefeng.com/wiki/0014316089557264a6b348958f449949df42a6d3a2e542c000/00143193331387014ccd1040c814dee8b2164bb4f064cff000)
* 字符串拼接join方法
str.join(iterable)
```
L = ["<0112>", "<32>", "<1024x768>", 60, "<1>", "<100.0>", "<500.0>"]
print(''.join(str(x) for x in L))
```
* 如何判断字符串a是否以字符串b开头或结尾,str.startswith(),str.endswith()
```
a="abcdefg||fadfa.py"
a.endswith(('.py','.sh'))
```
* 如何用Python来进行查询和替换一个文本字符串？
```
s = '\tabd\t124\txyz\r\n'
print(re.sub('\t|\r|\n','',s))
```
* 一次性拆分字符串 re.split(),str.split()
```Python
"""
解决方案:
方法一:连续使用是str.split()方法,每次处理一种分隔符号
方法二:使用正则表达式的re.split()方法,一次性拆分字符串
"""
s = 'ab;cd|efg|hi,jklmn|topq;rst,uvw|txyz'
t = s.split(';')
t1 = re.split(r'[,;|\t]+',s)
```
* Python里面match()和search()的区别？
```
re模块中match(pattern,string[,flags]),检查string的开头是否与pattern匹配。
re模块中re.search(pattern,string[,flags]),在string搜索pattern的第一个匹配值。
```
* Python re.findall()方法
```
#寻找一段字符串中的11位数字（手机号），返回列表
import re
str1="13832244324gdsjsfhauer13632996133"
re.findall(r'\d{11}',str1)
```
* 用Python匹配HTML tag的时候，<.*>和<.*?>有什么区别？
答：术语叫贪婪匹配( <.*> )和非贪婪匹配(<.*?> )
前者是贪婪匹配，会从头到尾匹配 <a>xyz</a>，而后者是非贪婪匹配，只匹配到第一个 >。


* 如何去掉字符串中不需要的字符

```
"""
解决方案:
方法1:字符串strip(),lstrip(),rstrip()方法去掉字符串两段字符
方法2:删除单个固定位置的字符,可以使用切片+拼接的方式
方法3:字符串的replace()方法或正则表达式re.sub()删除任意位置字符
方法4:字符串translate()方法,可以同时删除多种不同字符
"""

s='  nick2008@gmail.com  '
print(s.strip(' '))
print('----------------')
s = '====+-----'
print(s.strip('-='))
print('----------------')
s='  nick2008  @gmail.com  '
print(s[2:11]+s[12:23])
print('----------------')

s = '\tabd\t124\txyz\r\n'
print(s.replace('\t',''))
print('----------------')
s = '\tabd\t124\txyz\r\n'
print(re.sub('\t|\r|\n','',s))
print('----------------')
s = '\tabd\t124\txyz\r\n'
print(s.translate(None,'\t\r\n'))

s = '\tabd\t124\txyz\r\n'
print(s.replace('\t',''))
u = u'uulàlà,là,māmá'
print u.translate(dict.fromkeys([0x0,0x0101,0x1]))
```

* 补充 单引号，双引号，三引号的区别

答：单引号和双引号是等效的，如果要换行，需要符号(\),三引号则可以直接换行，并且可以包含注释

如果要表示Let’s go 这个字符串

单引号：s4 = ‘Let\’s go’

双引号：s5 = “Let’s go”

s6 = ‘I realy like“python”!’

这就是单引号和双引号都可以表示字符串的原因了


## 20 迭代器和生成器

这个是stackoverflow里python排名第一的问题,值得一看: http://stackoverflow.com/questions/231767/what-does-the-yield-keyword-do-in-python

这是中文版: http://taizilongxu.gitbooks.io/stackoverflow-about-python/content/1/README.html

这里有个关于生成器的创建问题面试官有考：
问：  将列表生成式中[]改成() 之后数据结构是否改变？
答案：是，从列表变为生成器

```python
>>> L = [x*x for x in range(10)]
>>> L
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
>>> g = (x*x for x in range(10))
>>> g
<generator object <genexpr> at 0x0000028F8B774200>
```
通过列表生成式，可以直接创建一个列表。但是，受到内存限制，列表容量肯定是有限的。而且，创建一个包含百万元素的列表，不仅是占用很大的内存空间，如：我们只需要访问前面的几个元素，后面大部分元素所占的空间都是浪费的。因此，没有必要创建完整的列表（节省大量内存空间）。在Python中，我们可以采用生成器：边循环，边计算的机制—>generator
###大数据的文件读取
```Python
with open(path,'rb') as file:
    for line in file:
        print(file)
```
###yield语句的用法
相当于给函数运行打断点，下次循环或者调用时在这里终止程序
yield简单说来就是一个生成器，这样函数它记住上次返 回时在函数体中的位置。对生成器第 二次（或n 次）调用跳转至该函树）调用跳转至该函数。
## 21 `*args` and `**kwargs`

用`*args`和`**kwargs`只是为了方便并没有强制使用它们.

当你不确定你的函数里将要传递多少参数时你可以用`*args`.例如,它可以传递任意数量的参数:

```python
>>> def print_everything(*args):
        for count, thing in enumerate(args):
...         print '{0}. {1}'.format(count, thing)
...
>>> print_everything('apple', 'banana', 'cabbage')
0. apple
1. banana
2. cabbage
```

相似的,`**kwargs`允许你使用没有事先定义的参数名:

```python
>>> def table_things(**kwargs):
...     for name, value in kwargs.items():
...         print '{0} = {1}'.format(name, value)
...
>>> table_things(apple = 'fruit', cabbage = 'vegetable')
cabbage = vegetable
apple = fruit
```

你也可以混着用.命名参数首先获得参数值然后所有的其他参数都传递给`*args`和`**kwargs`.命名参数在列表的最前端.例如:

```
def table_things(titlestring, **kwargs)
```

`*args`和`**kwargs`可以同时在函数的定义中,但是`*args`必须在`**kwargs`前面.

当调用函数时你也可以用`*`和`**`语法.例如:

```python
>>> def print_three_things(a, b, c):
...     print 'a = {0}, b = {1}, c = {2}'.format(a,b,c)
...
>>> mylist = ['aardvark', 'baboon', 'cat']
>>> print_three_things(*mylist)

a = aardvark, b = baboon, c = cat
```

就像你看到的一样,它可以传递列表(或者元组)的每一项并把它们解包.注意必须与它们在函数里的参数相吻合.当然,你也可以在函数定义或者函数调用时用*.

http://stackoverflow.com/questions/3394835/args-and-kwargs

## 22 装饰器
装饰器是一个很著名的设计模式，经常被用于有切面需求的场景，较为经典的有计时统计、插入日志、缓存计算结果、性能测试、事务处理等。装饰器是解决这类问题的绝佳设计，有了装饰器，我们就可以抽离出大量函数中与函数功能本身无关的雷同代码并继续重用。概括的讲，**装饰器的作用就是为已经存在的对象添加额外的功能。**
装饰器的作用和功能：
* 引入日志
* 函数执行时间统计
* 执行函数前预备处理
* 执行函数后的清理功能
* 权限校验等场景
* 缓存

下面举例说明

#### 装饰器用做日志记录
```Python
from functools import wrapper
def log(func):
    @functools.wraps(func) # 将func的属性传递给wrapper
    def wrapper(*args, **kw):
        print('call %s():' % func.__name__)
        f=func(*args, **kw)
        print('end call %s():' % func.__name__)
        return f    
    return wrapper
```

#### 如何定义带参数的装饰器
```
import functools

def log(text):
    def decorator(func):
        @functools.wraps(func)
        def wrapper(*args, **kw):
            print('%s %s():' % (text, func.__name__))
            return func(*args, **kw)
        return wrapper
    return decorator
# 同时支持@log和@log('execute')
def log2(text):
    def decorator(func):
        @functools.wraps(func)
        def wrapper(*args, **kw):
            if isinstance(text,str):
                print('%s %s():' % (text, func.__name__))
            else:
                print('%s():' % func.__name__)
            return func(*args, **kw)
        return wrapper
    if callable(text):
        return decorator(text)
    else:
        return decorator
```

#### 装饰器用做执行时间统计
```

from functools import wrapper
from time import time
def metric(func):
    @functools.wraps(func)
    def wrapper(*args, **kw):
        t0 = time()
        func(*args, **kw)
        print('%s executed in %s ms' % (func.__name__, (time() - t0) * 1000))
        return func
    return wrapper
```
#### 装饰器用做缓存
```

def meomo(func):
    cache = {}
    def wrap(*args):
        if args not in cache:
            cache[args] = func(*args)
        return cache[args]
    return wrap
@meomo
def fibonacci(n):
    if n<=1:
        return 1
    cache = fibonacci(n-1)+fibonacci(n-2)
    return cache
"""一个共有十个10个台阶的楼梯,从下面走到上面,一次只能迈1-3个台阶,
并且不能后退,走完这个楼梯共有多少种方法"""
'''
@meomo
def climb(n,steps):
    count = 0
    if n == 0:
        count +=1
    elif n>0:
        for step in steps:
            count += climb(n-step,steps)
    return count
```

这个问题比较大,推荐: http://stackoverflow.com/questions/739654/how-can-i-make-a-chain-of-function-decorators-in-python

中文: http://taizilongxu.gitbooks.io/stackoverflow-about-python/content/3/README.html

## 23 Python中重载

引自知乎:http://www.zhihu.com/question/20053359

函数重载主要是为了解决两个问题。

1. 可变参数类型。
2. 可变参数个数。

另外，一个基本的设计原则是，仅仅当两个函数除了参数类型和参数个数不同以外，其功能是完全相同的，此时才使用函数重载，如果两个函数的功能其实不同，那么不应当使用重载，而应当使用一个名字不同的函数。

好吧，那么对于情况 1 ，函数功能相同，但是参数类型不同，python 如何处理？答案是根本不需要处理，因为 python 可以接受任何类型的参数，如果函数的功能相同，那么不同的参数类型在 python 中很可能是相同的代码，没有必要做成两个不同函数。

那么对于情况 2 ，函数功能相同，但参数个数不同，python 如何处理？大家知道，答案就是缺省参数。对那些缺少的参数设定为缺省参数即可解决问题。因为你假设函数功能相同，那么那些缺少的参数终归是需要用的。

好了，鉴于情况 1 跟 情况 2 都有了解决方案，python 自然就不需要函数重载了。

## 24 `__new__`和`__init__`的区别

这个`__new__`确实很少见到,先做了解吧.

1. `__new__`是一个静态方法,而`__init__`是一个实例方法.
2. `__new__`方法会返回一个创建的实例,而`__init__`什么都不返回.
3. 只有在`__new__`返回一个cls的实例时后面的`__init__`才能被调用.
4. 当创建一个新实例时调用`__new__`,初始化一个实例时用`__init__`.

[stackoverflow](http://stackoverflow.com/questions/674304/pythons-use-of-new-and-init)

ps: `__metaclass__`是创建类时起作用.所以我们可以分别使用`__metaclass__`,`__new__`和`__init__`来分别在类创建,实例创建和实例初始化的时候做一些小手脚.

## 25 单例模式

> ​	单例模式是一种常用的软件设计模式。在它的核心结构中只包含一个被称为单例类的特殊类。通过单例模式可以保证系统中一个类只有一个实例而且该实例易于外界访问，从而方便对实例个数的控制并节约系统资源。如果希望在系统中某个类的对象只能存在一个，单例模式是最好的解决方案。
>
> `__new__()`在`__init__()`之前被调用，用于生成实例对象。利用这个方法和类的属性的特点可以实现设计模式的单例模式。单例模式是指创建唯一对象，单例模式设计的类只能实例
**这个绝对常考啊.绝对要记住1~2个方法,当时面试官是让手写的.**

### 1 使用`__new__`方法

```python
class Singleton(object):
    def __new__(cls, *args, **kw):
        if not hasattr(cls, '_instance'):
            orig = super(Singleton, cls)
            cls._instance = orig.__new__(cls, *args, **kw)
        return cls._instance

class MyClass(Singleton):
    a = 1
```

### 2 共享属性

创建实例时把所有实例的`__dict__`指向同一个字典,这样它们具有相同的属性和方法.

```python

class Borg(object):
    _state = {}
    def __new__(cls, *args, **kw):
        ob = super(Borg, cls).__new__(cls, *args, **kw)
        ob.__dict__ = cls._state
        return ob

class MyClass2(Borg):
    a = 1
```

### 3 装饰器版本

```python
def singleton(cls):
    instances = {}
    def getinstance(*args, **kw):
        if cls not in instances:
            instances[cls] = cls(*args, **kw)
        return instances[cls]
    return getinstance

@singleton
class MyClass:
  ...
```

### 4 import方法

作为python的模块是天然的单例模式

```python
# mysingleton.py
class My_Singleton(object):
    def foo(self):
        pass

my_singleton = My_Singleton()

# to use
from mysingleton import my_singleton

my_singleton.foo()

```
**[单例模式伯乐在线详细解释](http://python.jobbole.com/87294/)**

## 26 Python中的作用域

Python 中，一个变量的作用域总是由在代码中被赋值的地方所决定的。

当 Python 遇到一个变量的话他会按照这样的顺序进行搜索：

本地作用域（Local）→当前作用域被嵌入的本地作用域（Enclosing locals）→全局/模块作用域（Global）→内置作用域（Built-in）

## 27 GIL线程全局锁

 Python代码的执行由Python 虚拟机(也叫解释器主循环，CPython版本)来控制，Python 在设计之初就考虑到要在解释器的主循环中，同时只有一个线程在执行，即在任意时刻，只有一个线程在解释器中运行。对Python 虚拟机的访问由全局解释器锁（GIL）来控制，正是这个锁能保证同一时刻只有一个线程在运行。线程的执行速度非常之快，会让你误以为线程是并行执行的（并行），但是实际上都是轮流执行（并发或者串行）。**对于io密集型任务，python的多线程起到作用，但对于cpu密集型任务，python的多线程几乎占不到任何优势，还有可能因为争夺资源而变慢。**
 在多线程环境中，Python 虚拟机按以下方式执行：
1. 设置GIL
2. 切换到一个线程去运行
3. 运行：
    a. 指定数量的字节码指令，或者
    b. 线程主动让出控制（可以调用time.sleep(0)）
4. 把线程设置为睡眠状态
5. 解锁GIL
6. 再次重复以上所有步骤
 在调用外部代码（如C/C++扩展函数）的时候，GIL 将会被锁定，直到这个函数结束为止（由于在这期间没有Python 的字节码被运行，所以不会做线程切换）。
join方法 子进程结束切换到父进程
多进程应该避免共享资源。在多线程中，我们可以比较容易地共享资源，比如使用全局变量或者传递参数。在多进程情况下，由于每个进程有自己独立的内存空间，以上方法并不合适。此时我们可以通过共享内存和Manager的方法来共享资源。但这样做提高了程序的复杂度，并因为同步的需要而降低了程序的效率。

见[Python 最难的问题](http://www.oschina.net/translate/pythons-hardest-problem)

解决办法就是多进程和下面的协程(协程也只是单CPU,但是能减小切换代价提升性能).

## 28 协程

### [参考廖雪峰](https://www.liaoxuefeng.com/wiki/0014316089557264a6b348958f449949df42a6d3a2e542c000/001432090171191d05dae6e129940518d1d6cf6eeaaa969000)

简单点说协程是进程和线程的升级版,进程和线程都面临着内核态和用户态的切换问题而耗费许多切换时间,而协程就是用户自己控制切换的时机,不再需要陷入系统的内核态.

Python对协程的支持是通过generator实现的。


## 29 闭包

闭包(closure)是函数式编程的重要的语法结构。闭包也是一种组织代码的结构，它同样提高了代码的可重复使用性。

当一个内嵌函数引用其外部作作用域的变量,我们就会得到一个闭包. 总结一下,创建一个闭包必须满足以下几点:

1. 必须有一个内嵌函数
2. 内嵌函数必须引用外部函数中的变量
3. 外部函数的返回值必须是内嵌函数

感觉闭包还是有难度的,几句话是说不明白的,还是查查相关资料.

重点是函数运行后并不会被撤销,就像16题的instance字典一样,当函数运行完后,instance并不被销毁,而是继续留在内存空间里.这个功能类似类里的类属性,只不过迁移到了函数上.

闭包就像个空心球一样,你知道外面和里面,但你不知道中间是什么样.

## 30 lambda函数

其实就是一个匿名函数,为什么叫lambda?因为和后面的函数式编程有关.

推荐: [知乎](http://www.zhihu.com/question/20125256)


## 31 Python函数式编程

这个需要适当的了解一下吧,毕竟函数式编程在Python中也做了引用.

推荐: [酷壳](http://coolshell.cn/articles/10822.html)

python中函数式编程支持:

filter 函数的功能相当于过滤器。调用一个布尔函数`bool_func`来迭代遍历每个seq中的元素；返回一个使`bool_seq`返回值为true的元素的序列。

```python
>>>a = [1,2,3,4,5,6,7]
>>>b = filter(lambda x: x > 5, a)
>>>print b
>>>[6,7]
```

map函数是对一个序列的每个项依次执行函数，下面是对一个序列每个项都乘以2：

```python
>>> a = map(lambda x:x*2,[1,2,3])
>>> list(a)
[2, 4, 6]
```

reduce函数是对一个序列的每个项迭代调用函数，下面是求3的阶乘：

```python
>>> reduce(lambda x,y:x*y,range(1,4))
6
```

filter函数用于对序列的每个项进行迭代，不满足条件的就会被踢出序列
```python
>>> filter(lambda x>0:x,range(-10,4))
[1,2,3]
```
补充：用filter求素数
```
def _odd_iter():
    n = 1
    while True:
        n = n + 2
        yield n
def _not_divisible(n):
    return lambda x: x % n > 0
def primes():
    yield 2
    it = _odd_iter() # 初始序列
    while True:
        n = next(it) # 返回序列的第一个数
        yield n
        it = filter(_not_divisible(n), it) # 构造新序列
# 打印1000以内的素数:
for n in primes():
    if n < 1000:
        print(n)
    else:
        break
```

## 32 Python里的拷贝

引用和copy(),deepcopy()的区别

```python
import copy
a = [1, 2, 3, 4, ['a', 'b']]  #原始对象

b = a  #赋值，传对象的引用
c = copy.copy(a)  #对象拷贝，浅拷贝
d = copy.deepcopy(a)  #对象拷贝，深拷贝

a.append(5)  #修改对象a
a[4].append('c')  #修改对象a中的['a', 'b']数组对象

print 'a = ', a
print 'b = ', b
print 'c = ', c
print 'd = ', d

输出结果：
a =  [1, 2, 3, 4, ['a', 'b', 'c'], 5]
b =  [1, 2, 3, 4, ['a', 'b', 'c'], 5]
c =  [1, 2, 3, 4, ['a', 'b', 'c']]
d =  [1, 2, 3, 4, ['a', 'b']]
```
切片的对象，切片是浅拷贝还是深拷贝
切片的对象有list,tuple,str
“=”,copy,slice属于浅拷贝
deepcopy就属于深拷贝
浅拷贝和深拷贝的区别在于深拷贝是被复制的对象作为一个新的个体独立存在,
任意改变其一不会对另一个对象造成影响,而浅拷贝不会产生新的独立对象


## 33 Python是如何进行内存管理的
(http://developer.51cto.com/art/201007/213585.html)

答:从三个方面来说,一对象的引用计数机制,二垃圾回收机制,三内存池机制

* 1、对象的引用计数机制

Python内部使用引用计数，来保持追踪内存中的对象，所有对象都有引用计数。

引用计数增加的情况：

1，一个对象分配一个新名称

2，将其放入一个容器中（如列表、元组或字典）

引用计数减少的情况：

1，使用del语句对对象别名显示的销毁

2，引用超出作用域或被重新赋值

sys.getrefcount( )函数可以获得对象的当前引用计数

多数情况下，引用计数比你猜测得要大得多。对于不可变数据（如数字和字符串），解释器会在程序的不同部分共享内存，以便节约内存。

* 2、垃圾回收

1，当一个对象的引用计数归零时，它将被垃圾收集机制处理掉。

2，当两个对象a和b相互引用时，del语句可以减少a和b的引用计数，并销毁用于引用底层对象的名称。然而由于每个对象都包含一个对其他对象的应用，

因此引用计数不会归零，对象也不会销毁。（从而导致内存泄露）。为解决这一问题，解释器会定期执行一个循环检测器，搜索不可访问对象的循环并删除它们。

* 3、内存池机制

Python提供了对内存的垃圾收集机制，但是它将不用的内存放到内存池而不是返回给操作系统。

1，Pymalloc机制。为了加速Python的执行效率，Python引入了一个内存池机制，用于管理对小块内存的申请和释放。

2，Python中所有小于256个字节的对象都使用pymalloc实现的分配器，而大的对象则使用系统的malloc。

3，对于Python对象，如整数，浮点数和List，都有其独立的私有内存池，对象间不共享他们的内存池。也就是说如果你分配又释放了大量的整数，用于缓存这些整数的内存就不能再分配给浮点数。

## 34 Python的List和Dict的实现原理

推荐:
[列表](http://www.jianshu.com/p/J4U6rR)
[字典](https://blog.csdn.net/shouting3901/article/details/80468735)

* 字典按照键值对的形式进行存储，时间复杂度为O(1)
* 字典的底层是通过哈希表实现的，使用开放地址法解决冲突。所以其查找的时间复杂度会是O(1)，哈希函数求哈希值

## 35 Python的is和==
is是对比地址,==是对比值
is 比较的是两个实例对象是不是完全相同,is关键字是查看两个对象是否相同的唯一标准，他们是不是同一个对象,
占用的内存地址是否相同,即比较他们的id
== 比较的是两个实例对象的内容是否相同,即他们的内存地址可以不同,默认调用eq方法
切片slice is->False ==->True
序列直接复制=  is->True
大量创建相同内容的字符串，is->True
小整数对象[-5,256]在全局解释器范围内被放入缓存共重复使用
a=1 b=1 a is b ->True ==->True
a=257 b=257 a is b ->True ==->True

is运算符比==效率高,在变量和None进行比较时,应该使用is
## 36 read,readline和readlines

* read        读取整个文件
* readline    读取下一行,使用生成器方法
* readlines   读取整个文件到一个迭代器以供我们遍历



## 37 Python2和3的区别
推荐：[Python 2.7.x 与 Python 3.x 的主要差异](http://chenqx.github.io/2014/11/10/Key-differences-between-Python-2-7-x-and-Python-3-x/)

#### 补充：Python的编码问题
python3 bytes和str都可以代表字符序列,前者的实例包含原始的8位值;bytes.decode('utf-8')
后者的实例包含unicode字符 str.encode('utf-8')

python2 str和Unicode都可以代表字符序列,与python3不同的是,str的实例包含原始的8位值,str.decode('utf-8')
而Unicode的实例则包含unicode字符,unicode.encode(‘utf-8’)

python2 str <--> python3 bytes
python2 unicode <--> python3 str

python2 str.decode(‘utf-8’)–>unicode
unicode.encode(‘utf-8’)–>str
python3 bytes.decode(‘utf-8’)–>str
str.encode(‘utf-8’) –>bytes

# 数据库

## 1 事务

数据库事务(Database Transaction) ，是指作为单个逻辑工作单元执行的一系列操作，要么完全地执行，要么完全地不执行。
彻底理解数据库事务: http://www.hollischuang.com/archives/898

## 2 数据库索引

推荐: http://tech.meituan.com/mysql-index.html

[MySQL索引背后的数据结构及算法原理](http://blog.codinglabs.org/articles/theory-of-mysql-index.html)

聚集索引,非聚集索引,B-Tree,B+Tree,最左前缀原理

## 3 Redis原理

### Redis是什么？

1. 是一个完全开源免费的key-value内存数据库
2. 通常被认为是一个数据结构服务器，主要是因为其有着丰富的数据结构 strings、map、 list、sets、 sorted sets

### Redis数据库

> ​	通常局限点来说，Redis也以消息队列的形式存在，作为内嵌的List存在，满足实时的高并发需求。在使用缓存的时候，redis比memcached具有更多的优势，并且支持更多的数据类型，把redis当作一个中间存储系统，用来处理高并发的数据库操作

- 速度快：使用标准C写，所有数据都在内存中完成，读写速度分别达到10万/20万
- 持久化：对数据的更新采用Copy-on-write技术，可以异步地保存到磁盘上，主要有两种策略，一是根据时间，更新次数的快照（save 300 10 ）二是基于语句追加方式(Append-only file，aof)
- 自动操作：对不同数据类型的操作都是自动的，很安全
- 快速的主--从复制，官方提供了一个数据，Slave在21秒即完成了对Amazon网站10G key set的复制。
- Sharding技术： 很容易将数据分布到多个Redis实例中，数据库的扩展是个永恒的话题，在关系型数据库中，主要是以添加硬件、以分区为主要技术形式的纵向扩展解决了很多的应用场景，但随着web2.0、移动互联网、云计算等应用的兴起，这种扩展模式已经不太适合了，所以近年来，像采用主从配置、数据库复制形式的，Sharding这种技术把负载分布到多个特理节点上去的横向扩展方式用处越来越多。

### Redis缺点

- 是数据库容量受到物理内存的限制,不能用作海量数据的高性能读写,因此Redis适合的场景主要局限在较小数据量的高性能操作和运算上。
- Redis较难支持在线扩容，在集群容量达到上限时在线扩容会变得很复杂。为避免这一问题，运维人员在系统上线时必须确保有足够的空间，这对资源造成了很大的浪费。




## 4 MyISAM和InnoDB

MyISAM 适合于一些需要大量查询的应用，但其对于有大量写操作并不是很好。甚至你只是需要update一个字段，整个表都会被锁起来，而别的进程，就算是读进程都无法操作直到读操作完成。另外，MyISAM 对于 SELECT COUNT(*) 这类的计算是超快无比的。

InnoDB 的趋势会是一个非常复杂的存储引擎，对于一些小的应用，它会比 MyISAM 还慢。他是它支持“行锁” ，于是在写操作比较多的时候，会更优秀。并且，他还支持更多的高级应用，比如：事务。

mysql 数据库引擎: http://www.cnblogs.com/0201zcr/p/5296843.html
MySQL存储引擎－－MyISAM与InnoDB区别: https://segmentfault.com/a/1190000008227211

# 网络

## 1 三次握手

1. 客户端通过向服务器端发送一个SYN来创建一个主动打开，作为三次握手的一部分。客户端把这段连接的序号设定为随机数 A。
2. 服务器端应当为一个合法的SYN回送一个SYN/ACK。ACK 的确认码应为 A+1，SYN/ACK 包本身又有一个随机序号 B。
3. 最后，客户端再发送一个ACK。当服务端受到这个ACK的时候，就完成了三路握手，并进入了连接创建状态。此时包序号被设定为收到的确认号 A+1，而响应则为 B+1。

## 2 四次挥手

_注意: 中断连接端可以是客户端，也可以是服务器端. 下面仅以客户端断开连接举例, 反之亦然._

1. 客户端发送一个数据分段, 其中的 FIN 标记设置为1. 客户端进入 FIN-WAIT 状态. 该状态下客户端只接收数据, 不再发送数据.
2. 服务器接收到带有 FIN = 1 的数据分段, 发送带有 ACK = 1 的剩余数据分段, 确认收到客户端发来的 FIN 信息.
3. 服务器等到所有数据传输结束, 向客户端发送一个带有 FIN = 1 的数据分段, 并进入 CLOSE-WAIT 状态, 等待客户端发来带有 ACK = 1 的确认报文.
4. 客户端收到服务器发来带有 FIN = 1 的报文, 返回 ACK = 1 的报文确认, 为了防止服务器端未收到需要重发, 进入 TIME-WAIT 状态. 服务器接收到报文后关闭连接. 客户端等待 2MSL 后未收到回复, 则认为服务器成功关闭, 客户端关闭连接.

图解: http://blog.csdn.net/whuslei/article/details/6667471

## 3 ARP协议

地址解析协议(Address Resolution Protocol)，其基本功能为透过目标设备的IP地址，查询目标的MAC地址，以保证通信的顺利进行。它是IPv4网络层必不可少的协议，不过在IPv6中已不再适用，并被邻居发现协议（NDP）所替代。

## 4 urllib和urllib2的区别

这个面试官确实问过,当时答的urllib2可以Post而urllib不可以.

1. urllib提供urlencode方法用来GET查询字符串的产生，而urllib2没有。这是为何urllib常和urllib2一起使用的原因。
2. urllib2可以接受一个Request类的实例来设置URL请求的headers，urllib仅可以接受URL。这意味着，你不可以伪装你的User Agent字符串等。


## 5 Post和Get
[GET和POST有什么区别？及为什么网上的多数答案都是错的](http://www.cnblogs.com/nankezhishi/archive/2012/06/09/getandpost.html)
[知乎回答](https://www.zhihu.com/question/31640769?rf=37401322)

get: [RFC 2616 - Hypertext Transfer Protocol -- HTTP/1.1](http://tools.ietf.org/html/rfc2616#section-9.3)
post: [RFC 2616 - Hypertext Transfer Protocol -- HTTP/1.1](http://tools.ietf.org/html/rfc2616#section-9.5)



## 6 Cookie和Session

|      | Cookie                     | Session |
| :--- | :------------------------- | :------ |
| 储存位置 | 客户端                        | 服务器端    |
| 目的   | 跟踪会话，也可以保存用户偏好设置或者保存用户名密码等 | 跟踪会话    |
| 安全性  | 不安全                        | 安全      |

session技术是要使用到cookie的，之所以出现session技术，主要是为了安全。

## 7 apache和nginx的区别

nginx 相对 apache 的优点：
* 轻量级，同样起web 服务，比apache 占用更少的内存及资源
* 抗并发，nginx 处理请求是异步非阻塞的，支持更多的并发连接，而apache 则是阻塞型的，在高并发下nginx 能保持低资源低消耗高性能
* 配置简洁
* 高度模块化的设计，编写模块相对简单
* 社区活跃

apache 相对nginx 的优点：
* rewrite ，比nginx 的rewrite 强大
* 模块超多，基本想到的都可以找到
* 少bug ，nginx 的bug 相对较多
* 超稳定

## 8 网站用户密码保存

1. 明文保存
2. 明文hash后保存,如md5
3. MD5+Salt方式,这个salt可以随机
4. 知乎使用了Bcrypy(好像)加密

## 9 HTTP和HTTPS


| 状态码       | 定义               |
| :-------- | :--------------- |
| 1xx 报告    | 接收到请求，继续进程       |
| 2xx 成功    | 步骤成功接收，被理解，并被接受  |
| 3xx 重定向   | 为了完成请求,必须采取进一步措施 |
| 4xx 客户端出错 | 请求包括错的顺序或不能完成    |
| 5xx 服务器出错 | 服务器无法完成显然有效的请求   |

403: Forbidden
404: Not Found

HTTPS握手,对称加密,非对称加密,TLS/SSL,RSA

## 10 XSRF和XSS

* CSRF(Cross-site request forgery)跨站请求伪造
* XSS(Cross Site Scripting)跨站脚本攻击

CSRF重点在请求,XSS重点在脚本


## 12 RESTful架构(SOAP,RPC)

推荐: http://www.ruanyifeng.com/blog/2011/09/restful.html


## 15 CGI和WSGI
CGI是通用网关接口，是连接web服务器和应用程序的接口，用户通过CGI来获取动态数据或文件等。
CGI程序是一个独立的程序，它可以用几乎所有语言来写，包括perl，c，lua，python等等。

WSGI, Web Server Gateway Interface，是Python应用程序或框架和Web服务器之间的一种接口，WSGI的其中一个目的就是让用户可以用统一的语言(Python)编写前后端。

官方说明：[PEP-3333](https://www.python.org/dev/peps/pep-3333/)


## 18 socket

推荐: http://www.360doc.com/content/11/0609/15/5482098_122692444.shtml

Socket=Ip address+ TCP/UDP + port

## 19 浏览器缓存

推荐: http://www.cnblogs.com/skynet/archive/2012/11/28/2792503.html

304 Not Modified

## 20 HTTP1.0和HTTP1.1

推荐: http://blog.csdn.net/elifefly/article/details/3964766

1. 请求头Host字段,一个服务器多个网站
2. 长链接
3. 文件断点续传
4. 身份认证,状态管理,Cache缓存

HTTP请求8种方法介绍
HTTP/1.1协议中共定义了8种HTTP请求方法，HTTP请求方法也被叫做“请求动作”，不同的方法规定了不同的操作指定的资源方式。服务端也会根据不同的请求方法做不同的响应。

GET

GET请求会显示请求指定的资源。一般来说GET方法应该只用于数据的读取，而不应当用于会产生副作用的非幂等的操作中。

GET会方法请求指定的页面信息，并返回响应主体，GET被认为是不安全的方法，因为GET方法会被网络蜘蛛等任意的访问。

HEAD

HEAD方法与GET方法一样，都是向服务器发出指定资源的请求。但是，服务器在响应HEAD请求时不会回传资源的内容部分，即：响应主体。这样，我们可以不传输全部内容的情况下，就可以获取服务器的响应头信息。HEAD方法常被用于客户端查看服务器的性能。

POST

POST请求会 向指定资源提交数据，请求服务器进行处理，如：表单数据提交、文件上传等，请求数据会被包含在请求体中。POST方法是非幂等的方法，因为这个请求可能会创建新的资源或/和修改现有资源。

PUT

PUT请求会身向指定资源位置上传其最新内容，PUT方法是幂等的方法。通过该方法客户端可以将指定资源的最新数据传送给服务器取代指定的资源的内容。

DELETE

DELETE请求用于请求服务器删除所请求URI（统一资源标识符，Uniform Resource Identifier）所标识的资源。DELETE请求后指定资源会被删除，DELETE方法也是幂等的。

CONNECT

CONNECT方法是HTTP/1.1协议预留的，能够将连接改为管道方式的代理服务器。通常用于SSL加密服务器的链接与非加密的HTTP代理服务器的通信。

OPTIONS

OPTIONS请求与HEAD类似，一般也是用于客户端查看服务器的性能。 这个方法会请求服务器返回该资源所支持的所有HTTP请求方法，该方法会用’*’来代替资源名称，向服务器发送OPTIONS请求，可以测试服务器功能是否正常。JavaScript的XMLHttpRequest对象进行CORS跨域资源共享时，就是使用OPTIONS方法发送嗅探请求，以判断是否有对指定资源的访问权限。 允许

TRACE

TRACE请求服务器回显其收到的请求信息，该方法主要用于HTTP请求的测试或诊断。

HTTP/1.1之后增加的方法

在HTTP/1.1标准制定之后，又陆续扩展了一些方法。其中使用中较多的是 PATCH 方法：

PATCH

PATCH方法出现的较晚，它在2010年的RFC 5789标准中被定义。PATCH请求与PUT请求类似，同样用于资源的更新。二者有以下两点不同：

但PATCH一般用于资源的部分更新，而PUT一般用于资源的整体更新。
当资源不存在时，PATCH会创建一个新的资源，而PUT只会对已在资源进行更新。

# 编程题


## 1 列表复制问题
```
list1=[None,None]
list2=list1*2 -->[None,None,None,None]
list3=[list1]*2 -->[[None,None],[None,None]]
```
## 2 求列表第三大的那个值
```
import random
b = [random.randint(1,10000) for i in range(1000)]
max1 = b[0]
max2 = b[1]
max3 = b[2]
for k in b:
    if k>max1:
        max1,max2,max3 = k,max1,max2
    if k>max3 and k<max2:
        max3 = k
    if k>max2 and k<max1:
        max3 = max2
        max2 = k
print('{0},{1},{2}'.format(max1,max2,max3))
```
## 3 实现一个队列
[参考博客园](https://www.cnblogs.com/chongyou/p/7099326.html)
```
# 首先获取节点，包含next指针和该节点位置上元素的值
class Node(object):
    def __init__(self, val):
        self.next = None
        self.val = val


class Queue(object):
    def __init__(self):
        self.first = None
        self.last = None

    # 进队操作
    def enter(self, n):
        # 实例节点
        n = Node(n)
        # 进队之前先判断队列是否为空，即判断first是否为None
        if self.first == None:
            # 此时last==first==n
            self.first = n
            self.last = self.first
        else:
            # 将last的指针设置为n，值设置为n
            self.last.next = n
            self.last = n

    # 出队
    def quit(self):
        if self.first == None:
            return None
        else:
            tmp = self.first.val
            self.first = self.first.next
        return tmp

    # 保存队列元素到列表
    def allQuit(self):
        Lists = []
        while self.first != None:
            Lists.append(self.first.val)
            self.first = self.first.next
        return Lists


if __name__ == '__main__':
    q = Queue()
    q.enter(1)
    q.enter(2)
    q.enter(3)
    # print(q.quit())
    # print(q.quit())
    # print(q.quit())
    # print(q.quit())

    print(q.allQuit())

```
## 4 实现一个堆栈
[参考](https://www.cnblogs.com/chongyou/p/7099692.html)

```
class Stack(object):
    def __init__(self):
        self.top = None

    # 获取栈顶的值
    def peek(self):
        if self.top != None:
            return self.top.val
        else:
            return None

    # 入栈操作
    def push(self, n):
        n = Node(n)  # 实例化节点
        n.next = self.top
        self.top = n
        return n.val

    # 出栈操作
    def pop(self):
        if self.top == None:
            return None
        else:
            tmp = self.top.val
            # return self.top.val
            self.top = self.top.next  # 栈顶元素下移一位
            return tmp
if __name__ == '__main__':
    s = Stack()
    # s.peek()
    s.push(1)
    print(s.peek())
    s.push(2)
    print(s.peek())
    s.push(3)
    print(s.peek())
    print(s.pop())
    print(s.pop())
    print(s.pop())
    print(s.pop())           
```
## 5 用Python实现一个单向链表 
[参考](https://blog.csdn.net/qq490691606/article/details/49945287)
```
"""节点类"""


class Node(object):
    def __init__(self, data):
        self.data = data
        self.nex = None

def __init__(self):
    """初始化链表"""
    self.head = None

def __len__(self):
    pre = self.head
    length = 0
    while pre:
        length += 1
        pre = pre.nex
    return length

"""追加节点"""

def append(self, data):
    """
    1.head 为none :head-->node
    2.tail.nex-->node
    :param data:
    :return:
    """
    node = Node(data)
    if self.head is None:
        self.head = node
    else:
        pre = self.head
        while pre.nex:
            pre = pre.nex
        pre.nex = node
# 获取节点
def get(self, index):
    """
    :param index:
    :return:
    """
    index = index if index >= 0 else len(self) + index
    if len(self) < index or index < 0:
        return None
    pre = self.head
    while index:
        pre = pre.nex
        index -= 1
    return pre
"""设置节点"""

def set(self, index, data):
    node = self.get(index)
    if node:
        node.data = data
    return node
"""插入节点"""

def insert(self, index, data):
    """
    1.index 插入节点位置包括正负数
    2.找到index-1-->pre_node的节点
    3.pre_node.next-->node
      node.next-->pre_node.next.next
    4.head
    :param index:
    :param data:
    :return:
    """
    node = Node(data)
    if abs(index + 1) > len(self):
        return False
    index = index if index >= 0 else len(self) + index + 1
    if index == 0:
        node.nex = self.head
        self.head = node
    else:
        pre = self.get(index - 1)
        if pre:
            nex = pre.nex
            pre.nex = node
            node.nex = nex
        else:
            return False
    return node
"""删除某个元素"""

def delete(self, index):
    f = index if index > 0 else abs(index + 1)
    if len(self) <= f:
        return False
    pre = self.head
    index = index if index >= 0 else len(self) + index
    prep = None
    while index:
        prep = pre
        pre = pre.nex
        index -= 1
    if not prep:
        self.head = pre.nex
    else:
        prep.nex = pre.nex
    return pre.data
"""反转链表"""

def __reversed__(self):
    """
    1.pre-->next 转变为 next-->pre
    2.pre 若是head 则把 pre.nex --> None
    3.tail-->self.head
    :return:
    """

    def reverse(pre_node, node):
        if pre_node is self.head:
            pre_node.nex = None
        if node:
            next_node = node.nex
            node.nex = pre_node
            return reverse(node, next_node)
        else:
            self.head = pre_node

    return reverse(self.head, self.head.nex)
"""清空链表"""

def clear(self):
    self.head = None
```
## 6 用Python实现一个双向链表 
[参考](https://blog.csdn.net/qq490691606/article/details/49948263)
参考原文 代码省略


## 7 台阶问题/斐波那契

一只青蛙一次可以跳上1级台阶，也可以跳上2级。求该青蛙跳上一个n级的台阶总共有多少种跳法。

```python
fib = lambda n: n if n <= 2 else fib(n - 1) + fib(n - 2)
```

第二种记忆方法

```python
def memo(func):
    cache = {}
    def wrap(*args):
        if args not in cache:
            cache[args] = func(*args)
        return cache[args]
    return wrap


@memo
def fib(i):
    if i < 2:
        return 1
    return fib(i-1) + fib(i-2)
```

第三种方法

```python
def fib(n):
    a, b = 0, 1
    for _ in xrange(n):
        a, b = b, a + b
    return b
```

## 8 变态台阶问题

一只青蛙一次可以跳上1级台阶，也可以跳上2级……它也可以跳上n级。求该青蛙跳上一个n级的台阶总共有多少种跳法。

```python
fib = lambda n: n if n < 2 else 2 * fib(n - 1)
```

## 9 去除列表中的重复元素

用集合

```python
list(set(l))
```

用字典

```python
l1 = ['b','c','d','b','c','a','a']
l2 = {}.fromkeys(l1).keys()
print l2
```

用字典并保持顺序

```python
l1 = ['b','c','d','b','c','a','a']
l2 = list(set(l1))
l2.sort(key=l1.index)
print l2
```

列表推导式

```python
l1 = ['b','c','d','b','c','a','a']
l2 = []
[l2.append(i) for i in l1 if not i in l2]
for i in l1:
   if i not in l2:
       l2.append(i)
```

sorted排序并且用列表推导式.

l = ['b','c','d','b','c','a','a']
[single.append(i) for i in sorted(l) if i not in single]
print single



## 10 创建字典的方法

### 1 直接创建

```python
dict = {'name':'earth', 'port':'80'}
```

### 2 工厂方法

```python
items=[('name','earth'),('port','80')]
dict2=dict(items)
dict1=dict((['name','earth'],['port','80']))
```

### 3 fromkeys()方法

```python
dict1={}.fromkeys(('x','y'),-1)
dict={'x':-1,'y':-1}
dict2={}.fromkeys(('x','y'))
dict2={'x':None, 'y':None}
```

## 11 合并两个有序列表

知乎远程面试要求编程

>  尾递归

```python
def _recursion_merge_sort2(l1, l2, tmp):
    if len(l1) == 0 or len(l2) == 0:
        tmp.extend(l1)
        tmp.extend(l2)
        return tmp
    else:
        if l1[0] < l2[0]:
            tmp.append(l1[0])
            del l1[0]
        else:
            tmp.append(l2[0])
            del l2[0]
        return _recursion_merge_sort2(l1, l2, tmp)

def recursion_merge_sort2(l1, l2):
    return _recursion_merge_sort2(l1, l2, [])
```

>  循环算法

思路：

定义一个新的空列表

比较两个列表的首个元素

小的就插入到新列表里

把已经插入新列表的元素从旧列表删除

直到两个旧列表有一个为空

再把旧列表加到新列表后面


```pyhton
def loop_merge_sort(l1, l2):
    tmp = []
    while len(l1) > 0 and len(l2) > 0:
        if l1[0] < l2[0]:
            tmp.append(l1[0])
            del l1[0]
        else:
            tmp.append(l2[0])
            del l2[0]
    tmp.extend(l1)
    tmp.extend(l2)
    return tmp
```


> pop弹出

```Python
a = [1,2,3,7]
b = [3,4,5]

def merge_sortedlist(a,b):
    c = []
    while a and b:
        if a[0] >= b[0]:
            c.append(b.pop(0))
        else:
            c.append(a.pop(0))
    while a:
        c.append(a.pop(0))
    while b:
        c.append(b.pop(0))
    return c
print merge_sortedlist(a,b)

```
## 12 归并排序
```
def merge(a, b):
    c = []
    h = j = 0
    # 依次便利，拿到兩個數組更小的元素，
    while j < len(a) and h < len(b):
        # 如果0索引位置的元素a更小，添加a[0]到c，再將a[1]與b[0]比較，依次類推，剩余最后的元素就是两个数组的最大值
        if a[j] < b[h]:
            c.append(a[j])
            j += 1
        else:
            c.append(b[h])
            h += 1

    if j == len(a):
        for i in b[h:]:
            c.append(i)
    else:
        for i in a[j:]:
            c.append(i)

    return c


def merge_sort(lists):
    if len(lists) <= 1:
        return lists
    middle = len(lists)//2
    left = merge_sort(lists[:middle])
    right = merge_sort(lists[middle:])
    return merge(left, right)

if __name__ == '__main__':
    a = [4, 7, 8, 3, 5, 9,10]
    print(merge_sort(a))
```

## 13 质数和日期问题
```
class PrimeNumbers(object):
    def __init__(self, start, end):
        self.start = start
        self.end = end

    def isPrimeNumber(self, k):
        if k < 2:
            return False
        for i in range(2, k):
            if k % i == 0:
                return False
        return True

    def __iter__(self):
        for k in range(self.start, self.end + 1):
            if self.isPrimeNumber(k):
                yield k


#print(isinstance(PrimeNumbers(1,100)))


if __name__ == '__main__':
    a = PrimeNumbers(1, 100)
    f = a.__iter__()
    L = []
    for i in f:
        L.append(i)
    print(L)

```

```
# 写一个函数，计算给定日期是该年的第几天和周数
def count(year,month,day):
    count=0
    if (year%4==0 and year%100!=0) or year%400==0:
        print('%d年是闰年，2月份有29天！'%year)
        list1=[31,29,31,30,31,30,31,31,30,31,30,31]
        for i in range(month-1):
            count=count+list1[i]
        return count+
    else:
        print('%d年是平年，2月份有29天！' % year)
        li2 = [31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31]
        for i in range(month-1):
            count +=li2[i]
        return count+day
if __name__ == "__main__":
    year = int(input('请输入年份：'))
    month = int(input('请输入月份：'))
    day = int(input('请输入日期：'))
    count = count(year,month,day)
    print('%d年%d月%d日是今年的第%d天！'%(year,month,day,count))
```
## 14 二分查找


```python

#coding:utf-8
def binary_search(list,item):
    low = 0
    high = len(list)-1
    while low<=high:
        mid = (low+high)/2
        guess = list[mid]
        if guess>item:
            high = mid-1
        elif guess<item:
            low = mid+1
        else:
            return mid
    return None
mylist = [1,3,5,7,9]
print binary_search(mylist,3)

```

参考: http://blog.csdn.net/u013205877/article/details/76411718



## 15 打印文件夹
```
def print_directory_contents(sPath):
    """
    这个函数接受文件夹的名称作为输入参数，
    返回该文件夹中文件的路径，
    以及其包含文件夹中文件的路径。

    """
    import os                                       
    for sChild in os.listdir(sPath):                
        sChildPath = os.path.join(sPath,sChild)
        if os.path.isdir(sChildPath):
            print_directory_contents(sChildPath)
        else:
            print sChildPath
```

## 16 找零问题


```python

#coding:utf-8
#values是硬币的面值values = [ 25, 21, 10, 5, 1]
#valuesCounts   钱币对应的种类数
#money  找出来的总钱数
#coinsUsed   对应于目前钱币总数i所使用的硬币数目

def coinChange(values,valuesCounts,money,coinsUsed):
    #遍历出从1到money所有的钱数可能
    for cents in range(1,money+1):
        minCoins = cents
        #把所有的硬币面值遍历出来和钱数做对比
        for kind in range(0,valuesCounts):
            if (values[kind] <= cents):
                temp = coinsUsed[cents - values[kind]] +1
                if (temp < minCoins):
                    minCoins = temp
        coinsUsed[cents] = minCoins
        print ('面值:{0}的最少硬币使用数为:{1}'.format(cents, coinsUsed[cents]))

```

思路: http://blog.csdn.net/wdxin1322/article/details/9501163

方法: http://www.cnblogs.com/ChenxofHit/archive/2011/03/18/1988431.html




## 17 二叉树节点

```python

class Node(object):
    def __init__(self, data, left=None, right=None):
        self.data = data
        self.left = left
        self.right = right

tree = Node(1, Node(3, Node(7, Node(0)), Node(6)), Node(2, Node(5), Node(4)))

```

## 17 前中后序遍历

深度遍历改变顺序就OK了

```python

#coding:utf-8
#二叉树的遍历
#简单的二叉树节点类
class Node(object):
    def __init__(self,value,left,right):
        self.value = value
        self.left = left
        self.right = right

#中序遍历:遍历左子树,访问当前节点,遍历右子树

def mid_travelsal(root):
    if root.left is None:
        mid_travelsal(root.left)
    #访问当前节点
    print(root.value)
    if root.right is not None:
        mid_travelsal(root.right)

#前序遍历:访问当前节点,遍历左子树,遍历右子树

def pre_travelsal(root):
    print (root.value)
    if root.left is not None:
        pre_travelsal(root.left)
    if root.right is not None:
        pre_travelsal(root.right)

#后续遍历:遍历左子树,遍历右子树,访问当前节点

def post_trvelsal(root):
    if root.left is not None:
        post_trvelsal(root.left)
    if root.right is not None:
        post_trvelsal(root.right)
    print (root.value)

```

## 18 求最大树深

```python
def maxDepth(root):
        if not root:
            return 0
        return max(maxDepth(root.left), maxDepth(root.right)) + 1
```

## 19 求两棵树是否相同

```python
def isSameTree(p, q):
    if p == None and q == None:
        return True
    elif p and q :
        return p.val == q.val and isSameTree(p.left,q.left) and isSameTree(p.right,q.right)
    else :
        return False
```

## 20 前序中序求后序

推荐: http://blog.csdn.net/hinyunsin/article/details/6315502

```python
def rebuild(pre, center):
    if not pre:
        return
    cur = Node(pre[0])
    index = center.index(pre[0])
    cur.left = rebuild(pre[1:index + 1], center[:index])
    cur.right = rebuild(pre[index + 1:], center[index + 1:])
    return cur

def deep(root):
    if not root:
        return
    deep(root.left)
    deep(root.right)
    print root.data
```
## 21 广度遍历和深度遍历二叉树

给定一个数组，构建二叉树，并且按层次打印这个二叉树

## 22 快排

```python
#coding:utf-8
def quicksort(list):
    if len(list)<2:
        return list
    else:
        midpivot = list[0]
        lessbeforemidpivot = [i for i in list[1:] if i<=midpivot]
        biggerafterpivot = [i for i in list[1:] if i > midpivot]
        finallylist = quicksort(lessbeforemidpivot)+[midpivot]+quicksort(biggerafterpivot)
        return finallylist

print quicksort([2,4,6,7,1,2,5])

# 使用lambda函数实现
quicksort=lambda data:data if len(data)<2 else quicksort([item for item in data[1:] if item<=data[0]])+[data[0]]+quicksort([item for item in data[1:] if item>data[0]])

print quicksort([2,4,6,7,1,2,5])
```


>  更多排序问题可见：[数据结构与算法-排序篇-Python描述](http://blog.csdn.net/mrlevo520/article/details/77829204)
## 23 层次遍历

```python

def lookup(root):
    row = [root]
    while row:
        print(row)
        row = [kid for item in row for kid in (item.left, item.right) if kid]

```

## 24 深度遍历

```python

def deep(root):
    if not root:
        return
    print root.data
    deep(root.left)
    deep(root.right)

if __name__ == '__main__':
    lookup(tree)
    deep(tree)
```

