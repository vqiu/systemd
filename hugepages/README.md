### 动态方式（systemd）

&emsp;&emsp;使用systemd 启动方式可以大致理解为动态，进入系统中可以自由更改

- 在系统启动加入以下参数,
```
default_hugepagesz=1G hugepagesz=1G
```


### 动态方式（系统启动方式）
&emsp;&emsp;该方式随系统启动就分配巨页空间，一旦采用此方式，巨页空间不能更改

-  在系统启动时就指定页数
```
default_hugepagesz=1G hugepagesz=1G hugepages=${page_number}
```
