##  一、基础知识

可以直接通过命令行交互环境进行python编程

Python除了使用Python本身编写外，还可以混合使用像c语言、java语言等编写。

![](img/python基础/python1.png)

![](img/python基础/python2.png)

## 二、安装

​		MacOS、Linux中自带了Python，可以直接使用，可以安装其他版本。（可以安装不同版本）

（一）Windows环境下Python开发环境搭建。

​		两方面：下载安装，配置环境变量path。

 ~~~
D:\Dev\python\Python37
D:\Dev\python\Python37\Scripts
 ~~~

​		官网：python.org

（二）文件夹

​		DLLs动态库、include C语言头文件、Lib Python的库、libs打包的库、Scripts这里边有一些工具，最好也设为环境变量（pip和easy_install是安装第三方库的，如命令行pip install ipython）。

（三）pyqt5安装
~~~
pip install PyQt5 
pip install PyQt5-tools

cv2
pip install  opencv-python
~~~

​		使用pip命令安装完成之后，PyQt5的包会出现在Python目录下Lib/site-packages目录下。

测试:

~~~
import sys
from PyQt5 import  QtWidgets,QtCore
app =  QtWidgets.QApplication(sys.argv)
widght =  QtWidgets.QWidget()  
widght.resize(400,400)  
widght.setWindowTitle('HelloWorld!')
widght.show()  
sys.exit(app.exec())  
~~~

## 三、Python解释器

当安装好Python，并设置好了环境变量，就可以使用解释器。

1. 打开解释器

   Windows用户打开命令行输入python。

   Mac用户打开终端（Terminal）

   ‘>>>’代表命令提示符，‘...’代表续行符。

2. 退出编辑器

   输入quit(),还可以Windows用户（Ctrl+z，回车），Mac（Command+Z）

## 四、Python开发工具大全

初级阶段：Windows：Atom，notepad++。Linux和Mac：Atom，Emacs

高级阶段：pycharm，Eclipse+pydev

（一）Atom

Atom是GitHub开发的一款免费的，功能非常强大的编辑器，它可以通过安装包的方式来扩展其功能，可以使用它来开发很多应用。例：Web前段，js，css，HTML，Python，Ruby等。

1.> Atom官网：http://atom.io/

2.> 命令进入一个文件夹后，可使用atom ./，在Atom中打开。

3.> 安装Python开发包，这个包可以直接执行Python。如：atom-runner运行快捷键alt+r，script(建议)。文件-设置-安装。script运行快捷键ctrl+shift+b。

4.> Atom输出中文可能乱码，可以在系统中添加一个：PYTHONIOENCODING环境变量，值设置为：utf-8.

（二）Eclipse+pydev

等待。

（三）pycharm

\1. PyCharm简介

PyCharm是一个著名的IDE公司JetBrains的产品，该公司以开发IDE著称，著名的IDE有：java的intellij IDEA，ios开发工具AppCode、PHP开发工具Phpstorm，以及Python开发工具Pycharm。

2.下载安装

下载地址： http://www.jetbrains.com/。有专业版和免费版。

3.使用pucharm开发Python

打开pycharm选择创建项目，在向导选型“pure python”项目，并选择项目位置和使用的解释器。

## 五、编程基础

### 1.打印语句与打印地址

命令行中‘aaa’可输出aaa。

在python中字符串，单引号和双引号是一样的。

Python文件以py为后缀名。

Python2中print ‘aaa’可以输出，但是python3不可以，必须print(‘aaa’).

id()打印对象的地址，地址指针。

### 2.Python变量和数据类型

1>数据类型是动态的，会随给变量赋的值来更改类型。

2>数字(int,float)，字符串str（可以用‘’，“”，“““ ”””），列表list（方括号括起来），元组tuple（圆括号括起来），字典dict（大括号括起来的键值对），对象。

~~~
对字典的遍历  
for i in 字典名.keys()    
	print(i)    
	print(字典名[i]) 
~~~

3>type(变量)判断类型

### 3.Python编码规范

1>分号，可以加，一般不加

2>行长度，每行不超过80个字符，以下情况除外：①长的导入模块语句②注释里的URL

3>缩进，用4个空格缩进代码，绝对不能用tab。

 ~~~
#与起始变量对齐
foo = long_function_name(var_one,var_two,
						 var_three,var_four)

 ~~~

![](img/python基础/python3.png)

 ![](img/python基础/python4.png)

4>空行。顶级定义之间空两行，比如函数或者类定义。方法定义，类定义与第一个方法之间，都应该空一行。

5>空格。括号内不要有空格

不要在逗号，分号，冒号前面加空格，但应该在它们后面加空格（除了在行尾）。

参数列表，索引或切片的左括号前不要加空格。

在二元操作符两边都加一个空格。

当“=”用于指示关键字参数或默认参数值时，不要在其两侧加空格。

 ![](img/python基础/python5.png)

 ![](img/python基础/python6.png)

   ![](img/python基础/python7.png)

![](img/python基础/python8.png)

模块名称就是文件名。

### 4.Python标识符和关键字

 ![](img/python基础/python9.png)

暂时不写函数题或类体时可写一个pass

### 5.Python注释

\#单行注释，'''多行注释'''(三个单引号或双引号都可以)

   ![](img/python基础/python10.png)

   ![](img/python基础/python11.png)

![](img/python基础/python12.png)

![](img/python基础/python13.png)

### 6.基础

   ~~~
name = '老郭'
age = 20

print('%s,%d' % (name,age))

print(name + str(age))
   ~~~

~~~
列表
list = ['111','222','333','444','555']
print(list[0])

print(list[1:3])
~~~

~~~
循环
for x in  range(10):
	print(x,end='') #end=’’,不换行
range(10)是0到9
range(1,10)是1到9
range(1,10,2)，2为步长  
~~~

使用format输出

~~~
x,y,z = 1,2,3
result =   x > y or y > z  
print("result:{0}".format(result))  
~~~

## 六、Python数字

### 1.Python程序的构成

​		包及其子包，包里面包含模块，模块里面包含语句，语句包含表达式，表达式建立并处理对象。

​	![](img/python基础/python14.png)	

​	p1为包，p2为子包，mod1.py为模块。

### 2.Python中所有类型都是对象。

​		Python中的内置对象：数字、字符串、列表、字典、元组、文件、集合、其他类型（类型、None、布尔型）、编程单元（函数、模块、类）。一旦创建了对象，就会和特定的操作集合绑定。

### 3.Python的数字类型：

​		整数和浮点数、复数、固定精度的十进制数、有理数、布尔类型、无穷的整数精度、各种数字内置函数和模块。

### 4.Python数字常量

1>整数

​	整数包括：正数，负数，0。

​	显示格式：十进制（默认），二进制（0b），八进制（0o），十六进制（0x），

​	转换函数：转二进制bin(l),转八进制oct(l),转十六进制hex(),转换为base进制int(str,base)

2>浮点数

​	带小数的数字，可以使用科学计数法3.14e-10。

3>复数

​	复数包括实部和虚部

~~~
num = 3 + 4j
print(num.real) #3.0
print(num.imag) #4.0

c = complex(3,4)
print(c)    # (3+4j)  
~~~

4>分数

​	使用分数需要使用Python中的Fraction模块，需要导入包：

~~~
from fractions  
import Fraction
f1 = Fraction(3,4)  
print(f1)  # 3/4  
~~~

### 5.Python数字显示格式

~~~
十进制%d
整数%i
无符号整数%u
八进制%o
十六进制%x 大写%X
浮点指数%e  大写%E
浮点十进制%f  %F
将指数展开%g  %G
~~~

### 6.小数对象Decimal

1>小数运算是不精确的，由于计算机内部结构的局限性。

​		为了更精确的进行小数运算，python提供了Decimal类来实现小数的精确计算。

2>使用Decimal

~~~
from decimal  
import Decimal     
a=3.14  
b=2.5  
print(a+b)     # 5.640000000000001    

a =  Decimal('3.14')  
b = Decimal('2.5')  
print(a + b)    #5.64  
~~~

3>设置全局精度

~~~
import decimal     
decimal.getcontext().prec  = 4  #精确到后4位  print(decimal.Decimal(1)/decimal.Decimal(7))  #0.1429  
~~~

### 7.Python数字内置函数和模块

1>常用函数：绝对值abs，幂pow，四舍五入round，最大值max，最小值min，和sum

~~~
print(pow(2,3))     
print(round(3.1415926,4))     
print(max([1,5,3,6,9]))     
print(sum((1,2,3,4,5)))  
~~~

2>模块math

圆周率常量pi，自然对数底数常量e，向下取整floor，向上取整ceil，x的y次方pow(x,y)，x的平方根sqrt(x)，以e为底的x次方exp(x),截取整数trunc

~~~
import math     
print(math.pi)  
print(math.trunc(3.14)) #3 
~~~

3>模块random

![](img/python基础/python15.png)

 ~~~
import random     
print(random.choice(range(1,3)))     
print(random.randrange(1,100,2))     
l = [1,2,3,4]  
random.shuffle(l);  
print(l)     
print(random.uniform(1,10))     
#random.randint(1,100)  
 ~~~

## 七、Python运算

### 1.Python算术运算

​		+，-，*，/，%，幂运算**，整除//

### 2.python关系运算

​		==,!=,>,<,>=,<=,(注意Ture就是1)

### 3.Python赋值运算

​		=,+=,-=,*=,/=.%=,**=,//=

~~~
一次为多个变量赋值
x,y,z  = 1,2,3  
~~~

### 4.Python逻辑运算

and,or,not

~~~
x,y,z = 1,2,3     
print(y or z)    #2  
print(y and z)   #3  
~~~

短路与

~~~
def a():
	print('a')
    return True  
def b():    
	print('b')
    return False     
if b() and a():  
    print('end...')  
输出b  
~~~

### 5.python成员运算

  in，指定成员在序列中  not in，指定成员不在序列中  

~~~
s = 'Hello World!'
l = [1,'xx',3]
t = (5,'xx',7)

result = False

result = 'x' not in s
print(result)	#Ture

result = 1 in l
print(result)	#Ture

result = 5 in t
print(result)	#Ture

~~~

~~~
for x in s:
    print(x)

for x in l:
    print(x)

for x in t:
    print(x)

for x in range(10):
    print(x,end='')
 
~~~

### 6.python身份运算

​	is,两个对象是一个对象  

​	is not，两个对象不是一个对象  

1> 可变对象和不可变对象

​	可变对象是指对象的值可以被修改。

​	不可变对象是指对象的值不可以被修改。

​	Python中的可变对象有列表、字典、自定义类创建的对象

​	Python中不可变对象有数字、字符串、元组。
~~~ 
a = 100  
print(id(a))

t = (1,2,3)  
# t[1] = 3   #错误

l = [1,2,3]  
l[1] = 5  
print(l)  
~~~
2> is和==区别

is比较的对象的地址（或引用），==比较的对象内容

~~~
#不可变类型
a = 100
b = 100

print(a is b)	#True
print(a == b)	#True
print(id(a))	#140724938632944
print(id(b))	#140724938632944

~~~

~~~
#可变类型
list1 = [1,2,3]
list2 = [1,2,3]

print(id(list1))		#1512773083784
print(id(list2))		#1512773083848

print(list1 is list2)	#False
print(list1 == list2)	#True

~~~

### 7.Python位运算

​	&，|，异或^,非~,<<，>>

 

## 八、序列综述

### 1.序列简介

​		序列包括：字符串、列表、元组

​		序列包含一些有序的元素，可以通过下标索引来访问；或者切片（开始下标和结束标志）来访问。例如：

~~~
  s = '123'  
  print(s[0])  
  print(s[0:2])  
  print(len(s))  
~~~

### 2.序列操作符

1> 成员操作符（in，not in）

2> 连接操作符（+）

~~~
s1 = '123'
s2 = 'lihai'
s = s1 + s2
print(s)
~~~

~~~
name = 'chensen'
age = 22
msg = name + str(age)		#注意类型必须相同
print(msg)
~~~

3> 重复操作符(*)

~~~
t1 = ('haha','lihai')
t = t1 * 2
print(t)			# ('haha', 'lihai', 'haha', 'lihai')
~~~

4> 切片操作符（[],[:],[::]）

​	序列索引范围是

​		① 正索引：[0，len(seq)-1]

​		② 负索引：[-1，-len(seq)]，-1就是最后一个

  	切片范围：[0:len(seq)]

~~~
l = [1,2,3,4]
print(l[-2:])		#[3,4]
print(l[:])			#[1,2,3,4]
print(l[-4:])		#[1,2,3,4]
~~~

~~~
range(10)是0到9
range(1,10)是1到9
range(1,10,2)，2为步长
~~~

~~~
切片中使用步长和在range中使用步长类似
l = [1,2,3,4]
print(l[::2])		#[1,3]
print(l[::-3])		#[4,1]
print(l[::-1])		#[4,3,2,1]
~~~

### 3.Python序列内建函数

1>序列工厂函数

​	① str(obj)，返回字符串的对象表示

 ~~~
class Person(object):
    def __init__(self, name,age):
        self.name = name
        self.age = age
    def __str__(self):
        return self.name + "," + str(self.age)
p1 = Person('chensen',22)
print(p1)
 ~~~

​	② list(iter)，根据迭代器返回一个列表

~~~
列表的构建可以直接使用list=[1,2,3,4]
或
list1 = list('asd')
print(list1)		# ['a', 's', 'd']

t = (1,2,3,4)
list2 = list(t)
print(list2)		# [1, 2, 3, 4]
~~~

​	③ tuple(iter) ，根据迭代器返回一个列表

​	元组的构建方式：

​		1.1使用一对括号（）表示空元组。

​		1.2对单个元组使用尾随逗号：a,或(a,)

​		1.3以逗号分隔项目：a,b,c or (a,b,c)

​		1.4使用tuple()内建:tuple()或tuple(iterable)

~~~
t = 1,2,3
t1 = (1,2,3)
t2 = 1,2,3,
~~~

2>操作函数

① enumerate(iter),返回具有索引的迭代项。

~~~
list1 = ['a',1,'b',2]
for i,x in enumerate(list1):
    print(i,x)

#0 a
#1 1
#2 b
#3 2
~~~

~~~
s = 'iloveu'
e = enumerate(s)
print(e.__next__())

#(0, 'i')
~~~

② len(seq)：获取序列长度

③ max(iter,key=None)

~~~
d1 = {'name':'Java','price':100}
d2 = {'name':'C','price':200}
d3 = {'name':'Python','price':10}

l1 = [d1,d2,d3]

a = max(l1,key = lambda x:x['name'])
print(a)
#{'name': 'Python', 'price': 10}

b = max(l1,key = lambda x: x['price'])
print(b)
#{'name': 'C', 'price': 200}
~~~

④ min(iter,key=None)

⑤ reversed(seq)：返回逆序迭代器

⑥ sorted(iterable,func=None,key=None,reverse=False)

​	iterable是可迭代类型。

​	Key：用列表元素的某个属性或函数进行作为关键字，有默认值，迭代集合中的一项。

​	Reverse：排序规则，reverse=True降序，有默认值

​	返回值：是一个经过排序的可迭代类型，与Iterable一样

~~~
list1 = [1,5,8,3,84,65,99,132]
print(sorted(list1))
print(sorted(list1,reverse=True))

#[1, 3, 5, 8, 65, 84, 99, 132]
#[132, 99, 84, 65, 8, 5, 3, 1]
~~~

~~~
list2 = [(3,'cat'),(1,'bag'),(2,'apple')]

print(sorted(list2,key = lambda x : x[0]))
print(sorted(list2,key = lambda x : x[1]))
#[(1, 'bag'), (2, 'apple'), (3, 'cat')]
#[(2, 'apple'), (1, 'bag'), (3, 'cat')]
~~~

⑦ sum(seq,init=0)

~~~
list1 = [1,2,3]
print(sum(list1,100))
#106
~~~

⑧ zip([it0,it1,……itN])

​		接受一系列可迭代对象作为参数，将对象中对应的元素打包成一个个tuple（元组），然后返回由这些tuples组成的list（列表）

​		若传入的参数的长度不等，则返回list的长度和参数中长度最短的对象相同

~~~
x = [1,2,3]
y = [7,8,9]
z = [5,80,55]

xyz = zip(x,y,z)
print(list(xyz))
#[(1, 7, 5), (2, 8, 80), (3, 9, 55)]
~~~

~~~
x = [1,2,3]
y = [7,8,9,10]

xy = zip(x,y)
print(list(xy))
#[(1, 7), (2, 8), (3, 9)]
~~~

~~~
#zip()与*操作符一起可以用来unzip一个列表。就是变回来
x = [1,2,3]
y = [7,8,9]
z = [5,80,55]

xyz = zip(x,y,z)
u = zip(*xyz)
print(list(u))
#[(1, 2, 3), (7, 8, 9), (5, 80, 55)]
~~~

## 九、Python字符串

### 1.Python字符串简介

1>字符串的创建

​		可以通过单引号，双引号，三引号（'''）来创建一个字符串。单引号和双引号意义相同，三引号一般用来创建大段的字符串内容

2>获得字符和子串：通过索引和子串

3>单引号双引号嵌套使用

~~~
s1 = "hello 'cs'!!!"
print(s1)
#hello 'cs'!!!

s2 = 'hello "cs"!!!'
print(s2)
#hello "cs"!!!
~~~

4>关于字符类型。Python中没有专门的字符类型，单个的字符使用单引号或双引号括起来，就是字符类型。

5> Python中字符串是不可变类型，不能被修改

### 2.Python转义字符

~~~
\,在行位，表示续行
\a，响铃
\000，空
\v，纵向制表符	\r换行
\t，横向制表符	\f换页
\\,\’,\”
\b,\n
\oyy,八进制数
\xyy,十六进制
\other,其他字符以普通格式输出

~~~

~~~
s1 = 'aaaaaaaaaaaa'\
     'bbbbbbbbbbbb'\
     'cccccccccccccccc'
print(s1)

~~~

### 3.字符串运算符

~~~
+，字符串连接
[]索引获取字符
in，not in，成员运算符
%，格式化字符串
*，重复输出字符串
[:]截取字符串中的一部分
r/R，原始字符串，不进行转义（raw）

~~~

~~~
print(R'C:\www\baidu\n\com')
print(r'C:\www\baidu\n\com')
print('name = %s,age=%d'%('cs',22))

~~~

### 4. Python字符串格式化

1>格式化指令

| %c，格式化字符及其ASCII码      | %s，格式化字符串                        |
| ------------------------------ | --------------------------------------- |
| %d，格式化整数                 | %u，格式化无符号整型                    |
| %o，格式化无符号八进制数       | %x，格式化无符号十六进制                |
| %X，格式化无符号十六进制(大写) | %f,格式化浮点数字，可指定小数点后的精度 |
| %e，用科学计数法格式化浮点数   | %E，作用同%e                            |
| %g，%f和%e的简写               | %G，%f和%E的简写                        |

2>辅助指令

| *，定义宽度或者小数点精度                                    | -，用作左对齐                              |
| ------------------------------------------------------------ | ------------------------------------------ |
| +，在正数前面显示加号（+）                                   | ，在正数前面显示空格                       |
| #，在八进制前面显示零（‘0o’），在十六进制前面显示“0x”或“0X”（取决于用的是x还是X） | 0，显示的数字前面填充‘0’，而不是默认的空格 |
| %，’%%’输出一个单一的%                                       | (var)，映射变量（字典参数）                |
| m.n.  m是显示的最小总宽度，n是小数点后的位数（如果可用）     |                                            |

~~~
a = 1000
print('%#o'%a)  #0o1750
print('%#x'%a)  #0x3e8
print('%#X'%a)	#0X3E8

print('%4.2e'%0.314)	#3.14e-01
print('%08.3f'%0.314)   #0000.314

print('%+d'%100)	#+100
print('%100')       #%100
print('%s%d'%('%',10))   #%10 
~~~

### 5. Python字符串内建函数

1>  capitalize()

​		将字符串的第一个字符转换为大写

~~~
s = 'asd'
s1 = s.capitalize()
print(s1)

~~~

2>  center(width, fillchar)

​		返回一个指定的宽度width居中的字符串，fillchar为填充的字符，默认为空格。如果width小于或等于len(s)则返回原始字符串。

~~~
s = 'asd'
s1 = s.center(10,'#')
print(s1)
输出###asd####
~~~

3>  count(str,beg=0,end=len(string))

​		返回str在string里面出现的次数，如果beg或者end指定则返回指定范围内str出现的次数

~~~
s = 'this is a string'
print(s.count('s',7))		#7表示从索引7开 始 
~~~

4>  endswith(suffix,beg=0,end=len(string))

​		检查字符串是否以obj结束，如果beg或者end指定则检查指定的范围内是否以obj结束，如果是，返回True，否则返回False。

5>  expandtabs(tabsize=8)

​		把字符串string中的tab符号转为空格，tab符号默认的空格数是8

~~~
s = 'hello\tworld'
print(s)	#hello	world
print(s.expandtabs(2))	#hello world
~~~

6>  find(str,beg=0,end=len(string))

​		检测str是否包含在字符串中，如果beg和end指定范围，则检查是否包含在指定范围内，如果是返回开始的索引值，否则返回-1。

7>  index(str,beg=0,end=len(string))

​		跟find()方法一样，只不过如果str不在字符串中会报一个异常。

8>  isalnum()

​		如果字符串至少有一个字符并且所有字符都是字母或数字则返回True，否则返回False。

~~~
s = 'asd123'
s1 = 'asdqwe!1'
print(s.isalnum())	#True
print(s1.isalnum())	#False
~~~

9>  istitle()

​		如果字符串是标题化的（见title()）则返回True，否则返回False。

~~~
s = 'Hello world'
s1 = 'hello world'
s2 = 'Hello World'
print(s.istitle())	#False
print(s1.istitle())	#False
print(s2.istitle())	#True
~~~

10> join(seq)

​		以指定字符串作为分隔符，将seq中所有元素（的字符串表示）合并为一个新的字符串

~~~
l = ['asd','123']
print('#'.join(l))
输出asd#123
~~~

11> ljust(width[,fillchar])，对应于rjust(width[,fillchar])

​		返回一个原字符串左对齐，并使用fillchar填充至长度width的新字符串，fillchar默认为空格。

 ~~~
s = 'hello'
print(s.ljust(20,'#'))
print(s.rjust(20,'#'))
输出
hello###############
###############hello
 ~~~

12> maketrans()

​		创建字符串映射的转换表，对于接受两个参数的最简单的调用方式，第一个参数是字符串，表示需要转换的字符，第二个参数也是字符串表示转化的目标

~~~
instr = 'abc'
outstr = '123'
str_trantab = str.maketrans(instr,outstr)
str1 = 'Black Jack'
print(str1.translate(str_trantab))
#Bl13k J13k
~~~

13> split(str=””,num=string.count(str))

​		num=string.count(str)以str为分隔符截取字符串，如果num有指定值，则仅截取num个字符串

~~~
s = 'name=cs;age=22;email=cs;sex=nan'
print(s.split(';'))
print(s.split(';',2))
输出
['name=cs', 'age=22', 'email=cs', 'sex=nan']
['name=cs', 'age=22', 'email=cs;sex=nan']
~~~

## 十、Python数据结构

### 1.Python列表简介

1>列表元素的类型可以是任意的，可以是相同类型，也可以是不同类型，大部分情况是相同的。

2>列表可以通过索引，切片的方式访问其元素

3>列表串联操作，使用+

~~~
l1 = [1,2,3]
l2 = list('abc')
print(l1+l2)
#[1, 2, 3, 'a', 'b', 'c']
~~~

4>列表是可变的，其内容可以被修改

5>可以改变列表大小

~~~
l1 = [1,2,3,4,5]
l1[0:2] = []
print(l1)
输出[3, 4, 5]
~~~

6>  可以用len函数，获得列表长度

7>  列表可以嵌套，类似二维数组

~~~
row1 = [1,2,3]
row2 = [4,5,6]

table = [row1,row2]
print(table)
print(table[0][2])
print(table[1][1])

输出
[[1, 2, 3], [4, 5, 6]]
3
5
#遍历
for i in table:
	for j in i:
		print(j)
~~~

### 2.Python列表的方法

1>list.append(x),将项目添加到列表的末尾。

2>list.extend(L),通过添加另外一个列表来扩展列表

3>list.insert(I,x),在给定位置插入项目，i参数的前面

4>list.remove(x),从列表中删除值为x的第一个项目

5>list.pop([i]),删除列表中给定位置的项目，并返回。list.pop()删除顶部

6>list.clear()从列表中删除所有项目。相当于del a[:].

7>list.index(x),返回值为x的第一个项目的列表的索引

8>list.count(x),返回x出现在列表中的次数

9>list.sort(key=None,reverse=False)排序列表中的项

~~~
l1 = [1,5,99,86,74,96,2,71]
l1.sort()
print(l1)
l1.sort(reverse=True)
print(l1)
输出
[1, 2, 5, 71, 74, 86, 96, 99]
[99, 96, 86, 74, 71, 5, 2, 1]
~~~

**sort 与 sorted 区别：**

​		sort 是应用在 list 上的方法，属于列表的成员方法，sorted 可以对所有可迭代的对象进行排序操作。  list 的 sort 方法返回的是对已经存在的列表进行操作，而内建函数 sorted 方法返回的是一个新的 list，而不是在原来的基础上进行的操作。  sort使用方法为ls.sort()，而sorted使用方法为sorted(ls)  

10>list.reverse(),列表中的元素按位置反转。

### 3.python列表推导式

1>列表推导式的概念

​		列表推导式提供一个生成列表的简洁方法

​		列表推导式由一对方括号组成，方括号包含一个表达式，其后跟随一个for子句，然后是零个或多个for或if子句。结果将是一个新的列表，其值来自将表达式在其后的for和if子句的上下文中求值得到的结果。

~~~
表达式为一个元组
list = [(x,y) for x in [1,2,3] for y in [7,8,9] if x != y]
print(list)
list = [(x,y) for x in [1,2,3] for y in [1,8,9] if x != y]
print(list)
输出
[(1, 7), (1, 8), (1, 9), (2, 7), (2, 8), (2, 9), (3, 7), (3, 8), (3, 9)]
[(1, 8), (1, 9), (2, 1), (2, 8), (2, 9), (3, 1), (3, 8), (3, 9)]

~~~

~~~
list = [2 * x + 1 for x in range(10)]
print(list)
输出
[1, 3, 5, 7, 9, 11, 13, 15, 17, 19]
~~~

~~~
list = []
for x in range(10):
    list.append(x)
print(list)
print(x)
输出
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
9
x还有值，如果使用上边，则不会
~~~

### 4.Python元组

1>定义元组

~~~
t = 1,2,3  
t = (1,2,3)  
print(t[0])  
~~~

2>访问元组

3>元组可以嵌套

~~~
t = ((1,'tom'),(2,'kite'),(3,'rose'))
print(t[0])
print(t[0][1])
输出
(1, 'tom')
tom
~~~

4>元组是不可变的

~~~
t = (1,2,3)
t[0] = 20		#错误
~~~

5>元组可以包含可变对象

嵌套元组里面的内容可以是可变的

~~~
t = ([1,2,3],[4,5,6])
t[0][0] = 10
print(t)
输出
([10, 2, 3], [4, 5, 6])
~~~

6>元组方法

​	①  tuple.count(x)计算某个元素的个数

​	②  tuple.index(x)，第一次出现某个元素的索引

7>元组和列表的区别

​	①  元组是不可变的，通常包含各种各样的元素，这些元素可以通过索引，切片访问

​	②  列表是可变的，它们的元素通常是相同类型，并通过迭代列表来访问

### 5.Python集合

1>创建集合

​	①  大括号字面量

​	②  set()函数

~~~
s1 = {1,2,3}
print(s1)
s2 = set('hello')
print(s2)
输出
{1, 2, 3}
{'l', 'e', 'h', 'o'}
~~~

2>集合的特点

​	元素不能重复，元素无顺序

3>集合常用方法

​	①  s.add(x)

​	②  s.remove(x)

​	③  s.pop()

​		**会按照hash值排序 然后删除排序好的最左边一个**

~~~
s = {43,54,2,67}
s.pop()
print(s)
输出
{2, 43, 54} 
~~~

​	④  s.clear()

~~~
s = {43,54,2,67}
s.clear()
print(s)
输出
set()
~~~

​	⑤  s.update(x)，合并两个集合，重复元素只会出现一次，**注意与add区别**

~~~
s = {43,54,2,67}
s.add('hello')
s.update('world')
print(s)
输出
{'w', 2, 67, 'd', 43, 'r', 54, 'o', 'l', 'hello'}
~~~

4>集合操作

​	①  difference(-),在a里面但不在b里面

​	②  intersection(&)，既在a里面又在b里面

​	③  union(|)，在a里面或者在b里面

​	④  symmetric_difference(^)，在a或者b里面，但不同时在两个里面

~~~
s1 = {1,2,3,4,5}
s2 = {3,4,5,6,7}
print(s1 - s2)	#{1, 2}
print(s1.difference(s2))	#{1, 2}

print(s1 & s2)	#{3, 4, 5}
print(s1.intersection(s2))	#{3, 4, 5}

print(s1 | s2)	#{1, 2, 3, 4, 5, 6, 7}
print(s1.union(s2))		#{1, 2, 3, 4, 5, 6, 7}

print(s1 ^ s2)	#{1, 2, 6, 7}
print(s1.symmetric_difference(s2))	#{1, 2, 6, 7}
~~~

### 6.Python字典

1>字典特点

​	①  key:value的键值对

​	②  key不能重复，value可以重复

2>创建方法

​	①  大括号字面量

​	②  dict()函数

~~~
s1 = {'name':'cs','age':20}
print(s1)
s1.clear()
print(s1)

s2 = dict([('name','cs'),('age',20)])
print(s2)
输出
{'name': 'cs', 'age': 20}
{}
{'name': 'cs', 'age': 20}
~~~

3>访问字典

​	可以通过key访问value，例字典[‘key’]

4>添加item

~~~
s1 = {}
print(s1)
s1['name'] = 'ch'
print(s1)
输出
{}
{'name': 'ch'}
~~~

5>常用方法

​	get(x)通过key获得value。例：字典.get(key)

​	items()：获得所有的items。

​	keys()：获得所有keys。

​	values():获得所有的values

~~~
s1 = {'name':'cs','age':20,1:2}
print(s1)
print(s1.get(1))
print(s1.get('name'))
print(s1.keys())
print(s1.items())
print(s1.values())
输出
{'name': 'cs', 'age': 20, 1: 2}
2
cs
dict_keys(['name', 'age', 1])
dict_items([('name', 'cs'), ('age', 20), (1, 2)])
dict_values(['cs', 20, 2])
~~~

6>遍历方法

~~~
s1 = {'name':'cs','age':20,1:2}
for x in s1:
    print(x,end='-')
    print(s1[x])

print()
for x in s1.keys():
    print(x,'-',s1.get(x))

print()
for k,v in s1.items():
    print(k,v)
输出
name-cs
age-20
1-2

name - cs
age - 20
1 - 2

name cs
age 20
1	2 
~~~

7>字典推导式

和列表推导式类似，是快速生成字典的方法。大括号里面前面是一个表达式，后面是若单个循环或者条件判断，最后的到一个字典

~~~
values = ['cs','zs','ls']
d = {str(k)+'hhh' : values[k] for k in range(3)}
print(d)
输出
{'0hhh': 'cs', '1hhh': 'zs', '2hhh': 'ls'}
~~~

### 7.Python循环技巧

1>使用items方法遍历字典

2>enumerate()函数获得序列索引

~~~
list1 = ['a',1,'b',2]
for i,x in enumerate(list1):
    print(i,x)
输出
0 a
1 1
2 b
3 2
~~~

3>使用zip()函数遍历两个或者多个序列

~~~
x = [1,2,3]
y = [7,8,9]
z = [5,80,55]
xyz = zip(x,y,z)
print(list(xyz))

for x,y,z in zip(x,y,z):
    print(x,y,z)
输出
[(1, 7, 5), (2, 8, 80), (3, 9, 55)]
1 7 5
2 8 80
3 9 55 
~~~

4>使用sorted()函数排序

~~~
list1 = [1,5,8,3,84,65,99,132]

for x in sorted(list1):
    print(x,end=',')
输出
1,3,5,8,65,84,99,132,
~~~

## 十一、Python流程控制

### 1.Python分支语句

1>条件判断语法

~~~
if condition_1:
	statement_block_1
elif condition_2:
	statement_block_2
else:
	statement_block_3
~~~

2>注意

①  每个条件后面都有冒号，表示接下来是满足条件后要执行的语句块

②  使用缩进来划分语句块，相同缩进数的语句在一起组成一个语句块

③  在Python中非0，非None，非空即为真

④  在Python中没有switch-case语句

~~~
p = None

if p:
    print('p')
else:
    print('x')
输出 x
~~~

~~~
a,b = 100,2

if a > b:
    m = a
else:
    m = b
print(m)
输出 100
~~~

### 2.Python循环语句while

1>while循环语法

~~~
while 循环条件:
	语句
~~~

注意：在Python中没有do-while循环

~~~
import time

while True:
    print('loop...')
    time.sleep(1)		#ctrl+q退出进程
~~~

~~~
from time import sleep

while True:
    print('loop...')
    sleep(10)
~~~

~~~
x = 50
while True:
    n = int(input('请输入一个数：'))
    if x == n:
        print('恭喜你猜对了')
        break
    elif x < n:
        print('猜大了')
        continue
    elif x > n:
        print('猜小了')
        continue
~~~

### 3.Python range函数

​	Range函数使用一个范围函数，可以指定一个遍历范围：

~~~
range(stop)指定结束，0到stop-1
range(start,stop)指定开始和结束
range(start,stop,step)指定开始，结束和步长
~~~

### 4.Python for循环

1>for循环语法

~~~
for <variable> in <sequence>:
	<statements>
else:
	<statement>

~~~

~~~
list = []

for x in list:
    print(x)
else:
    print('no')
输出no
~~~

2>带索引的range

~~~
list = ['java','c','python']

for x in range(len(list)):
    print('%d,%s' % (x,list[x]))
输出
0,java
1,c
2,python

或
list = ['java','c','python']

for i,x in enumerate(list):
    print(i,x)
~~~



## 十二、Python迭代器和生成器

### 1.Python迭代器

1>iter函数和next函数

​	使用iter(序列)函数可以获得一个迭代器，使用next(迭代器)函数可以获得迭代器中的下一条数据。

~~~
s = 'java'
list = ['java','c','python']
t = ('java','c','python')
it1 = iter(s)
it2 = iter(list)
it3 = iter(t)
print(type(it1))
print(type(it2))
print(type(it3))

print(next(it1))
print(next(it2))
print(next(it3))

print(next(it1))
print(next(it2))
print(next(it3))
输出
<class 'str_iterator'>
<class 'list_iterator'>
<class 'tuple_iterator'>
j
java
java
a
c
c
~~~

2>StopIteration函数

​	当迭代器中没有数据时，就会抛出一个StopIteration异常，利用该异常判断迭代结束。

~~~
list = ['java','c','python']
it1 = iter(list)

while True:
    try:
        print(next(it1))
    except StopIteration as si:
        print('迭代结束')
        break

~~~

3>迭代字典

~~~
dict = {'name':'cs','age':22,'sex':'nan'}

it = iter(dict)

for x in it:
    v = dict[x]
    print(x,v)
输出
name cs
age 22
sex nan
~~~

4>使用for循环迭代
~~~
s = 'hello world'
it = iter(s)

for x in it:
    print(x,end=',')
输出
h,e,l,l,o, ,w,o,r,l,d,
~~~

### 2.Python生成器

1>什么是生成器

​		如果一个函数里面使用了yeild关键字，那么这个函数就是一个生成器（可以让函数执行停下来，下一次调用接着执行）

​		生成器是一种推导逻辑，调用生成器返回迭代器

2>生成器的创建方法

​	①  改列表推导式[]为()

~~~
g = (2 *x for x in range(3))
print(next(g))
print(next(g))
print(next(g))
输出
0
2
4
~~~

②  使用带有yield关键字的函数

~~~
def f():
    print('step1')
    yield 1
    print('step2')
    yield 2
    print('step3')
    yield 3

g = f()

next(g)
print(next(g))
print(next(g))
输出
step1
step2
2
step3
3
~~~

3>斐波那契数列

~~~
def fib(n):
    a,b,counter = 0,1,0
    while True:
        if counter > n:
            break
        a,b = b,a + b			#不是a=b，b=a+b
        yield a
        counter += 1

g = fib(10)

for x in g:
    print(x,end=' ')			# 1 1 2 3 5 8 13 21 34 55 89

~~~

~~~
def fib(n):
    a,b,counter = 0,1,0
    while True:
        if counter > n:
            break
        a,b = b,a + b
        print(a,end=' ')
        counter += 1

fib(10)
#1 1 2 3 5 8 13 21 34 55 89
~~~

## 十三、Python函数

### (一)Python函数简介

1>什么是函数

​	具有独立单元的功能代码。函数为了实现代码重用

2>如何定义函数

~~~
def functionname(params):
	代码块
	[return 值]		#[return]
~~~

### (二)Python函数的参数

1>必需参数

​	指调用函数时，必需传递的参数，如果不传递参数，调用会发生错误。

2>关键字参数

​	可以根据参数的名称来为参数赋值，可以不按照参数的顺序。
~~~
def about(name,age,site):
    print(name,age,site)

about(age=12,name='cs',site='12a3')

输出
cs 12 12a3
~~~


3>默认参数

​	可以在定义函数时为参数指定默认值，调用函数时可以不为参数赋值，使用默认值。

~~~
def about(name='cs',age=None,site=None):
    print(name,age,site)

about(12,'12a3')

about(age=12,site='123as')
输出
12 12a3 None
cs 12 123as
~~~

4>不定长参数

​	可以在参数前面添加一个星号（*），表示该参数是不定长参数

~~~
def f3(*args):
    for x in args:
        print(x,end=" ")

f3(1,23,3)
输出1 23 3
~~~

5>lambda表达式，匿名函数

~~~
语法：
lambda [arg1 [,arg2,……argn]]：expression
lambda表达式返回一个函数，可以像函数一样调用。
~~~

~~~
f = lambda a,b:a+b
print(f(1,3))
输出4 
~~~

### (三)Python函数递归

~~~
n = 10
def f():
    global n
    print(n);
    n -= 1
    if(n > 0):
        f()
    else:
        return
f()
~~~

~~~
阶乘
def f(n):
    if n < 0:
        return 'cuowu'
    elif n==1 or n == 0:
        return 1
    else:
        return n * f(n-1)
print(f(3))
~~~

~~~
斐波那契数列1：
def fib(n):
    a,b,counter = 0,1,0
    while True:
        if counter > n:
            break
        a,b = b,a + b
        yield a
        counter += 1
g = fib(10)
for x in g:
    print(x,end=' ')
    
斐波那契数列2： 
def fib(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fib(n-1) + fib(n-2)

for x in range(1,11):
    print(fib(x),end=' ')

~~~

### (四)Python变量的作用域

1.变量作用域

（1）L(Local)，局部作用域

（2）E(Enclosing),闭包函数外的函数中

（3）G(Global),全局作用域

（4）B(Built-in),内建作用域

~~~
# Enclosing闭包
def outer():
    number = 100
    def innter():
        print(number)
    innter()
    print(number)
outer()
~~~

~~~
#Built-in内建
import math
print(math.pi) 
~~~

2.变量的查找规则

局部->闭包->全局->内建

3.Python代码块不会引入新的作用域（除def、class、lambda都不会引入）

~~~
if True:
    a = 100
    print(a)
print(a)
~~~

~~~
for x in range(1):
    print(x)

print(x)
~~~

4.局部变量和全局变量

​	定义在函数内部的变量拥有一个局部作用域，定义在函数外部的拥有全局作用域。

​	局部变量只能在其被声明的函数内部访问，而全局变量可以在整个程序范围内访问。

5.闭包

​		如果在一个内部函数里，对在外部作用域（但不是在全局作用域）的变量进行引用，那么内部函数就被认为是闭包（closure）

​		定义在外部函数内的但由内部函数引用或者使用的变量被称为自由变量。闭包在函数式编程中是一个重要的概念。

​		闭包（closure），是引用了自由变量的函数。这个被引用的自由变量将和这个函数一同存在，即使已经离开了创造它的环境也不例外。

​		闭包和函数调用没什么相关，而是关于使用定义在其他作用域的变量。

~~~
def line_conf():
    b = 15
    def line(x):
        return 2 * x + b
    return line

my_line = line_conf()
print(my_line(3))
~~~

​		line函数中引用了高层级的变量b，但b信息存在于line的定义之外，称b为line的环境变量。事实上，line作为line_conf的返回值时，line已经包括了b的取值（尽管b并不隶属于line）。

​		一个函数和它的环境变量合在一起，就构成了一个闭包。在Python中，所谓的闭包是一个包含有环境变量取值的函数对象。

~~~
def counter(start_at = 0):
    count = [start_at]
    def incr():
        count[0] += 1
        return count[0]
    return incr

count = counter(5)
print(count())
print(counter(2)())
输出
6
3
~~~

6.global和nonlocal关键字

​	当内部作用域想修改外部作用域的变量时，就要用到global和nonlocal关键字了。

​	global是局部修改全局，nonlocal是修改嵌套的闭包作用域。

~~~
m = 100
def fun():
    global m
    m = 40

fun()
print(m)
~~~

~~~
def outer():
    m = 10
    def inner():
        nonlocal m
        m -= 1
        print(m)
    inner()

outer()

~~~

7.lambda作用域

Lambda表达式本质上是一个匿名函数，所有变量的作用域和函数相同。

## 十四、Python模块和包

### （一）Python模块简介

1.为什么要使用模块

​		初学者都是在命令行交互环境学习Python，但是要想把代码保存下来，必须使用文件。模块是组织Python代码的一种逻辑方式，文件是模块的物理实现。

​		模块可以实现代码的重用，一个模块需要另一个模块时，可以导入（import）

2.模块的命名空间

​		每个模块都有自己的命名空间，例如：系统math模块中有一个fabs绝对值函数，访问该函数可以使用math.fabs()这种方式。如果你自己也创建了一个模块叫foo，里面也有一个fabs函数，可以使用foo.fabs()这种方式来访问。通过模块名称可以区分名称空间。

3.模块的搜索路径

​		导入一个模块，会在一定的搜索路径中进行搜索，如果找到了就导入，否则，会抛出异常。默认的搜索路径是在编译或安装时指定的。默认的搜索路径保存在系统环境变量PYTHONPATH中。

​		在程序运行期间可以同系统模块sys.path进行访问。sys.path是一个列表，可以根据需要，使用append添加自己的模块搜索路径。

​		使用sys.modules可以找到当前导入了哪些模块和他们来自什么地方。

~~~
命令行
import sys
sys.path查看
sys.path.append(r’路径’)，r就是使用原生路径，不使用转义字符 
~~~

### （二）Python导入模块

~~~
import m1
import m2
……
或
import m1,m2[,……mn]
~~~

~~~
可以使用from-import语句导入指定的模块属性。语法：
from module import name1,name2[,name3……,nameN]
~~~

~~~
可以把导入的模块重新命名，使用as关键字
import Tkinter as tk
from cgi import FieldStorage as form
~~~

### （三）Python模块特性

1.导入模块会被执行

​	当导入模块时，模块会被执行

​	模块可以被导入多次，但是只能执行一次。

~~~
导入时执行
import m1	

m1.py文件
print('hello')
~~~

~~~
导入时不执行
import m1	


m1.py文件
def main():
    print('hello')

if __name__ == '__main__':
    main()
~~~

2.模块的内建函数

​	import(),import语句会调用__import__()函数，可以重写该函数实现一些特点目的。

​	globals()返回全局名称空间字典

​	locals()返回局部名称空间字典。

​	reload()可以重新导入一个已经加载的模块。

### （四）Python包管理

1.什么是包

​		当一个项目中模块非常多的时候，可以增加一些逻辑，使用包来管理模块。包对应系统中的文件夹。包可以包含子包和模块，就像文件夹可以有子文件夹和文件。

​		注意：包中有一个特殊文件“\__init__.py”，当导入包的时候这个文件会被执行。

2.使用import导入包

~~~
语法：
import p.subp
~~~

使用from-import导入包

~~~
语法：
from p.m import x
~~~

~~~
目录结构
com.baidu.test-hello.py
com.baidu.utils-WebUtil.py
com.baidu.entity-MyUrl.py

WebUtil.py文件
def sync(url):
    print(url)


MyUrl.py文件
GLOBAL_URL = 'http://qwe'


hello.py文件
import sys
sys.path.append(r'E:\Workspace\PythonWork')

import com.baidu.utils.WebUtil
com.baidu.utils.WebUtil.sync('http://127')

from com.baidu.utils import WebUtil
WebUtil.sync('http://127')

from com.baidu.utils.WebUtil import sync
sync('http://sad127')


from com.baidu.entity.MyUrl import *
print(GLOBAL_URL)
~~~



## 十五、Python输入输出

### （一）Python文件对象

1.文件对象

​		文件对象可以是磁盘上的一个文件，也可以是一个socket连接，还可以是一个web http连接，只要获得了文件对象file，就可以对其进行读写操作。

2.open函数

~~~
f = open(file_name,access_mode=’r’,encoding=’utf-8’)
~~~

3.文件读写

~~~
f.read()全部读		f.readline()	f.read(2)读两个字节
f.write()
~~~

~~~
目录结构：
PythonWork-text.txt
PythonWork.com.baidu.utils.FileUtil.py

def file_open():
    f = open('text.txt','r',encoding='utf-8')
    print(f.read(2))
    for line in f:
        print(line)

def file_append():
    f = open('text.txt','a')
    f.write('asdsadasd')

def main():
    file_open()

if __name__ == '__main__':
	main()
~~~

4.文件内移动

~~~
f.seek(offset)
~~~

5.异常处理

~~~
try-except-finally
with open as f
~~~

~~~
def file_close():
    try:
        f = open('text.txt')
        f.seek(2)
        print(f.read())
    except Exception as e:
        print(e)
    finally:
        if f:
        	f.close()
    print(f.closed)


def main():
    file_close()

if __name__ == '__main__':
    main()
~~~

~~~
#这样也可以关闭
def file_close():
    with open('text.txt') as f:
        print(f.read())
    print(f.closed)


def main():
    file_close()

if __name__ == '__main__':
    main()
~~~

### （二）Python文件打开方式

| 访 问 模 式 | 说明                                                         |
| :------: | :----------------------------------------------------------- |
|    r     | 以只读方式打开文件。文件的指针将会放在文件的开头。这是默认模式。 |
|    w     | 打开一个文件只用于写入。如果该文件已存在则将其覆盖。如果该文件不存在，创建新文件。 |
|    a     | 打开一个文件用于追加。如果该文件已存在，文件指针将会放在文件的结尾。也就是说，新的内容将会被写入到已有内容之后。如果该文件不存在，创建新文件进行写入。 |
|    rb    | 以二进制格式打开一个文件用于只读。文件指针将会放在文件的开头。这是默认模式。 |
|    wb    | 以二进制格式打开一个文件只用于写入。如果该文件已存在则将其覆盖。如果该文件不存在，创建新文件。 |
|    ab    | 以二进制格式打开一个文件用于追加。如果该文件已存在，文件指针将会放在文件的结尾。也就是说，新的内容将会被写入到已有内容之后。如果该文件不存在，创建新文件进行写入。 |
|    r+    | 打开一个文件用于读写。文件指针将会放在文件的开头。           |
|    w+    | 打开一个文件用于读写。如果该文件已存在则将其覆盖。如果该文件不存在，创建新文件。 |
|    a+    | 打开一个文件用于读写。如果该文件已存在，文件指针将会放在文件的结尾。文件打开时会是追加模式。如果该文件不存在，创建新文件用于读写。 |
|   rb+    | 以二进制格式打开一个文件用于读写。文件指针将会放在文件的开头。 |
|   wb+    | 以二进制格式打开一个文件用于读写。如果该文件已存在则将其覆盖。如果该文件不存在，创建新文件。 |
|   ab+    | 以二进制格式打开一个文件用于追加。如果该文件已存在，文件指针将会放在文件的结尾。如果该文件不存在，创建新文件用于读写。 |

~~~
def copy_image():
    with open('logo.png','rb') as rf:
        with open('test.png','wb') as wf:
            content = rf.read()
            wf.write(content)


def main():
    copy_image()

if __name__ == '__main__':
    main()

~~~

区别：

​	①  r只读，r+读写，不创建

​	②  w新建只写，w+新建读写，二者都可将文件内容清0。以w方式打开，不能读。

​	③  以a，a+方式打开文件，附加方式打开。a：附加写方式打开，a+：附加读写方式打开。

w+和r+区别：r+可读可写，若文件不存在报错。w+可读可写，文件不存在创建。

r+和a+区别：a+进行追加写，r+进行覆盖写。

 

## 十六、Python异常处理

### （一）Python异常和错误

1.什么是错误

​		错误是在编译期间出现的，常见的错误有两种情况：

​		①语法错误：代码不符合解释器或编译器的语法规则；

​		②逻辑错误：不完整或者不合法输入或者计算错误。

2.什么是异常

​		异常是在运行期出现，程序在运行期间出现问题，导致程序无法运行，常见的情况有：

​		①程序有逻辑或者算法错误。

​		②运行过程中计算机错误（内存不够或IO错误）

3.二者区别

​		错误是在编译期间出现的，异常是在运行期出现的，语法错误可以修改，逻辑错误很难发现和修改。

​		①  异常的产生，检查到错误或者解释器认为是异常，它将抛出这个异常。

​		②  异常处理，截获异常，忽略或者终止程序处理异常。

### （二）Python常见错误

1.SyntaxError，语法错误

2.ZeroDivisionError，被0除错误

3.IndexError

4.ValueError，比如将字符串转换为int型（int（str）），但str中不全是数字。

5.NameError,名字没有被定义。

6.FileNotFoundError，文件未找到错误

7.ModuleNotFoundError，ImportError，包或模块不存在

### （三）Python try-except

1.try-except语法：

~~~
try:
	代码块
	……
except IndexError as e:
	处理异常代码块

~~~

### （四）Python捕获多个异常

~~~
try:
	代码块
	……
except Exception1 as e1:
	处理异常代码块
except Exception1 as e2:
	处理异常代码块

~~~

### （五）Python try-finally结构 

 ~~~
try:
	代码块
	……
except IndexError as e:
	处理异常代码块
finally:
	不管是否有异常发生都会执行的代码块

注意：finally部分的代码块，不管是否有异常发生，都会执行，常用来释放资源。例如：打开的外部文件，数据库连接等。
 ~~~

### （六）Python raise assert

1.raise主动抛出异常

​		raise可以在一定条件下，主动抛出异常。

~~~
list = [1,2,3]
i = 10
if i >= len(list):
    raise IndexError
else:
    print(list[i])
~~~

2.assert断言

​		当assert函数中的表达式运算结果为False时，就会抛出一个AssertionError异常。

~~~
a = 101
assert(a == 101)

s = input('请输入年龄：')
age = int(s)
assert(age > 0)
print(age)
 
~~~

### （七）Python自定义异常

1.自定义异常

两步：①继承Exception，②重写init和str方法。

~~~
class MyException(Exception):
    def __init__(self, info):
        super().__init__(self)
        self.error_info = info
    def __str__(self):
        return '自定义异常' + self.error_info



try:
    print('code:')
    a = 10
    b = 2
    if a > b:
        raise MyException('error---')
except MyException as e:
    print(e)


输出
code:
自定义异常error---
~~~

## 十七、Python面向对象

### （一）Python类和对象 

~~~
class Person(object):
    def ride(self,b):
        b.run()

class Biycle(object):
    def run(self):
        print('run...')

p = Person()
b = Biycle()
p.ride(b)
输出
run...
~~~

### （二）Python创建类并实例化

创建类的语法

~~~
class ClassName(object):
	属性定义
	方法定义
~~~

### （三）Python构造方法

构造方法是一个特殊的方法，名称为init，作用是用来初始化实例变量。

Python不支持方法重载，也不支持构造方法重载

### （四）Python self关键字

1.self是指当前对象本身

​	谁调用该方法，当前对象就是谁。

2.在类里边的方法第一个参数必须是self

3.self其实是可以写成this的

4.self一般用来指定同名的实例变量与参数

### （五）Python类、实例、静态方法

1.静态方法

​	使用@staticmethod标识，可以不用实例化，直接通过类名调用。

注意：静态方法中没有self参数。

~~~
class Person(object):
    def getName():
        return 'cs'
    getName = staticmethod(getName)

print(Person.getName())


现在使用：
class Person(object):
    @staticmethod
    def getName():
        return 'cs'

print(Person.getName()) 
~~~

2.实例方法

​		必须实例化才能调用

​		静态方法不能访问实例变量，也不能访问类变量，python没有静态变量

3.类方法

​		类方法和静态方法类似，不能访问实例变量，能访问类变量。使用@classmethod标识，但是第一个参数必须是类本身cls。

~~~
class MyClass(object):
    cv = 1
    def __init__(self,v1,v2):
        self.v1 = v1
        self.v2 = v2

    @staticmethod
    def myStaticM1():
        print('myStaticM1')
        # print(self.v1)#不能调用实例变量
        # print(cv)	#不能调用类变量
		print(MyClass.cv)#可以访问

    @classmethod
    def myClassM1(cls):
        print('myClassM1')
        print(cls.cv)

MyClass.myStaticM1()
MyClass.myClassM1()

m = MyClass('10','20');
print(m.cv)
print(m.v1)
输出
myStaticM1
1
myClassM1
1
1
10

print(MyClass.cv)#可以访问
~~~

### （六）Python类属性、实例属性

1.类属性

​		是在方法外面声明的属性，可以通过类名称或者实例名称访问。

​		实例方法可以访问类属性。

2.实例属性

​		是在init方法中初始化的属性，叫做实例属性，必须实例化才能访问。

### （七）Python内存管理与析构方法

1.Python内存管理

​	①  Python内存管理是自动完成的

​	②  Python通过垃圾回收器来管理内存

​	③  实现原理是引用计数，引用计数为0，自动清除内存。

2.析构方法

​	析构方法__del__，当对象被从内存释放时，调用析构方法。

​	程序结束时或对象引用为空（对象为None）。

### （八）Python继承

1.继承的语法：支持多重继承。

~~~
class ClassName(父类,超类):
~~~

~~~
class Site(object):
    sid = 1001
    def __init__(self, name,age,score):
        self.name = name
        self.age = age
        self.score = score
    def about(self):
        print(self.name,self.age,self.score)

class SiteE(Site):
    pass

site = SiteE('asd',12,55)
site.about()

~~~

~~~
class Site(object):
    sid = 1001
    def __init__(self, name,age,score):
        self.name = name
        self.age = age
        self.score = score
    def about(self):
        print(self.name,self.age,self.score)

class SiteE(Site):
    def __init__(self):
        super().__init__('asd',12,55)

site = SiteE()
site.about()

~~~

### （九）Python方法覆盖

super关键字：调用父类的初始化方法super().\__init__()；调用父类的其他方法和属性。

 

### （十）Python接口和抽象类

1.抽象方法

 ~~~
class OpenClose(object):
    def open(self):
        pass
    def close(self):
        pass
 ~~~

2.抽象类

​		拥有一个或者多个抽象方法的类，叫做抽象类

​		抽象类不能实例化，只能作为子类继承。

~~~
import abc

class USB(metaclass = abc.ABCMeta):
    @abc.abstractmethod
    def read(self):
        pass
    def write(self):
        print('write')

class MyUSB(USB):
    def read(self):
        print('read')

myUsb = MyUSB()
myUsb.read()
myUsb.write()

~~~

3.接口

​		接口里面没有任何实现的方法，所有的方法都是抽象方法。

~~~
import abc

class USB(metaclass = abc.ABCMeta):
    @abc.abstractmethod
    def read(self):
        pass

    @abc.abstractmethod
    def write(self):
        pass

class MyUSB(USB):
    def read(self):
        print('read')
    def write(self):
        print('write')

myUsb = MyUSB()
myUsb.read()
myUsb.write()

或者
class OpenClose(object):
    def open(self):
        pass
    def close(self):
        pass
~~~

### （十一）Python类、实例的内建函数

1. issubclass(sub,sup)

   判断一个类是否是另一个类的子类

2. isinstance(obj,cls)

   判断一个对象是否是一个类的实例

3. 属性操作

   hasattr()、getattr()、setattr()、delattr()属性操作不限于类，只是在类中使用频繁。

   ~~~
   class Person(object):
       def __init__(self,name):
           self.name = name
   
   p = Person('tom')
   print(hasattr(p,"name"))
   print(getattr(p,'name'))
   setattr(p,'name','haha')
   print(p.name)
   
   delattr(p,'name')
   print(p.name)			#错误
   
   ~~~

4. dir显示模块/类/实例的内容

   ~~~
   class Person(object):
       pid = 1001
       def __init__(self,name):
           self.name = name
       def get_name(self):
           return self.name
   
   print(dir(Person))
   
   p = Person("cs")
   print(dir(p))
   注意dir(Person)没有'name'，而dir(p)中有
   ~~~

5. super()引用父类

6. vars(模块/类/实例/不写)

   和dir()类似，只是给定的对象参数必须有一个\__dict__属性。

   dir()和vars()的区别就是：dir()只打印属性，vars()则打印属性与属性的值。

   vars():函数以字典形式返回参数中每个成员的当前值，如果vars函数没有带参数,那么它会返回包含当前局部命名空间中所有成员的当前值的一个字典。

### （十二）Python组合关系

1. 概念

（1）   类和类之间的关系大的可以分为两种：继承和组合

（2）   组合又分为1:1，1：n，n:n

（3）   组合关系之依赖关系-参数传递

（4）   组合关系之关联关系-一个类包含另一个类

（5）   如何使用继承is a和组合has a 

----

~~~
class Author(object):
    def __init__(self,name,age):
        self.name = name
        self.age = age

class Course(object):
    def __init__(self,name,runtime,author):
        self.name = name
        self.runtime = runtime
        self.author = author

class Site(object):
    def __init__(self,name,address,courses):
        self.name = name
        self.address = address
        self.courses = courses

a = Author('cs',20)
py = Course('Python',100,a)
java = Course('Java',120,a)
s = Site('网易',
	'Http://123.132.212.45',[py,java])

print(s.address)
for x in s.courses:
    print(x.name,x.runtime,x.author.name)
输出
Http://123.132.212.45
Python 100 cs
Java 120 cs
~~~

### （十三）Python序列化和反序列化

1. 概念

（1）   对象序列化就是把对象持久保存成文件格式。

（2）   对象反序列化就是把对象从文件转换为对象。

（3）   Python提供了两个模块来实现序列化：cPickle和pickle。这两个模块功能是一样的，区别在于cPickle是c语言写的，速度快。pickle是纯Python写的，速度慢。使用pickle的dumps或者dump序列化。使用pickle的load方法反序列化。

（4）   不光是对象，像列表、字典都可以。

~~~
try:
    import cPickle as pickle
except ImportError as e:
    import pickle
    print(e)

class Person(object):
    def __init__(self,name,age):
        self.name = name
        self.age = age

p = Person('as',12)

with open('demo.data','wb') as f:
    b = pickle.dumps(p)
    f.write(b)
with open('demo.data','rb') as f1:
    p = pickle.load(f1)
    print(p.name)
    print(p.age)
 
~~~

### （十四）Python访问控制

1. 概念

（1）   Python没有真正的访问控制，只是通过变量名称来约定。

（2）   前面有一个下划线_foo是受保护的（自己和继承可以使用）。

（3）   前面有两个下划线__foo是私有的（自己可以使用）。

 ~~~
class Foo(object):
    a = 1
    _b = 2
    __c = 3
    def __init__(self,x,y,z):
        self.x = x
        self._y = y
        self.__z = z
    def m1(self):
        print('m1')
    def _m2(self):
        print('m2')
    def __m3(self):
        print('m3')

print(Foo.a)
print(Foo._b)
# print(Foo.__c)
print(Foo._Foo__c)

f = Foo(4,5,6)
# print(f.__c)
print(f._Foo__c)
print(f.x)
print(f._y)
# print(f.__z)
print(f._Foo__z)

f.m1()
f._m2()
# f.__m3()
f._Foo__m3()

注释内容是错误用法。

 ~~~

## 十七、Python GUI-tkinter

### （一）Python GUI简介 

1.tkinter库（python内置的库）

（1）tkinter提供了一个强大的，与平台无关的窗口工具包

（2）tkinter的主要优点是它的速度很快。

（3）虽然，在Tk8.5中得到了极大地改进，然而，tkinter界面让人觉得过时。不过GUI库还有更多其他的选择，你可能会对这些感兴趣。

~~~
from tkinter import *

class UIApplication(Frame):
    def __init__(self,master=None):
        Frame.__init__(self,master)
        self.pack()
        self.create_ui()
    def create_ui(self):
        self.lable = Label(self,text='我的GUI')
        self.lable.pack()


app = UIApplication()
app.master.title = 'Hello'
app.mainloop()
~~~

### （二）Python GUI按钮 和命令

~~~
from tkinter import *

class UIApplication(Frame):
    def __init__(self,master=None):
        Frame.__init__(self,master)
        self.pack()
        self.create_ui()

    def create_ui(self):
        self.lable = Label(self,text='我的GUI')
        self.lable.pack()
        self.quit_btn = Button(self,text='Quit',command=self.quit)
        self.quit_btn.pack()

        self.click_btn = Button(self,text='Click me',command=self.click)
        self.click_btn.pack()

    def click(self):
        print('click')


app = UIApplication()
app.master.title = 'Hello'
app.mainloop()

~~~

### （三）Python GUI输入框和提示框

~~~
from tkinter import *
import tkinter.messagebox as box

class UIApplication(Frame):
    def __init__(self,master=None):
        Frame.__init__(self,master)
        self.pack()
        self.create_ui()

    def create_ui(self):
        self.lable = Label(self,text='我的GUI')
        self.lable.pack()

        self.age_input = Entry(self)
        self.age_input.pack()

        self.btn_get = Button(self,text='get',command=self.get)
        self.btn_get.pack()

    def get(self):
        age = int(self.age_input.get())		#获得输入内容
        box._show('get age','age=%d' %age)	#显示提示框。


app = UIApplication()
app.master.title = 'Hello'
app.mainloop()
~~~

### （四）Python GUI复选按钮

 ~~~
from tkinter import *

class UIApplication(Frame):
    def __init__(self,master=None):
        Frame.__init__(self,master)
        self.pack()
        self.create_ui()

    def create_ui(self):
        self.lable = Label(self,text='我的GUI')
        self.lable.pack()

        self.check_var = BooleanVar()
        self.check_btn = Checkbutton(self,
			text='自动登录',variable=self.check_var,command=self.get)
        self.check_btn.pack()

    def get(self):
        if self.check_var.get() == 1:
            print('选中')
        else:
            print("未选中")

app = UIApplication()
app.master.title = 'Hello'
app.mainloop()

 ~~~

### （五）Python GUI单选按钮

~~~
from tkinter import *

class UIApplication(Frame):
    def __init__(self,master=None):
        Frame.__init__(self,master)
        self.pack()
        self.create_ui()

    def create_ui(self):
        self.lable = Label(self,text='我的GUI')
        self.lable.pack()

        self.var = IntVar()
        self.option1 = Radiobutton(self,text='option1',variable=self.var,
					value='1',command=self.get)
        self.option1.pack()

        self.option2 = Radiobutton(self, text='option2', variable=self.var, 
					value='2', command=self.get)
        self.option2.pack()

        self.option3 = Radiobutton(self, text='option3', variable=self.var, 
					value='3', command=self.get)
        self.option3.pack()

    def get(self):
        print('option:',self.var.get())

app = UIApplication()
app.master.title = 'Hello'
app.mainloop()

~~~

### （六）Python GUI菜单

~~~
from tkinter import *

class UIApplication(Frame):
    def __init__(self,master=None):
        Frame.__init__(self,master)
        self.pack()
        self.create_ui()

    def create_ui(self):
        self.lable = Label(self,text='我的GUI')
        self.lable.pack()

        self.menubar = Menu(self)
        menu_file = Menu(self.menubar,tearoff=0)
        menu_file.add_command(label='open',command=self.sel)
        menu_file.add_command(label='save',command=self.sel)
        menu_file.add_separator()
        menu_file.add_command(label='exit', command=self.quit)

        self.menubar.add_cascade(label='File',menu=menu_file)

    def sel(self):
        print('sel---')

app = UIApplication()
app.master.config(menu=app.menubar)
app.master.title = 'Hello'
app.mainloop()
~~~

### （七）Python GUI Grid布局

~~~
from tkinter import *

class UIApplication(Frame):
    def __init__(self,master=None):
        Frame.__init__(self,master)
        self.pack()
        self.create_ui()

    def create_ui(self):
        self.lable1 = Label(self,text='Frist').grid(row=0,column=0)
        self.lable2 = Label(self,text='Second').grid(row=1,column=0)
        self.lable3 = Label(self,text='third').grid(row=2,column=0)
        self.e1 = Entry(self).grid(row=0,column=1)
        self.e1 = Entry(self).grid(row=1,column=1)

app = UIApplication()
app.master.title = 'Hello'
app.mainloop()
~~~

## 十八、Python 多线程

### （一）Python thread模块

比较老的模块，现在使用threading。

1. thread模块的函数

   （1）   start_new_thread(function,args,kwargs=None)

   ​		创建一个新的线程，使用给定的args和可选的kwargs来执行function。

   （2）   allocate_lock()

   ​		分配LockType锁对象

   （3）   exit()

   ​		退出线程

2. LockType锁对象的方法

   （1）   acquire(wait=None)尝试获得锁对象

   （2）   release()释放锁

   （3）   locked()如果获得了锁对象则返回true，否则返回False

   ~~~
   import _thread
   from time import ctime,sleep
   
   # ctime获得当前系统时间
   def fun1(lock):
       for i in range(5):
           print('fun1:',i)
           sleep(1)
       lock.release()
   
   def fun2(lock):
       for i in range(5):
           print('fun2:',i)
           sleep(1)
       lock.release()
   
   
   def main():
       print('start:',ctime())
   
       locks = []
       for i in range(2):
           lock = _thread.allocate_lock()
           lock.acquire()
           locks.append(lock)
   
       _thread.start_new_thread(fun1,(locks[0],))
       _thread.start_new_thread(fun2,(locks[1],))
   
       for j in range(len(locks)):
           #如果锁定一直循环
           while locks[j].locked():
               pass
   
       print('stop:',ctime())
   
   if __name__ == '__main__':
       main()
   
   ~~~

### （二）Python threading模块

| 对象             | 描述                                                         |
| ---------------- | ------------------------------------------------------------ |
| Thread           | 表示一个执行线程的对象                                       |
| Lock             | 锁原语对象（和thread模块中的锁一样）                         |
| RLock            | 可重入锁对象，使单一线程可以（再次）获得已持有的锁（递归锁） |
| Condition        | 条件变量对象，使得一个线程等待另外一个线程满足特定的条件，比如改变状态或者某个数据值 |
| Event            | 条件变量的通用版本，任意数量的线程等待某个事件的发生，在该事件发生后所有的线程都将被激活 |
| Semaphore        | 为线程间共享的有限资源提供一个计数器，如果没有可用资源时会被阻塞 |
| BoundedSemaphore | 与Semaphore相似，不过它不允许超过初始值                      |
| Timer            | 与Thread类似，不过它要在运行前等待一定时间                   |
| Barrier          | 创建一个障碍，必须达到指定数量的线程后才可以继续             |

| 属性         | 描述                               |
| ------------ | ---------------------------------- |
| Thread类属性 |                                    |
| name         | 线程名                             |
| ident        | 线程的标识符                       |
| daemon       | 布尔值，表示这个线程是否是守护线程 |

| Thread类方法                                                 |                                                              |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| \__init__(group=None,target=None,name=None,args=(),kwargs={},verbose=None,daemon=None) | 实例化一个线程对象，需要一个可调用的target对象，以及参数args或者kwargs。还可以传递name和group参数，不过后者未实现。此外，verbose标志也是可接受的。而daemon的值将会设定thread.daemon的属性/标志 |
| start()                                                      | 开始执行该线程                                               |
| run()                                                        | 定义线程的方法。（通常开发者应该在子类中重写）               |
| join(timeout=None)                                           | 直至启动的线程终止之前一直挂起；除非给出了timeout(单位秒)，否则一直被阻塞 |
| getName()                                                    | 返回线程名（该方法已被弃用）                                 |
| setName()                                                    | 设定线程名（该方法已弃用）                                   |
| isAlive/is_alive()                                           | 布尔值，表示这个线程是否还存活（驼峰式命名，python2.6版本开始已被取代） |
| isDaemon()                                                   | 布尔值，表示是否是守护线程(已经弃用)                         |
| setDaemon(布尔值)                                            | 在线程start()之前调用，把线程的守护标识设定为指定的布尔值（已弃用） |

 

1. 创建Thread的实例，传给它一个函数

   可以使用Thread的初始化方法，为traget参数传递一个函数

   ~~~
   import threading
   from time import ctime,sleep
   
   def fun1():
       for i in range(5):
           print('fun1:',i)
           sleep(1)
   
   def fun2():
       for i in range(5):
           print('fun2:',i)
           sleep(1)
   
   def main():
       print('start:',ctime())
   
       t1 = threading.Thread(target=fun1)
       t2 = threading.Thread(target=fun2)
       t1.start()
       t2.start()
       t1.join()
       t2.join()
       print('stop:',ctime())
   
   if __name__ == '__main__':
       main()
   
   ~~~

2.创建Thread的实例，传给它一个可调用的类实例

 ~~~
import threading
from time import ctime,sleep

def fun1():
    for i in range(5):
        print('fun1:',i)
        sleep(1)

def fun2():
    for i in range(5):
        print('fun2:',i)
        sleep(1)

class MyThread(object):
    def __init__(self,func):
        self.func = func
    def __call__(self):
        self.func()


def main():
    print('start:',ctime())

    t1 = threading.Thread(target=MyThread(fun1))
    t2 = threading.Thread(target=MyThread(fun2))
    t1.start()
    t2.start()
    t1.join()
    t2.join()
    print('stop:',ctime())

if __name__ == '__main__':
    main()

 ~~~

3.派生Thread的子类，并创建子类的实例

​	继承Thread类，实现run方法实现

~~~
import threading
from time import ctime,sleep

def fun1():
    for i in range(5):
        print('fun1:',i)
        sleep(1)

def fun2():
    for i in range(5):
        print('fun2:',i)
        sleep(1)

class MyThread(threading.Thread):
    def __init__(self,func):
        threading.Thread.__init__(self)
        self.func = func
    def run(self):
        self.func()


def main():
    print('start:',ctime())

    t1 = MyThread(fun1)
    t2 = MyThread(fun2)
    t1.start()
    t2.start()
    t1.join()
    t2.join()
    print('stop:',ctime())

if __name__ == '__main__':
    main()

~~~

### （三）Python 线程同步

 

 

### （四）Python 

 

 

 