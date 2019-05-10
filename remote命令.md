> <alias>别名，<giturl>仓库地址，<new-giturl>新的仓库地址，<old-alias>旧的别名，<new-alias>新的别名
# 列出所有的远程仓库
```sh
git remote
```
# 列出所有远程仓库的详细信息，别名后面为远程仓库地址
```sh
git remote -v
git remote --verbose
```
# 添加远程仓库
```sh
git remote add <alias> <giturl>

# 例:
git remote add origin https://github.com/bin7096/git.git
```
# 修改远程仓库别名
```sh
git remote rename <old-alias> <new-alias>
```
# 删除别名对应的远程仓库
```sh
git remote rm
git remote remove <alias>
```
# 修改远程仓库的Url地址
```sh
git remote set-url <alias> <new-giturl>
```