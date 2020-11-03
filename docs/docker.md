# Docker

## 运行 Docker

`docker run -itd -v /mnt/md0/slw:/data --runtime=nvidia -e NVIDIA_VISIBLE_DEVICES=1 nvidia/cuda:9.0-base /bin/bash`

命令解释：

-itd 为后台运行

-v /mnt/md0/slw:/data 是将服务器上`/mnt/md0/slw`文件夹映射到docker中的`/data`，这样在docker中只需要访问`/data`就可以访问到对应的文件了

-e NVIDIA_VISIBLE_DEVICES=1 指定运行显卡为ID=1的显卡

nvidia/cuda:9.0-base 为docker镜像的名称，这里为基础的cuda9.0的镜像包，可替换为其他

### 其他 docker 镜像

```
tensorflow/tensorflow:1.12.3-gpu-py3
pytorch/pytorch:1.6.0-cuda10.1-cudnn7-devel
kundajelab/cuda-anaconda-base
```

## 进入 Docker

执行以下命令可以进入到docker容器中进行操作，其中的`01a`请自行替换成上一步操作中返回的容器ID

`docker exec -it 01a /bin/bash`

## 其他 Docker 命令

### 查看当前所有容器的状态

`docker container ls -a`

### 停止运行中的容器

`docker container stop 01a`

### 删除已经停止运行的容器

`docker container rm 01a`

## 替换 Ubuntu 镜像源

分别运行以下命令：

```
apt update
apt install wget sudo -y
wget https://cdn.dl.slinvent.com/Ubuntu_source.sh
bash Ubuntu_source.sh
```

选择2即可