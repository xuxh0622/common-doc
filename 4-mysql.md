##### 数据库备份

> 命令窗口操作

```bash
$ mysql -h 10.10.65.137 -p 7879 -u root -p111111  #登录-u 用户名 -p 密码 -h 地址
$ mysqldump -hhostname -uusername -ppassword -Pport databasename > backupfile.sql  #备份databasename数据库
$ mysql -hhostname -uusername -ppassword databasename < backupfile.sql  #恢复数据库备份
```

> mysql客户端操作

```mysql
mysql> CREATE DATABASE o2o CHARACTER SET utf8 COLLATE utf8_general_ci  #创建数据库
mysql> source backupfile.sql  #恢复数据库备份
# SELECT @@FOREIGN_KEY_CHECKS查看外键约束
mysql> SET FOREIGN_KEY_CHECKS=0  #禁用外键约束
mysql> SET FOREIGN_KEY_CHECKS=1;  #启动外键约束
```

#### 死锁

```mysql
mysql> show processlist  #查看死锁
```







