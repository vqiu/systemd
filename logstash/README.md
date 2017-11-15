### 常见错误
1. 使用systemd无法启动
- 版本: logstash-5.6.4

解决： 打开 ${LS_HOME}/config/startup.options 文件，
查看 LS_USER 与 LS_GROUP所对应的用户名[Default: logstash] ,建立对应的用户，再使用systemd 启动即可。
```
# groupadd logstash
# useradd logstash -g logstash -M -s /sbin/nologin
```
