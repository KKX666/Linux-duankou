# Linux 开放指定端口
**开启指定端口**
```
firewall-cmd --zone=public --add-port=端口号/tcp --permanent
```
**开启指定端口后必须重启防火墙 重启命令**
```
systemctl restart firewalld.service
```
启动firewalld
```
systemctl start firewalld
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
如果输入指定失败 请安装firewall
```
apt install firewall
```
如果输入指定失败 请安装firewall
```
apt install firewalld
```
运行 apt-get 时报如下错
```
E: Could not get lock /var/lib/dpkg/lock-frontend - open (11: Resource temporarily unavailable)
E: Unable to acquire the dpkg frontend lock (/var/lib/dpkg/lock-frontend), is another process using it?
```
解决方案
```
sudo rm /var/lib/dpkg/lock-frontend
sudo rm /var/lib/dpkg/lock
sudo rm /var/cache/apt/archives/lock
```
