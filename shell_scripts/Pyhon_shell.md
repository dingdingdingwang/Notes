# 置顶-markdown快捷键

```
Ctrl + 数字：直接设置几级的标题
Ctrl + Alt + L 自动让代码格式变整齐
```

# Python

```
ipython使用多行输入：Ctrl+字母O
ipython执行：Ctrl + Enter
```
## Python概述
```
1.安装Pythonp模块：
pip install modules
pip install modules -U
pip install git+https://github.xxxx.git

2.基础数据：
数据从用户来,到用户去
编程语言中的数据是分门别类的

3.Python中的数据类型：
1).字符串(给用户用的，人能看懂)
2).整数、浮点数(用来计算的数据)
3).布尔值(计算机理解的逻辑“是”和“否”)
```
## 创建数据
```
x = 1
y = 1.0
word = "say something : 007"
w_2 = 'good'
注释：三引号字符串，用于折行
w_3 = '''
a very long string here
this is extra line
'''
test = True
truth = False
a_very_long_name = "wow"
注释：全部大写的，默认为常量
THIS = "password"
THAT = 42
```
## 使用数据
```
1.print()用来打印数据
print(42)
2.len()用来测量字符串长度，包括空格在内
result = len("hello")
3.例子
In [1]: word = "say something : 007"

In [2]: len(word)
Out[2]: 19

In [3]: r = len(word)

In [4]: r
Out[4]: 19

4.关于"this".函数
In [5]: "this".capitalize()
Out[5]: 'This'

5.数据运算
r3 = x + THAT
In [6]: a = 1
In [7]: b = 42
In [8]: c = a + b
In [9]: c
Out[9]: 43
new_word = word + w_2 注释：这里的+用来合并字符串
In [10]: "hello" + 'world'
Out[10]: 'helloworld'
In [11]: "hello " + 'world'
Out[11]: 'hello world'

注释：错误例子
In [12]: 'hello' - 'h'
TypeError                                 Traceback (most recent call last)
Input In [12], in <cell line: 1>()
----> 1 'hello' - 'h'
TypeError: unsupported operand type(s) for -: 'str' and 'str'

5.布尔值运算
注释：真1假0
In [13]: a = True
In [14]: b = False
In [15]: a + b
Out[15]: 1
In [16]: c = True
In [17]: a + c
Out[17]: 2
In [18]: a and b
Out[18]: False
In [19]: a or b
Out[19]: True
```
## 修改数据
```
注释：通过二次赋值来进行修改

x = 1
x = 12
print(x)
In [20]: x = 1

In [21]: x = 12

In [22]: print(x)
12

In [23]: print(x + 1)
13

注释：这里的+代表着合并，左边代表未知的，右边代表的是已有的。
含义：从已有的x加1，赋值给新的x
x = x + 1
x += 1
```
## 删除数据
```
注释：del x
In [24]: a
Out[24]: True

In [25]: del a

In [26]: a
NameError                                 Traceback (most recent call last)
Input In [26], in <cell line: 1>()
----> 1 a

NameError: name 'a' is not defined
```
## 字符串
```
In [1]: type('this')
Out[1]: str

In [2]: type(b'this')
Out[2]: bytes

In [3]: 'this' + b'this'

TypeError                                 Traceback (most recent call last)
Input In [3], in <cell line: 1>()
----> 1 'this' + b'this'

TypeError: can only concatenate str (not "bytes") to str

In [4]: z = "中文"

In [5]: z
Out[5]: '中文'

In [6]: z.encode("utf-8")
Out[6]: b'\xe4\xb8\xad\xe6\x96\x87'

In [7]: f = b'\xe4\xb8\xad\xe6\x96\x87'

In [8]: f.decode("utf-8")
Out[8]: '中文'
```
### 字符串分类：
```
'capitalize','casefold','center','count','encode','endswith','expandtabs','find','format','format_map','index','isalnum','isalpha','isascii','isdecimal','isdigit','isidentifier','islower','isnumeric','isprintable','isspace','istitle','isupper','join','ljust','lower','lstrip','maketrans','partition','replace','rfind','rindex','rjust','rpartition','rsplit','rstrip','split','splitlines','startswith','strip','swapcase','title','translate','upper','zfill'

注释：l开头：从左开始。r开头：从右开始。

```
#### 文本处理
```

1. split()--rsplit()

In [9]: "that is code".split()
Out[9]: ['that', 'is', 'code']
In [10]: g = "that is code".split()
In [11]: g[-1]
Out[11]: 'code'

2. partition()--rpartition()
注释：partition()只会切第一个

In [12]: g = "that is code".partition(" ")
In [13]: g
Out[13]: ('that', ' ', 'is code')
In [14]: g = "that is code".rpartition(" ")
In [15]: g
Out[15]: ('that is', ' ', 'code')
In [16]: 'www.baidu.com.cn'.rpartition(".")
Out[16]: ('www.baidu.com', '.', 'cn')

3. replace()--translate()
            ↘-maketrans()

In [18]: "this".replace("i","I")
Out[18]: 'thIs'
In [19]: "this".replace("i","I").replace("t","T")
Out[19]: 'ThIs'
注释：可以链式调用(methods chain)

          ↗-lstrip()
4. strip()---rstrip()
          ↘-splitlines()

In [20]: 'hello:'.strip(':')
Out[20]: 'hello'

5. join()

In [21]: ".".join(["s","e","g"])
Out[21]: 's.e.g'

In [22]: " ".join(["this","is","great"])
Out[22]: 'this is great'

6. format()
```
#### 转码
```
7. encode()

8. decode()

9. str()
```
#### 文本索引
```
10. find()--rfind()

In [23]: 'hello'.find("e")
Out[23]: 1

In [25]: "hello world ,hi python".find("h")
Out[25]: 0

In [26]: "hello world ,hi python".find("w")
Out[26]: 6

11.  count()

12.  index()--rindex()
```
#### 装饰
```
13. swapcase()--casefold()

14. textwrap()

15. upper()

16. lower()

17. center()

18. zfill()

19. ljust()

20. rjust()

21. expandtabs() 

```
#### 判断类型
```
22. startswith()
    
In [29]: 'yk-1001'.startswith("yk")
Out[29]: True

23. endswith()

In [30]: '@163.com'.endswith("@163.com")
Out[30]: True

24. isalnum
注释：是否是数字

25. isalpha
注释：是否是字母表

26. isascii

27. isdecimal

28. isdigit

29. isidentifier

30. islower

31. isnumeric

32. isprintable

33. isspace

34. istitle

35. isupper
```
#### Other
```
36. u'something'
注释：就是正常的字符串，遗留产物

37. f'hello{name}'

38. b'that'
注释：字节(bytes)

39. r'there'
注释：字符串(正则专用)
```
## 数字
```
```
### 进制转化
```
```
#### bin()
```
注释：图片或者执行程序
0b1  => 1
0b10 => 2
```
#### oct()
```
注释：十进制
```
#### hex()
```
注释：加密/编码/汇编/嵌入式
0x10 => 16
0xff => 255
```
#### 位运算
```
符号：<<

符号：>>

符号：|

符号：~

符号：^

符号：&
```
### 浮点数
```
42.0
```
#### 精度问题
```
2.1+4.2 = ?

In [36]: 2.1 + 4.2
Out[36]: 6.300000000000001
```
##### round(3.14,1)
```
In [37]: round(3.14,1)
Out[37]: 3.1
```
##### Decimal 模块
```
```
##### format() 函数
```
```
##### 17位精度限制
```
1.1111111122222234
```
### 常规计算
```
```
#### 类型转化
```
40. float()

41. int()

In [38]: int(1.0)
Out[38]: 1
```
#### 数学运算
##### 自带函数
```
42. complex(2, 4)
注释：复数

In [39]: complex(2, 4)
Out[39]: (2+4j)

43. abs(-15)
注释：绝对值

In [40]: abs(-15)
Out[40]: 15

44. pow(2,2)
注释：平方

In [41]: pow(2,2)
Out[41]: 4

45. divmod(7,2)
注释：求商和余数

In [42]: divmod(7,2)
Out[42]: (3, 1)

46. sum()
注释：求和

In [43]: sum([1,2,3,4])
Out[43]: 10
```
##### math
```
47. math.sqrt(4)
注释：平方根
```
##### cmath
```
48. cmath.sqrt(-4)
49. 注释：平方根
```
##### numpy
```
```
##### pandas
```
```
#### 常用计算
```
50. 4/3

In [46]: 4/3
Out[46]: 1.3333333333333333

51. 2**3

In [47]: 2**3
Out[47]: 8

52. 17//3
注释：求商

In [48]: 17//3
Out[48]: 5

In [1]: 17.0 // 3.0
Out[1]: 5.0

53. 17%3
注释：求余

In [49]: 17%3
Out[49]: 2

54. 1.0 + 4

In [50]: 1.0 + 4
Out[50]: 5.0

55. 1 + 1

In [51]: 1 + 1
Out[51]: 2

56. (12 -1)*12 + 3*(4 -1)
注释：顺序由内到外的计算

In [52]: (12 -1)*12 + 3*(4 -1)
Out[52]: 141
```
## 布尔类型
```
```
### True/False
```
```
### 转化值bool()
```
```
#### 空
```
 ''
 []
 {}
 ()
 1
 0
 None
```
### 重要方法
```
 startswith()
 endswith()
 len()
 has_
 is_
```
### 逻辑运算
```
```
#### 关键词
```
 and
 or
 not
 is
 in
 符号：==
```
 ```
In [53]: a = 1

In [54]: b = 1

In [55]: a == b
Out[55]: True

In [56]: a is b
Out[56]: True

In [57]: x = [1,2]

In [58]: y = [1,2]

In [59]: x == y
Out[59]: True

In [60]: x is y
Out[60]: False
 ```
```
 符号：!=
 符号：>
 符号：<
 符号：>=
 符号：<=
```
#### 常见运算
```
 v == 1

 v > 1

 2 in [1,2,3]
 
In [61]: 2 in [1,2,3]
Out[61]: True

 not v.is_empty()
```
 ## 数据结构
 ### 概述
 ```
1. 列表-集合型数据结构
a = []
2. 字典 - dict = {key:value }
b = {}
注释：列表和字典，标号都是从0开始，例如第三个元素的标号为2
注释：可以这样记-列表是给机器使用的，字典是给人使用的。
 ```
 #### 创建
 ```
c = [1, 2, 3, 4, "hello", True]

c = [12, "room-221", 3] 

c = {"John Doe": 1} 

c = list()

c = dict()
 ```
#### 使用
 ```
 print(a)

 total = 2 + c[2]

print(c["John Doe"])
注释：字典的取值写法：dict[key]
In [5]: c = {"John Doe": 1}
In [6]: print(c["John Doe"])
Out[6]: 1
In [7]: c.get("John Doe")
Out[7]: 1

a = [12, "room-221", 3]
c = a + [7, 8, 9]
注释：列表合并的写法
In [9]: a = [12, "room-221", 3]
   ...: c = a + [7, 8, 9]

In [10]: c
Out[10]: [12, 'room-221', 3, 7, 8, 9]

错误示例：
c = {"John Doe": 1} 
d = c + {"James Five":2}
print(d)
In [12]: c = {"John Doe": 1}
    ...: d = c + {"James Five":2}
    ...: print(d)
TypeError                                 Traceback (most recent call last)      
Input In [12], in <cell line: 2>()
      1 c = {"John Doe": 1}
----> 2 d = c + {"James Five":2}
      3 print(d)

TypeError: unsupported operand type(s) for +: 'dict' and 'dict'

正确示例：
c = {"John Doe": 1} 
c.update({"James Five":2})
print(c)
In [15]: c = {"John Doe": 1}
    ...: c.update({"James Five":2})
    ...: print(c)
{'John Doe': 1, 'James Five': 2}
注释：字典更新的写法
 ```
 #### 修改
```
d["key"] = "value"
d.update()

In [16]: c = [1, 2, 3]

In [17]: c.append(4)

In [18]: c
Out[18]: [1, 2, 3, 4]

In [19]: c.remove(2)

In [20]: c
Out[20]: [1, 3, 4]

In [22]: c.append(1)

In [23]: c
Out[23]: [1, 3, 4, 1]
注释：添加在末尾

In [25]: z =  {"John":1}

In [26]: z.update({"James":"007"})

In [27]: z
Out[27]: {'John': 1, 'James': '007'}

In [28]: z.update({"James":"007"})
注释：和之前的元素重合了，因此不会再更新

In [29]: z
Out[29]: {'John': 1, 'James': '007'}

In [30]: z["John"] = "001"
注释：字典的修改

In [31]: z
Out[31]: {'John': '001', 'James': '007'}

In [32]: z['????']='pikachu'

In [33]: z
Out[33]: {'John': '001', 'James': '007', '????': 'pikachu'}
```
 #### 删除
 ```
c.remove()
d.pop("")
del c["name"]

In [34]: z.pop("John")
Out[34]: '001'

In [35]: z
Out[35]: {'James': '007', '????': 'pikachu'}
注释：删除法一

In [36]: del z["James"]

In [37]: z
Out[37]: {'????': 'pikachu'}
注释：删除法二
 ```
 #### 循环
 ```
 1. 列表循环
 c = [12, "room-221", 3]
for i in c:
    print(i)
注释：第一次i=12,第二次i="room-221",第三次i=3

1. 字典循环
 d = {"John":1,"James":2}
for i in d.keys():
    print(i)
    print(a[i])
 ```
```
 数据结构是数据的工具
 数据结构方便我们使用
 数据结构方便程序理解
 数据结构让数据清晰地分类
 经典的数据结构有八种
```
 ### 列表
 ```
 
              ↗--正向--a[0]
              |
              |
              |
              |
              |
        ↗索引----逆向--a[-1]
        |     |
        |     |
        |     |
        |     |       ↗--a[x]
        |     |       |
        |     ↘--技巧---a[x+1]
        |             |
        |             ↘--a[2x+1]
        |
        |
        |            ↗--a[1:3]
        |            |
        |     ↗-正向---a[2:]
        |     |
        |     |
        |     |       ↗--a[-3:-1]
        |     |      | 
        |     |--逆向---a[:-3]
[前:后]--切片--|  
        |     |       ↗--前面算数，后面不算
        |     |-口诀--|---前后相减是总数
        |     |       ↘--选定范围从左到右(从前到后)
        |     |
        |     |
        |     ↘--a[1:1000]注释：超出范围不会报错
        |
        |         ↗--混合索引切片-a[3:-1]
        |         |
        |         |
        |         |
        ↘容易懵的-|--在切片内走步--a(0:8:1]--a[0::1]--a[::1]
                  |              ↘--a(1:8:3]
                  |
                  |
                  ↘--口诀-走一步算一个
 ```
```
例子：
a = ['q', 'w', 'e', 'r', 't', 'y', 'u', 'i', 'o']
     0    1    2    3    4    5    6    7    8
    -9   -8   -7   -6   -5   -4   -3   -2   -1

In [40]: a = ['q', 'w', 'e', 'r', 't', 'y', 'u', 'i', 'o']

In [41]: a[1:3]
Out[41]: ['w', 'e']

In [42]: a[2:]
Out[42]: ['e', 'r', 't', 'y', 'u', 'i', 'o']

In [43]: a[-3:-1]
Out[43]: ['u', 'i']

In [44]: a[-1:-3]
Out[44]: []

In [45]: a[1:1000]
Out[45]: ['w', 'e', 'r', 't', 'y', 'u', 'i', 'o']

In [46]: a[3:-1]
Out[46]: ['r', 't', 'y', 'u', 'i']

In [47]: a[0:8]
Out[47]: ['q', 'w', 'e', 'r', 't', 'y', 'u', 'i']

In [48]: a[0:8:1]
Out[48]: ['q', 'w', 'e', 'r', 't', 'y', 'u', 'i']

In [49]: a[0:8:2]
Out[49]: ['q', 'e', 't', 'u']

In [50]: a[0::1]
Out[50]: ['q', 'w', 'e', 'r', 't', 'y', 'u', 'i', 'o']
注释：从某一位置到结尾，可以省略结尾

In [51]: a[::1]
Out[51]: ['q', 'w', 'e', 'r', 't', 'y', 'u', 'i', 'o']
注释：从头取到尾，那么开头和结尾都可以省略

In [52]: a[:]
Out[52]: ['q', 'w', 'e', 'r', 't', 'y', 'u', 'i', 'o']
注释：从头取到尾
```
#### 列表方法
```
1. 函数与方法
添加
1) a.append(x)


2) a.insert(x,i)
   注释：x表示插入的位置,i表示插入的值

In [53]: a = [1,2,3,4,5]

In [54]: i = 0

In [55]: a.insert(3,i)

In [56]: a
Out[56]: [1, 2, 3, 0, 4, 5]

3) 原有基础上 a.extend(list)
注释：插入一个列表

4) 制造新的 z = a + [0, 1, 2]
注释：在原有a的基础上，再合并一个列表

删除
1) a.remove(x)
2) a.clear()
3) a = []
修改
1) a[i] = "something"
查询
1) a[i]
2) a.count(x)
排序
1) a.reverse()
注释：翻转一个列表

2) a.sort()
复制
1) b = copy.copy(a)
2) b = a[:]
3) a.copy()
4) b = a
注释：这个方法不好，两个列表是同一个列表
In [57]: a = [1,2,3,4,5]

In [58]: b = a

In [59]: a
Out[59]: [1, 2, 3, 4, 5]

In [60]: b
Out[60]: [1, 2, 3, 4, 5]

In [61]: a.clear()

In [62]: a
Out[62]: []

In [63]: b
Out[63]: []

堆栈
1) drop = a.pop()
其他
1) list(range(12))
In [64]: range(12)
Out[64]: range(0, 12)

In [65]: list(range(12))
Out[65]: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11]

2) sum()
3) len()
2. 列表解析式
In [66]: import string

In [67]: string.ascii_letters
Out[67]: 'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ'   

1) 正常的
a list = [i for i in a]
In [69]: s = [i for i in string.ascii_letters]

In [70]: s
Out[70]: 
['a','b','c','d', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l','m', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']

2)带条件判断的
a list = [i for i in a if a>4]

In [71]: [i for i in string.ascii_letters if i.isupper()]
Out[71]: 
 ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']

3. 操作技巧  
1) 解压/unpack
b,*_,c = a

In [80]: f = [1,2]

In [81]: j,k = f

In [82]: j
Out[82]: 1

In [83]: k
Out[83]: 2

2) 成员判断
   x in a
In [77]: 'Z' in s
Out[77]: True

In [78]: 'z' in s
Out[78]: True

In [84]: s
Out[84]: 
['a','b','c','d', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l','m', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']

In [85]: first,*others,last = s

In [86]: first
Out[86]: 'a'

In [87]: last
Out[87]: 'Z'

In [88]: first,*others,before_last,last = s

In [89]: before_last
Out[89]: 'Y'
```
### 字典
```
d = {
    "key1":1,
    "key2":2,
    "key3":3,
    "key4":4,
    "key5":5
}
```
#### 方法与函数
```
```
##### 创建
```
1) d = {} 注释：创建一个空的字典
In [94]: d = {}

In [95]: d
Out[95]: {}

2) d = dict(k=v)
In [90]: d = dict(key1=1)

In [91]: d
Out[91]: {'key1': 1}

In [92]: d = dict(key1=1,key2=2)

In [93]: d
Out[93]: {'key1': 1, 'key2': 2}

3) d = {}.fromkeys{[1,2,3],"hello"}

In [102]: d = {}.fromkeys([i for i in string.ascii_letters],"hi")
In [103]: d
Out[103]: 
{'a': 'hi','b': 'hi','c': 'hi','d': 'hi','e': 'hi','f': 'hi','g': 'hi','h': 'hi','i': 'hi','j': 'hi','k': 'hi','l': 'hi','m': 'hi','n': 'hi','o': 'hi','p': 'hi','q': 'hi','r': 'hi','s': 'hi','t': 'hi','u': 'hi','v': 'hi','w': 'hi','x': 'hi','y': 'hi','z': 'hi','A': 'hi','B': 'hi','C': 'hi','D': 'hi','E': 'hi','F': 'hi','G': 'hi','H': 'hi','I': 'hi','J': 'hi','K': 'hi','L': 'hi','M': 'hi','N': 'hi','O': 'hi','P': 'hi','Q': 'hi','R': 'hi','S': 'hi','T': 'hi','U': 'hi','V': 'hi','W': 'hi','X': 'hi','Y': 'hi','Z': 'hi'}
In [104]: d['a'] = 1
In [105]: d
Out[105]: 
{'a': 1,'b': 'hi','c': 'hi','d': 'hi','e': 'hi','f': 'hi','g': 'hi','h': 'hi','i': 'hi','j': 'hi','k': 'hi','l': 'hi','m': 'hi','n': 'hi','o': 'hi','p': 'hi','q': 'hi','r': 'hi','s': 'hi','t': 'hi','u': 'hi','v': 'hi','w': 'hi','x': 'hi','y': 'hi','z': 'hi','A': 'hi','B': 'hi','C': 'hi','D': 'hi','E': 'hi','F': 'hi','G': 'hi','H': 'hi','I': 'hi','J': 'hi','K': 'hi','L': 'hi','M': 'hi','N': 'hi','O': 'hi','P': 'hi','Q': 'hi','R': 'hi','S': 'hi','T': 'hi','U': 'hi','V': 'hi','W': 'hi','X': 'hi','Y': 'hi','Z': 'hi'}
In [106]: d.update({"zz":12})
In [107]: d
Out[107]: 
{'a': 1,'b': 'hi','c': 'hi','d': 'hi','e': 'hi','f': 'hi','g': 'hi','h': 'hi','i': 'hi','j': 'hi','k': 'hi','l': 'hi','m': 'hi','n': 'hi','o': 'hi','p': 'hi','q': 'hi','r': 'hi','s': 'hi','t': 'hi','u': 'hi','v': 'hi','w': 'hi','x': 'hi','y': 'hi','z': 'hi','A': 'hi','B': 'hi','C': 'hi','D': 'hi','E': 'hi','F': 'hi','G': 'hi','H': 'hi','I': 'hi','J': 'hi','K': 'hi','L': 'hi','M': 'hi','N': 'hi','O': 'hi','P': 'hi','Q': 'hi','R': 'hi','S': 'hi','T': 'hi','U': 'hi','V': 'hi','W': 'hi','X': 'hi','Y': 'hi','Z': 'hi','zz': 12}

```
##### 添加
```
1) 添加/覆盖--d[key] = value 注释：推荐
In [96]: d = dict(key1=1)
In [97]: d['key6'] = 6
In [98]: d
Out[98]: {'key1': 1, 'key6': 6}
In [99]: d['key1'] = 15
In [100]: d
Out[100]: {'key1': 15, 'key6': 6}

2) 添加/覆盖一个或多个--d.update({}) 注释：推荐
                     ↘ d.update(key=value,key=value)

3) 一次性添加--d.setdefault() 注释:将键值对锁定，不能修改
In [108]: d.setdefault("xx",12)
Out[108]: 12
In [109]: d
Out[109]: 
{'a': 1,'b': 'hi','c': 'hi','d': 'hi','e': 'hi','f': 'hi','g': 'hi','h': 'hi','i': 'hi','j': 'hi','k': 'hi','l': 'hi','m': 'hi','n': 'hi','o': 'hi','p': 'hi','q': 'hi','r': 'hi','s': 'hi','t': 'hi','u': 'hi','v': 'hi','w': 'hi','x': 'hi','y': 'hi','z': 'hi','A': 'hi','B': 'hi','C': 'hi','D': 'hi','E': 'hi','F': 'hi','G': 'hi','H': 'hi','I': 'hi','J': 'hi','K': 'hi','L': 'hi','M': 'hi','N': 'hi','O': 'hi','P': 'hi','Q': 'hi','R': 'hi','S': 'hi','T': 'hi','U': 'hi','V': 'hi','W': 'hi','X': 'hi','Y': 'hi','Z': 'hi','zz': 12,'xx': 12}
In [110]: d.setdefault("xx",42)
Out[110]: 12
In [111]: d
Out[111]: 
{'a': 1,'b': 'hi','c': 'hi','d': 'hi','e': 'hi','f': 'hi','g': 'hi','h': 'hi','i': 'hi','j': 'hi','k': 'hi','l': 'hi','m': 'hi','n': 'hi','o': 'hi','p': 'hi','q': 'hi','r': 'hi','s': 'hi','t': 'hi','u': 'hi','v': 'hi','w': 'hi','x': 'hi','y': 'hi','z': 'hi','A': 'hi','B': 'hi','C': 'hi','D': 'hi','E': 'hi','F': 'hi','G': 'hi','H': 'hi','I': 'hi','J': 'hi','K': 'hi','L': 'hi','M': 'hi','N': 'hi','O': 'hi','P': 'hi','Q': 'hi','R': 'hi','S': 'hi','T': 'hi','U': 'hi','V': 'hi','W': 'hi','X': 'hi','Y': 'hi','Z': 'hi','zz': 12,'xx': 12}

```
##### 删除
```
1) d.clear()

2) d.popitem() 注释：挤出字典的最后一个
In [114]: d.popitem()
Out[114]: ('zz', 12)
In [115]: d
Out[115]: 
{'a': 1,'b': 'hi','c': 'hi','d': 'hi','e': 'hi','f': 'hi','g': 'hi','h': 'hi','i': 'hi','j': 'hi','k': 'hi','l': 'hi','m': 'hi','n': 'hi','o': 'hi','p': 'hi','q': 'hi','r': 'hi','s': 'hi','t': 'hi','u': 'hi','v': 'hi','w': 'hi','x': 'hi','y': 'hi','z': 'hi','A': 'hi','B': 'hi','C': 'hi','D': 'hi','E': 'hi','F': 'hi','G': 'hi','H': 'hi','I': 'hi','J': 'hi','K': 'hi','L': 'hi','M': 'hi','N': 'hi','O': 'hi','P': 'hi','Q': 'hi','R': 'hi','S': 'hi','T': 'hi','U': 'hi','V': 'hi','W': 'hi','X': 'hi','Y': 'hi','Z': 'hi'}

In [116]: k,v = d.popitem()

In [117]: k
Out[117]: 'Z'

In [118]: v
Out[118]: 'hi'

3) 指名 d.pop(key)
In [112]: d.pop('xx')
Out[112]: 12
In [113]: d
Out[113]: 
{'a': 1,'b': 'hi','c': 'hi','d': 'hi','e': 'hi','f': 'hi','g': 'hi','h': 'hi','i': 'hi','j': 'hi','k': 'hi','l': 'hi','m': 'hi','n': 'hi','o': 'hi','p': 'hi','q': 'hi','r': 'hi','s': 'hi','t': 'hi','u': 'hi','v': 'hi','w': 'hi','x': 'hi','y': 'hi','z': 'hi','A': 'hi','B': 'hi','C': 'hi','D': 'hi','E': 'hi','F': 'hi','G': 'hi','H': 'hi','I': 'hi','J': 'hi','K': 'hi','L': 'hi','M': 'hi','N': 'hi','O': 'hi','P': 'hi','Q': 'hi','R': 'hi','S': 'hi','T': 'hi','U': 'hi','V': 'hi','W': 'hi','X': 'hi','Y': 'hi','Z': 'hi','zz': 12}

4)d[key] = None

```
##### 修改
```
1) d[key] = value


2) d.update({})
```
##### 查询
```
1) d[key]

2) 安全查询 d.get(key)
In [119]: d['aaaaa']
KeyError                                  Traceback (most recent call last)      
Input In [119], in <cell line: 1>()
----> 1 d['aaaaa']

KeyError: 'aaaaa'

In [120]: d.get('aaaaa')

In [121]: result = d.get('aaaaa')

In [122]: print(result)
None

3)d.keys()


4)d.values()


5)d.items()


```
##### 复制
```
1) d.copy()


2) copy.copy()


```
##### 字典转列表
```
1) d.values()
In [123]: d.values()
Out[123]: dict_values([1, 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi', 'hi'])
注释：dict_values是一种类似列表，但不是真正意义上的列表

In [124]: list(d.values())
Out[124]: 
[1,'hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi','hi']
注释：这里的列表才是真正意义上的列表

2) list(d.values())

3) for i in d.values():pass

for group in d.values():
    k,v = group
    print(k)
    print(v)
```
##### 列表转字典/空字典填充/造一个字典
```
1) z = {}.formkeys([1,2,3],"hello")

```
##### 成员判断
```
key in d
```
##### 字典推导式
```
1) {k:d[k] for k in d.keys()}


2) {k:d[k] for k in d.keys() if key.startswith('haha')}

In [6]: d = {}.fromkeys([i for i in string.ascii_letters],"hi")

In [7]: d
Out[7]:
{'a': 'hi','b': 'hi','c': 'hi','d': 'hi','e': 'hi','f': 'hi','g': 'hi','h': 'hi','i': 'hi','j': 'hi','k': 'hi','l': 'hi','m': 'hi','n': 'hi','o': 'hi','p': 'hi','q': 'hi','r': 'hi','s': 'hi','t': 'hi','u': 'hi','v': 'hi','w': 'hi','x': 'hi','y': 'hi','z': 'hi','A': 'hi','B': 'hi','C': 'hi','D': 'hi','E': 'hi','F': 'hi','G': 'hi','H': 'hi','I': 'hi','J': 'hi','K': 'hi','L': 'hi','M': 'hi','N': 'hi','O': 'hi','P': 'hi','Q': 'hi','R': 'hi','S': 'hi','T': 'hi','U': 'hi','V': 'hi','W': 'hi','X': 'hi','Y': 'hi','Z': 'hi'}
In [8]: z = {k:d[k] for k in d.keys() if k.isupper()}
In [9]: z
Out[9]: 
{'A': 'hi','B': 'hi','C': 'hi','D': 'hi','E': 'hi','F': 'hi','G': 'hi','H': 'hi','I': 'hi','J': 'hi','K': 'hi','L': 'hi','M': 'hi','N': 'hi','O': 'hi','P': 'hi','Q': 'hi','R': 'hi','S': 'hi','T': 'hi','U': 'hi','V': 'hi','W': 'hi','X': 'hi','Y': 'hi','Z': 'hi'}

```
##### 字典解压(unpack)
```
注释：字典的键值解压
a,b = d

```
### 流控制(Flow Control)
```
1) 流控制 =  条件判断 + 循环
    a) 条件判断：分流数据；
    b) 循环：批量处理数据；

2) 流控制 = 数据的控制
```
#### TODO 把式
```
1) if else elif


2) 多个独立事件判断 -- if ... if


3) 一个事件多种特征的连续判断 -- if ... elif


```
#### TODO 细则
```
user_input = "12"
if user_input:
    print("hello")
print("world")

In [1]: user_input = "12"
   ...: if user_input:
   ...:     print("hello")
   ...: print("world")
hello
world

user_input = "" #空等同于False
if user_input:
    print("hello")
print("world")

In [2]: user_input = "" #空等同于False
   ...: if user_input:
   ...:     print("hello")
   ...: print("world")
world

user_input = "12"
another_thing = True
if user_input:
    print("hello")
if another_thing:
    print("haha there we go")
print("world")

In [3]: user_input = "12"
   ...: another_thing = True
   ...: if user_input:
   ...:     print("hello")
   ...: if another_thing:
   ...:     print("haha there we go")
   ...: print("world")
hello
haha there we go
world

user_input = "12"
another_thing = False
# condition chain
if user_input:
    print("hello")
elif user_input.startswith("1"):
    print("we got 1")
elif user_input.endswith("2"):
    print("we got 2")

if another_thing:
    print("haha there we go")
print("world")

In [6]: user_input = "12"
   ...: another_thing = False
   ...: if user_input:
   ...:     print("hello")
   ...: elif user_input.startswith("1"):
   ...:     print("we got 1")
   ...: elif user_input.endswith("2"):
   ...:     print("we got 2")
   ...:
   ...: if another_thing:
   ...:     print("haha there we go")
   ...: print("world")
hello
world

user_input = ""
another_thing = False
# condition chain
if user_input:
    print("hello")
elif user_input.startswith("1"):
    print("we got 1")
elif user_input.endswith("2"):
    print("we got 2")

if another_thing:
    print("haha there we go")
else:
    print("nothing")

print("world")

In [9]:

   ...: # condition chain
   ...: if user_input:
   ...:     print("hello")
   ...: elif user_input.startswith("1"):
   ...:     print("we got 1")
   ...: elif user_input.endswith("2"):
   ...:     print("we got 2")
   ...:
   ...: if another_thing:
   ...:     print("haha there we go")
   ...: else:
   ...:     print("nothing")
   ...:
   ...: print("world")
nothing
world
```
## 流控制
```
```
### 事件捕捉技巧
```
```
#### 单一事件捕捉
例子：场景介绍，发帖回复别人

```python
 print("write your comment.")
 post = input()

if 1 < len(post) < 10:
    print(f'you said : { post }')
else:
    print('comment cant be less than 1 more than 10')
-------------------------------------------------------------------   
In [1]:  print("write your comment.")
   ...:  post = input()
   ...:
   ...: if 1 < len(post) < 10:
   ...:     print(f'you said : { post }')
   ...: else:
   ...:     print('comment cant be less than 1 more than 10')
write your comment.
hello
you said : hello
------------------------------------------------------------------
In [2]:  print("write your comment.")
   ...:  post = input()
   ...:
   ...: if 1 < len(post) < 10:
   ...:     print(f'you said : { post }')
   ...: else:
   ...:     print('comment cant be less than 1 more than 10')
write your comment.
wqeasdasdasdjiowqieeqw
comment cant be less than 1 more than 10
--------------------------------------------------------------------
In [7]:  print("write your comment.")
   ...:  post = input()
   ...: if 1 < len(post) < 10:
   ...:     print(f'you said : { post }')
   ...: elif "@" in post:
   ...:     print("Invalid input")
   ...: else:
   ...:     print('comment cant be less than 1 more than 10')
   ...:
write your comment.
@
Invalid input
```


```
边界
极值
```
#### 多事件捕捉

例子：场景介绍，发帖回复别人

```python
user_db = {
    "admin":"123"
}

if not user in user_db or password != user_db.get(user):
    print("user not exist wrong password")
    # block
print(f"Welcom back { user }")
```



```
1)
关联性
    a)非
    b)或
    c)且

2)顺序性
```
#### 【正向】【逆向】捕捉
```python
【正向】
示例：
user_db = {
    "Fin": "human"
}
print("Your name below：")
user = input()
if user in user_db:
    print("User exis， Please input your passwd")
    print("Your passwd below：")
    password = input()
    print("login successfull!")
else :
    print("User not exist exit!")
    exit()
---------------------------------------------------------
演示：
In [2]: user_db = {
   ...:     "Fin": "human"
   ...: }
   ...: print("Your name below：")
   ...: user = input()
   ...: if user in user_db:
   ...:     print("user exis and input your passwd")
   ...:     print("Your passwd below：")
   ...:     password = input()
   ...:     print("login successfull!")
   ...: else :
   ...:     print("User not exist， exit!")
   ...:     exit()
   ...:
Your name below
Fin
user exis and input your passwd
Your passwd below
human
login successfull!
---------------------------------------------------------
【逆向】
示例：
user_db = {
    "Fin": "human"
}
print("Your name below：")
user = input()
if not user in user_db:
    print("user not exis exit!")
    exit()
else :
    print("Your passwd below：")
    password = input()
    if password != user_db.get(user):
        print("wrong passwd exit!")
        exit()
    else :
        print("login successfull!")
---------------------------------------------------------
演示：
In [1]: user_db = {
   ...:     "Fin": "human"
   ...: }
   ...: print("Your name below：")
   ...: user = input()
   ...: if not user in user_db:
   ...:     print("user not exis exit!")
   ...:     exit()
   ...: else :
   ...:     print("Your passwd below：")
   ...:     password = input()
   ...:     if password != user_db.get(user):
   ...:         print("wrong passwd exit!")
   ...:         exit()
   ...:     else :
   ...:         print("login successfull!")
Your name below
Fin
Your passwd below
human
login successfull!
```
### 条件表达式技巧
```
print("write your comment.")
post = input()

if "@" in post:
    print("Invalid word")
elif len(post) > 10:
    print("comment cat less thwan 1 word more than 10 words")
elif not post:
    print("comment cant less than 1 word more than 10 words")
else:
    print("You said:",post)
---------------------------------------------------------------------
In [1]: print("write your comment.")
   ...: post = input()
   ...:
   ...: if "@" in post:
   ...:     print("Invalid word")
   ...: elif len(post) > 10:
   ...:     print("comment cat less thwan 1 word more than 10 words")
   ...: elif not post:
   ...:     print("comment cant less than 1 word more than 10 words")
   ...: else:
   ...:     print("You said:",post)
   ...:
write your comment.
wjw
You said: wjw
```
#### 表达式
```
1)函数方法
any()-其中有一个真，就为真。全是假，则为假。
In [4]: any([0,0,0,0])
Out[4]: False
In [5]: any([1,0,0])
Out[5]: True
2)列表解析
示例：
import string

print(string.punctuation)
#l = [p in "@iceking" for p in string.punctuation]

print("write your comment.")
post = input()

if any(p in post for p in string.punctuation):
    print("Invalid word")
elif len(post) > 10:
    print("comment cat less thwan 1 word more than 10 words")
elif not post:
    print("comment cant less than 1 word more than 10 words")
else:
    print("You said:",post)
-----------------------------------------------------------------------
演示：
In [6]: import string
   ...:
   ...: print(string.punctuation)
   ...: #l = [p in "@iceking" for p in string.punctuation]
   ...:
   ...: print("write your comment.")
   ...: post = input()
   ...:
   ...: if any(p in post for p in string.punctuation):
   ...:     print("Invalid word")
   ...: elif len(post) > 10:
   ...:     print("comment cat less thwan 1 word more than 10 words")
   ...: elif not post:
   ...:     print("comment cant less than 1 word more than 10 words")
   ...: else:
   ...:     print("You said:",post)
   ...:
!"#$%&'()*+,-./:;<=>?@[\]^_`{|}~
write your comment.
#happy
Invalid word
-----------------------------------------------------------------------
演示：
In [7]: import string
   ...:
   ...: print(string.punctuation)
   ...: #l = [p in "@iceking" for p in string.punctuation]
   ...:
   ...: print("write your comment.")
   ...: post = input()
   ...:
   ...: if any(p in post for p in string.punctuation):
   ...:     print("Invalid word")
   ...: elif len(post) > 10:
   ...:     print("comment cat less thwan 1 word more than 10 words")
   ...: elif not post:
   ...:     print("comment cant less than 1 word more than 10 words")
   ...: else:
   ...:     print("You said:",post)
   ...:
!"#$%&'()*+,-./:;<=>?@[\]^_`{|}~
write your comment.
happy
You said: happy
```
#### 三元表达-三元运算/三目运算
```
示例：
import random

a = "first" if random.choice([True,False]) else  "last"
print(a)
---------------------------------------------------------------------
In [8]: import random
   ...:
   ...: a = "first" if random.choice([True,False]) else  "last"
   ...: print(a)
first

In [9]: import random
   ...:
   ...: a = "first" if random.choice([True,False]) else  "last"
   ...: print(a)
last

In [10]: import random
    ...:
    ...: a = "first" if random.choice([True,False]) else  "last"
    ...: print(a)
first

In [11]: import random
    ...:
    ...: a = "first" if random.choice([True,False]) else  "last"
    ...: print(a)
last
```
### 注意事项-流的【终止符】
```
```
#### raise
```
```
#### sys.exit()
```
import sys
无论在哪儿使用，都会直接退出程序。
通常引用在编写命令行程序中。
```
#### 循环中
```
a)continue


b)break


```
#### 函数中
```
return


```

## 循环

```
a)循环是可以被控制的--break,continue,pass
------------------------------break-例子1-------------------------------
for i in range(20):
    if i == 4:
        break
    print(i)
0
1
2
3
----------------------------break-例子2---------------------------------
for i in [1, 2, 3, 4, 5, 9, 0, 3, 4, 9, 0]:
    if i == 0:
        break
    print(12 / i)
12.0
6.0
4.0
3.0
2.4
1.3333333333333333
------------------------------continue-例子1----------------------------
for i in range(20):
    if i == 4:
        continue
    print(i)
0 1 2 3 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19
--------------------------------continue-例子2--------------------------
for i in [1, 2, 3, 4, 5, 9, 0, 3, 4, 9, 0]:
    if i == 0:
        continue
    print(12 / i)
12.0
6.0
4.0
3.0
2.4
1.3333333333333333
4.0
3.0
1.3333333333333333
------------------------------------------------------------------------
b)
map()
reduce()
filter()

```

### 两种循环方式介绍

```python
a)
for loop
------------------------------------------------------------------------
z = [1, 2, 3, 4, 5, 6]
for i in z:
    print(i)
for i in range(20):
    print(i)

1 2 3 4 5 6 0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19
------------------------------------------------------------------------
s = [(1, 2),(3, 4),(5, 6)]
for i in s:
    print(i)
for i,j in s:
    print(i,j)
(1, 2)
(3, 4)
(5, 6)
1 2
3 4
5 6
------------------------------------------------------------------------
s = [(1, 2),(3, 4),(5, 6)]
for i in s:
    for j in i:
        print(j)
123456
------------------------------------------------------------------------
n = [1, 2, 3, 4]
m = [6, 7, 8, 9]
for i, j in zip(n,m):
    print(i, j)
1 6
2 7
3 8
4 9
注释：zip()前提n和m的长度是一样的
------------------------------------------------------------------------
z = [1, 2, 3, 4, 5]
for i in z:
    a = 1
    print(i)
1 2 3 4 5
b)
while loop
```

### for循环的特征

```
for i in [1,2,3]:
	do
for循环后端跟一个可以迭代的数据结构。
数据驱动型
```



### while 循环的特征

```
while 条件判断:
	do
while循环后面跟一个条件，循环直到这个条件不成立为止。
条件驱动型
```

### 死循环

```
while True，这个True就是死循环了。
```

### 函数

```
|一般参数

		 --|--定理1;所有参数在使用的时候都能以关键词参数的形式传参数
|关键词参数--|
		 --|--定理2:在定义函数时设置的关键词参数一般是用做默认参数
		 --|
		 --|--定理3:无论是在哪一个阶段，一般参数和关键词参数混用的时候是在一般参数的后面

	  |--偏函数--参数太多带状态生成不通用途的函数
|种类--|
	  |--装饰器
	  |
	  |--闭包 


      |--*args
|参数--|
	  |--**kwargs


			  |--同一个模块里面的函数
|不同位置的函数--|
			  |--不同模块包里面的函数
			  |
			  |--类里面的函数--@staticmethod



		 |--场景--|--简单的函数
		 |     --|
		 |     --|--函数作为参数的时候 map
		 |
		 |
|匿名函数--|
		 |--有参 lambda x:x+1
		 |
		 |--带条件 lambda x:x+1 ifisinstance(x,int)


|递归



匿名函数--
```



#### 函数概述

```
函数是最基本的数据处理单位
```

#### 函数 模块 包

```

```

#### 函数创建的原则

```
a)面向过程式
例子：
第一步：先扫描系统版本
第二步：检查环境变量
第三步：查找目标路径是否为空
b)面向功能式
面向功能和模块

c)按照数据分类

```

#### 函数的使用

```python
使用函数func()
z = print()

通常来说，函数都有一个结果，没设置结果返回None

import requests as r
r.get()

#给函数改名字，当一个函数的名字特别长时，可以通过修改函数的名字，来简化代码
pt = print 
pt('hello')

```

#### 函数的定义

```python
def name
def name_long_long():
	pass

#定义函数
def function():
    return 'something' #something指结果
#使用/调用函数
function()
```

#### 参数迷思

```
a = 1
b = 2
def add(a, b):
	return a+b

def do(first_int,second_int):
	return first_int * second_int
do(a,b)
```

#### 类型推断 trick--自动联想参数

```python
# 函数名(参数：参数类型)
# 函数名() -> 返回值的类型:
def example(head:str,butt:str) -> str:
	if head.startswith('?'):
		pass
	return head + ' ' + butt
e = example("hello","there")
print(e)
```

#### One more thing

```python
# 装饰器
# rule
# (func) -> func
------------------------------------------------------------------------
# lambda 参数:返回值
作用：
一行快速写函数，不需要给函数起名字
示例：
lambda : func() + 1
等同于
def no_name():
	return func() + 1
------------------------------------------------------------------------
def useless(func):
 return lambda:func() + 1
@useless
def one():
	return 1
print(one())
------------------------------------------------------------------------
def useless(func):
	def deco():
		return func() + 1
	return deco
@useless # 装饰器：接收一个函数，返回一个函数
def one():
	return 1
print(one())
```

#### 关键词传参

```python
def data_gen(m,d):
    return f'2019-{m}-{d}'

print(data_gen(11,11))
print(data_gen(m=11,d=11)) # 关键词参数
结果：
PS D:\WJWLearning> & D:/Python3.8/python.exe d:/WJWLearning/test.py
2019-11-11
2019-11-11
------------------------------------------------------------------------
def data_gen(m, d, y=2019):
    return f'{y}-{m}-{d}'

print(data_gen(11,11))
print(data_gen(m=11,d=11,y=2018))
PS D:\WJWLearning> & D:/Python3.8/python.exe d:/WJWLearning/test.py
2019-11-11
2018-11-11
------------------------------------------------------------------------
def formatter(num):
    if 1 <= num <=9:
        return f'0{num}'
    return num

def data_gen(m, d, y=2019):
    m = formatter(m)
    d = formatter(d)
    return f'{y}-{m}-{d}'

print(data_gen(8,11))
print(data_gen(m=11,d=11,y=2018))
PS D:\WJWLearning> & D:/Python3.8/python.exe d:/WJWLearning/test.py
2019-08-11
2018-11-11
```

#### 偏函数

```
def formatter(num):
    if 1 <= num <=9:
        return f'0{num}'
    return num

def date_gen(m, d, y=2019,sep='-'):
    m = formatter(m)
    d = formatter(d)
    return f'{y}{sep}{m}{sep}{d}'

# 偏函数：简化带有复杂参数的函数
def date_slash(m,d):
    return date_gen(m,d,y=2019,sep='/')

print(date_gen(m=1,d=11,y=2018))
print(date_slash(11,12))

PS D:\WJWLearning> & D:/Python3.8/python.exe d:/WJWLearning/test.py
2018-01-11
2019/11/12
------------------------------------------------------------------------
def formatter(num):
    if 1 <= num <=9:
        return f'0{num}'
    return num

def date_gen(m, d, y=2019,sep='-', with_prefix=None):
    m = formatter(m)
    d = formatter(d)
    if with_prefix:
        return f'{with_prefix}:{y}{sep}{m}{sep}{d}'
    return f'{y}{sep}{m}{sep}{d}'

# 偏函数：简化带有复杂参数的函数
def date_slash(m,d):
    return date_gen(m,d,y=2019,sep='/',with_prefix="日期")

print(date_gen(m=1,d=11,y=2018))
print(date_slash(11,12))

PS D:\WJWLearning> & D:/Python3.8/python.exe d:/WJWLearning/test.py
2018-01-11
日期:2019/11/12
```

#### 装饰器

#### 闭包

```
def setup():
	def inner():
		pass
	return inner
	
installer = setup()
install()
```

#### *args ,**kwargs

```
*args
用来给函数传递任意数量的参数，是个元组

**kwargs
用来给函数传递任意数量的成键值对的参数
```

```python
def formatter(num):
    if 1 <= num <=9:
        return f'0{num}'
    return num

def date_gen(m, d, y=2019,sep='-', with_prefix=None):
    m = formatter(m)
    d = formatter(d)
    if with_prefix:
        return f'{with_prefix}:{y}{sep}{m}{sep}{d}'
    return f'{y}{sep}{m}{sep}{d}'

# 偏函数：简化带有复杂参数的函数
def date_slash(m,d):
    return date_gen(m,d,y=2019,sep='/',with_prefix="日期")

def show(*args,**kwargs):
    print(args)
    print(kwargs)

print(date_gen(m=1,d=11,y=2018))
print(date_slash(11,12))
print(show(1,2,3,something='hello'))

PS D:\WJWLearning> & D:/Python3.8/python.exe d:/WJWLearning/test.py
2018-01-11
日期:2019/11/12
(1, 2, 3)
{'something': 'hello'}
None
------------------------------------------------------------------------
def formatter(num):
    if 1 <= num <=9:
        return f'0{num}'
    return num

def date_gen(m, d, y=2019,sep='-', with_prefix=None):
    m = formatter(m)
    d = formatter(d)
    if with_prefix:
        return f'{with_prefix}:{y}{sep}{m}{sep}{d}'
    return f'{y}{sep}{m}{sep}{d}'

# 偏函数：简化带有复杂参数的函数
def date_slash(m,d):
    return date_gen(m,d,y=2019,sep='/',with_prefix="日期")

def date_with_sub(m,d,*args):
    sub = f'''
    |
    +--> { ''.join(args) }
    '''
    main_str = date_gen(m,d,y=2019,sep='/',with_prefix="日期")
    return main_str + sub

print(date_gen(m=1,d=11,y=2018))
print(date_slash(11,12))
print(date_with_sub(12,12,"buy a lot","sleep","eat"))

PS D:\WJWLearning> & D:/Python3.8/python.exe d:/WJWLearning/test.py
2018-01-11
日期:2019/11/12
日期:2019/12/12
    |
    +--> buy a lotsleepeat
    |
```

#### 不同位置的函数

##### 同级文件--可被其他同级文件调用

```
pkg.py内容如下：

DEBUG = True
PORT = '8000'
PWD = 'le9Jfh6J'

def gen(num):
    print(num)

def make():
    print("well done")
------------------------------------------------------------------------
test.py内容如下：

import pkg

pkg.DEBUG
pkg.make()
pkg.gen()
pkg.PORT
pkg.PWD
```

##### 类

```python
class Nothing:
    @staticmethod
    def useless():
        print("nothing")
Nothing.useless()

class Tools:
    @staticmethod
    def knife():
        print("nothing")
Tools.knife()
```

##### 匿名函数

```
lambda:
lambda函数的使用场景就是,当一个函数是简单的返回拼接值的时候，比如说返回一个以这个值为基准且比它加1的一个数。
```

```python
result = lambda x:x+1
print(result(12))
PS D:\WJWLearning> & D:/Python3.8/python.exe d:/WJWLearning/test.py
13
------------------------------------------------------------------------
result2 = map(lambda x:x+1,[1,2,3])
print(list(result2))
PS D:\WJWLearning> & D:/Python3.8/python.exe d:/WJWLearning/test.py
[2, 3, 4]
```

##### 递归

```
def some():
    return some()

场景：扫描文件
def scan():
    # lots stuff here
    if find this:
        return 'file'
    scan()
```

## 示例：文件搜索

```python
# 王军伟
# 2022/03/22
# 文件扫描程序

#思路：
#告诉计算机文件的位置
##使用路径描述位置
###绝对路径,从根目录开始
###内置OS模块：路径，目录，文件，其他操作系统
#描述文件的特征
##描述文件特征
##用条件判断来帅选：包含fish，以.png结尾
#比对后打印文件名
##用循环来实现逐个比对

import os
path = 'D:\WJWDevOps\心得'
files = os.listdir(path)

for f in files:
    if 'docker' in f and f.endswith('.png'):
        print('Found it!' + f)
```

## 示例：文件按格式自动归类

```python
# 王军伟
# 2022/03/22
# 文件按格式自动归类

#思路：
#如何移动文件
##使用内置模块
##shutil.move
#归类的规则是什么
##手动预设文件夹
##自动创建文件夹（本次）

#coding:utf-8
import os
import shutil

path = './' # 当前目录
files = os.listdir(path)

for f in files:
    # f.png
    # ./png
    folder_name = './' + f.split('.')[-1] # 比如file_name.png -> ['file_name','png']
    if not os.path.exists(folder_name):
        os.makedirs(folder_name) # makefolder()
        shutil.move(f,folder_name) # movefiletofolder()
    else:
        shutil.move(f,folder_name) # movetofolder()
```

## 示例：自动解压并删除zip

```python
# 王军伟
# 2022/03/22
# 如何自动解压并删除zip

#思路：
# scan -- unzip -- delete
#如何解压
##使用内置模块来实现--shutil.unpack_archive
#如何删除zip
##使用内置模块OS来实现--os.remove
#如何检测zip文件的出现
##如何判断某文件是zip
##如何让函数每一秒都执行--While True

#coding:utf-8
import os
import shutil

def scan_file():
    files = os.listdir()
    for f in files:
        if f.endswith('.zip'):
            return f

def unzip_it(f):
    folder_name = f.split('.')[0]
    target_path = './' + folder_name
    os.makedirs(target_path)
    shutil.unpack_archive(f,target_path)

def delete(f):
    os.remove(f)

while True:
    zip_file = scan_file()
    if zip_file:
        unzip_it(zip_file)
        delete(zip_file)
```

## 示例：自动压缩文件

```
监测image 文件夹,如果包含的文件大于等于5个，则将这些文件压缩到archive1.zip文件中，并删除这些文件。当再次监测到文件多于5个的时候，生成archive2 ,z1p压缩包, 以此类推。

问题拆解提示
该问题可以拆解为如下若干子问题:
1.如何监测文件夹中的文件多于5个?
	OS库中的listdir函数可以获取一个文件夹中的所有文件名并存入list 变量中，那么统计这个list变量中元素的个数，即可得到文件夹中的文件数。同时，利用while True和time.sleep()的配合，可以实现每隔一段时间执行一段代码的功能。
2.如何生成压缩包?
	利用shutil 库中的 make. archive函数来生 成压缩包。
3.如何删除文件?
	利用OS库中的remove函数来删除文件。因为要删除文件夹中的所有文件，所以配合listdir 函数生成的 files变量一起使用。
shutil库中的make. archive函数可以生成压缩包， 使用方法如下:
make. archive(path1，'zip', path2)
其中path1 是生成压缩包的路径(包含压缩包名称)，path2 是需要被压缩的文件夹。
```

```Python
# 王军伟
# 2022/03/23
# 如何自动压缩文件

#coding:utf-8
from shutil import make_archive
import os
import time

#指定需要监测的文件夹
image_path = './image'

#指定压缩包存放的文件夹
output_path = './output'

#记录生成了多少个压缩包
zip_count = 0

#利用while True使用程序持续运行
while True:
    files = os.listdir(image_path)
    #files变量中存储了路径下所有文件的文件名，len()函数可以获取list变量包含多少个元素
    #files_count即为路径下文件的个数
    files_count = len(files)
    if files_count >= 5:
        zip_count = zip_count + 1
        #指定压缩包的名称以及路径
        zip_name = output_path + '/' + 'archive' + str(zip_count)
        #压缩文件
        make_archive(zip_name,'zip',image_path)
        #删除压缩过的文件
        for f in files:
            os.remove(image_path + '/' + f)
    # 休眠1秒，达到每一秒监测一次的结果
    time.sleep(1)
```

## 示例：删除重复文件

```python
# 王军伟
# 2022/03/23
# 如何删除重复文件

#问题拆解提示
#如何删除重复文件可以拆解为以下4个子问题:
#1.如何将所有文件都存放到一个list变量中?
#2.如何判断两个文件的内容是否一致?
#3.如何判断在很多文件中找到一对重复的文件?
#4.如何删除文件?
#问题解决提示
#1.假设我们的文件夹只有一层， 没有嵌套的文件夹，那么，利用os模块中的listdir函数和for循环配合，就可以浏览所有文件。在浏览文件的同时，记录下每个文件的路径，并存储到ist变量中，我们就得到了所有文件的集
#2.利用filecmp模块中的cmp函数，判断两个文件的内容是否-致。如果一致，函数返回True;如果不一致， 函数返回False.
#3.对一个list变量，使用双审for循环，或以对list中的元索进行两两对比。第一层循环相当于从list中取出一个元素x，第二层循环相当于取出list中的另一个元索y，比较所有的x和y，即实现了对list中所有元索的两两对比。
#4.利用os模块中的remove函数，可以删除指定位置的文件。

# coding:utf-8
import os
import filecmp

#需要把路径替换成你的文件夹所在路径，当把这个代码文件放在要处理的文件夹外层时，可以使用下面的相对路径写法
path = './problem3_files'

# 已知路径下存在两个文件夹pic1和pic2
dirs = ['pic1','pic2']

# 将指定目录下的所有文件的路径存储到all_files变量中
def get_all_files(path, dirs):
    all_files = []
    for d in dirs:
        cur_path = path + '/' + d
        files = os.listdir(cur_path)
        for f in files:
            all_files.append(cur_path + '/' + f)
        return all_files

#比较两个文件的内容是否一致
def cmp_files(x, y):
    if filecmp.cmp(x, y):
        # 如果一致，则删除第二个，保留第一个，并输出信息
        os.remove(y)
        print("路径\"" + y + "\"下的文件是重复文件，已经删除")

# 调用函数，获取文件列表
all_files = get_all_files(path, dirs)

# 用双重for循环来比较文件是否有重复
for x in all_files:
    for y in all_files:
        #如果x和y不是相同的文件，而且都存在，则执行后续操作
        if x != y and os.path.exists(x) and os.path.exists(y):
            # 比较两个文件内容是否一致
            cmp_files(x, y)
```

## 示例：定制群发微信消息

```
# 如何读取csv?
## 使用内置模块csv
# 如何按对应信息发送到微信?
## 使用第三方库wxpy
```

```python
import
import

```

