# 网络相关的一些查询命令


### 查询dns

* 探测DNS解析过程的，包括分析CNAME记录(https://zh.wikipedia.org/wiki/CNAME%E8%AE%B0%E5%BD%95)和A记录 的
2个命令都可以  dig 命令或 nslookup 命令 参考(https://www.cnblogs.com/liujiacai/p/8366236.html)
``` java
nslookup  pic.wanwustore.cn
```
``` java
dig  pic.wanwustore.cn
```


### 网络相关的
* 查看连接时长的 第一个tcp的时长 第二个是ssl的时长的
``` java
curl -w "TCP handshake: %{time_connect}, SSL handshake: %{time_appconnect}\n" -so /dev/null https://www.alipay.com
```
