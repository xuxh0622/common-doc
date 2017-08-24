##### 常用命令

> 基于`C:\Users\alice\.m2`下面`setting.xml`配置文件

```bash
$ mvn clean test  #测试
$ mvn clean package  #打包放到targe目录下
$ mvn clean package -P dev -Dmaven.test.skip=true
$ mvn clean install  #发布到本地仓库
$ mvn clean deploy  #发布到远程仓库
```

##### 版本发布

```bash
$ mvn clean -P prod -X -Darguments="-DskipTests -Dmaven.test.skip=true -Dmaven.javadoc.skip=true -Dmaven.source.skip=true" release:prepare #跳过测试
$ mvn release:prepare -P prod -X #打release包，然后升级snapshot，提交新的pom文件
$ mvn release:rollback -P prod #回退，但不会删除prepare生成的标签，需要手动删除
$ git tag -d [tag-name]  #删除远程标签
$ mvn release:perform -P prod -X #版本发布，签出release，执行mvn deploy命令打包并部署构件至仓库
```

