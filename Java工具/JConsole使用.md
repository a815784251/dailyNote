# JConsole基本使用
JConsole是一款JDK自带的Java性能监控工具，位于JDK安装目录下/bin/jconsole.exe。可以用于连接本地或者远程Java运行程序，实现各项资源消耗和性能监控。
以下是远程连接时远程应用程序需要添加的配置:
  
  1.  -Djava.rmi.server.hostname=远程IP //设置远程访问IP
  2. -Dcom.sun.management.jmxremote.port=60001 //远程连接端口
  3. -Dcom.sun.management.jmxremote.ssl=false //不启用ssl连接

重新启动远程应用程序以后，打开Jconsole连接即可，如下图
