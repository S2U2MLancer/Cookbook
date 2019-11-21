# Systemd的使用

Systemd是Linux系统工具，用来启动守护进程, 
取代了initd, 成为系统的第一个进程（PID 等于 1），其他进程都是它的子进程.

## 查看系统启动耗时

```shell
$ systemd-analyze
```

## hostnamectl

```shell
# 显示当前主机的信息
$ hostnamectl

# 设置主机名。
$ sudo hostnamectl set-hostname rhel7
```

## 本地化管理

```shell
# 查看本地化设置
$ localectl
```

## 时区管理

```shell
# 查看当前时区设置
$ timedatectl
```

## 系统服务管理

systemctl是 Systemd 的主命令，用于管理系统.

每一个Unit都有一个配置文件，告诉Systemd怎么启动这个Unit, 配置文件的后缀名，就是该Unit的种类
每个系统服务都是一个以.service为后缀的Unit.

Systemd默认从目录**/etc/systemd/system/**读取配置文件。
但是，里面存放的大部分文件都是符号链接，指向目录**/usr/lib/systemd/system/**，真正的配置文件存放在那个目录。

```shell
# 激活开机启动
$ systemctl enable <unit>
# 撤销开机启动
$ systemctl disable <unit>
# 查看状态
$ systemctl status <unit>
```

### 列出所有的Unit

```shell
$ systemctl list-unit-files
```

每个Unit有下面几种状态:

- enabled：已建立启动链接
- disabled：没建立启动链接
- static：该配置文件没有[Install]部分（无法执行），只能作为其他配置文件的依赖
- masked：该配置文件被禁止建立启动链接

### 重新加载修改的Unit

```shell
$ sudo systemctl daemon-reload
$ sudo systemctl restart <unit>
```

### 定义Unit

- Unit, 配置文件的第一个区块，用来定义 Unit 的元数据，以及配置与其他 Unit 的关系
- Service, 只有Service类型的 Unit 才有这个区块
- Install, 配置文件的最后一个区块，用来定义如何启动，以及是否开机启动

Target是一个Unit组，包含许多相关的Unit。
启动某个 Target 的时候，Systemd 就会启动里面所有的 Unit。

## 系统日志管理

```shell
# 显示尾部的最新20行日志
$ sudo journalctl -n 20
```

## Reference

- [Systemd 入门教程](http://www.ruanyifeng.com/blog/2016/03/systemd-tutorial-commands.html)