## linux下面操作

```shell
[zookeeper * bin] zkServer.sh start  #启动服务  
[zookeeper * bin]zkServer.sh stop  #关闭服务 
[zookeeper * bin] cd ../logs  #跳转到logs文件地址  
[zookeeper * logs] tail -f zookeeper-leader.log  #查看日志
[zookeeper * bin] zkCli.cmd -server 127.0.0.1  #访问客户端
[zk: 127.0.0.1(CONNECTED) 4] /dubbo  #查看提供的服务
[zk: 127.0.0.1(CONNECTED) 4] /dubbo/com.alice.service
.TestService/providers  #查看注册服务详细信息
```

