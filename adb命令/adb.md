# adb 相关的命令
[官网地址](https://developer.android.com/studio/command-line/adb?gclid=Cj0KCQjwt_nmBRD0ARIsAJYs6o2frvMVn3AWDzhbfbwHQOuM5P2C51LjSYm_WVuWSBhht5fsJNlXCisaAsNPEALw_wcB)
### 通过adb连接手机的
* 连接手机的
``` Java
adb connect 192.168.12.100:5555
```
* 断开连接
``` Java
adb disconnect 192.168.12.100
```
* 监听某个端口
``` Java
adb tcpip 5555
```
* 列出所有已连接的设备
``` Java
adb devices
```
### 通过adb命令查看文件或者安装应用
* adb install , 安装apk到手机上
``` Java
adb install 路劲
```
* adb uninstall -k 包名 卸载应用加-k是保留 缓存目录
``` Java
adb uninstall com.z87v7ake.i2bsu67k
```



* adb pull , 将 Android 设备上的文件或者文件夹复制到本地
eg: 查看anr日志
``` Java
adb pull /data/anr/traces.txt
```
默认是当期目录下 后面可以跟要复制到的目录
adb pull 要复制的文件  要复制到啥地方


* 在连接上手机之后进入手机目录
``` Java
adb shell
```
 进入手机目录之后就可以使用 ls cd 等操作

* 把logcat的日志打印到本地
``` Java
 adb logcat *:E -v time >/Users/lixiaonan/Desktop/log.txt
```
其中* 可以换成tag 标签具体的值  E是日志级别  V是全部 D debug  I Info  E  error 日志
后面的是路径   可以自己修改
