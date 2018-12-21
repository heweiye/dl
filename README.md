#### 配置rclone开机自动挂载
``` bash
wget https://github.com/heweiye/VPSVPS/raw/master/rcloned && nano rcloned
```
修改一下内容：
NAME=""  #rclone name名，及配置时输入的Name
REMOTE=''  #远程文件夹，Google Drive网盘里的挂载的一个文件夹
LOCAL=''  #挂载地址，VPS本地挂载目录

使用命令：
#Debian系统
``` bash
apt-get install sudo -y
```
``` bash
mv rcloned /etc/init.d/rcloned
chmod +x /etc/init.d/rcloned
update-rc.d -f rcloned defaults
bash /etc/init.d/rcloned start
```
检测信息显示rclone启动成功即可。
