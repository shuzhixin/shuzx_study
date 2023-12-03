### MacOS上安装MySQL



1、brew install mysql

2、brew info mysql

启动mysql

sudo brew services start mysql

shuzhideMBP:~ shuzx$ sudo brew services start mysql

Password:

Warning: Taking root:admin ownership of some mysql paths:

  /usr/local/Cellar/mysql/8.0.27/bin

  /usr/local/Cellar/mysql/8.0.27/bin/mysqld_safe

  /usr/local/opt/mysql

  /usr/local/var/homebrew/linked/mysql

This will require manual removal of these paths using `sudo rm` on

brew upgrade/reinstall/uninstall.

Warning: mysql must be run as non-root to start at user login!

==> Successfully started `mysql` (label: homebrew.mxcl.mysql)

------

- 服务启动方法：

We've installed your MySQL database without a root password. To secure it run:

​    mysql_secure_installation

MySQL is configured to only allow connections from localhost by default

To connect run:

​    mysql -uroot

To restart mysql after an upgrade:

  brew services restart mysql

Or, if you don't want/need a background service you can just run:

  /usr/local/opt/mysql/bin/mysqld_safe --datadir=/usr/local/var/mysql

------

- 客户端启动方法：