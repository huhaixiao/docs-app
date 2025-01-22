# CentOS

```shell
pwd
sudo yum update
sudo yum install git

systemctl status nginx

# systemctl
service --status-all
service nginx start
service nginx status
service nginx -s quit
systemctl start nginx
systemctl stop nginx.service
nginx -v

# 是否文件夹/所有者(owner)/所属组(group)/其他用户(others)
drwxrwxrwd
chmod 777 nginx.conf
# 查看用户权限
ls -l
id user
groups user

# 查看 CentOS 版本
cat /etc/redhat-release
```

## yum

yum（Yellowdog Updater, Modified）

```shell
sudo yum install git
```

## 防火墙

```shell
sudo yum install iptables-services
service iptables status
```

## 切换用户

```shell
# # stands for root user
su root
# $ stands for user
su username
```