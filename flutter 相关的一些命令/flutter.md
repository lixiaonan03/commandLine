# git相关操作命令的

### 把一个现有项目添加到远程仓库上

1. 在目录中创建新的 Git 仓库。 你可以在任何时候、任何目录中这么做，完全是本地化的。  这一步就相当于把本地目录搞成本地仓库
```
 git init
```
2. 拷贝一个 Git 仓库到本地，让自己能够查看该项目，或者进行修改。这一步可以简单理解成和远程仓库建立连接
```
git clone git@git.oschina.net:lxn03/gitdemo.git
```
3. 添加需要追踪的新文件和待提交的更改， 新项目中，添加所有文件很普遍，可以在当前工作目录执行命令：
`git add .`
因为 Git 会递归地将你执行命令时所在的目录中的所有文件添加上去，所以如果你将当前的工作目录作为参数， 它就会追踪那儿的所有文件了。如此，git add .就和 git add README hello.rb 有一样的效果。 此外，效果一致的还有 `git add *`不过那只是因为我们这还木有子目录，不需要递归地添加新文件。
4.  执行 git commit 就将它实际存储快照了。
```
git commit -m “提交日志”
```
5.git push -u origin  master将你的本地改动推送到远端仓库 其中origin是别名 master是分支名
```
git push [alias] [branch]
```
### 分支相关的
* 查看远程分支
```
git remote update origin --prune
```
* 拉取远程并创建本地分支
```
git checkout -b 本地分支名x origin/远程分支名x
```
* 查看本地分支
```
git branch -a
```

### tag 相关的
* 创建tag
```
git tag -a tag名称 -m "提交记录"
```
* pushtag到远程分支
```
git push --tags
```
* 查看tag
```
git ls-remote --tags
```
