# lab121 服务器使用指南
## Documentaion for lab121

> Written by Ryo Shen

1. 每天零点校园网会自动刷新，请使用`w3m sohu.com`进行登录。

2. 推荐使用 docker 配置环境，这样可以有效防止把服务器上面的环境搞乱。

3. $HOME 文件夹（/home/USER）总容量为 512G，推荐将训练中间生成生成的模型文件等**大文件**存放在 `/mnt/md0/USER` 下。

服务器配置：

```
CPU：Intel® Xeon® Bronze 3204 1.90GHz 6 Cores 6 Threads
内存：32G DDR4 2666MHz
硬盘：512GB SSD + 3 * 10TB HDD
GPU：2 * NVIDIA GeForce RTX 2080 Ti 11GB
操作系统：Ubuntu 18.04
服务器型号：Dell Precision 7920 Tower
```