# ***docker***
## ***docker拉取镜像***
- docker search 镜像名
- docker pull 镜像名
- docker开启、关闭、重启：
  - systemctl start docker
  - systemctl stop docker
  - systemctl restart docker
## ***docker修改镜像***
- 查看被修改的容器 ：docker ps -l，返回container id
- 提交指定容器保存为新的镜像： docker commit （container id）（ new image name）
- 查看本地所有镜像：docker images
## ***构造镜像***
1.编写dockerfile文件

2.将要运行的JavaWeb项目和dockerfile文件放入同一个文件夹下执行构造命令
```
//dockerName 构建的镜像名称 
// . 当前目录
sudo docker build  -t (dockerName) (.)
```
## ***镜像的查看与删除***
```
查看镜像：
sudo docker images
删除镜像：
sudo docker rmi 镜像名称/tag
```
## ***由镜像生成容器***
```
sudo docker run  --name (containerName) -p (masterPort:port) -d (dockerName)
```
## ***查看当前运行中的容器***
```
sudo docker ps
无参    --当前正在运行的容器信息
-a      --所有被创建出的容器信息
```
## ***删除容器***
- 删除容器前首先要保证容器已经停止运行,使用命令：
```
sudo docker stop 容器名/tag
```
- 使用命令来删除容器：
```
sudo docker rm 容器名/tag
```