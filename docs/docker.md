# Docker

`docker run -itd -v /mnt/md0/wmk:/data --runtime=nvidia -e NVIDIA_VISIBLE_DEVICES=1 nvidia/cuda:9.0-base /bin/bash`

`docker exec -it 01a /bin/bash`