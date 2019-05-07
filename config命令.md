# 配置文件的存储位置
> 这些变量可以被存储在三个不同的位置：
* 系统级配置文件（Win在git安装目录，Mac在/usr/local/git中的etc/gitconfig文件）：包含了适用于系统所有用户和所有库的值。如果你传递参数选项` --system`给git config，它将明确的读写这个文件。
* 全局配置文件（Win是C:\Users\<用户名>\\.gitconfig，Mac是~/.gitconfig文件）：具体到你的用户。你可以通过传递` --global`选项使git读或写这个特定的文件。
* 仓库级配置（位于当前目录下git目录中的gitconfig文件）：无论你当前在用的库是什么，特定指向该单一的库。每个级别重写前一个级别的值。因此，在./git/gitconfig中的值覆盖了在/etc/gitconfig中的同一个值。

<font color="red">注：--local：仓库级，--global：全局级，--system：系统级</font>
# 查看配置信息
```sh
# 查看当前生效配置
git config --list
git config -l
# 指定查看全局配置
git config --global -l
```
# 编辑配置信息
```sh
git config --edit
git config -e
# 指定编辑全局配置
git config --global -e
```
# 添加配置项
```sh
# 全局示例，<name>为配置项，<value>为配置内容
git config --global --add <name> <value>
```
# 获取配置项
```sh
# 全局示例，<name>为配置项
git config --global --get <name>
```
# 删除配置项
```sh
# 全局示例，<name>为配置项
git config --global --unset <name>
```
# 更改git缓存区大小
> 如果提交的内容较大，缓存较小时，提交会失败。缓存单位：bit。
```sh
# 全局示例，大小500MB
git config --global http.postBuffer 524288000
```
# 配置用户名和密码
> 安装git后首先要做的事情是设置你的用户名和邮箱地址，避免每次提交反复输入用户名等信息。
```sh
# 全局示例，记住用户名
git config --global user.name "username"
# 全局示例，记住邮箱
git config --global user.email "email"
```
# 配置缓存密码
> 默认缓存时间15分钟
```sh
# 全局示例
git config --global credential.helper cache
```
# 配置密码缓存时间
> 配置单位：秒。
```sh
# 全局示例，配置密码缓存一天
git config --global credential.helper 'cache --timeout=86400'
```
# 配置客户端长期存储用户名和密码
> 每次操作代码仓库都要输入用户名和密码也是一件麻烦事
```sh
# 全局示例
git config --global credential.helper store
```
# 配置git的默认编辑器
> 自定义编辑器时，需要将编辑器的可执行文件路径写到PATH环境变量中。
```sh
# 全局示例，配置vscode为git的默认编辑器，vscode的默认可执行文件名为Code。
git config --global core.editor Code
```
# 配置代码比较工具
> git可接受kdiff3、tkdiff、meld、xxdiff、emerge、vimdiff、gvimdiff、ecmerge和opendiff作为有效的合并工具。
```sh
# 全局示例，设置默认合并工具为vimdiff
git config --global merge.tool vimdiff
```
# 配置比较工具高亮显示改动状态
> 调用 git status/git diff 命令时以高亮或彩色方式显示改动状态
```sh
# 全局示例
git config --global color.ui true
```
