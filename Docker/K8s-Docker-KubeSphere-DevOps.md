# 云平台核心

笔记：[Docker命令实战 · 语雀 (yuque.com)](https://www.yuque.com/leifengyang/oncloud/ox16bw)

## 1、为什么用云平台

- 环境统一
- 按需付费 

- 即开即用 
- 稳定性强

- ......

国内常见云平台：

- [阿里云](https://promotion.aliyun.com/ntms/act/ambassador/sharetouser.html?userCode=50sid5bu&utm_source=50sid5bu)、百度云、[腾讯云](https://curl.qcloud.com/iyFTRSJb)、[华为云](https://activity.huaweicloud.com/discount_area_v5/index.html?fromacct=d1a6f32e-d6d0-4702-9213-eafe022a0708&utm_source=bGVpZmVuZ3lhbmc==&utm_medium=cps&utm_campaign=201905)、青云......

国外常见云平台：

- 亚马逊 AWS、微软 Azure ...

## 1、公有云

购买云服务商提供的公共服务器

公有云是最常见的云计算部署类型。公有云资源（例如服务器和存储空间）由第三方云服务提供商拥有和运营，这些资源通过 Internet 提供。在公有云中，所有硬件、软件和其他支持性基础结构均为云提供商所拥有和管理。Microsoft Azure 是公有云的一个示例。

在公有云中，你与其他组织或云“租户”共享相同的硬件、存储和网络设备，并且你可以使用 Web 浏览器访问服务和管理帐户。公有云部署通常用于提供基于 Web 的电子邮件、网上办公应用、存储以及测试和开发环境。

公有云优势：

- **成本更低**：无需购买硬件或软件，仅对使用的服务付费。
- **无需维护**：维护由服务提供商提供。

- **近乎无限制的缩放性**：提供按需资源，可满足业务需求。
- **高可靠性**：具备众多服务器，确保免受故障影响。

- - 可用性： N个9   9   全年的故障时间： 365×24×3600×(1-99.9999%)

## 2、私有云

自己搭建云平台，或者购买

私有云由专供一个企业或组织使用的云计算资源构成。私有云可在物理上位于组织的现场数据中心，也可由第三方服务提供商托管。但是，在私有云中，服务和基础结构始终在私有网络上进行维护，硬件和软件专供组织使用。

这样，私有云可使组织更加方便地自定义资源，从而满足特定的 IT 需求。私有云的使用对象通常为政府机构、金融机构以及其他具备业务关键性运营且希望对环境拥有更大控制权的中型到大型组织。

私有云优势：

- **灵活性更强**：组织可自定义云环境以满足特定业务需求。
- **控制力更强**：资源不与其他组织共享，因此能获得更高的控制力以及更高的隐私级别。

- **可伸缩性更强**：与本地基础结构相比，私有云通常具有更强的可伸缩性。

***没有一种云计算类型适用于所有人。多种不同的云计算模型、类型和服务已得到发展，可以满足组织快速变化的技术需求。\***

***部署云计算资源有三种不同的方法：公共云、私有云和混合云。采用的部署方法取决于业务需求。\***

# 2、核心构架

## 0、所需软件

官网：https://electerm.html5beta.com/

Github：https://github.com/electerm/electerm/releases

## 1、基础概念

- 云服务器作为应用的最终载体
- VPC为所有云服务器提供网络隔离

- 所有云服务器都是绑定某个私有网络
- 安全组控制每个服务器的防火墙规则

- 公网IP使得资源可访问
- 端口转发的方式访问到具体服务器

## 2、实战操作

1、开通按量付费服务器

你做完了吗？

2、开通基于VPC的服务器集群

理解VPC了吗？

# docker基本概念

## 1、解决问题

### 1、统一标准

- 应用构建

  - Java、C++、JavaScript
  - 打成软件包
  - 微软都是统一以.exe结尾的运行软件
  - docker build ... 镜像

- 应用分享

  - 所有软件的镜像放到一个指定地方 docker hub

- 应用运行

  - 统一标准的 **镜像**
  - docker run

- ...

  容器化


#### 虚拟化技术

1. 基础镜像GB级别

2. 创建使用稍微复杂

3. 隔离性强

4. 启动速度慢

5. 移植与分享不方便

   ...

#### 	 容器化技术

1. 基础镜像MB级别

2. 创建简单

3. 隔离性强

4. 启动速度秒级

5. 移植与分享方便

   ...

#### 2、资源隔离

- CPU、memory资源隔离与限制

- 访问设备隔离与限制

- 网络隔离与限制

- 用户、用户组隔离限制

- ......

  # 2、架构

  ![](D:\运维\architecture.svg)

- Docker_Host:
  - 安装Docker的主机
  
- Docker Daemon:
  - 运行在Docker主机上的Docker后台进程
  
- Client:
  - 操作Docker主机的客户端（命令行、UI等)
  
- Registry:
  - 镜像仓库
  - Docker Hub-[Docker - Official Image | Docker Hub](https://hub.docker.com/_/docker)
  
- lmages:
  - 镜像。带环境打包好的程序，可以直接启动运行
  
- Containers
  - 容器，由镜像启动起来正在运行中的程序

交互逻辑

​	装好Docker，然后去软件市场寻找镜像，下载并运行，查看容器状态日志等排错

#### 3、安装

- ①移除以前docker相关包

-  ```bash
   sudo yum remove	docker*
   				docker-client \
   				docker-client-latest \
   				docker-common \
   				docker-latest \
   				docker-latest-logrotate \
   				docker-logrotate \
   				docker-engine
   ```

- ②配置yum源

- ```bash
  sudo yum install -y yum-utils
  sudo yum-config-manager \
  --add-repo \
  http://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo
  ```

- ③安装docker

- ```bash
  sudo yum install -y docker-ce docker-ce-cli containerd.io
  
  
  #以下是在安装k8s的时候使用
  yum install -y docker-ce-20.10.7 docker-ce-cli-20.10.7  containerd.io-1.4.6
  ```

- ④查看docker

- ```bash
  docker ps
  docker info
  ```

- ⑤启动

- ```bash
  systemctl enable docker --now
  ```

- ⑥配置加速

  这里额外添加了docker的生产环境核心配置cgroup

- ```bash
  sudo mkdir -p /etc/docker
  sudo tee /etc/docker/daemon.json <<-'EOF'
  {
    "registry-mirrors": ["https://82m9ar63.mirror.aliyuncs.com"],
    "exec-opts": ["native.cgroupdriver=systemd"],
    "log-driver": "json-file",
    "log-opts": {
      "max-size": "100m"
    },
    "storage-driver": "overlay2"
  }
  EOF
  sudo systemctl daemon-reload
  sudo systemctl restart docker
  ```

# **Docker命令实战**

**常用命令 **

![](D:\运维\image.png)

# 基础实战

## 1、找镜像

​	去[docker hub](http://hub.docker.com)，找到nginx镜像

```bash
docker pull nginx  #下载最新版

镜像名:版本名（标签）

docker pull nginx:1.20.1


docker pull redis  #下载最新
docker pull redis:6.2.4

## 下载来的镜像都在本地
docker images  #查看所有镜像

redis = redis:latest #不指定版本号，只写一个镜像名，代表删除最新的镜像

## 移除镜像
docker rmi 镜像名:版本号/镜像id
```

## 2、启动容器

启动nginx应用容器，并映射88端口，测试的访问

```bash
docker run [OPTIONS] IMAGE [COMMAND] [ARG...]

【docker run  设置项   镜像名  】 镜像启动运行的命令（镜像里面默认有的，一般不会写）

# -d：后台运行 -p：端口映射，主机端口映射到容器端口 --name：镜像运行时的名字 --restart=always: 开机自启
docker run --name=mynginx -d --restart=always -p 88:80 nginx 

docker ps # 查看正在运行的容器

docker ps -a # 查看所有

docker rm  容器id/名字 # 删除停止的容器

docker rm -f mynginx  #强制删除正在运行中的

docker stop 容器id/名字 #停止容器

docker start 容器id/名字 #再次启动

docker update 容器id/名字 --restart=always #应用开机自启
```

## 3、修改容器内容

修改默认的index.html 页面

### ①进容器内部修改

```bash
# 进入容器内部的系统，修改容器内容 -it：交互模式
docker exec -it 容器id  /bin/bash
```

### ②挂载数据到外部修改

```bash
docker run --name=mynginx   \
-d  --restart=always \
-p  88:80 -v /data/html:/usr/share/nginx/html:ro  \
nginx

# 修改页面只需要去 主机的 /data/html
```

## ③提交改变

将自己修改好的镜像提交

```bash
docker commit [OPTIONS] CONTAINER [REPOSITORY[:TAG]]

docker commit -a "leifengyang"  -m "首页变化" 341d81f7504f guignginx:v1.0
```

### 镜像传输

```bash
# 将镜像保存成压缩包至当前目录下
docker save -o abc.tar guignginx:v1.0

# 别的机器加载这个镜像
docker load -i abc.tar

# 离线安装
```

## ④推送远程仓库

推送镜像到docker hub；应用市场

```bash
docker tag local-image:tagname new-repo:tagname
docker push new-repo:tagname
```

```bash
# 把旧镜像的名字，改成仓库要求的新版名字
docker tag guignginx:v1.0 leifengyang/guignginx:v1.0

# 登录到docker hub
docker login       

docker logout（推送完成镜像后退出）

# 推送
docker push leifengyang/guignginx:v1.0


# 别的机器下载
docker pull leifengyang/guignginx:v1.0
```

## ⑤补充

```bash
docker logs 容器名/id   #排错

docker exec -it 容器id /bin/bash


# docker 经常修改nginx配置文件
docker run -d -p 80:80 \
-v /data/html:/usr/share/nginx/html:ro \
-v /data/conf/nginx.conf:/etc/nginx/nginx.conf \
--name mynginx-02 \
nginx


#把容器指定位置的东西复制出来 
docker cp 5eff66eec7e1:/etc/nginx/nginx.conf  /data/conf/nginx.conf
#把外面的内容复制到容器里面
docker cp  /data/conf/nginx.conf  5eff66eec7e1:/etc/nginx/nginx.conf
```

# 进阶实战

## 1、编写自己的应用

编写一个HelloWorld应用：https://start.spring.io/

示例代码：  https://gitee.com/leifengyang/java-demo.git

## 2、将应用打包成镜像

编写Dockerfile将自己的应用打包镜像

### 1、以前

Java为例

- SpringBoot打包成可执行jar
- 把jar包上传给服务

- 服务器运行java -jar

### 2、现在

所有机器都安装Docker，任何应用都是镜像，所有机器都可以运行

### 3、怎么打包-Dockerfile

```bash
FROM openjdk:8-jdk-slim #包的运行环境
LABEL maintainer=leifengyang #包的作者

COPY target/*.jar   /app.jar

ENTRYPOINT ["java","-jar","/app.jar"]
```

```bash
docker build -t java-demo:v1.0 . # . 表示在当前目录下工作
```

思考：

每个应用每次打包，都需要本地编译、再上传服务器、再进行docker构建，如果有1000个应用要打包镜像怎么办？有没有更好的方式？

## 3、启动容器

启动应用容器

```bash
docker run -d -p 8080:8080 --name myjava-app java-demo:v1.0 
```

分享镜像

```bash
# 登录docker hub
docker login

#给旧镜像起名
docker tag java-demo:v1.0  leifengyang/java-demo:v1.0

# 推送到docker hub
docker push leifengyang/java-demo:v1.0

# 别的机器
docker pull leifengyang/java-demo:v1.0

# 别的机器运行
docker run -d -p 8080:8080 --name myjava-app java-demo:v1.0 
```

## 4、部署中间件

部署一个Redis+应用，尝试应用操作Redis产生数据

```bash
docker run [OPTIONS] IMAGE [COMMAND] [ARG...]

#redis使用自定义配置文件启动

docker run -v /data/redis/redis.conf:/etc/redis/redis.conf -v /data/redis/data:/data -d --name myredis -p 6379:6379 --restart=always redis:latest redis-server /etc/redis/redis.conf
```

