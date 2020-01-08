# 其他一些命令操作

### android打包和签名相关命令

* 给android空包签名的命令
```
jarsigner -verbose -keystore 密钥库位置 -signedjar 签名后的apk 签名前的apk 别名
```
注意：给Qihuunsign.apk签名密匙库文件及别名必须要验证的apk一致。否则会导致验证不能通过。
 例如：要对Qihuunsign.apk 文件签名 希望签名后的文件名为 Qihusign.apk 密匙库文件为 d:\project\360Wallpaper.keystore别名(Alias)为QIHU360 那么签名的命令为:
jarsigner -verbose -keystore d:\project\360Wallpaper.keystore -signedjar d:\qihusign.apk d:\Qihuunsign.apk   QIHU360


* 生成签名(安卓打包)文件
```
keytool -genkey -alias yushan(别名) -keypass yushan(别名密码) -keyalg RSA(算法) -keysize 1024(密钥长度) -validity 365(有效期，天单位) -keystore e:\yushan.keystore(指定生成证书的位置和证书名称) -storepass 123456(获取keystore信息的密码)
```

* 获取facebook需要的散列秘钥的
```
keytool -exportcert -alias ya(别名) -keystore 0131app1.jks(签名文件的) | openssl sha1 -binary | openssl base64
```
