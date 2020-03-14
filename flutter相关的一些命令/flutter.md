# flutter相关命令

### 基础操作命令

1. 查看基础安装配置信息的
```
  flutter doctor
```
2. 命令获取新依赖项后会写入一个 lockfile 文件以确保下次执行该命令时会使用相同的依赖项版本。如果 lockfile 已经存在，pub get 命令会尽可能地使用锁定的依赖项版本。如果某个依赖项没有被锁定，则 Pub 会获取所有 限定的版本 中最新的那个依赖项版本。这是 pub get 命令与 pub upgrade 命令最大的不同点，后者总是会去尝试使用依赖项的最新版本。
（注意使用此命令，可以生成 .android .ios 等文件，在混合接入使用的时候可以使用）
```
flutter pub get
```
3.创建新的项目的（注意在项目同级的目录下创建flutter moule (注意是项目同级的目录下 有可能flutter项目和android项目不是一个仓库)）
```
flutter create -t module 项目名
```
