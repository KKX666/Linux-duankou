# Linux 开放指定端口
**开启指定端口**
```
firewall-cmd --zone=public --add-port=端口号/tcp --permanent
```
**开启指定端口后必须重启防火墙 重启命令**
```
systemctl restart firewalld.service
```
查看防火墙状态
```
systemctl status firewalld.service
```
开启防火墙
```
systemctl start firewalld.service
```
禁止开机启动
```
systemctl disable firewalld.service
```
开启开机启动
```
systemctl enable firewalld.service
```
查看已开放端口
```
firewall-cmd --list-ports
```
如果无法定位软件包 请更新本地源文件
```
sudo apt-get update
```
