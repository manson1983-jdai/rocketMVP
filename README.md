# rocketMVP
## 0 安装docker客户端
推荐版本 docker CE 18.09.3

## 1 下载docker镜像
docker pull tequiladj/node1:v0.0.8

docker pull tequiladj/node2:v0.0.8

docker pull tequiladj/node3:v0.0.8

docker pull tequiladj/node4:v0.0.8

## 2 检查是否下载完整 
使用命令docker images，观察是否存在以下四个镜像文件：
- tequiladj/node1:v0.0.8
- tequiladj/node2:v0.0.8
- tequiladj/node3:v0.0.8
- tequiladj/node4:v0.0.8
  

## 3 运行docker镜像
docker network rm rocket

docker network create rocket

docker run -dit -p 8888:80 -p 8101:8101 --network=rocket --name node1 --privileged=true tequiladj/node1:v0.0.8 

docker run -dit -p 8102:8102 --network=rocket --name node2 --privileged=true tequiladj/node2:v0.0.8 

docker run -dit -p 8103:8103 --network=rocket --name node3 --privileged=true tequiladj/node3:v0.0.8

docker run -dit -p 8104:8104 --network=rocket --name node4 --privileged=true tequiladj/node4:v0.0.8


在浏览器中打开http://0.0.0.0:8104/，
即可观察到出块情况
