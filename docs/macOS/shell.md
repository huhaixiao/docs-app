# shell

- [《linux shell 脚本 入门到实战详解[⭐建议收藏！！⭐]》](https://blog.csdn.net/weixin_42313749/article/details/120524768?utm_source=app&app_version=5.5.0)
- [《shell脚本语言(超全超详细)》](https://blog.csdn.net/weixin_43288201/article/details/105643692?utm_source=app&app_version=5.5.0)
- shell命令可以分为以下三类：
 - 内建函数(built-in function)：shell自带的功能
 - 可执行文件(executable file)：保存在shell之外的脚本，提供了额外的功能。
 - 别名(alias)：给某个命令的简称

```shell

# 查看占用了8000端口的进程
lsof -i tcp:8000
# 根据PID停掉某个进程
kill -9 {PID}

# 查看本地IP; en:0 字段查看IPv4
ifconfig

# sed ??
sed -i "s:old_value:new_value:g" src/index.ts

# 返回命令对应的可执行文件的绝对路径
which date
which pwd
which $SHELL

# 可以用type命令查看命令类型。
# 如果是内建函数会返回builtin字样，
# 如果是可执行文件，将返回文件的路径
type date
type pwd

date
cal
echo $SHELL

# log 输出到文件
yarn ios > error.txt

whoami

ls -la
ls -l <file>

drwxrwxrwx

groups $(whoami)

id -a $(whoami)
```

```shell
cd ~ # 返回Root用户位置
cd - # 返回上一次目录
cd .. # 返回上一级目录
cd ~/Desktop # 进入桌面位置

find *.txt # 找到当前目录下所有的txt文件
ls
ls -l
ls -la

mkdir dirname
touch filename.ext

rm filename.ext
rmdir emptyDirname

ctrl+a # 光标到行首
ctrl+e # 光标到行尾
ctrl+c # 终止进程

command+k # 清屏
```

```shell
# linux ubuntu
# install nodejs
apt install nodejs

# checkout architecture
arch

# checkout shell type
echo $0
```

## zsh

- Z-Shell macOS default Shell

```shell
# restart zsh
source ~/.zshrc
```

### .zshrc

```shell
alias python=python3
# setup zsh's proxy
export http_proxy=http://127.0.0.1:8080
export https_proxy=http://127.0.0.1:8080
```

## bash

- Bourne Again SHell
- `~/.bash_profile`
