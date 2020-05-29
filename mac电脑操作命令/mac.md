# mac 电脑上使用的的一些相关命令


### 关于文件系统的
* 重启Finder的
``` Java
killall Finder
```

### 公私钥相关的
* 查看是否有公私钥的
``` Java
ls ~/.ssh
```
* 创建公私钥的（rsa是算法的  john@example.com 相当于一个注释的）
``` Java
ssh-keygen -t rsa -C "john@example.com"
```
* 查看公私钥的 （其中 id_rsa.pub 就是公钥文件名）
``` Java
cat ~/.ssh/id_rsa.pub
```

### Homebrew 软件安装相关命令的
* 显示已经安装的所有软件包 （默认安装在 /usr/local/etc/ 这个目录底下）
``` Java
brew list
```
* 安装或卸载软件
``` Java
brew install 安装软件名
brew uninstall 卸载软件名
```
* 查看软件包信息
``` Java
brew info 软件名
```

### 环境变量相关的操作的
* 打开配置环境变量文件(使用  bash shell)
``` Java
open ~/.bash_profiles
```
* 打开配置环境变量文件(使用  zsh shell)
``` Java
open ~/.zshrc
```

### 查看进程和端口使用情况的
* 查看端口使用情况,其中adb端口的5037
```java
 lsof -I : 端口
```
* 杀死某个进程的
```java
kill 进程号
```

### redis相关的
* 打开本地local bin目录
``` Java
cd /usr/local/bin
```
* 启动redis服务
``` Java
./redis-server
```
* 关闭redis
``` Java
./redis-cli shutdown
```

### mongo相关的
参考 https://www.jianshu.com/p/b15d293930bc
1、找到运行路径或者 配置环境变量
* 启动mongo
``` Java
mongod --dbpath /Users/lixiaonan/Documents/monggo/db(数据库地址 默认 /usr/data/db)
```
