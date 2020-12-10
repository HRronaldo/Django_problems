---
description: >-
  ERROR 2002 (HY000): Can't connect to local MySQL server through socket
  '/var/run/mysqld/mysqld.sock'
---

# Ubuntu 18.04 解决MySQL ERROR 2002 \(HY000\)

ps：你的mysql的配置在/etc/mysql/mysql.conf.d目录下的mysqld.cnf文件，打开如下：  
    可以看到：socket = /var/run/mysqld/mysqld.sock  等信息

我的虚拟机是/var/run下面没有mysqld目录，执行下面命令，然后目录和sock文件就都有了  
`sudo mkdir -p /var/run/mysqld  
sudo chown mysql /var/run/mysqld  
sudo service mysql restart`  


现在就都有了：  
然后执行：mysql -u root -p   然后提示你输入密码，即可

