# Ubuntu 常用命令

## 添加用户

`sudo adduser username`

- 请勿使用弱密码

## 添加用户到用户组

`sudo usermod -aG groupA user`

- 如需使用`/mnt/md0`目录，需添加用户到 lab121 用户组
- 如需免root使用docker，需添加用户到 docker 用户组

## 修改文件夹权限
`sudo chown -R slw:slw file_path/`
