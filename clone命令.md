# 默认克隆master分支到当前目录下
> <giturl>远程仓库地址，<dir>本地目录，<branch>远程分支名称
```sh
git clone <giturl>
```
# 支持的多种协议
```sh
git clone http[s]://xxx.git
git clone ssh://xxx.git
git clone git://xxx.git
git clone /xxx.git
git clone file://xxx.git
git clone ftp[s]://xxx.git
git clone rsync://xxx.git

# SSH协议还有一种写法，以github为例
git clone git@github.com:xxxx/xxx.git
```
# 指定本地仓库目录
```sh
git clone <giturl> <dir>
```
# 指定获取某个分支到指定目录
```sh
git clone -b <branch> <giturl> <dir>
```
# 三种克隆的区别
* 全克隆
* 单一克隆
* 深度克隆
## 全克隆
执行`git clone <giturl>`将远程仓库中的所有分支都拉取到本地。优点：所有分支一次性拉取到本地，分支切换十分方便。缺点：占用空间大，且大型仓库克隆时耗费时间长，失败率高。
## 单一克隆
执行`git clone -b <branch> <giturl>`与全克隆结果一致，都是将远程仓库的所有分支拉取到本地。可以加上参数` --single-branch`克隆单一分支。优点：占用空间小，克隆速度快。缺点：只能看到单一分支，无法切换。
## 深度克隆
执行`git clone --depth 10 <giturl>`可以获取最近10次的所有分支代码，默认是master分支，想要指定分支，可以结合` -b <branch> --single--branch`使用。