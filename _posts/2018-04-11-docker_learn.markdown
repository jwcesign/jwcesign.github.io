---
layout:     post
title:      "Docker入门"
subtitle:   " \"Docker\""
date:       2018-03-30 12:00:00
author:     "CESIGN"
header-img: "img/post-bg-2015.jpg"
catalog: true
tags:
    - Docker
---
> "Docker学习"

##  Docker介绍
Docker是一个开源的引擎，可以轻松的为任何应用创建一个轻量级的、可移植的、自给自足的容器。开发者在笔记本上编译测试通过的容器可以批量地在生产环境中部署，包括VMs（虚拟机）、bare metal、OpenStack 集群和其他的基础应用平台。
## Docker原理
Docker原理介绍：[link](http://dockone.io/article/783)

## Docker安装
~~~
apt-get install docker
apt-get install docker.io
~~~
## 选择仓库（记得重启）
~~~
vim /etc/docker/daemon.json
{ "registry-mirrors":["http://hub-mirror.c.163.com"]}
~~~
## 基础命令
查看版本
~~~
docker --version
~~~
搜索可用镜像
~~~
docker search image_words
~~~
拉取镜像
~~~
docker pull image_name
~~~
删除镜像
~~~
//可能需要先停止并删除正在运行的容器
docker rmi image_id
//错误:image is referenced in multiple repositories
docker rmi respository_name
~~~
在容器中运行命令
~~~
docker run image_name cmd
~~~
查看所有容器
~~~
docker ps -a
~~~
查看运行中的容器
~~~
docker ps
~~~
删除容器
~~~
docker rm con_id
//删除所有
docker rm $(docker ps -aq)
~~~
在容器中安装程序
~~~
docker run image_name apt-get install software
~~~
保存对容器的修改（镜像）
~~~
//先查看容器ID
docker ps -l
//保存
docker commit id_start user/des_or_keyword
~~~
把保存的镜像上传到docker hub
~~~
docker tag image_name user_name/res_name
docker push user_name/res_name
~~~
检查运行中的镜像
~~~
//查看运行中的容器
docker ps
//查看容器的详细信息
docker inspect con_id
~~~
—— cesign 后记于 2018.03
