# apache
apache安装

安装版本
搜狐镜像：http://mirrors.sohu.com/下
http://mirrors.sohu.com/apache/httpd-2.4.28.tar.gz

apr下载
http://apache.osuosl.org/apr/（旧）
http://apache.osuosl.org/（旧）

http://mirror.bit.edu.cn/apache/
http://mirror.bit.edu.cn/apache/apr/apr-1.6.3.tar.gz
http://mirror.bit.edu.cn/apache/apr/apr-util-1.6.1.tar.gz

wget http://oss.aliyuncs.com/aliyunecs/onekey/apache/apr-1.5.0.tar.gz
wget http://oss.aliyuncs.com/aliyunecs/onekey/apache/apr-util-1.5.3.tar.gz

安装pcre
wget http://zy-res.oss-cn-hangzhou.aliyuncs.com/pcre/pcre-8.38.tar.gz

Mysql下载地址：
http://mirrors.sohu.com/mysql/MySQL-5.6/mysql-5.6.36.tar.gz

Php下载地址：
http://mirrors.sohu.com/php/php-5.5.38.tar.gz




安装apr

cd /usr/local/src/
wget http://oss.aliyuncs.com/aliyunecs/onekey/apache/apr-1.5.0.tar.gz
tar zxvf apr-1.5.0.tar.gz
cd apr-1.5.0
./configure --prefix=/usr/local/apr
make && make install


安装apr-util

cd /usr/local/src/
wget http://oss.aliyuncs.com/aliyunecs/onekey/apache/apr-util-1.5.3.tar.gz
tar zxvf apr-util-1.5.3.tar.gz 
cd apr-util-1.5.3
./configure --prefix=/usr/local/apr-util --with-apr=/usr/local/apr
make && make install



安装pcre

cd /usr/local/src/
wget http://zy-res.oss-cn-hangzhou.aliyuncs.com/pcre/pcre-8.38.tar.gz 
tar zxvf pcre-8.38.tar.gz
cd pcre-8.38
./configure --prefix=/usr/local/pcre
make && make install



编译安装Apache

cd /usr/local/src/
wget http://zy-res.oss-cn-hangzhou.aliyuncs.com/apache/httpd-2.4.23.tar.gz 
tar zxvf httpd-2.4.23.tar.gz
cd httpd-2.4.23
./configure \
--prefix=/usr/local/apache --sysconfdir=/etc/httpd \
--enable-so --enable-cgi --enable-rewrite \
--with-zlib --with-pcre=/usr/local/pcre \
--with-apr=/usr/local/apr \
--with-apr-util=/usr/local/apr-util \
--enable-mods-shared=most --enable-mpms-shared=all \
--with-mpm=event
make && make install




