# 配置文件的存储位置
> 这些变量可以被存储在三个不同的位置：
* ./etc/gitconfig文件：包含了适用于系统所有用户和所有库的值。如果你传递参数选项` --system`给git config，它将明确的读写这个文件。
* ~/.gitconfig文件：具体到你的用户。你可以通过传递` --global`选项使git读或写这个特定的文件。
* 位于当前目录下git目录中的config文件：无论你当前在用的库是什么，特定指向该单一的库。每个级别重写前一个级别的值。因此，在./git/config中的值覆盖了在/etc/gitconfig中的同一个值。
# 配置用户名和密码
> 安装git后首先要做的事情是设置你的用户名和邮箱地址，避免每次提交反复输入用户名等信息。
```sh
git config --global user.name "username"

git config --global user.email "email"
```
# 配置客户端长期存储用户名和密码
> 每次操作代码仓库都要输入用户名和密码也是一件麻烦事
```sh
git config --global credential.helper store
```