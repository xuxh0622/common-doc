##### 简单说明

- `JAVA_HOME`:jdk的安装路径
- `classpath`：java加载类路径，只有类在classpath中java命令才能识别，在路径前加了个"."表示当前路径。
- `path`：系统在任何路径下都可以识别java,javac命令。

##### 高级配置

- `新建JAVA_HOME`:C:\Program Files\Java\jdk1.6.0_14
- `新建classpath`：.;%JAVA_HOME%\lib;%JAVA_HOME%\lib\tools.jar
- `新建path`：%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin
- `控制台`：javac查看是否正常

