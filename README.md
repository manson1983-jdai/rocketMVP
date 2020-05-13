# rocketMVP
## 下载docker镜像
docker pull tequiladj/node1:v0.0.8
docker pull tequiladj/node2:v0.0.8
docker pull tequiladj/node3:v0.0.8
docker pull tequiladj/node4:v0.0.8

## 检查是否下载完整 
docker images

## 运行docker镜像
docker run -dit -p 8888:80 -p 8101:8101 --name node1 --privileged=true tequiladj/node1:v0.0.8 
docker run -dit -p 8102:8102 --name node2 --privileged=true tequiladj/node2:v0.0.8 
docker run -dit -p 8103:8103 --name node3 --privileged=true tequiladj/node3:v0.0.8
docker run -dit -p 8104:8104 --name node4 --privileged=true tequiladj/node4:v0.0.8

在浏览器中打开http://0.0.0.0:8104/，即可观察到出块情况
