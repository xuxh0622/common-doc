##### 数据库备份

> 命令窗口操作

```bash
$ sudo service mysqld restart  #重启数据库 
$ mysql -h 127.0.0.1 -P 3307 -u root -p111111  #登录 -P 端口-u 用户名 -p密码 -h 地址
#mysqldump -h 127.0.0.1 -u root -proot test > d:/test.sql
$ mysqldump -hhostname -uusername -ppassword -Pport databasename > backupfile.sql  #备份databasename数据库
$ mysql -hhostname -uusername -ppassword databasename < backupfile.sql  #恢复数据库备份
```

> mysql客户端操作

```mysql
#创建数据库及对应访问用户 
mysql>CREATE DATABASE test CHARACTER SET utf8 COLLATE utf8_general_ci;
mysql>CREATE USER 'test_user' IDENTIFIED BY 'test_user';
mysql>GRANT ALL ON test.* TO 'test_user'@'%' IDENTIFIED BY 'test_user';
mysql>GRANT ALL ON test.* TO 'test_user'@'localhost' IDENTIFIED BY 'test_user';
mysql>FLUSH PRIVILEGES;

mysql> source backupfile.sql  #恢复数据库备份
# SELECT @@FOREIGN_KEY_CHECKS查看外键约束
mysql> SET FOREIGN_KEY_CHECKS=0  #禁用外键约束
mysql> SET FOREIGN_KEY_CHECKS=1;  #启动外键约束
```

#### 死锁

```mysql
mysql> show processlist  #查看死锁
```







