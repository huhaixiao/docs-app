# nginx

## 安装

### CentOS

```shell
# 安装 nginx 依赖包
yum -y install gcc gcc-c++ make libtool zlib zlib-devel openssl openssl-devel pcre pcre-devel

# 从 nginx 官网下载安装包
wget http://nginx.org/download/nginx-1.18.0.tar.gz

# 解压被下载的文件
tar -zxvf nginx-1.18.0.tar.gz

cd nginx-1.18.0

# 配置 nginx
./configure --prefix=/usr/local/nginx

# 编译 & 安装
make && make install

# /usr/local/src/nginx-1.6.2
cd /usr/local/nginx
sbin/nginx
```
