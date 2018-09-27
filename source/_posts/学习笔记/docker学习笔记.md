---
title: Docker学习笔记
date: 2017-10-27 22:28:41
tags:
---

docker images 列出所有镜像
docker run 镜像名：版本 通过某个镜像启动容器
-t 让Docker分配一个伪终端并绑定到容器的标准输入上
-i 让容器的标准输入保持打开
-d 让容器在后台已守护态运行

docker ps 查看容器信息、
-a 查看终止状态的容器
docker logs 获取容器输出信息
docker stop 停止一个容器
docker start 启动一个终止状态的容器
docker restart 重启一个运行态的容器
docker export 导出某个容器 导出容器快照到本地文件
docker import 导入某个容器 从容器快照文件导入为镜像
docker rm 删除一个终止状态的容器
-f 删除一个运行状态的容器，docker会发送SIGKILL信号给容器


dockerfile
# 注释
FROM ubuntu:14.04
MAINTAINER Docker Chen <chenyuzhao.karl@gamil.com>
Run apt-get install ruby

docker build -t="my/ubuntu:1.0" 生成镜像 -t 添加标记

ADD 复制本地文件到镜像
EXPOSE 开放端口
CMD 描述容器启动后运行的程序

docker push 上传自己创建的镜像到仓库中


