# 计算机硬件组成部分
	● 输入设备:键盘、鼠标、触控屏等
	● 主机设备:主板、中央处理器(CPU)、主存储器(内存)、网卡、声卡、显示卡等
	● 输出设备:屏幕、耳机、打印机、投影仪等
	● 外部存储设备:硬盘、软盘、光盘、U盘、蓝光光驱等
	● CPU缓存
	● 硬盘:传统硬盘(HDD)==固态硬盘(SSD)
	● CPU比较主流的厂商
		。AMD公司
		。Interl公司
	● CPU架构
		。x86架构，8086架构，80286，80386, x86称号
		。8位、16位、32位、64位，CPU一次可以处理的数据量,
		。32位CPU一次可以从内存中读取大约3.25G左右的数据量
		。64位CPU一次可以从内存中读取大约128G左右的数据量
	● CPU核心
		。单核心，一颗CPU只能有一个运算单元
		。多核心，一颗CPU里边有两个以上的运算单元
	● 计算机什么最重要?想要让计算机运行起来，足够的电力
# 云计算
	什么叫云计算:网络资源出租
	三种云模式:公有云，私有云，混合云
	++ laaS云模式:提供基础设施服务的一种模式(机房、网络、电力、物理服务器、内存、硬盘、网卡、
	CPU、IP地址)
	++ PaaS云模式:平台级服务(主要是针对与开发人员,开发-个软件,对外提供服务,运行环境，软件代
	码编译程二进制，上传给云厂 商，提供一一个运行的环境，运行起来对外提供服务)
	++ SaaS云模式:软件级服务(比较高级,作为一个用户,什么都不想做，购买人家做好的，网站，邮件，博
	客，不想搭建，不想去维护，直接拿过来就使用，完全可以的，厂商哪里花钱购买人家提前搭建好的服
	务就可以了，网站服务合适的时间运行起来被别人访问，网站后期的维护工作，专门]的人去帮助我们去维
	护，故障率最低的一种模式，客户什么都不需要操心,花钱)
# 世界三大云厂商:
	++ 第一:亚马逊, AWS
	++ 第二:微软, Azure
	++ 第三:中国，阿里云，在全球15个地区建立的200多个数据中心https://www.aliyun.com/ #阿里云地址
# 虚拟化
	虚拟化.
	++ VMware虚拟机软件:帮我们虚拟出一套完整硬件平台，内存条，硬盘,风扇，鼠标，键盘，显卡，CPU等,安装系统
	++ 企业级虚拟化: KVM虚拟化，在Linux系统管理虚拟机的
# Linux内核
	++ 由Linus率领的内核项目团队统一发布
	++ 内核的作用:管理进程、内存、文件系统、设备控制、网络管理
	++ 版本号含义linux内核版本有两种:稳定版和开发版
	++ 版本号:主版本.次版本.释出版本-修改版本
	++ 如: 3.10.0-693.17.1.el7.x86_64
	++ 注: el表示Enterprise Linux, 7表示RHEL7版本操作系统
	++ x86_64表示CPU结构，即64位
	++ 一般用头两个数字(主次版本)描述内核系列
	++ 释出版本:在主次版本架构不变的情况下，新增的功能累积到一定程度后释出的内核版本
	++ 修改版本:修改一些bug等
# Linux版本
	++ 发行版的名称和版本由发行方决定
	1.Red Hat Enterprise Linux 5/6/7/8
		++ Red Hat (红帽公司)创建于1993年，是目前世界上资深的Linux厂商，也是最获认可的Linux品牌
	2.RHEL~Red Hat Enterprise Linux （企业版）
		-http://www.redhat.com
	3.CentOS~CentOS （RHEL的社区克隆版本,免费版本）
		-http://www.centos.org/
	4.Fedora~Fedora Core （由Red Hat桌面版发展而来，免费版本）
		-http://fedoraproject.org/
	5.Ubuntu Linux
	6.Suse Linux Enterprise
	7.Debian Linux
# Linux在企业中的应用
	++ IT服务器Linux系统应用领域
	++ 嵌入式Linux系统应用领域
	++ 高性能大型运算
	++ 个人桌面Linux应用领域
# RHCE
	++ 系统化的学习
	++ 非常友好
# 图形界面
	++ Ctrl+Shift +号//调整命令终端变大
	++ Ctrl-号 //调整命令终端变小

|软件包管理体系名称|格式|软件包管理工具|常见对应的发行版本|
|---|---|---|---|
|APT|.deb|apt,apt-get,aptitude |Debian,Ubuntu,Deepin|
|RPM/Redhat|.rpm|yum,dnf|Redhat,CentOS,Fedora|
|RPM/openSUSE|.rpm|YaST,zypper|openSUSE|
|Pacman/AUR|.pkg.xz|Pacman,Yaourt|Arch,Manjaro|

# Linux系统:
	++ 多用户的系统:允许同时有很多个用户登录系统，使用系统里的资源
	++ 多任务的系统:允许同时执行多个任务
	++ 严格区分大小写/命令/选项/参数/文件名/目录名
	++ 一切皆文件:硬件设备(内存、CPU、网卡、显示器、硬盘等等，以文件的形式存在)
	++ 不管是文件还是目录都是以倒挂的树形结构，存在云系统的/目录下，/(根)是Linux系统的起点，Linux目录结构：（树形结构）。
	命令行环境输入：ls /
	Linux目录的层次分隔：斜杠/
	最顶层 就是一个 /，表示根目录
	常见一级目录：
	● /(根) :系统所有数据都存放在根目录下
	● /bin/ 、/sbin（管理员权限）:存放用户和管理员必备的可执行的二进制程序文件
	● /boot: 存放Linux系统内核及引导系统程序所需要的文件目录
	● /dev:存放硬件设备的目录，如键盘、鼠标、硬盘、光盘等等
	● /etc:存放各种系统配置文件，用户信息文件
	● /root: 超级管理员的家目录
	● /home:系统普通用户的家目录
	● /lib: 存放系统中的程序运行所需要的共享库及内核模块
	● /ib64 :存放函式库
	● /opt: 安装第三方软件的目录
	● /srv:服务启动之后需要访问的数据目录
	● /tmp: 一般用户或正在执行的程序临时存放文件的目录,任何人都可以访问，重要数据不可放置在此目录下
	● /var: 存放系统执行过程中经常变化的文件，如随时都在变化的日志文件就存放/var/log下
	● /mnt ：管理员手动挂载一些外部设备的目录 
	● /media ：自动识别并挂载的设备目录
	● /proc: Linux伪文件系统，该目录下的数据存在于内存当中，不占用磁盘空间
	
	● /run :程序或服务启动后，存放PID的目录
	● /sys: 存放被建立在内存中的虚拟文件系统,内核系统数据（虚拟）
	● /usr: 操作系统软件资源所放置的目录
		++ /usr/bin: 与/bin目录相同，存放用户可以使用的命令程序
		++ /usr/lib: 与/lib目录相同，存放系统中的程序运行所需要的共享库及内核模块
		++ /usr/etc: 用于存放安装软件时使用的配置文件
		++ /usr/games: 与游戏比较相关的数据放置处
		++ /usr/include: C/C+ +等程序语言的档头(header)与包含档(include)放置处
		++ /usr/lib64: 与/1ib64目录相同, 存放函式库
		++ /usr/libexec: 不经常被使用的执行程序或脚本会放置在此目录中
		++ /usr/local: 额外安装的软件存放目录
		++ /usr/sbin: 该目录与/sbin目录相同，存放用户可执行的二进制程序文件
		++ /usr/share: 放置只读架构的杂项数据文件
		++ /usr/src: 一般软件源代码建议存放该目录下
	
	++ 对于Linux系统而言，目录还是文件没有扩展名一说(.txt .jpg .png .GIF) .sh(脚本文件) .conf (配置文件) .log (日志文件) .rpm (软件包) .tar (压缩包)



# 查看CPU信息
	●	/proc/cpuinfo文件用于存放系统CPU信息
	●	lscpu 用于显示CPU架构信息
	●	命令格式: lscpu [-选项]
		
		#查看/proc/cpuinfo文件内容
		[root@1oca1host ~]# cat /proc/cpuinfo

|序号|项目|解释|
|------|------|------|
|1|processor|#系统中逻辑处理核的编号。对于单核处理器，则可认为是其CPU编号。对于多核处理器则可以是物理核、或者使用超线程技术虚拟的逻辑核|
|2|vendor_id|#CPU制造商|
|3|cpu family|#CPU产品系列代号|
|4|mode1|#CPU属于其系列中的哪一代的代号|
|5|mode1 name|#CPU属于的名字及其编号、标称主频|
|6|stepping|#CPU属于制作更新版本|
|7|cpu MHZ|#CPU的实际使用主频|
|8|cache size|#CPU二级缓存大小|
|9|physical id|#单个CPU的标号|
|10|siblings|#单个CPU逻辑物理核数|
|11|core id| #当前物理核在其所处CPU中的编号，这个编号不一定连续 |
|12|cpu cores|#该逻辑核所处CPU的物理核数|
|13|apicid|#用来区分不同逻辑核的编号，系统中每个逻辑核的此编号必然不同，此编号不一定连续|
|14|fpu|#是否具有浮点运算单元(Floating Point Unit)|
|15|fpu_exception|#是否支持浮点计算异常|
|16|cpuid level|#执行cpuid指令前，eax寄存器中的值，根据不同的值cpuid指令会返回不同的内容|
|17|wp|#表明当前CPU是否在内核态支持对用户空间的写保护(Write Protection)|
|18|flags|#当前CPU支持的功能|
|19|bogomips|#在系统内核启动时粗略测算的CPU速度(Million Instructions Per Second)|
|20|clf1ush size|#每次刷新缓存的大小单位|
|21|cache_alignment|#缓存地址对齐单位|
|22|address sizes|#可访问地址空间位数|
|23|power management| #对能源管理的支持，有以下几个可选支持功能:|

	#使用1scpu查看cpu信息
	[root@1ocalhost ~]# 1scpu

|序号|项目|解释|
|---|---|---|
|1|Architecture|#架构|
|2|CPU(s)|#逻辑cpu颗数|
|3|Thread(s) per core|#每个核心线程|
|4|core(s) per socket|#每个cpu插槽核数/每颗物理cpu核数|
|5|CPU socket(s)|#cpu插槽数|
|6|Vendor ID|#cpu厂 商ID|
|7|CPU family|#cpu系列|
|8|Mode1|#型号|
|9|stepping|#步进|
|10|CPU MHZ|#cpu主频|
|11|Vi rtualization|#cpu支 持的虚拟化技术|
|12|L1d cache|#一级缓存(google了下，这具体表示表示cpu的L1数据缓存)|
|13|L1i cache|#一级缓存(具体为L1指令缓存)|
|14|L2 cache|#二级缓存|

# 查看系统内存信息
	●	/proc/meminfo文件用于存放系统内存信息
	●	free 用于查看内存使用情况
	●	命令格式: free [-选项]
	●	常用选项: -h #以人类易读方式显示大小(KB，MB，GB)
	
	#查看/proc/memi nfo文件内容
	[root@1ocalhost ~]# cat /proc/meminfo
	MemTotal:        4000208 kB #所有可用的内存大小，物理内存减去预留位和内核使用。系统从加电开始到引导完成，firmware/BIOS要预留一些内存，内核本身要占用一些内存，最后剩下可供内核支配的内存就是MemTotal。这个值在系统运行期间一般是固定不变的，重启会改变。
	MemFree:          955896 kB #表示系统尚未使用的内存。
	MemAvailable:    2960540 kB #真正的系统可用内存，系统中有些内存虽然已被使用但是可以回收的，比如cache/buffer、s1ab都有一部分可以回收，所以这部分可回收的内存加上MemFree才是系统可用的内存
	Buffers:            3168 kB #用来给块设备做缓存的内存，(文件系统的metadata、 pages)
	Cached:          2141740 kB #分配给文件缓冲区的内存，例如vi一个文件，就会将未保存的内容写到该缓冲区
	SwapCached:            0 kB #被高速缓冲存储用的交换空间(硬盘的swap)的大小
	Active:          1073832 kB #经常使用的高速缓冲存储器页面文件大小
	Inactive:        1242096 kB #不经常使用的高速缓冲存储器文件大小
	Active(anon):     255368 kB #活跃的匿名内存
	Inactive(anon):    41636 kB #不活跃的匿名内存
	Active(file):     818464 kB #活跃的文件使用内存
	Inactive(file):  1200460 kB #不活跃的文件使用内存
	Unevictable:       10892 kB #不能被释放的内存页
	Mlocked:           10892 kB #系统调用mlock家族允许程序在物理内存上锁住它的部分或全部地址空间。这将阻止Linux将这个内存页调度到交换空间(swap space) ，即使该程序已有一段时间没有访问这段空间
	SwapTotal:             0 kB #交换空间总内存
	SwapFree:              0 kB #交换空间空闲内存
	Dirty:                12 kB #等待被写回到磁盘的
	Writeback:             0 kB #正在被写回的
	AnonPages:        181912 kB #未映射页的内存/映射到用户空间的非文件页表大小
	Mapped:            92372 kB #映射文件内存
	Shmem:            116348 kB #已经被分配的共享内存
	Slab:             366312 kB #内核数据结构缓存
	SReclaimable:     273240 kB #可收回s1ab内存
	SUnreclaim:        93072 kB #不可收回slab内存
	KernelStack:        3584 kB #内核消耗的内存
	PageTables:        12280 kB #管理内存分页的索引表的大小
	NFS_Unstable:          0 kB #不稳定页表的大小
	Bounce:                0 kB #在低端内存中分配一个临时buffer作为跳转，把位于高端内存的缓存数据复制到此处消耗的内存
	WritebackTmp:          0 kB 	#FUSE用于临时写回缓冲区的内存
	CommitLimit:     2000104 kB 	#系统实际可分配内存
	Committed_AS:    1314076 kB 	#系统当前已分配的内存
	VmallocTotal:   34359738367 kB 	#预留的虚拟内存总量
	VmallocUsed:       95128 kB 	#已经被使用的虚拟内存
	VmallocChunk:   34359537660 kB 	#可分配的最大的逻辑连续的虚拟内存
	Percpu:              960 kB
	HardwareCorrupted:     0 kB
	AnonHugePages:    100352 kB
	CmaTotal:              0 kB
	CmaFree:               0 kB
	HugePages_Total:       0
	HugePages_Free:        0
	HugePages_Rsvd:        0
	HugePages_Surp:        0
	Hugepagesize:       2048 kB
	DirectMap4k:      110680 kB
	DirectMap2M:     4038656 kB
	
	#使用free命令查看内存使用情况
	[root@1oca1host ~]# free -h

|项目|total|used|free|shared|buff/cache|available|
|---|---|---|---|---|---|---|
|Mem:|972M|344M|238M|13M|389M|424M|
|Swap:|2.0G|OB|2.0G|

	#解释: Mem物理内存统计信息

|项目|解释|
|---|---|
|total|#物理内存总量|
|used|#以使用的内存总量|
|free|#空闲内存总量|
|shared|#共享内存总量|
|buff/cache|#块设备与普通文件占用的缓存数量|
|available|#还可以被应用程序使用的物理内存大小|

	#解释: Swap内存交换空间，当物理内存不足时，可以使用硬盘空间充当内存使用
	total: #交换分区内存总量
	used:  #正在使用的交换分区内存
	free:  #空闲交换分区内存

# 查看网卡信息
	●	网卡配置文件地址: /etc/sysconfig/network-scripts/网卡名
	●	ifconfig 用于显示和设置网卡的参数
	命令格式： ifconfig[网卡名]
	
	[root@wjw ~]# cat /etc/sysconfig/network-scripts/ifcfg-enp5s0 
	TYPE=Ethernet 	#网卡类型=以太※
	PROXY_METHOD=none #代理方式=关闭
	BROWSER_ONLY=no #只是浏览器=否
	BOOTPROTO=dhcp #获取IP地址的方式=固定IP※
	DEFROUTE=yes #是否设置默认路由=是
	IPV4_FAILURE_FATAL=no #是否开启ipv4致命检测=否( 如果i pv4配置失败禁用设备)
	IPV6INIT=yes 
	IPV6_AUTOCONF=yes 
	IPV6_DEFROUTE=yes
	IPV6_FAILURE_FATAL=no
	IPV6_ADDR_GEN_MODE=stable-privacy
	NAME=enp5s0 #物理网卡设备名字※
	UUID=3aa721f2-1ec0-4e90-b4fc-77b67864996e #网卡UUID
	DEVICE=enp5s0 #网卡名字※
	ONBOOT=yes #开机或重启时是否启动网卡※
	IPV6_PRIVACY=no
	
	[root@wjw network-scripts]# ifconfig 
	enp5s0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
	    	inet 10.20.18.51  netmask 255.255.254.0  broadcast 10.20.19.255
	    	inet6 fe80::1a76:4997:c7d8:3cbb  prefixlen 64  scopeid 0x20<link>
	    	ether c0:3f:d5:e0:9d:3e  txqueuelen 1000  (Ethernet)
	    	RX packets 23153629  bytes 2838031848 (2.6 GiB)
	    	RX errors 0  dropped 2  overruns 0  frame 0
	    	TX packets 3402812  bytes 329705760 (314.4 MiB)
	    	TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

|序号|项目|解释|
|---|---|---|
|1|ens32|#网卡名称※|
|2|flags=4163| #标志|
|3|<UP|#网卡处于活跃状态※|
|4|BROADCAST|#支持广播|
|5|RUNNING|#网线已接入|
|6|MULTICAST|#支持组播|
|7|mtu 1500| #最大传输单元(字节)，表示此网卡一次能传输的最大数据包 ※|
|8|inet 192. 168.0.29|#IPV4地址※|
|9|netmask 255.255. 255.0|#子网掩码※|
|10|broadcast 192. 168.0.255|#广播地址※|
|11|inet6 fe80: : 8d50:c4d5:97b0:9d64|#IPV6地址|
|12|prefixlen 64 scopeid 0x20<1ink> |#前缀64作用域0x20|
|13|ether 00:0c:29:b0:cf:c8|#网卡MAC地址※|
|14|xqueuelen 1000|#网卡设置的传送队列长度|
|15|(Ethernet)|#网卡连接类型|
|16|RX packets 3948|#接收正确的数据包※|
|17|bytes 1811465 (1.7 MiB)|#接收的数据量与字节※|
|18|RX errors 0 dropped 0 overruns 0 frame 0|#接收到的错误包、丢弃的数据包数、由于速度过快而丢失的数据包、发生frame错误而丢失的数据包数※|
|19|TX packets 100|#发送的正确的数据包数※|
|20|bytes 8116 (7.9 KiB)|#发送的数据量、字节※|
|21|TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0|#发送时产生错误的数据包数、丢弃的数据包数、由于速度过快而丢失的数据包数、发生carrier错误而丢失的数据包数、冲突信息包的数目※|

```bash
#只查看指定的网卡
[root@wjw ~]# ifconfig enp5s0
lo:本地回环网卡，不是物理网卡，通过软件虚拟出来的一个网卡，127.0.0.1, 用于测试本机的联通性
[root@localhost ~]# ping 127.0.0.1
virbro:虚拟化的网络接口，通过软件技术虚拟出来的一个网卡，192.168.122.1, KVM虛拟化技术的时候
```

## Linux系统文件类型

	- 表示文件
	d 表示目录
	l 表示链接文件
	b 表示跨设备文件
	c 表示字符设备文件
	p 表示管道设备文件
	s 表示套接字文件
### Linux系统下的归属关系
	在Linux系统下，文件给用户分成了三类
		u所有者:文件或目录的拥有者，拥有者的权限通常是最大的
		g所属组:文件或目录属于哪一个组,所属组的权限略微比所有者小
		o其他人:既不是文件或目录的所有者，也部署于文件或目录组内的成员，其他人的权限通常最小的权限
	
		//以长格式显示目录下所有内容，包括详细的属性信息
		[ root@localhost ~]# 1s -1
		-rw-r--r--. 1 root root 1831 3月 13 17:45 initial-setup-ks.cfg
		drwxr-xr-x. 2 root root 6    3月 13 17:47 公共
		lrwxrwxrwx. 1 root root 7    3月 13 17:15 bin -> usr/bin
		#解释
			第一个位置（-|d|l）表示该文件的类型
			rw- r-- r--: 所有者u、所属组g、其他人o的权限
			Linux系统基本权限
			r：读取
			w：写入 
			x：执行 
			-：没有权限
			权限的顺序：rwxrwxrwx
		1:代表文件的引用次数，只针对与做了硬连接的文件才有效
		root:文件的所有者
		root:文件的所属组
		1831:文件的大小，默认以字节为单位显示大小
		3月 13 17:45:文件最近一次的修改时间
		initial-setup-ks.cfg:文件名
### Linux系统辨别目录与文件的方法
	++ 蓝色表示目录(windows系统里的文件夹)
	++ 白色表示文件
	++ 浅蓝色表示链接文件(类似于windows系统的快捷方式)
	++ 绿色表示可执行文件
	++ 红色表示压缩文件
	++ 黄色表示设备文件(硬盘、键盘、鼠标、网卡、CPU硬件设备都是以文件的形式存在的)
	++ 红色闪动文件-->表示链接文件不可用
	++ 紫色表示图片
## Linux系统的运行级别
```bash
Linux系统运行级别: linux系统有7个运行级别，不同的运行级别运行的程序和功能都不一样，而Linux系统默认是运行在一个标准的级别上，系统运行级别文件/etc/inittab文件
	运行级别0:所有进程被终止,机器将有序的停止，关机时系统处于这个运行级别(关机)
	运行级别1:单用户模式，(root用户进行系统维护) ，系统里运行的所有服务也都不会启动
	运行级别2:多用户模式(网络文件系统NFS服务没有被启动)
	运行级别3:完全多用户模式，(有NFS网络文件系统) 标准的运行级别
	运行级别4:系统未使用
	运行级别5:登录后，进入带GU的图形化界面，标准的运行级别
	运行级别6:系统正常关闭并重启
指令： runlevel
	[root@wjw /]# runlevel
	N 3
	#解释：3表示当前系统处于的运行级别
	#解释: N代表没有从任何级别跳转过来
指令：init 2
	#解释：切换到级别2
```
# 命令基础 
### 命令行概述、格式、快捷键
	1.命令行：管理员输入的一串用来完成XX任务的字符，按Enter键提交。
	2.解释器：Linux系统中的一个用来翻译/解释器管理员提交的命令行的特殊程序（/bin/bash），通常称为shell（外壳，包在Linux内核外边的一层壳），负责把用户提交的指令变成内核能理解并执行的指令。
	3.内核：操作系统（控制计算机硬件的软件平台）的最核心的部分（kernel，nt），主要用来管理CPU处理器、内存、磁盘等各种硬件设备
#### 命令

```bash
◆命令提示符含义介绍
[当前用户名@主机名 当前所在工作目录] 用户提示符

◆管理员提示符为#
[root@localhost ~]#
解释:当前用户名为root@主机名为localhost当前所在目录为~家目录#当前用户身份是超级管理员

◆普通用户提示符为$
[isi@localhost ~]$
++ ~家目录:用户的私有场所，其他用户不能随便访问
++ root超级管理员的家目录: /root
++ 普通用户的家目录: /home/用户名同名
	eg. lisi用户的家目录: /home/lis
```

#### 命令行的基本格式：命令名字 [-选项……] [参数……]

	++ 命令字：命令本身（实现什么功能）
	++ 选项:
		++ 短选项: -l -a -d -h (单个字符)，可以合并使用: -la -lh
		++ 长选项: --help (单词)，长选项通常是不能合并使用的
		++ 选项的作用，控制命令的执行方式、效果
		++ 参数的作用，为命令提供操作对象。命令的执行对象，文件/目录/程序等
		++ 选项可以有多个，参数也可以有多个
### 常用的快捷键
	Tab ：自动补全命令的名字、文件路径、服务名、软件名
	Ctrl + L ：清屏
	Ctrl + C ：放弃当前任务
	Ctrl + a ：将当前光标移动至行首
	Ctrl + u ：清空至行首
	Ctrl + w :删除一个单词
	Ctrl + e ：将当前光标移动至行尾
	Ctrl + backspace ：删除
	Esc + . : 快速粘贴前一条命令的最后一个参数
	键盘上下键调出历史命令
	exit : 退出系统
### 常用命令
#### A
	◆alias命令用于设置命令别名，用户可以使用alias自定义命令别名来简化命令的复杂度
	●.bashrc 文件存放命令别名
	[root@wjw ~]# cat .bashrc 
	# .bashr
	# User specific aliases and functions
	alias rm='rm -i'
	alias cp='cp -i'
	alias mv='mv -i'
	# Source global definitions
	if [ -f /etc/bashrc ]; then
		. /etc/bashrc
	fi
	export PATH=/root/anaconda3/bin:$PATH
	
	++命令格式:
		alias [别名]=[命令] #注意事项:等号(=)前后不能有空格
		unalias别名 #取消别名
		eg.
		[root@localhost ~]# alias #该命令直接使用可列出当前系统所有别名
		[root@localhost ~]# alias hn=hostname #设置别名
		[root@localhost ~]# unalias hn #取消别名
	
		[root@wjw ~]# alias
		alias cp='cp -i'
		alias egrep='egrep --color=auto'
		alias fgrep='fgrep --color=auto'
		alias grep='grep --color=auto'
		alias l.='ls -d .* --color=auto'
		alias ll='ls -l --color=auto'
		alias ls='ls --color=auto'
		alias mv='mv -i'
		alias rm='rm -i'
		alias which='alias | /usr/bin/which --tty-only --read-alias --show-dot --show-tilde'
		[root@wjw ~]# which ls
		alias ls='ls --color=auto'
		/usr/bin/ls
		[root@wjw ~]# /usr/bin/ls
		[root@wjw ~]# ls
	
		#取消本次命令的别名功能"\"
		[root@test ~]# \ls
---
	◆
#### B
#### C
	◆cd(change directory) ： 用来改变工作目录
		++使用 ~ 表示当前用户的主目录， ~zhangsan表示zhangsan的主目录（/home/zhangsan）
		++常用快捷操作
			~表示为家目录
			.表示当前目录
			..表示上一级目录
			-可在两路径之间来回切换
---
	◆cat命令：用来阅读短文件，直接显示整个文件的全部内容
			● cat (英文全拼: concatenate) 命令用于查看文本文件内容
			● 命令格式: cat [选项]文件名
			● 常用选项:
				-n #查看文件时以行号的形式显示文件内容
---
	◆cp ：用来复制文档
		常用选项 -r,(recursive) 复制目录(包含该目录下所有的子目录和文件)
			eg. cp file1 file2 
			eg. cp -r mulu1 mulu2
		-p保留源文件属性不变(如:修改时间、归属关系、权限)
---


---
		◆
#### D
	◆date命令用
	●date命令用于显示或设置系统日期与时间，24小时制，12个月，31天。
	●命令格式: 
		date [-选项] [+格式符] #查看系统日期时间
		date [-选项] [MMDDhhmm[[CC]YY][.SS]] #设置日期时间
	常用选项: -S 设置日期时间
	●格式符:
		。+%Y	年份
		。+%B	月份
		。+%d	日
		。+%H	时
		。+%M	分
		。+%S	秒
		。+%F	年-月-日
		。+%X 时:分:秒
	eg.[root@wjw ~]# date
		 Fri Dec 17 05:15:48 -03 2021
		 [root@wjw ~]# date +%Y
		 2021
		 [root@wjw ~]# date +%B
		 December
		 [root@wjw ~]# date +%d
		 17
		 [root@wjw ~]# date +%H
		 05
		 [root@wjw ~]# date +%M
		 18
		 [root@wjw ~]# date +%S
		 04
		 [root@wjw ~]# date +%F
		 2021-12-17
		 [root@wjw ~]# date +%X
		 05:18:10 AM
		 [root@wjw ~]# date +%F-(加什么符号显示什么符号,除了空格)%X
		 2021-12-17-(加什么符号显示什么符号,除了空格)05:20:36 AM
		 [root@wjw ~]# date -s 'XX-XX-XX XX:XX:XX' #要用引号，表示一个整体
		 ※※※解释：
		 ''单引号：屏蔽特殊符号的功能，引用整体
		 ""双引号：引用整体，不会屏蔽特殊符号的功能
	
	#Linux的两种时钟
	系统时钟:内核通过CPU的工作频率去计算的时间
	硬件时钟:
	eg.
		 #显示并设置系统与硬件按时钟
		 [root@wjw ~]# clock
		 Fri 17 Dec 2021 05:32:20 AM -03  -0.544968 seconds
		 [root@wjw ~]# date
		 Fri Dec 17 16:32:13 -03 2021
		 [root@wjw ~]# hwclock -w #将硬件时钟同步为系统时钟-Set the Hardware Clock to the current System Time.
		 [root@wjw ~]# hwclock -s #将系统时钟同步为硬件时钟-Set the System Time from the Hardware CLock.
---
	◆ cal显示日历
	[root@wjw ~]# cal
	December 2021   
	Su Mo Tu We Th Fr Sa
	          1  2  3  4
	 5  6  7  8  9 10 11
	12 13 14 15 16 17 18
	19 20 21 22 23 24 25
	26 27 28 29 30 31
	
	[root@wjw ~]# cal 2021 #查看2021年的全年月份
---
	◆

#### E
	◆ echo命令：用于输出指定的字符串和变量
		命令格式: echo [-选项] [参数]
		范例:
		[root@localhost -]# echo abc
		[root@localhost -]# echo $SHELL
		[root@wjw wjw]# echo wjw > 1.txt 
		[root@wjw wjw]# cat 1.txt 
		wjw
---
	◆
---
	◆
#### F
```bash
◆ FACL访问控制列表
	● FACL (Filesystemctl Access Control List)文件系统访问控制列表:利用文件扩展属性保存额外的访问控制权限，单独为每一个用户量身定制一个权限
	● 命令格式: setfacl 选项 归属关系:权限 文档
	● 常用选项:
		。-m	设置权限
		。-x	删除指定用户权限
		。-b	删除所有用户权限
	eg.
		[ root@localhost ~]# setfac1 -m u:natasha:rx /yunwei/
		[root@1ocalhost ~]# 11 -d /yunwei/
		drwxrWx---+ 2 root yunwei 54 4月11 16:43 /yunwei/
		[root@localhost ~]# 11 -d /test
		drwx rwxrwt.2 root root 42 4月11 16:11 /test
		#
		[root@localhost ~]# getfac1 /yunwei
		getfac1: Removing leading '/' from absolute path names
		# file: yunwei
		# owner: root
		# group: yunwei
		user: : rwx
		user: natasha:r-x
		group: :rwx
		mask: : rwx
		other: :---

		#用户测试权限
		[natasha@localhost ~]$ 1s /yunwei/
		1s:无法打开目录/yunwei/:权限不够
		[natasha@localhost ~]$ setfac1 -m u:natasha:rx /yunwei 
		setfac1: /yunwei: 不允许的操作
		[natasha@locaThost ~]$ 1s /yunwei/
		he11.sh kenji. txt
		lisi. txt

		#
		[natasha@localhost yunwei]$ rm -rf kenji. txt
		rm:无法删除"kenji. txt":权限不够
		[natasha@localhost yunwei]$ touch natasha. txt
		touch:无法创建"natasha. txt":权限不够
		[natasha@localhost yunwei]$ vim kenji. txt

		#
		[root@localhost ~]# setfac1 -m u:tom:rx /yunwei
		[root@localhost ~]# setfac1 -m u:jack:rx /yunwei 
		[root@localhost ~]# setfacl -m u:hary:rx /yunwei
		[root@1oca1host ~]# getfac1 /yunwei
		getfac1: Removing leading‘ /' from absolute path names
		# file: yunwei
		# owner: root
		# group: yunwei
		user: : rwx
		user:hary:r-x
		user: tom: r-x
		user: natasha:r-x
		user:jack:r-x
		group: : rwx
		mask: : rwx
		other: :---

		#删除指定用户ACL权限
		[root@localhost ~]# setfac1 -X u:tom /yunwei
		[root@1ocalhost ~]# getfac1 /yunwei
		getfacl: Removing 1eading ' /' from absolute path names
		# file: yunwei
		# owner: root
		# group: yunwei
		user: : rwx
		user:hary:r-x
		user: natasha:r-x
		user:jack:r-x
		group: : rwx
		mask: : rwx 
		other: :---
		
		#清除所有用户ACL权限
		[root@localhost ~]# setfac1 -b /yunwei
		[root@Tocalhost ~]# getfac1 /yunwei
		getfac1: Removing leading '/' from absolute path names
		# file: yunwei
		# owner: root
		# group: yunwei
		user: : rwx
		group: : rwx
		other: :---
```

---

```bash
◆
```



#### G

#### H
	◆ head命令:用来显示文件开头部分内容，默认显示文件开头10行内容
		命令格式: head [选项]参数
		常用选项: -n<行数>指定显示的行数 -f动态显示
		eg.
			[root@localhost ~]# head /etc/passwd
			[root@localhost ~]# head /etc/fstab
			[root@1oca1host ~]# head /etc/group
			[root@localhost ~]# head /etc/hostname
			[root@localhost ~]# head /etc/hosts
			[root@1ocalhost ~]# head /etc/sysconfig/network-scripts/ifcfg-ens32
			#查看存放DNS配置文件信息
			[root@1ocalhost ~]# head /etc/resolv. conf
			#使用-n指定显示文件前多少行内容
			[root@1oca1host ~]# head -n 5 /etc/passwd
			[root@localhost ~]# head -n 6 /etc/passwd
			[root@1ocalhost ~]# head -n 15 /etc/passwd
			[root@1ocalhost ~]# head -n 20 /etc/passwd
---
	◆hash：与hash表有关
		hash命令：查看hash表
		hash -r：删除hash表
---
	◆help：help命令帮助手册
		● help命令用于查看shell内部命令的帮助信息，包括使用方法、选项等..
		● 命令格式: help [选项]命令
			命令格式: 命令 --help
---
	◆history管理历史命令
	history命令用于显示历史记录和执行过的命令，登录shell时会读取~./bash_ history历史文件中记录下的命令，当退出或登出shel时，会自动保存到历史命令文件，该命令单独使用时，仪显示历史命令
	++命令格式:
		history [-选项] [参数]
	++常用选项:
		-a 追加本次新执行的命令至历史命令文件中
		-d 删除历史命令中指定的命令
		-c 清空历史命令列表
			eg.[root@test ~]# help history #历史命令帮助
				 [root@test ~]# history #查看历史命令
				 [root@test ~]# cat .bash_history #查看历史命令文件
				 [root@test ~]# history -a #将历史命令缓存立刻写入.bash_history文件中
				 [root@test ~]# history -d 655 #按偏移量删除历史命令
				 [root@wjw ~]# history -c #只是清空缓存
				 [root@wjw ~]# rm -rf .bash_history #实际清空历史命令

快捷操作:|解释|备注|
|---|---|---|
!N|#调用命令历史中第N条命令|
|!string|调用命令历史中以strind开头的命令|字符调用会调用最近一次使用的命令|
|!!|重复执行上一条命令|

	[root@wjw ~]# cat /etc/profile
	...
	46 HISTSIZE=1000 #默认能记录的最大命令条数
---
		◆hostname命令用于显示和设置主机名
		/etc/hostname文件用于存放主机名
		命令格式: hostname [-选项] [新名称]
		注意：主机名显示·（点）前面的内容，比如xxx.yyy，那么显示的时候就是xxx。
		eg.
		#查看主机名
		[root@localhost ~]# hostname
		#临时修改主机名(立刻生效，服务器重启以后失效)
		[root@localhost ~]# hostname xxx
		#临时设置新主机名
		[root@test ~]# hostnamectl set-hostname xxx
		#命令行永久修改主机名(立刻生效，不需要重启系统)
		[root@localhost ~]# hostnamect1 set-hostname xxx
		#进入/etc/hostname文件中修改，需要重启系统才能生效
		[root@wjw ~]# vim /etc/hostname 
---

#### I
#### J
#### K
#### L
	◆ls(list) ： 用于查看目录下内容及目录和文件详细属性信息
		++常用选项
		-l，长格式（long）列出对象的详细信息
		-h，显示更易懂（human being）的容量单位（kB、MB、GB）
		-d，只看 目录（directory）/文件 本身的信息（即使参数是一个目录，下面还有内容也不会显示）
			一般用 -ld
		-a/A，列出隐藏文档（名称以.开头的文档）
		-i，查看inode号（系统任何的文件或目录都有一个唯一的编号）
		-R，递归查看目录下所有内容(从头到尾)
---
	◆less ：用来阅读长文件，先显示文件的第一屏内容。
		通过PageUP和PageDown翻页阅读，q退出
		/字符串 :#搜索指定字符电(n从上向下搜索，N从下向上搜索)
		-N #以行号形式显示文件内容
		G:直接跳转到文件最后一行
		gg:直接跳转到文件行首
#### M
	◆mkdir(make directory) ： 创建新的目录
	命令格式: mkdir [-选项]目录名
		常用选项：
		-p，递归创建多层目录（parent），如果目录已经存在，也不会 提示错误。
		注意事项:目录还是文件的名字，除了以"/"以外的任意名称,"/"根目录，路径分隔符
		文件或目录的名字长度不能超过255个字符
---
	◆mv ：移动/改名文档
		比如 mv file1 file2 、mv mulu1 mulu2
		mv命令参数(选项)：
	
	-b ：若需覆盖文件，则覆盖前先行备份。 
	
	-f ：force 强制的意思，如果目标文件已经存在，不会询问而直接覆盖；
	
	-i ：若目标文件已经存在时，就会询问是否覆盖！
	
	-u ：若目标文件已经存在，且源文件比较新，才会更新
	
	-t ：指定mv的目标目录，该选项适用于移动多个源文件到一个目录的情况，此时目标目录在前，源文件在后。
	
	-v ：显示过程
---
	◆man获取命令帮助手册
		●man命令用于查看系统命令的帮助信息，包括使用方法、选项、使用例子等，对比--help，mna输出的信息更加详细
		●命令格式: man [-选项] 命令
		●常用快捷操作
			。向下键向下移一行
			。向上键向上移一行
			。[Page Down]向下翻一页
			。[Page Up]向上翻一页
			。/关键字#搜索关键字，配合n (向下查询)、N (向上查询)
			。q退出
---
	◆软连接与硬连接
		● Linux中的链接文件类似于windows中的快捷方式
		● 软连接特点:软连接可以跨分区，可以对目录进行链接,源文件删除后，链接文件不可用
		● 连接命令格式: ln -s 源文件路径 目标路径
		●	硬链接特点:硬连接不可以跨分区，不可以对目录进行链接,源文件删除后，链接文件仍然可用
		●	硬连接命令格式: ln 源文件路径 目标路径
		注意:创建链接时一定要写目录或文件的绝对路径，哪怕是在当前路径下，也要写绝对路径
		●	硬连接的文件可以实现同步更新，并且保持属性不变，并且硬连接文件的i节点号相同
---
	◆locate命令
		locate命令会从var/lib/mlocate/mLocate.db这个数据库中查找文件所在位置，速度更快。


#### N
#### O
#### P
	◆pwd(print working directory) ：打印当前的工作目录
#### Q
#### R
	◆rmdir（remove directory）命令：删除空目录
	命令格式：rmdir [-选项]目录名
---
	◆rm ：用来删除文档
		常用选项 
		-r, 删除目录的时候需要加; 
		-f,强制(force)删除文档时需要加
		* 常用字符，代表任意、所有
		比如 rm -rf /* 删根操作(慎做！！！)
---
	◆rz命令：从本地上传至服务器

#### S
	◆su(substitute user) : 切换到另外一个用户身份，建议加上 -l 选项（简写为 -）来模拟登录过程
		++管理员切换到其他用户，不需要密码
		++普通用户切换到其他用户，需要验证对方的的密码
---
	◆stat：查看文件原数据
		[ root@Localhost ~]# stat hello. txt
		文件: "hello. txt"
		大小: G 块: 0 I0块: 4096 普通空文件
		设备: fd00h/ 64768d Inode: 33575020 硬链接: 1
		权限: (0644/ -rw-r--r--) Uid: ( 0/ root) Gid: ( 0/ root)
		环境:unconfined u:object r :admin home t:sO
		最近访问: 2021-03-14 16:38: 14.349861770 +0800
		最近更改: 202103- 14 16:38: 14.349861770 +0800
		最近改动: 2021-03-14 16:38: 14.349861770 +0800
		创建时间: -
---
	◆sz命令：从服务器下载至本地
---
	◆sleep命令: 用来将目前动作延迟一段时间
		命令格式: sleep 时间
		常用选项:s 秒 m 分钟 h 小时 d 日
		[root@host20 -]# sleep5 #默认以秒为单位
		[root@host20 -]# sleep 5m
---
	◆su命令
		●su命令用于切换当前用户身份到其他用户身份
		●命令格式: su [-选项] [用户名]
			eg.
				#只切换用户身份，环境没有改变
				root@localhost ~]# su user1
				[user1@1ocalhost root]$ ls
				T's:无法打开目录.:权限不够
				[user1@localhost root]$ cd
				[user1@1oca1host ~]$ exit
				exit
				#切换用户身份，连同环境一起切换
				[root@1ocalhost ~]# su - user1
				上一次登录:六4月10 16:54:40 CST 2021pts/1 上
				[user1@localhost ~]$ pwd
				/home/user1
				#普通用户切换为root (需婴输入root用户的密码)
				[user1@localhost ~]$ su - root
				密码:
				上一次登录:六4月10 16:05:17 CST 2021从192. 168.0.1pts/2上

---


---
	◆

#### T
	◆touch ：用来测试创建指定名称的文件（内容为空）
		● touch命令用于创建新的空白文件
		● 命令格式: touch [-选项]文件名
		#如果存在同名文件时，touch命令没有提示，但原有文件不会被覆盖
		[ root@1 ocalhost ~]# touch t1
---
	◆tail命令:用来显示文件末尾部分内容，默认显示文件末尾10行内容
		命令格式: tail [选项]参数
		常用选项: 
			-n<行数>指定显示的行数
			-f动态显示
		eg.
			[root@1ocalhost ~]# tail /etc/passwd
			3使用-n指定显示文件前末尾多少行内容
			[root@localhost ~]# tail -n 5 /etc/passwd
			[root@localhost ~]# tail -n 5 /etc/sysconfig/network-scripts/ifcfg-ens32
			IPADDR="192.168.0.50"
			PREFIX="24"
			GATEWAY="192.168.0.254"
			DNS1="114.114.114.114"
			IPV6_ PRIVACY="no"
		#动态查看文件内容
			root@localhost ~]# tail -f t1

#### U
	 ◆查看内核信息uname命令用于显示系统内核信息
		● 命令格式: uname [-选项..]
		● 常用选项:
		++ -s: 显示内核名称
		++ -r：显示内核版本
		eg.
		[root@1ocalhost ~]# uname
		Linux
		[root@1ocalhost ~]# uname -rs
		Linux 3.10.0-957.e17. x86_ _64
			
		#Linux内核官网
		https: //www. kerne1. org/

|项目|解释|
|------|------|
|Linux|#内核名称|
|3|#主版本|
|10|#次版本|
|0|#释出版本|
|957|#修改版本|
|e17|#Enterprise Linux (企业版Linux)|
|x86_ 64|#CPU架构|

---
		◆ umask预设权限
		● umask用于显示或设置创建文件的权限掩码
		● 命令格式: umask [-p] [-S] [mode]
		eg.
			root@1ocalhost ~]# mkdir /test2
			[root@localhost ~]# ll -d /test2
			drwxr-xr-x.2 root root 6 4月11 15:05 /test2
			[root@localhost ~]# umask --help
			-bash: umask: --:无效选项
			umask:用法:umask [-p] [-s] [模式]
			[root@localhost ~]# umask -p
			umask 0022
			[root@localhost ~]# umask -S
			U=rwx,g=rX,O=rX
			[root@localhost ~]# umask g+W
			[root@localhost ~]# mkdir /test3
			[root@locaThost ~]# ll -d /test3
			drwxrwxr-x.2 root root 6 4月11 15:09 /test3
			[root@localhost ~]# umask g-W
			[root@localhost ~]# mkdir /test4
			[root@localhost ~]# ll -d /test4
			drwxr-xr-xI 2 root root 6 4月11 15:10 /test4

---
	◆
#### V
	◆vi/vim编辑器-vi(visual interface)，可视化界面，Unix/Linux系统中默认文件编辑器。
	vim，vi improved，vi编辑器的增强版，由vim-enhanced软件包提供。
	使用vi/vim创建/修改文件

#### W
	◆wc统计命令：wc用于统计文件的字节数、行数，并将统计的结果输出到屏幕
	命令格式: wc [-选项]文件名
	常用选项:
		-c #统计字节数
		-l #统计行数
	eg.
	[root@wjw ~]# wc /etc/passwd
	47   94  2442 /etc/passwd
	[root@wjw ~]# wc -c /etc/passwd
	2442 /etc/passwd
	[root@wjw ~]# wc -l /etc/passwd
	47 /etc/passwd

|项目|解释|
|---|---|
|47|行数|
|94|单词|
|2442|字节|

---
	◆
#### X
	◆
#### Y
	◆
#### Z
	◆
#### 其他符号
	◆管道符
	●管道符"|"：将命令的输出结果交给另外一条命令作为参数继续处理
	[root@wjw ~]# head -10 /etc/passwd
	root:x:0:0:root:/root:/bin/bash
	bin:x:1:1:bin:/bin:/sbin/nologin
	daemon:x:2:2:daemon:/sbin:/sbin/nologin
	adm:x:3:4:adm:/var/adm:/sbin/nologin
	lp:x:4:7:lp:/var/spool/lpd:/sbin/nologin
	sync:x:5:0:sync:/sbin:/bin/sync
	shutdown:x:6:0:shutdown:/sbin:/sbin/shutdown
	halt:x:7:0:halt:/sbin:/sbin/halt
	mail:x:8:12:mail:/var/spool/mail:/sbin/nologin
	operator:x:11:0:operator:/root:/sbin/nologin
	
	[root@wjw ~]# head -10 /etc/passwd |tail -5
	sync:x:5:0:sync:/sbin:/bin/sync
	shutdown:x:6:0:shutdown:/sbin:/sbin/shutdown
	halt:x:7:0:halt:/sbin:/sbin/halt
	mail:x:8:12:mail:/var/spool/mail:/sbin/nologin
	operator:x:11:0:operator:/root:/sbin/nologin
	
	[root@wjw ~]# head -10 /etc/passwd |tail -5 |wc -l
	5
	
	[root@wjw ~]# cat -n /etc/passwd |head -10 |tail -5
	 6	sync:x:5:0:sync:/sbin:/bin/sync
	 7	shutdown:x:6:0:shutdown:/sbin:/sbin/shutdown
	 8	halt:x:7:0:halt:/sbin:/sbin/halt
	 9	mail:x:8:12:mail:/var/spool/mail:/sbin/nologin
	10	operator:x:11:0:operator:/root:/sbin/nologin
	
	[root@wjw ~]# ifconfig enp5s0 |head -2
	enp5s0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
	    inet 10.20.18.51  netmask 255.255.254.0  broadcast 10.20.19.255
---
	◆重定向操作:将前面命令的输出结果，写入到其他的文本文件中
	●重定向的表示符号

|命令|解释|
|---|---|
|>|#重定向输出(覆盖)|
|>>|#重定向输出(追加)|
|<|#输入重定向(覆盖)|
|<<|#输入重定向(追加)|
|>|只收集正确的输出结果|
|2>|只收集错误的输出结果|
|&>|正确错误都收集| 

---
```bash
◆ 常用特殊符号的使用
Linux系统下通配符起到了很大的作用，对于不确定的文档名称可以使用以下特殊字符表示
*常用的特殊符号，在文件名上，用来代表任何多个任意字符
?常用的特殊符号，在文件名上，用来代表任意单个任意字符
[0-9] #在文件名上，用来代表多个字符或连续范围中的一个，若无则忽略
{a,b,cd,abcd} #在文件名上，用来代表多组不同的字符串，全匹配
	eg.
		[root@wjw ~]# ls /etc/*wd
		/etc/passwd
		[root@wjw ~]# ls /etc/*tab
		/etc/anacrontab  /etc/crontab  /etc/crypttab  /etc/fstab  /etc/inittab  /etc/mtab  /etc/rwtab  /etc/statetab
		[root@wjw ~]# ls /dev/tty?
		/dev/tty0  /dev/tty1  /dev/tty2  /dev/tty3  /dev/tty4  /dev/tty5  /dev/tty6  /dev/tty7  /dev/tty8  /dev/tty9
		[root@wjw ~]# ls /etc/host?
		/etc/hosts
		[root@wjw ~]# ls /etc/pass??
		/etc/passwd
		[root@wjw ~]# ls /etc/*ss*
		/etc/issue  /etc/issue.net  /etc/nsswitch.conf  /etc/nsswitch.conf.bak  /etc/passwd  /etc/passwd-

		/etc/gss:
		mech.d

		/etc/gssproxy:
		24-nfs-server.conf  99-nfs-client.conf  gssproxy.conf

		/etc/ssh:
		moduli      sshd_config         ssh_host_ecdsa_key.pub  ssh_host_ed25519_key.pub  			ssh_host_rsa_key.pub      ssh_config  ssh_host_ecdsa_key  ssh_host_ed25519_key    ssh_host_rsa_key

		/etc/ssl:
		certs

		/etc/sssd:
		conf.d
		[root@wjw ~]# ls /dev/tty[1-5]
		/dev/tty1  /dev/tty2  /dev/tty3  /dev/tty4  /dev/tty5
		[root@wjw ~]# ls /dev/tty[1,3,5,7,9]
		/dev/tty1  /dev/tty3  /dev/tty5  /dev/tty7  /dev/tty9
		[root@wjw ~]# ls /dev/tty{1,3,5,7,9,15,20,30}
		/dev/tty1  /dev/tty15  /dev/tty20  /dev/tty3  /dev/tty30  /dev/tty5  /dev/tty7  /dev/tty9
		[root@wjw ~]# ls /dev/tty{1..9}
		/dev/tty1  /dev/tty2  /dev/tty3  /dev/tty4  /dev/tty5  /dev/tty6  /dev/tty7  /dev/tty8  /dev/tty9	
```
---


	◆ grep文件内容过滤
			●grep用于查找文件中符合条件的字符串，它能利用正则表达式搜索文件中的字符串，并把匹配到的字符串的行打印出来
			●命令格式: grep [选项] "查找条件"目标文件
			●常用选项:
				。-n 	  #以行号形式输出
				。-i 	  #忽略字符串大小写
				。-V 	  #显示不包含匹配的行(排除)
			●常用正则表达式符号
				。^字符串	#显示以该字符串开头的行
				。$字符串   #显示以该字符串结尾的行
				。^$ 	  #显示空行
			●eg.


​	

# 内部命令和外部命令

	●什么是命令:用来实现某一种功能的指令或程序
	●命令的执行依赖于解释器(例如: /bin/bash) ，/etc/shels文件存放系统可用的shell
		用户---解释器(shell外壳)---内核
	●Linux命令的分类
			内部命令: shell程序自带的基本管理命令
			外部命令:	有独立的外部可执行程序文件命令
	●	type 	用于区别内部命令与外部命令
	●	which 用于查找可以执行程序文件位置
		总结:
		。	shell程序是用户和系统之间的接口，用于解释用户的命令
		。	查找命令对应的程序文件所在位置: which 命令
		。	shell程序大多数存放在/etc/shells文件中
		。	系统默认使用的shell为/bin/bash
		。	查看当前使用的shell: echo $SHELL
		。	区别内部命令与外部命令的方式: typt 命令
		。	shell程序查找可执行程序文件路径定义在$PATH环境变量中
		。	shell查找的外部命令路径结果会记录到缓存的hash表中


### 用户账号管理
	◆用户账号的作用:用户账号可用来登录系统，可以实现访问控制
		普通用户的权限非常小：仅可在自己的home目录和temp目录中进行操作
	 ●用户模板目录: /etc/skel/
		[root@wjw ~]# ls -a /etc/skel/
		.  ..  .bash_logout  .bash_profile  .bashrc  .mozilla
		解释：所有新创建的用户的家目录下都会生成这些文件。如果在这个(/etc/skel/)目录下新建其他的文件，那么相对应的在新建的用户的家目录下也会生成新建的文件。
		useradd创建用户
		●useradd命令用于创建新的用户
		●命令格式: useradd [-选项][用户名]
		●常用选项:
		。-u	指定用户UID
		。-d	指定用户家目录(了解)
		。-c	用户描述信息
		。-g	指定用户基本组(了解)
		。-G	指定用户附加组
		。-S	指定用户的shell
	
	◆/etc/passwd用户信息文件
	用户的基本信息存放在/etc/passwd文件
	[root@localhost ~]# vim /etc/passwd
	root :x:0:0: root:/root :/bin/bash
	#每个字段含义解释:用户名:密码占位符:UID:基本组GID:用户描述信息:家目录:解释器程序
	UID: 0超级用户
	UID: 1-499系统伪用户，不能登录系统并且没有家目录
	UID: 500-65535 普通用户
	
	组:
	基本组(初始组) :一个用户只允许有一一个基本组
	附加组(在基本组之外组) :一个用户可以允许有多个附加组
	
	◆id命令
	●id命令用于查看系统用户和用户所在组的信息
	●命令格式: id [-选项] [用户名]
	[root@wjw ~]# id wang
	uid=1002(wang) gid=1002(wang) groups=1002(wang)
	
	[root@localhost ~]# useradd user1
	#创建用户并指定用户的UID
	[root@localhost ~]# useradd -u 1100 user2
	#创建用户并指定用户的家目录
	[oot@1ocalhost ~]# useradd -d /opt/user3 user3
	#创建用户并指定UID与用户描述信息
	[root@localhost ~]# useradd -u 1400 -C yunwei user4
	#创建test组
	[root@1ocalhost ~]# groupadd test
	#创建用户指定用户UID、描述信息、基本组
	[root@localhost ~]# useradd -u 1500 -C xx0o@163.com -g test user5
	[root@localhost ~]# id user5
	#创建用户指定用户UID、描述信息、附加组
	[root@localhost ~]# useradd -u 1600 -C yunwei -G test xiaozhang
	[root@1ocalhost ~]# id xiaozhang
	uid=1600(xiaozhang) gid=1600(xiaozhang) 组=1600(xiaozhang) , 1401(test)
	#/sbin/nologin :禁止用户登录系统
	[root@localhost ~]# useradd -u 1800 -c test -S /sbin/nologin user8
	user8:x:1800:1800:test:/home/user8:/sbin/nologin
	
	◆/etc/default/useradd文件
	/etc/default/useradd存放用户默认值信息
	[root@1ocalhost ~]# vim /etc/defau1t/useradd
	# useradd defaults file
	GROUP= 100 #用户默认组
	HOME=/home #用户家目录
	INACTIVE=-1 #密码过期宽限天数(/etc/shadow文件第7个字段)
	EXPIRE= #密码失效时间(/etc/shadow文件第8个字段)
	SHELL=/bin/bash #默认使用的she11
	SKEL=/etc/ske1 #模板目录
	CREATE_MAIL_SPOOL=yes #是否建立邮箱
	
	◆/var/spool/mail/用户邮件目录
	[root@1ocalhost ~]# 1s /var/spoo1/mai1/
	laowang lisi rpc user1 user2 user3 user4 user5 user8 xiaozhang
	
	◆passwd设置用户密码
		●passwd命令用于设置用户密码
		●命令格式: passwd [-选项] [用户名]
		●密码规范:长度不能少于8个字符，复杂度(数字、字母区分大小写,特殊字符)，普通用户
		●密码规范：本次修改的密码不能和上次修改的密码太相近
		●常用选项
		。-S	查看密码信息
		。-l	锁定用户密码 注意：假如用户已经登陆，那么在当前状态下不会生效，只有当用户退出重新登陆时才会生效。
		。-u	解锁用户密码 注意：假如用户已经登陆，那么在当前状态下不会生效，只有当用户退出重新登陆时才会生效。
		。-d	删除密码 注意：假如用户已经登陆，那么在当前状态下不会生效，只有当用户退出重新登陆时才会生效。
		。--stdin 通过管道方式设置用户密码
		●非交互设置用户密码
		●命令格式: echo "密码”| passwd --stdin用户名
			[root@wjw ~]# passwd -S wang
			wang PS 2021-12-10 0 99999 7 -1 (Password set, SHA512 crypt.)
			[root@wjw ~]# useradd test1 #创建测试用户1
			[root@wjw ~]# echo 'XXoo123!@#' | passwd --stdin test1
			Changing password for user test1.
			passwd: all authentication tokens updated successfully.
	
	◆/etc/shadow用户密码文件
		●用户的密码信息存放在/etc/shadow文件中，该文件默认任何人都没有任何权限(不包括root)
		[root@localhost ~]# vim /etc/shadow
		root:$6$1ji5e8yg1rZWACI6SFONKr3qebZufQ.u0Mf/MbipzGw/MvvxS.vgxcy/duc4b/GU0U7tfe37wPQ4XJEXStqBuwvaJqq2/kY/g/783u/::0:99999:7::
		#每个字段含义解释: 
		第一字段:用户名
		第二字段:密码加密字符串，加密算法为SHA512散列加密算法，如果密码位是“*"或者“!!"表示密码已过期
		第三个字段:linux为何密码时间从1970年1月1号开始，最初计算机操作系统是32位，而时间也是用32位表示。因为用32位来表示时间的最大间隔是68年，而最早出现的UNIX操作系统考虑到计算机产生的年代和应用的时限综合取了1970年1月1日作为UNIX的纪元时间。密码最后一次修改日期，日期从1970年1月1日起， 每过一天时间戳加1。如果将这个数字改为0，那么用户在登陆时，系统会提示对密码进行修改。这个情况适用的场景：管理员分配给许多用户初始账号和密码，希望他们在进行登陆后自己修改密码。
			eg.
				#chage命令用于修改/etc/shadow文件信息，修改文件内容第三个字段(密码最后一次修改时间)
				[root@1ocalhost ~]# chage -d 0 user8
		第四个字段:密码修改的期限，如果该字段为0表示随时u可以修改密码，例如:该字段为10，代表10天之内不可以修改密
		第五个字段:密码有效期
		第六个字段:密码到期前警告时间(和第五个字段相比)
		第七个字段:密码过期后的宽限天数(和第五个字段相比)
		第八个字段:账号失效时间，日期从1970年1月1日起。如果该字段为-1，代表密码永不失效。注意：这个选项设置会覆盖掉前面的选项，比如设置密码立刻失效，那么之前的设置都会没用。
		第九个字段:保留
	
		◆usermod修改用户属性
		●tusermod命令用于修改已存在用户的基本信息
		●命令格式: usermod [-选项] 用户名
		●常用选项:
			。u修改用户UID
			。-d修改用户家目录
			。-g修改用户基本组
			。-c修改用户描述信息
			。-G添加用户附加组
			。-S修改用户shell
		eg.
			#修改用户UID (用户如果已经登录系统，则不允许修改)
			[root@localhost ~]# usermod -u 1111 user1
			[root@localhost ~]# id user1
			uid#修改用户的解释器
			[root@1ocalhost ~]# usermod -s /bin/bash user8
	
		◆userdel删除用户
			●userdel 用于删除给定的用户以及与用户相关的文件，该命令若不加选项仅删除用户账号,不删除用户相关文件
			●命令格式: userdel [.选项]用户名
			●常用选项:
				。-r删除用户同时，删除与用户相关的所有文件
			eg.
				#删除用户，仅删除账号，不删除家目录
				[root@localhost ~]# userde1 user8
				[root@loca1host ~]# 1s /home
				laowang 1isi
				userl user2 user4 user5 user8 xiaozhang
				[root@localhost ~]# id user8
				id: user8: no such user
				#删除用户，连同用户家目录一并删掉
				[root@localhost ~]# userde1 -r user4
				[root@1ocalhost ~]# 1s /home
				laowang 1isi
				userl user2 user5 user8 xi aozhang
				[root@localhost ~]# id user4
				id: user4: no such user
	
			◆chmod权限管理
		●	chmod (英文全拼: change mode)设置用户对文件的权限
		●	命令格式: chmod [选项] 归属关系+-=权限类别文件...
		●	root用户可以修改任何文件和目录的权限
		●	文件所有者也可以修改文件和目录的权限
		●	常用选项:
			。-R #递归修改，包含目录下所有的子文件与子目录
		●	归属关系: u-所有者 g-所属组 o-其他人
		●	权限类别: r读取 w写入 x执行 -没有权限
		●	权限数字表示: r:4 w:2 x:1 -:o
		●	操作:

|操作|解释|
|---|---|
|r|4|
|w|2|
|x|1|
|-|0|

|操作|解释|
|---|---|
|+|添加权限|
|-|去除权限|
|=|重新定义权限|

		eg.
			#查看文件详细属性
			[root@localhost ~]# 11 hello
			-rw-r--r--. 1 root root 426 3月28 15:00 hello
			#为文件所有者添加执行权限
			[roqt@1ocalhost ~]# chmod u+X hello
			[root@localhost ~]# ll hello
			-rwxr--r--. 1 root root 426 3月28 15:00 hello
			#为文件所属组添加写权限
			[root@1ocalhost ~]# chmod g+W he1lo
			[root@1ocalhost ~]# ll hello
			-rwxrw-r--. 1 root root 426 3月28 15:00 hello
			#为文件其他人添加写权限
			[root@localhost ~]# chmod O+W hello
			[root@localhost ~]# ll hello
			-rwxrw-rw-. 1 root root 426 3月28 15:00 hello
			#使用逗号(,)可以同时为多个用户授权
			[root@1ocalhost ~]# chmod g+X,O+X he1lo
			[root@localhost ~]# ll hello
			-rwxrwxrwx. 1 root root 426 3月28 15:00 hello
	
			#为文件所有者去除添加执行权限
			[root@1ocalhost ~]# chmod u-x hello
			[root@1ocalhost ~]# ll hello
			-rw-rwxrwx. 1 root root 426 3月28 15:00 hello
			#为文件所属组去除写权限
			[root@localhost ~]# chmod g-x he1lo
			[root@localhost ~]# ll hello
			-rW-rw-rwx. 1 root root 426 3月28 15:00 hello
			#为文件其他人去除写权限
			[root@1ocalhost ~]# chmod o-x he11o
			[root@1ocaThost ~]# ll hello
			-rw-rw-rw-. 1 root root 426 3月 28 15:00 he11o
			#使用逗号(,)可以同时为多个用户去除授权
			[ root@localhost ~]# chmod u-w,g-w,o-w hello
			[ root@localhost ~]# ll hello
			-r--r--r--. 1 root root 426 3月 28 15:00 hello
	
			#重新定义文件权限
			[root@1ocaThost ~]# chmod u=rwx hello
			[root@1ocalhost ~]# 11 he11o
			-rwxr--r--. 1 root root 426 3月 28 15:00 hello
			[root@localhost ~]# chmod g=rwx he11o
			[root@1ocalhost ~]# ll he11o
		-rwxrwxr--. 1 root root 426 3月 28 15:00 hello
			[root@1ocalhost ~]# chmod o=rwx he11o
			[root@localhost ~]# ll hello
			-rwxrwxrwx. 1 root root 426 3月 28 15:00 hello
	
			#对文件夹进行权限操作
			[root@locaThost ~]# mkdir /test
			[root@1ocaThost ~]# 11 -d /test
			drwxr-xr-x. 2 root root 6 4月11 14:30 /test
			[root@1ocalhost ~]# chmod g+w /test
			[root@1ocalhost ~]# 11 -d /test
			drwxrwxr-x. 2 root root 6 4月11 14:30 /test
			[root@1ocalhost ~]# chmod o+w /test
			[root@localhost ~]# 11 -d /test
			drwxrwxrwx. 2 root root 6 4月11 14:30 /test
	
			#重新定义文件夹权限
			[root@loca1host ~]# chmod u=rwx ,g=rx,o=rx /test
			[root@1ocalhost ~]# ll -d /test
			drwxr-xr-x. 2 root root 6 4月11 14:30 /test
			[root@loca1host ~]# chmod o=--- /test
			[root@loca1host ~]# ll -d /test
			drwxr-x---. 2 root root 6 4月11 14:30 /test
			[root@loca1host ~]# chmod ugo=rwx /test
			[root@loca1host ~]# ll -d /test
			drwxrwxrwx. 2 root root 6 4月11 14:30 /test
	
			#使用数字方法修改权限
			[root@1ocalhost ~]# 11 he11o
			-rwxrwxrwx. 1 root root 426 3月 28 15:00 hello
			所有者u:rwx 4+2+1=7
			所属组g:r   4
			其他人o:r   4
			[root@1ocalhost ~]# chmod 744 hello
			[root@loca1host ~]# ll hello
			-rwxr--r--. 1 root root 426 3月 28 15:00 he11o
	
	***！！！注意：设置权限时，设置权限为3可以成功，但是这是不对的。因为当一个文件不可读，但是可以进行写入操作这是冲突的。连文件里的内容都无法查看，根本不可能对其进行写的操作。***
	
	#去除所有用户权限
	[root@locaThost ~]# chmod 000 /hello.txt
	[root@1ocalhost ~]# ll /he11o.txt
	----------. 1 root student 0 4月 11 14:45 /hello.txt
	#递归修改权限
	[root@loca1host ~]# 11 -d /test
	drwxrwxrwx. 2 root root 21 4月11 14:37 /test
	[root@loca1host ~]# 1s /test
	abc.txt
	[root@loca1host ~]# 11 /test/abc. txt
	-rw-r--r--. 1 root root 0 4月11 14:37 /test/abc. txt
	[root@1ocalhost ~]# mkdir /test/xxoo
	[root@localhost ~]# 11 /test/xxoo/
	总用量0
	[root@localhost ~]# 11 -d /test/xxoo/
	drwxr-xr-x. 2 root root 6 4月11 14:54 /test/xxoo/
	[root@loca1host ~]# chmod -R 777 /test
	[root@localhost ~]# 11 /test/abc. txt
	- rwxrwxrwx. 1 root root 0 4月11 14:37 /test/abc. txt
	[root@loca1host ~]# 11 /test/xxoo
	总用量0
	[root@localhost ~]# 11 -d /test/xxoo
	drwxrwxrwx. 2 root root 6 4月11 14:54 /test/xxoo
	***！！！注意：用户对一个文件是否有权限进行删除，不是取决于用户对这个文件是否有权限，而是需要看当前用户对于文件所属的父目录是否存在权限进行操作***

---
	◆ chown归属关系管理
	● chown (英文全拼: change owner) 用于设置文件的所有者和所属组关系
	● 命令格式:
		。chown [选项] 所有者：所属组文档 #同时修改所有者和所属组身份
		。chown [-选项] 所有者 文档 #只修改所有者身份
		。chown [-选项] ：所属组 文档 #只修改所属组身份
	●常用选项:
		。-R 递归修改
		#修改文件的读写执行权限
		root@wjw /# chmod 744 /hello.txt 
		root@wjw /# ll hello.txt 
		-rwxr--r--. 1 root root 0 Dec 23 22:03 hello.txt*
		#只修改所有者身份
		root@wjw /# chown user1 /hello.txt 
		root@wjw /# ll /hello.txt 
		-rwxr--r--. 1 user1 root 0 Dec 23 22:03 /hello.txt*
		#只修改所属组身份
		root@wjw /# chown :user1 /hello.txt 
		root@wjw /# ll hello.txt 
		-rwxr--r--. 1 user1 user1 0 Dec 23 22:03 hello.txt*
		#同时修改所有者和所属组身份
		root@wjw /# chown 1isi:1isi /he11o. txt
		root@wjw /# ll /he1lo. txt
		-rwxr--r--. 1 1isi 1isi 4 4月11 15:26 /he11o. txt
	***！！！注意：chown命令只有管理员（root）有权限来进行修改***
	***chown -R命令：如果希望目录下面的所有子文件和子目录的归属关系都和父目录相同***
---
	SetUID特殊权限
		● SetUID (SUID) :对于一个可执行的文件用了SUID权限后，普通用户在执行该文件后，临时拥有文件所有者的身份，该权限只在程序执行过程中有效，程序执行完毕后用户恢复原有身份。
		● SetUID权限会附加在所有者的x权限位上，所有者的x权限标识会变成s
			eg.
		root@wjw /# which passwd
		/usr/bin/passwd
		root@wjw /# ll /usr/bin/passwd
		-rwsr-xr-x. 1 root root 28K Apr  1  2020 /usr/bin/passwd*
		● 设置SetUID命令格式: chmod u+s 文件名
		eg.
			#原先用户没有权限查看shadow文件，经过修改SUID后，有权限查看shadow文件了
			[root@localhost ~]# which cat
			/usr/bin/cat
			[root@localhost ~]# 11 /usr/bin/cat
			-rwxr-xr-x.1 root root 54160 10月31 2018 /usr/bin/cat
			[root@localhost ~]# chmod u+s /usr/bin/cat
			[root@localhost ~]# 11 /usr/bin/cat
			-rwsr-xr-x.1 root root 54160 10月31 2018 /usr/bin/cat
			[root@loca1host ~]# chmod u-S /usr/bin/cat
			[root@localhost ~]# 11 /usr/bin/cat
			-rwxr-xr-x.1 root root 54160 10月31 2018 /usr/bin/cat
			#
			[root@loca1host ~]# which vim
			/usr/bin/vim
			[root@loca1host ~]# 11 /usr/bin/vim
			-rwxr-xr-x.1 root root 2294208 10月31 2018 /usr/bin/vim
			[root@localhost ~]# chmod U+S /usr/bin/vim
			[root@localhost ~]# 11 /usr/bin/vim
			-rwsr-xr-x.1 root root 2294208 10月31 2018 /usr/bin/vim
			[root@localhost ~]# 11 /etc/passwd
			-rw-r--r--.1 root root 2737 4月10 17:26 /etc/passwd
			[root@loca1host ~]# chmod u-S /usr/bin/vim
			[root@localhost ~]# vim /etc/passwd
	***联想记忆：皇帝下旨到地方，那么圣旨就如同皇帝本人亲临***
	***！！！注意：生产环境中不可以随意修改SUID，这样会导致系统不安全***
---
	SetGID特殊权限
	● SetGID (SGID) :当对一个可执行的二进制文件设置了SGID后，普通用户在执行该文件时临时拥有其所属组的权限，该权限只在程序执行过程中有效，程序执行完毕后用户恢复原有组身份
	● 当对一个目录作设置了SGID权限后， 普通用户在该目录下创建的文件的所属组，均与该目录的所属组相同
	● SetGID权限会附加在所属组的x权限位上，所属组的x权限标识会变成s
	● 设置SetGID命令格式: chmod g+S文件名
	eg.
		[root@localhost ~]# mkdir /test6
		[root@locaThost ~]# chmod 777 /test6
		[root@localhost ~]# 11 -d /test6
		drwxrwxrwx. 2 root root 6 4月11 15:59 /test6
		[root@localhost ~]# chmod 9+S /test6
		[root@localhost ~]# 11 -d /test6
		drwxrwsrwx. 2 root root 6 4月11 15:59 /test6
		[root@localhost ~]# touch /test6/1.txt
		[root@localhost ~]# 11 /test6/1.txt
		-rw-r--r--. 1 root root 0 4月11 16:00 /test6/1.txt
		[root@1ocalhost ~]# chown :lisi /test6
		[root@1ocaThost ~]# 11 -d /test6
		drwxrwsrwx. 2 root lisi 19 4月11 16:00 /test6
		[root@localhost ~]# touch /test6/2. txt
		[root@localhost ~]# 11 /test6/2.txt
		-rw-r--r--. 1 root lisi 0 4月11 16:01 /test6/2.txt
---
	sticky BIT特殊权限
	● Sticky BITL(SBIT) :该权限只针对于目录有效，当普通用户对一个目录拥有w和x权限时,普通用户可以在此目录下拥有增删改的权限，应为普通用户对目录拥有w权限时，是可以删除此目录下的所有文件
	● 如果对一个目录设置了SBIT权限，除了root可以删除所有文件以外，普通用户就算对该目录拥有w权限，也只
	能删除自己建立的文件,不能删除其他用户建立的文件
	● SBIT权限会附加在其他人的x权限位上，其他人的x权限标识会变成t
	● 设置SBIT命令格式: chmod o+t目录名
	
		◆groupadd添加新组
		●groupadd用于创建-个新的工作组， 新组的信息将被添加到/etC/group文件中
		●命令格式: groupadd [-选项]组名
		●常用选项:
		。-g GID #指定组的GID
			eg.
				#创建组
				[root@1ocalhost ~]# groupadd -9 1555 student
				[root@localhost ~]# cat /etc/group
	
		/etc/group组信息文件
		●组信息存放在/etc/group文件中
		[root@localhost ~]# vim /etc/group
		root:x:0:
		#每个字段含义解释:组名:组密码占位符:GID:组中附加用户
		/etc/gshadow组密码文件
		●组密码信息存放在/etc/gshadow文件中
		[root@localhost ~]# vim /etc/gshadow
		root: : :
		#每个字段含义解释:组名:组密码:组内管理员:组中附加用户
---
		◆groupmod修改组属性
		●groupmod用于修改指定工作组属性
		●命令格式: groupmod [-选项] 组名
		●常用选项:
			。-g GID #修改组的GID
			。-n 新组名 #修改组名
		#修改组名
		[root@localhost ~]# groupmod -n stugrp student
		#修改组ID
		root@1ocaThost ~]# groupmod -g 1666 stugrp
---
		◆gpasswd组管理命令
		●gpasswd是Linux工作组文件/etc/group和/etc/gshadow管理工具，用于将用户添加到组或从组中删除
		●命令格式: gpasswd [-选项] 用户名 组名
		●常用选项:
			。-a #将用户添加到工作组
			。-d #将用户从工作组中删除
			eg.
				[root@1ocalhost ~]# useradd hary
				[root@localhost ~]# useradd tom
				[root@localhost ~]# useradd natasha
				[root@localhost ~]# useradd kenji
				[root@localhost ~]# useradd jack
				[root@localhost ~]# gpasswd -a hary stugrp
				正在将用户"hary"加入到“stugrp"组中
				[root@localhost ~]# gpasswd -a tom stugrp
				正在将用户“tom"加入到“stugrp"组中
				[root@localhost ~]# gpasswd -a kenji stugrp
				正在将用户"kenji"加入到“stugrp"组中
				[root@localhost ~]# gpasswd -a natasha stugrp
				正在将用户"natasha"加入到“stugrp"组中
				[root@localhost ~]# gpasswd -a jack stugrp
				正在将用户"jack"加入到“stugrp"组中
	
				#查看组文件信息
				[root@loca1host ~]# cat /etc/group
				stugrp:x:166:hary, tom, kenji ,natasha , jack
				#将用户从组中删除
				root@1ocaThost ~]# gpasswd -d tom stugrp
				[root@1ocalhost ~]# gpasswd -d hary stugrp
				正在将用户"hary"从"stugrp"组中删除
				[root@locaThost ~]# gpasswd -d jack stugrp
				正在将用户"jack"从"stugrp"组中删除
				[root@localhost ~]# gpasswd -d kenji stugrp
				正在将用户"kenji"从"stugrp"组中删除
				[root@localhost ~]# cat /etc/group
	
		◆groupdel删除组
		●groupdel 用于删除指定工作组
		●命令格式: groupdel 组名
			eg.
				[root@localhost ~]# groupde1 stugrp
			注意：删除组可以直接删除，相当于实际生活中一个团队直接解散了！








### 关机与重启
	关机与重启
	● linux 下常用的关机命令有: shutdown、halt、 poweroff. init
		。init 0 #关机
		。halt #立刻关机
		。poweroff #立刻关机
		。shutdown -h now #立刻关机
		。shutdown -h 10 #10分钟后自动关机
	● 重启命令: reboot shutdown
		。reboot #立刻重启
		。shutdown -r now #立刻重启
		。shutdown -r 10 #过+分钟后重启

## 服务器开关和安全开关
### 服务器开关systemctl
 	++ systemctl，系统控制器，用来管理Linux系统的开机/关机/服务资源运行状态
 	++ 直接执行systemctl列出可以管理的系统资源，包括各种系统服务
 	++ 控制服务当前运行状态 systemctl start|stop|status 服务名1 服务2 ...
 	 eg. systemctl start httpd
 	++ 控制服务开机自启状态 systemctl enable|disable 服务名1 服务2 ...
 	 eg. systemctl enable httpd
### 安全开关firewall、SELinux
	++ 防火墙的作用，内核的一套网络保护机制，通过firewall服务来控制
	++ 如何停止防火墙： systemctl disable firewall --now
	++ 安全增强型 Linux（Security-Enhanced Linux）简称 SELinux
	++ SELinux的作用，内核的一套系统保护机制，通过内核启动参数或者启动配置来控制
	
	++ 如何关闭SELinux机制（三种状态-Enforcing强制保护、Permissive宽松模式、Disabled禁用）
	# vi /etc/selinux/config
	SELinux = Enforcing|Permissive|Disabled => 重启后生效
	# setenforce 0|1                        =>立即变成宽松模式|强制模式
	# getenforce                            =>查看结果

### vi/vim文本编辑器
	●Vim是从vi发展出来的-一个文本编辑器，vim 具有程序编辑的能力，可以主动的以字体颜色辨别语法的正确性
	●vi/vim 共分为三种模式:命令模式、输入模式、底线命令模式(末行模式)
		。命令模式:刚刚启动vi/vim, 便进入了命令模式
		。输入模式:在命令模式下按a/i/o就进入了输入模式
		。ESC, 退出输入模式，切换到命令模式
		。底线命令模式:在命令模式下按下: (英文冒号)就进入了底线命令模式
	●命令格式: vim文件名
		。若目标文件不存在，则新创建文件并编辑
		。若目标文件以存在，则打开文件并编辑
	
			vim通常分为三种模式：底行模式、插入模式、命令行模式。
			（1）底行模式
			底行模式是进入vim的默认模式，可以退出vim或保存文件，也可以设置编辑坏境，进行复制、粘贴、删除等操作。
			（2）插入模式
			从底行模式输入i 进入插入模式即可进行文字输入，按Esc键退出插入模式返回命令行模式。
			（3）命令行模式
			控制屏幕光标的移动，字符、字或行的删除，移动复制某区段，进入插入模式或底行模式。
			通常也把底行模式归入命令行模式，这样Vim就被分成两种状态模式了。
	
	●命令模式:刚刚启动vi/vim, 便进入了命令模式

|序号|命令|解释|
|---|---|---|
|1|i|切换到输入模式，在当前光标所在字符前插入|
|2|I|进入插入模式并至光标于行首|
|3|a|(小a)切换到输入模式，在当前光标所在字符后插入|
|4|A|(大A)将光标置于行末|
|5|o|(小o)切换到输入模式，在当前光标所在行下插入新行|
|6|O|(大O)在当前行上加一行，并进入插入模式|
|7|:|切换到底线命令模式，以在最底一行输入命令|
|8|x|(小x)在命令模式 下删除当前光标所在的单字符|
|9|X|(大X)向前删除一个字符(3x向后删除3个字符、3X向前删除3个字符)|
|10|dd|(剪切)删除一整行内容，配合数字可删除指定范围内的行(3dd删除当前行开始的3行)|
|11|do|删至行首|
|12|d$|删至行尾|
|13|C|删除当前光标及光标后所有内容并进入输入模式|
|14|cc| 删除当前行并进入编辑模式|
|15|cw|删除当前字并进入编辑模式|
|16|c$|删除从当前位置至行末的字并进入编辑模式|
|17|u|恢复上一次修改内容，一次恢复一个操作，可多次恢复，直到恢复本次操作初始状态为止|
|※18|$|将光标移动至行尾|
|※19|0|将光标移动至行首|
|20|End|光标移动到当前行的最右端|
|21|Home|光标移动到当前行的最左端|
|22|gg|跳转至文件第一行|
|23|G|跳转至文件最后一行|
|24|yy|复制当前行，配合数字可以同时复制多行(3yy复制当前行开始的3行)|
|25|p|(小P)粘贴到当前光标的下一行|
|26|P|(大P)粘贴到光标的上一行|
|27|~|切换当前字符的大小写|
|28|.|重复前一个操作|
|29|Ctrl+r|重做前一个操作|
|30|h|向左移动光标(20h向左移动29个字符)|
|31|l|向右移动光标(20l向右移动20个字符)|
|32|k|向上移动光标(20k向上移动20行)|
|33|j|向下移动光标(20j向下移动20行)|
|34|J|将下一行和当前行连接为一行|
|35|xp|交换当前字符和下一个字符|
|36|/关键字|搜索文件内关键字，n从上向下快速定位关键字，N从下向上快速定位关键字|

	●底线命令模式可以输入单个或多个字符的命令,可用的命令非常多。

|序号|命令|解释|
|---|----|---|
|1|:w|保存|
|2|:w filename|另存为filename|
|3|:n,m w filename|将第n行到第m行另存为filename|
|4|:q|退出|
|5|:wq|保存并退出|
|6|:q!|强制退出不保存|
|7|:wq!|强制保存并退出|
|8|:set nu|以行号形式显示文件内容|
|9|:set nonu|取消行号显示|
|10|:行号|快速跳转到指定行|
|11|:r|(小r)读入另一个文件的数据,文件内容填加到光标的下一行|
|12|:R|(大R)替换光标所到之处的字符，直到按Esc键为止|
|13|/加关键字|查找关键字符，一直按n直到找到为止，/等同于?|

### 修改网卡IP地址
```bash
●网卡配置文件地址: /etc/sysconfig/network-scripts/网卡名
●ifconfig #用于显示和设置网卡的参数
●systemctl restart network #重启网络
●ifup 网卡名 #启动该网卡设备
●ifdown 网卡名 #禁用该网卡设备
	#重启网络(IP地址发生改变，当前终端会断开)
	[ root@test ~]# systemct1 restart network
	#查看所有网卡信息
	[root@test ~]# ip a

●使用命令修改网卡IP地址
nmcli connection modify 网卡名 ipv4.method manual ipv4.addresses Ip地址/掩码 connection.autoconnect yes
解释:
nmcli connection modify (修改)
网卡名ipv4.method (配置ipv4地址方法)
manual (手动配置)
ipv4.addresses (ipv4地址)
Ip地址/掩码connection.autoconnect yes (开机自动连接)
●激活网卡: nmcli connection up网卡名
●关闭网卡: nmcli connection down网卡名
●重启网卡: nmcli connection reload网卡名
	#使用命令修改网卡IPV地址
	[root@test ~]# nmc1i connection modify ens32 i pv4. method manua1 ipv4. addresses
	192.168.0.50/24 connecti on. autoconnect yes
	#激活网卡
	[root@test ~]# nmc1i connection up ens32
	[c:\~]$ ssh 192. 168.0.50

host命令
●host用于将一个域名解析到一个IP地址，或将一个IP地址解析到一个域名
	[root@wjw ~]# host www.baidu.com
	www.baidu.com is an alias for www.a.shifen.com.
	www.a.shifen.com has address 153.37.235.5
	www.a.shifen.com has address 153.37.235.4

nslookup命令
●nslookup用于查询域名解析是否正常,在网络故障时用来诊断网络问题
[root@wjw ~]# nslookup www.baidu.com
Server:		10.1.1.1
Address:	10.1.1.1#53

Non-authoritative answer:
www.baidu.com	canonical name = www.a.shifen.com.
Name:	www.a.shifen.com
Address: 153.37.235.4
Name:	www.a.shifen.com
Address: 153.37.235.5
```

# 课后作业

```bash
1.创建test1用户，并指定用户UID为6666,指定用户描述信息为test1 @163.com,指定用户解释器
为/sbin/nologin

[root@wjw ~]# useradd -u 6666 -c test1@163.com -s /sbin/nologin test1

2.创建名为stugrp组,将test1 用户加入到stugrp组

[root@wjw ~]# groupadd stugrp
[root@wjw ~]# gpasswd -a test1 stugrp

3.请写出/etc/passwd文件中每个字段含义

用户名密码占位符UID GID描述信息家目录解释器

4.创建test2用户，并设置密码为123456

[root@wjw ~]# useradd test2
[root@wjw ~]# passwd test2

5.修改root用户密码为123456

[root@wjw ~]# su root
[root@wjw ~]# passwd

6.请写出Linux系统下存放用户密码信息文件

 /etc/shadow

7.设置test2用户首次登录系统需要修改密码

[root@wjw ~]# chage -d 0 test2

8.使用root切换为test1用户身份

[root@wjw ~]# su - test1

9.将test2用户添加至stugrp组，并锁定用户密码

[root@wjw ~]# gpasswd -a test2 stugrp
[root@wjw ~]# passwd -l test2

10.删除test1用户，连同用户家目录一并删除

[root@wjw ~]# userdel -r test1

11.请写出Linux系统存放组信息文件，与组密码信息文件

/etc/group
/etc/gshadow

12.将test2用户从stugrp组中删除

[root@wjw ~]# gpasswd -d test2 stugrp

13.在根下创建upload目录,并修改目录所有者为test2用户，所属组为stugrp组,并将lisi用户加入到stugrp组,
修改所有者权限rwx,修改所属组权限为rwx,设置其他人没有任何权限

[root@wjw ~]# mkdir /upload
[root@wjw ~]# chown test2:stugrp /upload/
[root@wjw ~]# gpasswd -a lisi stugrp
[root@wjw ~]# chmod 770 /upload/

14.创建test3用户，非交互式设置用户密码为123456,并设置test3用户可以对upload目录拥有rx权限

[root@wjw ~]# useradd test3
[root@wjw ~]# echo 123456 | passwd --stdin test3
[root@wjw ~]# setfacl -m u:test3:rx /upload
[root@wjw ~]# getfacl /upload/

15.在根下创建shared目录,并同时设置所有人都有完全权限(至少两种方法设置)，要求所有普通用户在该目录
下只能修改自己创建的文件

[root@wjw ~]# mkdir /shared
[root@wjw ~]# chmod ugo=rwx /shared/
[root@wjw ~]# chmod 777 /shared/
[root@wjw ~]# chmod o+t /shared/
```

