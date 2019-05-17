# adb 相关的命令

### 通过adb连接手机的
* 连接手机的
``` Java
adb connect 192.168.12.100:5555
```
* 断开连接
``` Java
adb disconnect 192.168.12.100
```
- 监听某个端口
``` Java
adb tcpip 5555
```
### 通过adb查看手机目录和日志
* 在连接上手机之后进入手机目录
``` Java
adb shell
```
 进入手机目录之后就可以使用 ls cd 等操作

* 在连接上手机之后进入手机目录
``` Java
 adb logcat *:E -v time >/Users/lixiaonan/Desktop/log.txt
```
