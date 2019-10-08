# JConsole基本使用
JConsole是一款JDK自带的Java性能监控工具，位于JDK安装目录下/bin/jconsole.exe。可以用于连接本地或者远程Java运行程序，实现各项资源消耗和性能监控。
以下是远程连接时远程应用程序需要添加的配置:
  
  1. -Djava.rmi.server.hostname=远程IP //设置远程访问IP
  2. -Dcom.sun.management.jmxremote.port=60001 //远程连接端口
  3. -Dcom.sun.management.jmxremote.ssl=false //不启用ssl连接
  
重新启动远程应用程序以后，打开Jconsole连接即可，如下图
  
  ![connect](/图片/连接.png)
  
连接成功的界面是这样的:
  
  ![run](/图片/运行.png)
  
如果需要登录认证需要加上如下参数:
  1. -Dcom.sun.management.jmxremote.authenticate=true
  2. -Dcom.sun.management.jmxremote.pwd.file= {jmxremote.password}Path 

同时需要在/usr/lib/jvm/java-8-oracle/jre/lib/management下的jmxremote.access添加对应的用户名和权限(root为rw,access为600)。在jmxremote.password文件中添加用户名和密码。
