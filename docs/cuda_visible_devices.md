# 指定某块显卡运行

## 在终端执行程序时指定GPU 

```
CUDA_VISIBLE_DEVICES=1           Only device 1 will be seen
CUDA_VISIBLE_DEVICES=0,1         Devices 0 and 1 will be visible
CUDA_VISIBLE_DEVICES="0,`1"       Same as above, quotation marks are optional
CUDA_VISIBLE_DEVICES=0,2,3       Devices 0, 2, 3 will be visible; device 1 is masked
CUDA_VISIBLE_DEVICES=""          No GPU will be visible
```

## 在Python代码中指定GPU

```
import os
os.environ["CUDA_VISIBLE_DEVICES"] = "0"
```