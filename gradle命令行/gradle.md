# gradle相关的一些命令
备注：
1、gradlew代表 gradlewrapper，意思是gradle的一层包装，大家可以理解为在这个项目本地就封装了gradle，即gradle wrapper，在 /gradle/wrapper/gralde-wrapper.properties文件中声明了它指向的目录和版本,
和gradle 命令是一样的

2、as中的保证gradle运行环境和项目中JRE环境的一样
在gradle-wrapper.properties文件中设置
``` xml
 org.gradle.java.home=/Applications/Android Studio.app/Contents/jre/jdk/Contents/Home
```



### gradle打包apk（也可使用gradle面板上的按钮）
1、添加gradle权限（有的情况需要权限）
``` xml
chmod +x gradlew
```
2、打包命令（一个debug一个release）
``` xml
./gradlew assembledebug

./gradlew assemblerelease
```
3、查看失败原因
``` xml
./gradlew  compileRelease –stacktrace
```

### gradle其他命令
1、查看jar应用关系的
``` xml
./gradlew -q dependencies app:dependencies --configuration debugAndroidTestCompileClasspath
```
