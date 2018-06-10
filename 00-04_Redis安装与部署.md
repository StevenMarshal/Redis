# 4 Redis安装与部署

Redis的官方下载地址：http://redis.io/download  
当前最新的稳定版本是Stable 4.0.9。

步骤一：  
下载安装包：  

    wget http://download.redis.io/releases/redis-4.0.9.tar.gz

步骤二：  
编译源程序：  

    tar zxvf redis-4.0.9.tar.gz
    cd redis-4.0.9
    make
    cd src && make install

步骤三：  
移动文件，便于管理：  

    mkdir –p /usr/local/redis/bin
    mkdir –p /usr/local/redis/etc
    mv /lamp/redis-4.0.9/redis.conf /usr/local/redis/etc
    cd /lamp/redis-4.0.9/src
    mv mkreleasehdr.sh redis-benchmark redis-check-aof redis-check-dump redis-cli redis-server /usr/local/redis/bin

步骤四：  
启动Redis服务：  

    /usr/local/redis/bin/redis-server
    /usr/local/redis/etc/redis.conf

服务器默认端口为6379

步骤五：  
客户端连接：  

    /usr/local/redis/bin/redis-cli

步骤六：  
停止Redis实例：  
可以使用 

    /usr/local/redis/bin/redis-cli shutdown

也可使用 

    pkill redis-server

注：VMware Workstation 8
