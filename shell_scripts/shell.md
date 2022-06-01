# shell

## 一、shell概述

```shell
Shell俗称壳，是指“为使用者提供操作界面”的软件（命令解析器）。
它接收应用程序或者用户命令，然后调用操作系统内核，内核再调用硬件来操作。
```

```shell
系统最内层的是硬件，然后是Linux系统内核。shell介于用户和系统内核之间。

Shell Script指的是针对用shell所写的脚本。将一些shell规定的语法与命令，搭配正则表达式、管道命令与数据流重定向等功能，写成一个纯文本文件以达到我们想要的处理目的，再使用.sh的扩展名。

通过Shell工具来解释我们的命令或请求，再搭配Shell script可以批量处理命令，这样我们可以与计算机更好地交互。

Shell是一个功能相当强大的编程语言,易编写、易调试、灵活性强。
```

## 二、shell解释器

```shell
(1)Linux提供的Shell解释器有：
[root@wjw shell]# cat /etc/shells 
/bin/sh
/bin/bash
/usr/bin/sh
/usr/bin/bash
/usr/bin/fish
/bin/tcsh
/bin/csh
```

```shell
(2)bash和sh的关系
在Redhat系列的Linux操作系统中的/bin/sh是/bin/bash的链接。用sh执行脚本和bash执行脚本，效果是一样的。

[root@wjw bin]# ll | grep bash
-rwxr-xr-x.   1 root root      964536 Nov 24 13:33 bash
lrwxrwxrwx.   1 root root          10 Dec  8 03:45 bashbug -> bashbug-64
-rwxr-xr-x.   1 root root        6964 Nov 24 13:33 bashbug-64
lrwxrwxrwx.   1 root root           4 Dec  8 03:45 sh -> bash
```

```shell
(3)Centos默认的解释器是bash
[root@wjw bin]# echo $SHELL
/bin/bash
```

## 三、shell脚本入门

```shell
(1)脚本格式
脚本以#!/bin/bash开头(指定解析器)
```

```shell
(2)第一个shell脚本
创建一个名为helloworld.sh的文件，在其中写入
#!/bin/bash
echo "helloworld"
```

```shell
(3)执行脚本
[root@wjw shell]# bash helloworld.sh
```

```shell
(4)第二个shell脚本
#！/bin/bash
 cd /home/wjw/shell
 touch cls.txt
 echo "ban zhang" >> cls.txt
```

## 四、shell中的变量

### 1.常用系统变量

```shell 
$HOME
$PWD
$SHELL
$USER
...
[root@wjw shell]# echo $HOME
/root
[root@wjw shell]# echo $PWD
/home/wjw/shell
[root@wjw shell]# echo $SHELL
/bin/bash
[root@wjw shell]# echo $USER
root
```

### 2.自定义变量

```shell
(1)定义变量基本语法：变量=值
！！！注意：这里不能加空格
(2)声明静态变量:readonly 变量，注意:不能unset # 当电脑重新启动后，会消失
(3)unset 命令用于撤销变量：unset 变量
[root@wjw shell]# a=5
[root@wjw shell]# b=5
[root@wjw shell]# echo $a+$b
5+5
[root@wjw shell]# unset a
[root@wjw shell]# unset b
[root@wjw shell]# echo $a

[root@wjw shell]# echo $b

```

### 3.变量定义规则

```shell
(1)变量名称可以由字母、数字和下划线组成，但是不能以数字开头，环境变量名建议大写。
(2)等号两侧不能有空格。
(3)在bash中，变量默认类型都是字符串类型，无法直接进行数值运算。
[root@wjw shell]# a=5
[root@wjw shell]# b=5
[root@wjw shell]# echo $a+$b
5+5
(4)变量的值如果有空格，需要使用双引号或单引号括起来。
(5)可把变量提升为全局环境变量，可供其他Shell程序使用。
export 变量名
```

### 4.特殊变量：$n

```shell
基本语法
$n (功能描述: n为数字，$0 代表该脚本名称，$1-$9 代表第一到第九个参数，十以上的参数，十以上的参数需要用大括号包含，如${10})。
```

### 5.特殊变量：$#

```shell
基本语法
$# (功能描述:获取所有输入参数个数，常用于循环)。
```

### 6.特殊变量：$*、$@

```shell
基本语法
$* (功能描述: 这个变量代表命令行中所有的参数，$*把所有的参数看成一个整体)。
$@ (功能描述:这个变量也代表命令行中所有的参数,不过$@把每个参数区分对待)。
```

### 7.特殊变量：$?

```shell
基本语法
$? (功能描述:最后一次执行的命令的返回状态。如果这个变量的值为0,证明上一个命令正确执行;如果这个变量的值为非0[具体是哪个数，由命令自己来决定]，则证明上一个命令执行不正确了。)。
```

### 8.特殊变量：$$

```shell
Shell本身的PID（ProcessID）
```

### 9.特殊变量：$!

```shell
Shell最后运行的后台Process的PID
```

### 10.特殊变量：$0

```she
Shell本身的文件名
```



## 五、运算符

```shell
1.基本语法。
(1)“$((运算式))"或“$[运算式]”
(2) expr +, -, \*, /, % 加，减，乘，除，取余
注意: expr 运算符间要有空格。expr是一款表达式计算工具，使用它能完成表达式的求值操作。
2.实例
(1)
[root@wjw shell]# expr 2 + 3
5
(2)
[root@wjw shell]# expr 3 - 2
1
(3)-(a)
[root@wjw shell]# expr `expr 2 + 3` \* 4
20
注意：``符号为Esc下面那个符号，反引号。
(3)-(b)
[root@wjw shell]# s=$[(2+3)*4]
[root@wjw shell]# echo $s
20
(3)-(c)
[root@wjw shell]# n=$(((2+3)*4))
[root@wjw shell]# echo $n
20
```

## 六、条件判断

```shell
1.基本语法。
[ condition ] (注意condition前后要有空格)。
注意:条件非空即为true, [ atguigu ]返回true, [] 返回false。
2.常用判断条件
(1)两个整数之间比较
= 字符串比较
-lt 小于(less than)
-le 小于等于( less equal)
-eq 等于(equal)
-gt 大于(greater than) 
-ge 大于等于( greater equal)
-ne 不等于(Not equal)
(2)按照文件权限进行判断
-r 有读的权限(read )
-W 有写的权限(write) 
-x 有执行的权限(execute) 
(3)按照文件类型进行判断。
-f 文件存在并且是一个常规的文件(file)
-e 文件存在(existence)
-d 文件存在并是一个目录(directory)
(4)多条件判断(&& 表示前一条命令执行成功时，才执行后一条命令，|| 表示上一条命令执行
失败后，才执行下一条命令)。

(5)实例
[root@wjw shell]#  [ 23 -ge 22 ] 
[root@wjw shell]# echo $?
[root@wjw shell]# [ -w helloworld.sh ]
[root@wjw shell]# echo $?
0
[root@wjw shell]#  [ -e helloworld.sh ]
[root@wjw shell]# echo $?
0
[root@wjw shell]#  [ condition ] && echo OK || echo notok
OK
[root@wjw shell]#  [ condition ] && [ ] || echo notok
notok
```

## 七、流程控制(重点)

```shell
1.if判断
(1)基本语法
if [ 条件判断式 ];then
	程序
fi
或者
if [ 条件判断式 ]
then
程序
fi
注意事项:
(a) [ 条件判断式 ]，中括号和条件判断式之间必须有空格。
(b) if后要有空格
(2)实例：输入一个数字，如果是1，则输出ban zhang zhen shuai, 如果是2，则输出cls zhen mei,如果是其它，什么也不输出。
#!/bin/bash
if [ $1 -eq 1 ];then
        echo "ban zhang zhen shuai"
elif [$1 -eq 2 ];then
        echo "cls zhen mei"
fi
(3)运行
[root@wjw shell]# bash ifpanduan.sh 1
ban zhang zhen shuai
[root@wjw shell]# bash ifpanduan.sh 2
cls zhen mei
[root@wjw shell]# bash ifpanduan.sh 3
[root@wjw shell]# 
```

```shell
2.case语句
(1)基本语法
case $变量名 in
"值1")
	如果变量的值等于值1，则执行程序1
	;;
"值2")
	如果变量的值等于值2，则执行程序2
	;;
...省略其他分支...
*)
	如果变量的值都不是以上的值，则执行此程序
	;;
esac
注意事项:
(a) case 行尾必须为单词“in”，每一个模式匹配必须以右括号“)”结束。
(b)双分号 “;;”表示命令序列结束，相当于java中的break。
(c)最后的 “*)”表示默认模式，相当于java中的default。
(2)实例输入一个数字，如果是1,则输出banzhang, 如果是2,则输出cls, 如果是其它，输出renyao。
#!/bin/bash

case $1 in
"1")
        echo "ban zhang"
;;
"2")
        echo "cls"
;;
*)
        echo "renyao"
;;
esac
(3)运行
[root@wjw shell]# bash case.sh 1
ban zhang
[root@wjw shell]# bash case.sh 2
cls
[root@wjw shell]# bash case.sh 3
renyao
```

```shell
3.for循环
(1)-(1)基本语法1
for (( 初始值;循环控制条件;变量变化 ))
	do
		程序
	done
(1)-(2)实例：从1加到100
#!/bin/bash
s=0
for (( i=1;i<=100;i++ ))
do
        s=$[$s+$i]
done
        echo $s
(1)-(3)运行
[root@wjw shell]# bash for1.sh 
5050

```

```shell
(2)-(1)基本语法2
for 变量 in 值1 值2 值3...
do
	程序
done
(2)-(2)实例：打印所有输入参数
#!/bin/bash

for i in $*
do
        echo "ban zhang love $i"
done

(2)-(3)运行
[root@wjw shell]# bash for2.sh mm
ban zhang love mm
[root@wjw shell]# bash for2.sh mm cls
ban zhang love mm
ban zhang love cls
[root@wjw shell]# bash for2.sh mm cls bd
ban zhang love mm
ban zhang love cls
ban zhang love bd
```

```shell
(2)-(4)实例
#!/bin/bash

for i in "$*"
do
        echo "ban zhang love $i"
done

for j in "$@"
do
        echo "ban zhang love $j"
done

(2)-(5)运行
[root@wjw shell]# bash for2.sh mm
ban zhang love mm
ban zhang love mm
[root@wjw shell]# bash for2.sh mm cls
ban zhang love mm cls
ban zhang love mm
ban zhang love cls
[root@wjw shell]# bash for2.sh mm cls bd
ban zhang love mm cls bd
ban zhang love mm
ban zhang love cls
ban zhang love bd
(2)-(6)实例
#!/bin/bash

for i in $*
do
        echo "ban zhang love $i"
done

for j in $@
do
        echo "ban zhang love $j"
done

(2)-(7)运行
[root@wjw shell]# bash for2.sh mm
ban zhang love mm
ban zhang love mm
[root@wjw shell]# bash for2.sh mm cls
ban zhang love mm
ban zhang love cls
ban zhang love mm
ban zhang love cls
[root@wjw shell]# bash for2.sh mm cls bd
ban zhang love mm
ban zhang love cls
ban zhang love bd
ban zhang love mm
ban zhang love cls
ban zhang love bd
```

```shell
4.while循环
(1)基本语法
while [ 条件判断式 ]
do
	程序
done
(2)实例：从1加到100
#!/bin/bash
i=1
s=0
while [ $i -le 100 ]
do
        s=$[$s + $i]
        i=$[$i + 1]
done
        echo $s
(3)运行
[root@wjw shell]# bash while.sh 
5050
```

```
5.等待上一条命令执行结束在执行下一条
(1)基本语法
&& 符号
示例：shell1 && shell2 && shell3

```



## 八、read读取控制台输入

```shell
(1)基本语法。
read(选项)(参数)
选项:
	-p:指定读取值时的提示符:
	-t:指定逮取值时等待的时间(秒)
参数
	变量:指定读取值的变量名。
(2)实例：提示7秒内，读取控制台输入的名称。
#!/bin/bash
read -t 7 -p "Enter your name in 7 seconds" NAME
echo $NAME
(3)运行
[root@wjw shell]# bash read.sh 
Enter your name in 7 seconds wjw
wjw

```

## 九、函数

```shell
1.系统函数
(1)-(1)basename基本语法
basename [string / pathname] [suffix] 
功能描述: basename 命令会删掉所有的前缀包括最后一个(“/) 字符，然后将字符串显示出来。
选项:
suffix为后缀,如果suffix被指定了, basename会将pathname或string 中的suffx去掉。
(1)-(2)实例
[root@wjw wjw]# basename /home/wjw/wjw.txt
wjw.txt
[root@wjw wjw]# basename /home/wjw/wjw.txt .txt
wjw
(2)-(1)dirname 基本语法
dirname 文件绝对路径 
功能描述:从给定的包含绝对路径的文件名中去除文件名(非目录的部分)，然后返回剩下的路径(目录的部分) 。
(2)-(2)实例：获取wjw.txt文件的路径。
[root@wjw wjw]# dirname /home/wjw/wjw.txt 
/home/wjw
2.自定义函数
(1)基本语法
[ function ] funname[()]
{
	Action;
	[return int;]
}
funname
(2)经验技巧
(a)必须在调用函数地方之前，先声明函数，shell脚本是逐行运行。不会像其它语言一样先编译。
(b函数返回值，只能通过$?系统变量获得，可以显示加: return 返回，如果不加，将以最后一条命令运行结果，作为返回值。return 后跟数值n(0-255)。
(c)实例：计算两个输入参数的和
#!/bin/bash

function sum()
{
        s=0;
        s=$[$1 + $2]
        echo $s
}

read -p "input your number1" p1
read -p "input your number2" p2

sum $p1 $p2
(d)运行
[root@wjw wjw]# bash fun.sh 
input your number1 1
input your number2 2
3

```

## 十、shell工具（重点）

```shell
1.cut
cut的工作就是“剪”，具体的说就是在文件中负责剪切数据用的。cut命令从文件的每一行剪切字节、字符和字段并将这些字节、字符和字段输出。
(1)基本用法
cut [选项参数] filename
说明:默认分隔符是制表符。
(2)选项参数说明
	-f	列号，提取第几列
	-d	分隔符，按照指定分隔符分割列
(3)实例
banzhang.txt内容如下

hang shen(1space)
zhou zhen(1space)
wo  wo(2space)
lai  lai(2space) 
le  le(2space)

(4)运行
[root@wjw shell]# cut -d " " -f 1 banzhang.txt 
hang
zhou
wo
lai
le
[root@wjw shell]# cut -d " " -f 2,3 banzhang.txt 
shen
zhen
 wo
 lai
 le
[root@wjw shell]# cut -d " " -f 2 banzhang.txt 
shen
zhen



[root@wjw shell]# cut -d " " -f 3 banzhang.txt 


wo
lai
le
[root@wjw shell]# cat banzhang.txt | grep guan | cut -d " " -f 1
guan

[root@wjw shell]# echo $PATH
/root/anaconda3/bin:/usr/lib64/qt-3.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/root/bin:/usr/local/mpich/bin
[root@wjw shell]# echo $PATH | cut -d : -f 3-
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/root/bin:/usr/local/mpich/bin

！！！实例：切割ifconfig后打印的IP地址
[root@wjw shell]# ifconfig 
docker0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 172.17.0.1  netmask 255.255.0.0  broadcast 172.17.255.255
        inet6 fe80::42:1bff:fe7a:c3e9  prefixlen 64  scopeid 0x20<link>
        ether 02:42:1b:7a:c3:e9  txqueuelen 0  (Ethernet)
        RX packets 10  bytes 555 (555.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 14  bytes 1397 (1.3 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

 enp5s0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 10.20.18.51  netmask 255.255.254.0  broadcast 10.20.19.255
        inet6 fe80::1a76:4997:c7d8:3cbb  prefixlen 64  scopeid 0x20<link>
        ether c0:3f:d5:e0:9d:3e  txqueuelen 1000  (Ethernet)
        RX packets 6969780  bytes 1049689876 (1001.0 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 1455745  bytes 142286209 (135.6 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 591644  bytes 57375701 (54.7 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 591644  bytes 57375701 (54.7 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

veth24d5349: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet6 fe80::f8fb:b8ff:fe53:fb1f  prefixlen 64  scopeid 0x20<link>
        ether fa:fb:b8:53:fb:1f  txqueuelen 0  (Ethernet)
        RX packets 0  bytes 0 (0.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 8  bytes 788 (788.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

veth8dfb465: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet6 fe80::c4f6:71ff:fe57:610d  prefixlen 64  scopeid 0x20<link>
        ether c6:f6:71:57:61:0d  txqueuelen 0  (Ethernet)
        RX packets 0  bytes 0 (0.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 8  bytes 788 (788.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

vethd93815f: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet6 fe80::581f:a2ff:fe1d:e940  prefixlen 64  scopeid 0x20<link>
        ether 5a:1f:a2:1d:e9:40  txqueuelen 0  (Ethernet)
        RX packets 10  bytes 695 (695.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 18  bytes 1837 (1.7 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

virbr0: flags=4099<UP,BROADCAST,MULTICAST>  mtu 1500
        inet 192.168.122.1  netmask 255.255.255.0  broadcast 192.168.122.255
        ether 52:54:00:74:c5:96  txqueuelen 1000  (Ethernet)
        RX packets 0  bytes 0 (0.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 0  bytes 0 (0.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

[root@wjw shell]# ifconfig enp5s0 | grep "inet" | grep "netmask" | cut -d " " -f 10
10.20.18.51
```

```shell
2.sed
sed是一种流编辑器，它一次处理一行内容。处理时，把当前处理的行存储在临时缓冲区中，称为“模式空间”，接着用sed命令处理缓冲区中的内容，处理完成后，把缓冲区的内容送往屏幕。接着处理下一行，这样不断重复，直到文件末尾。文件内容并没有改变，除非你使用重定向存储输出。
(1)基本用法。
sed [选项参数] 'command' filename
(2)选项参数说明
-e 直接在指令列模式上进行sed的动作编辑
(3)命令功能描述
a 新增，a的后面可以接字符串，在下一行出现
d 删除
s 查找并替换
(4)实例
sed.txt内容如下
hang shen
zhou zhen
wo  wo
lai lai

le le
(4)-(a)将"mei nv"这个单词插入到sed.txt第二行下，打印。
[root@wjw shell]# sed "2a mei nv" sed.txt
hang shen
zhou zhen
mei nv
wo  wo
lai lai

le le
[root@wjw shell]# cat sed.txt 
hang shen
zhou zhen
wo  wo
lai lai

le le
！！！注意：文件并没有改变
(4)-(b)删除sed.txt文件所有包含wo的行
[root@wjw shell]# sed "/wo/d" sed.txt 
hang shen
zhou zhen
lai lai

le le
[root@wjw shell]# cat sed.txt 
hang shen
zhou zhen
wo  wo
lai lai

le le
！！！注意：文件并没有改变
(4)-(c)将sed.txt文件中wo替换为ni
[root@wjw shell]# sed "s/wo/ni/g" sed.txt
hang shen
zhou zhen
ni  ni
lai lai

le le
[root@wjw shell]# sed "s/wo/ni/" sed.txt
hang shen
zhou zhen
ni  wo
lai lai

le le
！！！注意：文件并没有改变
这里需要说明一下：g(global)表示全局替换，也就是说会替换掉所有位置，没有加g，那么仅会替换掉第一个。
(4)-(d)将sed.txt文件中的第二行删除并将wo替换为ni
[root@wjw shell]# sed -e "2d" -e "s/wo/ni/g" sed.txt 
hang shen
ni  ni
lai lai

le le
```

```shell
3.awk
一个强大的文本分析工具，把文件逐行的读入，以空格为默认分隔符将每行切片，切开的部分再进行分析处理。
(1)基本用法
awk [选项参数] 'pattern1 {actionl} pattern2 {action2}...' filename
pattern:表示AWK在数据中查找的内容，就是匹配模式
action:在找到匹配内容时所执行的一系列命令
(2)选项参数说明
-F 指定输入文件拆分分隔符
-v 赋值一个用户定义变量
(3)实例
(3)-(a)数据准备
[root@wjw shell]# cp /etc/passwd ./
(3)-(b)搜索passwd文件以root关键字开头的所有行，并输出该行的第7列。
命令：
[root@wjw shell]# awk -F : '/^root/ {print $7}' passwd
结果：
/bin/bash
注意：/^表示开头
(3)-(c)搜索passwd文件以root关键字开头的所有行，并输出该行的第1列和第7列，中间以“,”号分割。
命令：
[root@wjw shell]# awk -F : '/^root/ {print $1","$7}' passwd
结果：
root,/bin/bash
注意：只有匹配了pattern 的行才会执行action
(3)-(d)只显示/etc/passwd的第一列和第七列,以逗号分割，且在所有行前面添加列名user,shell在最后一行添加"dahaige, /bin/zuishuai"。
命令：
[root@wjw shell]# awk -F : 'BEGIN{print "user,shell"} {print $1","$7} END{print "dahaige,/bin/zuishuai"}' passwd
结果：
user,shell
root,/bin/bash
bin,/sbin/nologin
daemon,/sbin/nologin
adm,/sbin/nologin
lp,/sbin/nologin
sync,/bin/sync
shutdown,/sbin/shutdown
halt,/sbin/halt
mail,/sbin/nologin
operator,/sbin/nologin
games,/sbin/nologin
ftp,/sbin/nologin
nobody,/sbin/nologin
systemd-network,/sbin/nologin
dbus,/sbin/nologin
polkitd,/sbin/nologin
sshd,/sbin/nologin
postfix,/sbin/nologin
chrony,/sbin/nologin
virftp,/sbin/nologin
tss,/sbin/nologin
rpc,/sbin/nologin
setroubleshoot,/sbin/nologin
gluster,/sbin/nologin
libstoragemgmt,/sbin/nologin
unbound,/sbin/nologin
usbmuxd,/sbin/nologin
rtkit,/sbin/nologin
radvd,/sbin/nologin
ntp,/sbin/nologin
saslauth,/sbin/nologin
qemu,/sbin/nologin
pulse,/sbin/nologin
saned,/sbin/nologin
colord,/sbin/nologin
abrt,/sbin/nologin
geoclue,/sbin/nologin
gdm,/sbin/nologin
sssd,/sbin/nologin
gnome-initial-setup,/sbin/nologin
tcpdump,/sbin/nologin
avahi,/sbin/nologin
rpcuser,/sbin/nologin
nfsnobody,/sbin/nologin
mysql,/sbin/nologin
wjw,/bin/bash
wang,/bin/bash
test1,/bin/bash
git,/usr/bin/git-shell
user1,/bin/bash
apache,/sbin/nologin
dahaige,/bin/zuishuai
注意: BEGIN 在所有数据读取行之前执行；END在所有数据执行之后执行。
(3)-(e)将passwd文件中的用户id增加数值1并输出
[root@wjw shell]# awk -F : -v i=1 '{print $3+i}' passwd
1
2
3
4
5
6
7
8
9
12
13
15
100
193
82
1000
75
90
999
1001
60
33
998
997
996
995
114
173
76
39
994
108
172
993
992
174
991
43
990
989
73
71
30
65535
28
1002
1003
1004
1005
1006
49
(4)awk的内置变量
FILENAME 文件名。
NR 已读的记录数。从上到下，行号。
NF 浏览记录的域的个数(切割后，列的个数)
(4)-(a)统计passwd文件名，每行的行号，每行的列数
[root@wjw shell]# awk -F : '{print FILENAME "," NR "," NF}' passwd
运行：
passwd,1,7
passwd,2,7
passwd,3,7
passwd,4,7
passwd,5,7
passwd,6,7
passwd,7,7
passwd,8,7
passwd,9,7
passwd,10,7
passwd,11,7
passwd,12,7
passwd,13,7
passwd,14,7
passwd,15,7
passwd,16,7
passwd,17,7
passwd,18,7
passwd,19,7
passwd,20,7
passwd,21,7
passwd,22,7
passwd,23,7
passwd,24,7
passwd,25,7
passwd,26,7
passwd,27,7
passwd,28,7
passwd,29,7
passwd,30,7
passwd,31,7
passwd,32,7
passwd,33,7
passwd,34,7
passwd,35,7
passwd,36,7
passwd,37,7
passwd,38,7
passwd,39,7
passwd,40,7
passwd,41,7
passwd,42,7
passwd,43,7
passwd,44,7
passwd,45,7
passwd,46,7
passwd,47,7
passwd,48,7
passwd,49,7
passwd,50,7
passwd,51,7
(4)-(b)切割IP
[root@wjw shell]# ifconfig enp5s0
enp5s0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 10.20.18.51  netmask 255.255.254.0  broadcast 10.20.19.255
        inet6 fe80::1a76:4997:c7d8:3cbb  prefixlen 64  scopeid 0x20<link>
        ether c0:3f:d5:e0:9d:3e  txqueuelen 1000  (Ethernet)
        RX packets 8871352  bytes 1388317286 (1.2 GiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 1864380  bytes 181922275 (173.4 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
[root@wjw shell]# ifconfig enp5s0| grep "netmask" | awk -F " " '{print $2}'
运行：
10.20.18.51
(4)-(c)查询sed.txt中空行所在的行号
[root@wjw shell]# cat sed.txt 
hang shen
zhou zhen
wo  wo
lai lai

le le
[root@wjw shell]# awk '/^$/{print NR}' sed.txt 
运行：
5
注意：/^表示开头 $/表示结尾，中间没有内容，表示空行。
```

```shell
4.sort
sort命令是在Linux里非常有用，它将文件进行排序，并将排序结果标准输出。
(1)基本语法
sort(选项)(参数)
```

| 选项 |           说明           |
| :--: | :----------------------: |
|  -n  |    依照数值的大小排序    |
|  -r  |    以相反的顺序来排序    |
|  -t  | 设置排序时所用的分隔字符 |
|  -k  |     指定需要排序的列     |
| 参数 |   指定待排序的文件列表   |

```shell
(2)实例
[root@wjw shell]# cat sort.txt 
bb:40:5.4
bd:20:4.2
xz:50:2.3
cls:10:3.5
ss:30:1.6
运行：
[root@wjw shell]# sort -t : -nrk 2 sort.txt 
xz:50:2.3
bb:40:5.4
ss:30:1.6
bd:20:4.2
cls:10:3.5
```

## 十一、企业面试题

```shell
1.使用Linux命令查询file1中空行所在的行
[root@wjw shell]# '/^$/{print NR}' filename
2.有文件chengji.txt内容如下:
张三 40
李四 50
王五 60
使用Linux命令计算第二列的和并输出
[root@wjw shell]# chengji.txt | awk -F " " '{sum+=$2} END{print sum}'
150
3.Shell脚本里如何检查一个文件是否存在?如果不存在该如何处理?
#!/bin/bash
if [ -e file.txt ]; then
	echo "文件存在!"
else
	echo "文件不存在!"
fi
4.用shell写一个脚本，对文本中无序的一列数字排序,并计算求和
[root@wjw shell]# cat number.txt 
9
8
7
6
5
4
3
2
10
1
[root@wjw shell]# sort -n number.txt | awk '{a+=$0;print$0} END{print "SUM="a}'
1
2
3
4
5
6
7
8
9
10
SUM=55
5.请用shell脚本写出查找当前文件夹(/home)下所有的文本文件内容中包含有字符"shen"的文件名称。
[root@wjw home]# grep -r "shen" /home | cut -d ":" -f 1
/home/wjw/shell/banzhang.txt
/home/wjw/shell/sed.txt

```



# 正则表达式

| 字符 |                             说明                             |
| :--: | :----------------------------------------------------------: |
|  \   | 将下一字符标记为特殊字符、文本、反向引用或八进制转义符。例如，"n'匹配字符"n"。"\n"匹配换行符。序列"\\\\\\\\\"匹配"\\"， "\\\\\(\"匹配"("。 |
|  ^   | 匹配输入字符串开始的位置。如果设置了RegExp对象的Multiline属性，^还会与"\n"或"\r"之后的位置匹配。 |
|  $   | 匹配输入字符串结尾的位置。如果设置了RegExp对象的Multiline 属性，$还会与"\n"或"\r"之前的位置匹配。 |
|  *   | 零次或多次匹配前面的字符或子表达式。例如，zo*匹配"z"和"zoo"等效于{0,}。 |
|  +   | 一次或多次匹配前面的字符或子表达式。例如，"zo+"与"zo"和"zoo"匹配，但与"z"不匹配，等效于{1,}。 |

# 自动发布脚本

## 大屏前端mq-front.sh

#### 1.服务器打包发布一体

```shell
#!/bin/bash
cd /Auto_publish
echo "-------------------------------------"
echo "*STEP1 开始检测项目是否存在*"
echo "-------------------------------------"
if [ -d mq_front ];then
	echo "-------------------------------------"
	echo "SUCCESS:项目存在,正在pull更新代码"
	echo "-------------------------------------"
	cd /Auto_publish/mq_front
	git pull
	wait
else
	echo "-------------------------------------"
	echo "WARNING:项目不存在,正在clone项目"
	echo "-------------------------------------"
	git clone ssh://git@1.116.219.165/home/git/mq_front.git
	wait
fi
cd /Auto_publish/mq_front
echo "-------------------------------------"
echo "正在执行npm install"
echo "-------------------------------------"
npm install
wait
cd /Auto_publish/mq_front
echo "-------------------------------------"
echo "**STEP2 开始打包项目**"
echo "-------------------------------------"
npm run build
if [ $? -eq 0 ];then
	echo "-------------------------------------"
	echo "SUCCESS:npm run build运行成功"
	echo "-------------------------------------"
else
	echo "-------------------------------------"
	echo "ERROR:npm run build运行不成功！"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
	echo "-------------------------------------"
	echo "***STEP3 检测dist文件是否存在***"
	echo "-------------------------------------"
cd /Auto_publish/mq_front
if [ -d dist ]; then
	echo "-------------------------------------"
	echo "SUCCESS:dist目录存在"
	echo "-------------------------------------"
else
	echo "-------------------------------------"
	echo "ERROR:dist目录不存在！"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
echo "-------------------------------------"
echo "正在覆盖原文件"
echo "-------------------------------------"
rm -rf /apprun/mq-front/static
rm -f /apprun/mq-front/index.html
mv -fv /Auto_publish/mq_front/dist/* /apprun/mq-front
if [ $? -eq 0 ];then
	echo "-------------------------------------"
	echo "SUCCESS:原文件覆盖成功"
	echo "-------------------------------------"
	echo "SUCCESS:Done!"
	echo "-------------------------------------"
else
	echo "-------------------------------------"
	echo "ERROR:原文件覆盖不成功！"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
```

#### 2.本地打包和服务器发布

##### 本地打包控制服务器发布：mq-front.sh

```shell
#!/bin/bash
echo "-------------------------------------"
echo "*STEP1 开始检测项目是否存在*"
echo "-------------------------------------"
cd /Auto_publish
if [ -d mq_front ];then
	echo "-------------------------------------"
	echo "SUCCESS:项目存在,正在pull更新代码"
	echo "-------------------------------------"
	cd /Auto_publish/mq_front
	git pull
	wait
else
	echo "-------------------------------------"
	echo "WARNING:项目不存在,正在clone项目"
	echo "-------------------------------------"
	cd /Auto_publish/mq_front
	git clone ssh://git@1.116.219.165/home/git/mq_front.git
	wait
fi
cd /Auto_publish/mq_front
echo "-------------------------------------"
echo "正在执行npm install"
echo "-------------------------------------"
cd /Auto_publish/mq_front
npm install
wait
echo "-------------------------------------"
echo "**STEP2 开始打包项目**"
echo "-------------------------------------"
cd /Auto_publish/mq_front
npm run build
if [ $? -eq 0 ];then
	echo "-------------------------------------"
	echo "SUCCESS:npm run build运行成功"
	echo "-------------------------------------"
else
	echo "-------------------------------------"
	echo "ERROR:npm run build运行不成功！"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
echo "-------------------------------------"
echo "***STEP3 检测dist文件是否存在***"
echo "-------------------------------------"
cd /Auto_publish/mq_front
if [ -d dist ]; then
	echo "-------------------------------------"
	echo "SUCCESS:dist目录存在"
	echo "-------------------------------------"
else
	echo "-------------------------------------"
	echo "ERROR:dist目录不存在！"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
echo "-------------------------------------"
echo "正在传输文件"
echo "-------------------------------------"
scp -r /Auto_publish/mq_front/dist/* root@1.116.219.165:/Auto_publish/mq_front
wait
echo "-------------------------------------"
echo "正在删除已生成的文件"
echo "-------------------------------------"
rm -rf /Auto_publish/mq_front/dist
if [ $? -eq 0 ];then
	echo "-------------------------------------"
	echo "SUCCESS:删除成功"
	echo "-------------------------------------"
else
	echo "-------------------------------------"
	echo "ERROR:删除不成功！"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
echo "-------------------------------------"
echo "发布指令"
echo "-------------------------------------"
ssh root@1.116.219.165 'bash /Auto_publish/mq-front.sh'
wait

```

##### 服务器发布：mq-front.sh

```shell
#!/bin/bash
echo "-------------------------------------"
echo "正在发布"
echo "-------------------------------------"
cd /Auto_publish/mq_front
if [ -d static ]; then
	echo "-------------------------------------"
	echo "SUCCESS:static目录存在"
	echo "-------------------------------------"
else
	echo "-------------------------------------"
	echo "ERROR:static目录不存在！"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
	if [ -e index.html ]; then
	echo "-------------------------------------"
	echo "SUCCESS:index.html存在"
	echo "-------------------------------------"
else
	echo "-------------------------------------"
	echo "ERROR:index.html不存在！"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
echo "-------------------------------------"
echo "正在覆盖原文件"
echo "-------------------------------------"
rm -rf /apprun/mq-front/static
rm -f /apprun/mq-front/index.html
mv -fv /Auto_publish/mq_front/* /apprun/mq-front
if [ $? -eq 0 ];then
	echo "-------------------------------------"
	echo "SUCCESS:原文件覆盖成功"
	echo "-------------------------------------"
	echo "SUCCESS:Done!"
	echo "-------------------------------------"
else
	echo "-------------------------------------"
	echo "ERROR:原文件覆盖不成功！"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
```



## 后端mq-parent.sh

### 1.服务器打包发布一体

```shell
#!/bin/bash
cd /Auto_publish
echo "-------------------------------------"
echo "*STEP1 开始检测项目是否存在*"
echo "-------------------------------------"
if [ -d mq_parent ];then
	echo "-------------------------------------"
	echo "SUCCESS:项目存在,正在pull更新代码"
	echo "-------------------------------------"
	cd /Auto_publish/mq_parent
	git pull
	wait
else
	echo "-------------------------------------"
	echo "WARNING:项目不存在,正在clone"
	echo "-------------------------------------"
	git clone ssh://git@1.116.219.165/home/git/mq_parent.git
	wait
fi
	echo "-------------------------------------"
	echo "**STEP2 开始打包项目**"
	echo "-------------------------------------"
cd /Auto_publish/mq_parent
	echo "-------------------------------------"
	echo "检测mvn是否运行成功"
	echo "-------------------------------------"
mvn clean install
if [ $? -eq 0 ];then
    echo "-------------------------------------"
	echo "SUCCESS:mvn运行成功"
	echo "-------------------------------------"
else
    echo "-------------------------------------"
    echo "ERROR:mvn运行不成功"
    echo "Exit！"
    echo "-------------------------------------"
    exit 48
fi
cd /Auto_publish/mq_parent/mq-api/target
    echo "-----------------------------------------"
	echo "***STEP3***"
	echo "检测mq-api.jar文件是否存在!"
	echo "-----------------------------------------"
if [ -e mq-api.jar ]; then
    echo "-------------------------------------"
    echo "SUCCESS:文件存在!"
    echo "正在覆盖原文件"
    echo "-------------------------------------"
   	mv -fv /Auto_publish/mq_parent/mq-api/target/mq-api.jar /root/bn/api
   	cd /root/bn/api
   	echo "-------------------------------------"
	echo "****STEP4****"
	echo "检测mq-api.jar进程是否存在"
	echo "-------------------------------------"
	ps -elf | grep java | grep mq-api.jar | cut -d " " -f 8 | xargs kill -9
   	if [ $? -eq 0 ];then
   		echo "-------------------------------------"
   		echo "SUCCESS:原进程已杀死"
   		echo "正在重启mq-api.jar"
   		echo "-------------------------------------"
   	else
   	    echo "-------------------------------------"
   		echo "WARNING:原进程不存在"
   		echo "正在运行mq-api.jar"
   		echo "-------------------------------------"
   	fi
   	nohup java -jar -Xms128m -Xmx256m mq-api.jar &
   	cd /root/bn/api
   	tail -f nohup.out
   	echo "-------------------------------------"
   	echo "SUCCESS:Done!"
   	echo "-------------------------------------"
else
    echo "-------------------------------------"
	echo "ERROR:文件不存在!"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
```

### 2.本地打包和服务器发布

#### 本地打包控制服务器发布：mq-parent.sh

```shell
#!/bin/bash
cd /Auto_publish
	echo "-------------------------------------"
	echo "*STEP1*"
	echo "开始检测项目是否存在"
	echo "-------------------------------------"
if [ -d mq_parent ];then
	echo "-------------------------------------"
	echo "SUCCESS:项目存在,正在pull更新代码"
	echo "-------------------------------------"
	cd /Auto_publish/mq_parent
	git pull
	wait
else
	echo "-------------------------------------"
	echo "WARNING:项目不存在,正在clone"
	echo "-------------------------------------"
	git clone ssh://git@1.116.219.165/home/git/mq_parent.git
	wait
fi
	echo "-------------------------------------"
	echo "**STEP2 开始打包项目**"
	echo "-------------------------------------"
cd /Auto_publish/mq_parent
	echo "-------------------------------------"
	echo "开始运行mvn clean install"
	echo "-------------------------------------"
mvn clean install
if [ $? -eq 0 ];then
    echo "-------------------------------------"
	echo "SUCCESS:mvn运行成功"
	echo "-------------------------------------"
else
    echo "-------------------------------------"
    echo "ERROR:mvn运行不成功"
    echo "Exit！"
    echo "-------------------------------------"
    exit 48
fi
cd /Auto_publish/mq_parent/mq-api/target
    echo "-----------------------------------------"
	echo "***STEP3***"
	echo "检测mq-api.jar文件是否存在!"
	echo "-----------------------------------------"
if [ -e mq-api.jar ]; then
    echo "-------------------------------------"
    echo "SUCCESS:文件存在!"
    echo "正在传输mq-api.jar文件"
    echo "-------------------------------------"
   	scp /Auto_publish/mq_parent/mq-api/target/mq-api.jar root@1.116.219.165:/Auto_publish/mq_parent
   	wait
	rm -f /Auto_publish/mq_parent/mq-api/target/mq-api.jar
   	ssh root@1.116.219.165 'bash /Auto_publish/mq-parent.sh'
   	wait
else
    echo "-------------------------------------"
	echo "ERROR:文件不存在!"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
```

#### 服务器发布：mq-parent.sh

```shell
#!/bin/bash
cd /Auto_publish/mq_parent
	echo "-------------------------------------"
	echo "*STEP1*"
	echo "检测mq-api.jar文件是否存在!"
	echo "-------------------------------------"
if [ -e mq-api.jar ]; then
    echo "-------------------------------------"
    echo "SUCCESS:文件存在!"
    echo "正在覆盖原文件"
    echo "-------------------------------------"
    rm -f /root/bn/api/mq-api.jar
   	mv -fv /Auto_publish/mq_parent/mq-api.jar /root/bn/api
   	cd /root/bn/api
   	echo "-------------------------------------"
	echo "**STEP2**"
	echo "检测mq-api.jar进程是否存在"
	echo "-------------------------------------"
	NAME='mq-api.jar'
	echo $NAME
	ID=`ps -ef | grep "$NAME" | grep -v "$0" | grep -v "grep" | awk '{print $2}'`
	echo $ID
	for id in $ID
	do
	kill -9 $id
	echo "killed $id"
	done
   	nohup java -jar -Xms128m -Xmx256m mq-api.jar &
   	cd /root/bn/api
   	tail -f nohup.out
else
    echo "-------------------------------------"
	echo "ERROR:文件不存在!"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
```



```shell
ps -aux | grep mq-api.jar |grep -e Sl | cut -d " " -f 6 | xargs kill -9
ps -elf | grep java | grep mq-api.jar | cut -d " " -f 8 | xargs kill -9
	if [ $? -eq 0 ];then
		echo "-------------------------------------"
   		echo "SUCCESS:原进程已杀死"
   		echo "正在重启mq-api.jar"
   		echo "-------------------------------------"
   	else
   	    echo "-------------------------------------"
   		echo "WARNING:原进程不存在"
   		echo "正在运行mq-api.jar"
   		echo "-------------------------------------"
   	fi
```



## 管理端mq-admin.sh

### 1.服务器端打包发布一体

```shell
#!/bin/bash
cd /Auto_publish
	echo "-------------------------------------"
	echo "检测项目是否存在"
	echo "-------------------------------------"
if [ -d mq_admin ];then
	echo "-------------------------------------"
	echo "SUCCESS:项目已存在"
	echo "正在pull更新代码"
	echo "-------------------------------------"
	cd /Auto_publish/mq_admin
	git pull
	wait
else
	echo "-------------------------------------"
	echo "WARNING:项目不存在,正在clone"
	echo "-------------------------------------"
	cd /Auto_publish
	git clone ssh://git@1.116.219.165/home/git/mq_admin.git
	wait
fi
	echo "-------------------------------------"
	echo "正在覆盖原文件"
	echo "-------------------------------------"
mv -fv /Auto_publish/mq_admin/* /apprun/mq-admin
```

### 2.本地打包和服务器发布

#### 本地打包控制服务器发布

```shell
#!/bin/bash
cd /Auto_publish
echo "-------------------------------------"
echo "检测项目是否存在"
echo "-------------------------------------"
if [ -d mq_admin ];then
	echo "-------------------------------------"
	echo "SUCCESS:项目已存在"
	echo "正在pull更新代码"
	echo "-------------------------------------"
	cd /Auto_publish/mq_admin
	git pull
	wait
else
	echo "-------------------------------------"
	echo "WARNING:项目不存在,正在clone"
	echo "-------------------------------------"
	cd /Auto_publish
	git clone ssh://git@1.116.219.165/home/git/mq_admin.git
	wait
fi
echo "-------------------------------------"
echo "正在传输文件"
echo "-------------------------------------"
scp -r /Auto_publish/mq_admin/* root@1.116.219.165:/Auto_publish/mq_admin
wait
echo "-------------------------------------"
echo "发布指令"
echo "-------------------------------------"
ssh root@1.116.219.165 'bash /Auto_publish/mq-admin.sh'
wait
```

```shell
#!/bin/bash
cd /Auto_publish/mq_admin
echo "-------------------------------------"
echo "正在删除原文件"
echo "-------------------------------------"
rm -rf /apprun/mq-admin/*
wait
echo "-------------------------------------"
echo "正在覆盖原文件"
echo "-------------------------------------"
mv -fv /Auto_publish/mq_admin/* /apprun/mq-admin
```



## 云档案前端cloudfile-front.sh

### 1.服务器端打包发布一体

```shell
#!/bin/bash
cd /Auto_publish
	echo "-------------------------------------"
	echo "*STEP1*"
	echo "检测项目是否存在"
	echo "-------------------------------------"
if [ -d mq_cloudfile_front ];then
	echo "-------------------------------------"
	echo "SUCCESS:项目已存在"
	echo "正在pull更新代码"
	echo "-------------------------------------"
	cd /Auto_publish/mq_cloudfile_front
	git pull
	wait
else
	echo "-------------------------------------"
	echo "WARNING:项目不存在,正在clone"
	echo "-------------------------------------"
	git clone ssh://git@1.116.219.165/home/git/mq_cloudfile_front.git
	wait
fi
	cd /Auto_publish/mq_cloudfile_front
	echo "-------------------------------------"
	echo "正在执行npm install"
	echo "-------------------------------------"
	npm install -g yarn
	wait
	yarn
	wait
	echo "-------------------------------------"
	echo "**STEP2 正在打包项目"
	echo "-------------------------------------"
cd /Auto_publish/mq_cloudfile_front
export NODE_OPTIONS=--max_old_space_size=4096
npm run build
if [ $? -eq 0 ];then
    echo "-------------------------------------"
	echo "SUCCESS:npm run build运行成功"
	echo "-------------------------------------"
else
	echo "-------------------------------------"
	echo "ERROR:npm run build运行不成功！"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
	echo "-------------------------------------"
	echo "***STEP3 检测dist文件是否存在"
	echo "-------------------------------------"
cd /Auto_publish/mq_cloudfile_front
if [ -d dist ]; then
	echo "-------------------------------------"
	echo "SUCCESS:dist目录存在"
	echo "-------------------------------------"
else
	echo "-------------------------------------"
	echo "ERROR:dist目录不存在！"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
echo "-------------------------------------"
echo "正在覆盖原文件"
echo "-------------------------------------"
rm -rf /cloudfile/front/dist
mv -fv /Auto_publish/mq_cloudfile_front/dist /cloudfile/front
echo "-------------------------------------"
echo "SUCCESS:Done!"
echo "-------------------------------------"
```

```shell
	npm install -g create-vite-app
	wait
	npm install vite
	wait
	npm install
	wait	
```

### 2.本地打包和服务端发布

#### 本地打包控制服务器发布

```shell
#!/bin/bash
cd /Auto_publish
	echo "-------------------------------------"
	echo "*STEP1*"
	echo "检测项目是否存在"
	echo "-------------------------------------"
if [ -d mq_cloudfile_front ];then
	echo "-------------------------------------"
	echo "SUCCESS:项目已存在"
	echo "正在pull更新代码"
	echo "-------------------------------------"
	cd /Auto_publish/mq_cloudfile_front
	git pull
	wait
else
	echo "-------------------------------------"
	echo "WARNING:项目不存在,正在clone"
	echo "-------------------------------------"
	git clone ssh://git@1.116.219.165/home/git/mq_cloudfile_front.git
	wait
fi
	cd /Auto_publish/mq_cloudfile_front
	echo "-------------------------------------"
	echo "正在执行npm install"
	echo "-------------------------------------"
	npm install -g yarn
	wait
	yarn
	wait
	echo "-------------------------------------"
	echo "**STEP2 正在打包项目"
	echo "-------------------------------------"
cd /Auto_publish/mq_cloudfile_front
export NODE_OPTIONS=--max_old_space_size=4096
npm run build
if [ $? -eq 0 ];then
    echo "-------------------------------------"
	echo "SUCCESS:npm run build运行成功"
	echo "-------------------------------------"
else
	echo "-------------------------------------"
	echo "ERROR:npm run build运行不成功！"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
	echo "-------------------------------------"
	echo "***STEP3 检测dist文件是否存在"
	echo "-------------------------------------"
cd /Auto_publish/mq_cloudfile_front
if [ -d dist ]; then
	echo "-------------------------------------"
	echo "SUCCESS:dist目录存在"
	echo "-------------------------------------"
else
	echo "-------------------------------------"
	echo "ERROR:dist目录不存在！"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
	echo "-------------------------------------"
	echo "正在传输文件"
	echo "-------------------------------------"
scp -r /Auto_publish/mq_cloudfile_front/dist root@1.116.219.165:/Auto_publish/mq_cloudfile_front
wait
echo "-------------------------------------"
echo "正在删除已生成的文件"
echo "-------------------------------------"
rm -rf /Auto_publish/mq_cloudfile_front/dist
if [ $? -eq 0 ];then
	echo "-------------------------------------"
	echo "SUCCESS:删除成功"
	echo "-------------------------------------"
else
	echo "-------------------------------------"
	echo "ERROR:删除不成功！"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
echo "-------------------------------------"
echo "发布指令"
echo "-------------------------------------"
ssh root@1.116.219.165 'bash /Auto_publish/mq-cloudfile-front.sh'
wait
```

#### 服务器发布

```shell
#!/bin/bash
cd /Auto_publish/mq_cloudfile_front
if [ -d dist ]; then
	echo "-------------------------------------"
	echo "SUCCESS:dist目录存在"
	echo "-------------------------------------"
else
	echo "-------------------------------------"
	echo "ERROR:dist目录不存在！"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
echo "-------------------------------------"
echo "正在删除原文件"
echo "-------------------------------------"
rm -rf /cloudfile/front/dist
echo "-------------------------------------"
echo "正在覆盖原文件"
echo "-------------------------------------"
mv -fv /Auto_publish/mq_cloudfile_front/dist /cloudfile/front
echo "-------------------------------------"
echo "SUCCESS:Done!"
echo "-------------------------------------"
```



```shell
 npm i -g yarn
 yarn -v
 yarn add create-vite-app -g
 yarn build
 npm run build
 rm -rf /Auto_publish/mq_cloudfile_front/dist
 npm install vite
 wait
 npm install
 wait
 npm install -g create-vite-app
 wait
```

## 云档案后端mq-cloudfile-api.sh

### 1.服务器打包发布一体

```shell
#!/bin/bash
cd /Auto_publish
	echo "-------------------------------------"
	echo "*STEP1*"
	echo "检测项目是否存在"
	echo "-------------------------------------"
if [ -d mq_cloudfile_master ];then
	echo "-------------------------------------"
	echo "SUCCESS:项目已存在"
	echo "正在pull更新代码"
	echo "-------------------------------------"
	cd /Auto_publish/mq_cloudfile_master
	git pull
	wait
else
	echo "-------------------------------------"
	echo "WARNING:项目不存在,正在clone"
	echo "-------------------------------------"
	git clone ssh://git@1.116.219.165/home/git/mq_cloudfile_master.git
	wait
fi
	echo "-------------------------------------"
	echo "**STEP2**"
	echo "开始打包项目"
	echo "-------------------------------------"
cd /Auto_publish/mq_cloudfile_master
	echo "-------------------------------------"
	echo "检测mvn是否运行成功"
	echo "-------------------------------------"
mvn clean install
if [ $? -eq 0 ];then
	echo "-------------------------------------"
	echo "SUCCESS:mvn运行成功"
	echo "-------------------------------------"
else
	echo "-------------------------------------"
	echo "ERROR:mvn运行不成功"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
cd /Auto_publish/mq_cloudfile_master/cloudfile-api/target
	echo "-----------------------------------------"
	echo "***STEP3***"
	echo "检测cloudfile-api.jar文件是否存在!"
	echo "-----------------------------------------"
if [ -e cloudfile-api.jar ]; then
	echo "-------------------------------------"
	echo "SUCCESS:文件存在!"
	echo "正在覆盖原文件"
	echo "-------------------------------------"
   	mv -f cloudfile-api.jar /cloudfile/api
   	cd /cloudfile/api
   	echo "-------------------------------------"
	echo "****STEP4****"
	echo "检测cloudfile-api.jar进程是否存在"
	echo "-------------------------------------"
	ps -elf | grep java | grep cloudfile-api.jar | cut -d " " -f 8 | xargs kill -9
   	if [ $? -eq 0 ];then
   		echo "-------------------------------------"
   		echo "SUCCESS:原进程已杀死"
   		echo "正在重启cloudfile-api.jar"
   		echo "-------------------------------------"
   	else
		echo "-------------------------------------"
   		echo "WARNING:原先进程不存在"
   		echo "正在运行cloudfile-api.jar"
   		echo "-------------------------------------"
   	fi
   	nohup java -jar -Xms128m -Xmx256m cloudfile-api.jar &
   	cd /cloudfile/api
   	tail -f nohup.out
   	echo "-------------------------------------"
   	echo "SUCCESS:Done!"
   	echo "-------------------------------------"
else
	echo "-------------------------------------"
	echo "ERROR:文件不存在!"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
```

### 2.本地打包和服务器发布

#### 本地打包控制服务器发布：mq-cloudfile-api.sh

```shell
#!/bin/bash
cd /Auto_publish
	echo "-------------------------------------"
	echo "*STEP1*"
	echo "开始检测项目是否存在"
	echo "-------------------------------------"
if [ -d mq_cloudfile_master ];then
	echo "-------------------------------------"
	echo "SUCCESS:项目存在,正在pull更新代码"
	echo "-------------------------------------"
	cd /Auto_publish/mq_cloudfile_master
	git pull
	wait
else
	echo "-------------------------------------"
	echo "WARNING:项目不存在,正在clone"
	echo "-------------------------------------"
	git clone ssh://git@1.116.219.165/home/git/mq_cloudfile_master.git
	wait
fi
	echo "-------------------------------------"
	echo "**STEP2 开始打包项目**"
	echo "-------------------------------------"
cd /Auto_publish/mq_cloudfile_master
	echo "-------------------------------------"
	echo "开始运行mvn clean install"
	echo "-------------------------------------"
mvn clean install
if [ $? -eq 0 ];then
    echo "-------------------------------------"
	echo "SUCCESS:mvn运行成功"
	echo "-------------------------------------"
else
    echo "-------------------------------------"
    echo "ERROR:mvn运行不成功"
    echo "Exit！"
    echo "-------------------------------------"
    exit 48
fi
cd /Auto_publish/mq_cloudfile_master/cloudfile-api/target
    echo "-----------------------------------------"
	echo "***STEP3***"
	echo "检测cloudfile-api.jar文件是否存在!"
	echo "-----------------------------------------"
if [ -e cloudfile-api.jar ]; then
    echo "-------------------------------------"
    echo "SUCCESS:文件存在!"
    echo "正在传输cloudfile-api.jar文件"
    echo "-------------------------------------"
    cd /Auto_publish/mq_cloudfile_master/cloudfile-api/target
   	scp cloudfile-api.jar root@1.116.219.165:/Auto_publish/mq_cloudfile_master
   	wait
   	echo "-------------------------------------"
	echo "发布指令发出"
	echo "-------------------------------------"
   	ssh root@1.116.219.165 'bash /Auto_publish/mq-cloudfile-api.sh'
   	wait
else
    echo "-------------------------------------"
	echo "ERROR:文件不存在!"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
```

#### 服务器发布：mq-cloudfile-api.sh

```shell
#!/bin/bash
cd /Auto_publish/mq_cloudfile_master
	echo "-------------------------------------"
	echo "*STEP1*"
	echo "检测cloudfile-api.jar文件是否存在!"
	echo "-------------------------------------"
if [ -e cloudfile-api.jar ]; then
    echo "-------------------------------------"
    echo "SUCCESS:文件存在!"
    echo "正在覆盖原文件"
    echo "-------------------------------------"
    rm -f /cloudfile/api/cloudfile-api.jar
   	mv -fv /Auto_publish/mq_cloudfile_master/cloudfile-api.jar /cloudfile/api
   	cd /cloudfile/api
   	echo "-------------------------------------"
	echo "**STEP2**"
	echo "检测cloudfile-api.jar进程是否存在"
	echo "-------------------------------------"
	NAME='cloudfile-api.jar'
	echo $NAME
	ID=`ps -ef | grep "$NAME" | grep -v "$0" | grep -v "grep" | awk '{print $2}'`
	echo $ID
	for id in $ID
	do
	kill -9 $id
	echo "killed $id"
	done
   	nohup java -jar -Xms128m -Xmx256m cloudfile-api.jar &
   	cd /root/bn/api
   	tail -f nohup.out
else
    echo "-------------------------------------"
	echo "ERROR:文件不存在!"
	echo "Exit！"
	echo "-------------------------------------"
	exit 48
fi
```



```shell
kill -SIGINT $pid === kill -2 $pid
ps -aux | grep cloudfile-api.jar |grep -e Sl | cut -d " " -f 6 | xargs kill -9
rm -rf /Auto_publish/mq_cloudfile_master/cloudfile-api/target
rm -rf *
```

