### 注意

zookeeper 如果使用非root用户时，可能会出现如下错误：
```
<省略若干行>
Starting zookeeper ... /opt/wdf/app/zookeeper/bin/zkServer.sh: line 140: ./zookeeper.out: Permission denied
<省略若干行>
```
### 解决方式
  将 zookeeper 的 dataDir 权限配置 `sgid` 即可
```
$sudo chmod 2755 {{ dataDir }} {{ dataLogDir }}
```
