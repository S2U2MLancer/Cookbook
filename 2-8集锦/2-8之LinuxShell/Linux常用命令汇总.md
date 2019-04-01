# common linux command                                                                                                                                                                                                                                                                                        
### 线上查询及帮助命令
|命令|功能说明|常用参数|参数说明|链接|
|-|-|-|-|-|
|man|查看命令帮助，命令的词典，更复杂的还有info，但不常用。|1-9|1. 普通用户命令。5. 配置文件。8. root用户命令 |[man](http://man.linuxde.net/man)|
|help|查看shell内置命令的帮助，比如cd命令。|-h|查看该命令的帮助|[help](http://man.linuxde.net/help)|

### 文件和目录操作命令
|命令|功能说明|常用参数|参数说明|链接|
|-|-|-|-|-|
|ls|列出目录的内容及其内容属性信息。|-l, -a, -h|-l 列出详情模式， -a显示出所有文件包括隐藏文件， -h以常用的文件大小格式显示，如M,G,K等|[ls](http://man.linuxde.net/ls)|
|cd|切换目录|-P|如果切换的目录是链接文件，直接切换到实际目录|[cd](http://man.linuxde.net/cd)|
|cp|复制文件|-a， -r|-a复制的源文件不管是目录还是文件，直接复制并保留源文件的owner和group等权限。-r递归复制用于目录的复制|[cp](http://man.linuxde.net/cp)|
|find|以磁盘文件的方式查找文件|-name，-type|-name以文件名查找， -type f/d以文件类型查找，f为普通文件，d为目录|[find](http://man.linuxde.net/find)|
|mkdir|新建目录|-p，-v|-p递归创建目录，-v显示目录创建结果|[mkdir](http://man.linuxde.net/mkdir)|
|mv|移动或重命名文件或目录|--help|查看mv的详细帮助命令|[mv](http://man.linuxde.net/mv)|
|pwd|查看当前目录位置|-P|-P列出链接文件的真实目录路径不显示链接路径|[pwd](http://man.linuxde.net/pwd)|
|type|查看所接命令是shell内建命令还是软件包命令|-a|-a显示所接命令的所有可执行命令或别名|[type](http://man.linuxde.net/type)|
|rm|删除文件或目录|-r， -f|-r递归删除，用于删除目录。-f强制删除|[rm](http://man.linuxde.net/rm)|
|touch|创建一个空文件|-a，-d，-m|-a更改文件的访问时间。-d给出的时间替代为当前时间。-m更改文件的修改时间|[touch](http://man.linuxde.net/touch)|
|tree|树形显示目录下的内容|-a，-d，-f|-a列出所有文件。-d只列出目录。-f列出文件的全路径|[tree](http://man.linuxde.net/tree)|
|basename|显示全路径中的文件名|--help|--help显示帮助|[basename](http://man.linuxde.net/basename)|
|dirname|显示全路径中的目录名|--help|--help显示帮助|[dirname](http://man.linuxde.net/dirname)|
|file|查看文件类型，链接文件？压缩文件？文本文件？等等|-v，-h|-v查看该命令版本。-help|显示帮助|[file](http://man.linuxde.net/file)|
|md5sum|查看文件的md5值|-c|-c从文件中读取md5值，并和当前目录中的文件的md5值做比较|[md5sum](http://man.linuxde.net/md5sum)|
|cat|查看文件内容，并显示到stdout|--help|--help显示帮助|[cat](http://man.linuxde.net/cat)|
|less|查看文件内容，并设置前后翻页|--help|--help显示帮助|[less](http://man.linuxde.net/less)|
|head|查看文件的前面的行数|-n|-n具体接的行数|[head](http://man.linuxde.net/head)|
|tail|查看文件的末尾几行|-n，-f|-n具体的行数。-f动态显示文件的追加|[tail](http://man.linuxde.net/tail)|
|cut|截取文件内容|-b，-c，-d，-f|-b按字节大小。-c按字符大小。-d按给定的终止符代替tab。-f按给定的字段|[cut](http://man.linuxde.net/cut)|
|split|分割字符串或文件|-b，-l|-b按字节大小。-l按行数|[split](http://man.linuxde.net/split)|
|sort|排序|-r，-n，-t，-c|-c检查文件是否已经按照顺序排序。-n依照数值的大小排序。-r以相反的顺序来排序。-t指定排序时所用的栏位分隔字符|[sort](http://man.linuxde.net/sort)|
|uniq|去重|-c，-d，-u|-c在每列旁边显示该行重复出现的次数。-d仅显示重复出现的行列。-u仅显示出一次的行列|[uniq](http://man.linuxde.net/uniq)|
|wc|统计|-c，-l，-w|-c显示Bytes数。-l显示列数。-w显示字数|[wc](http://man.linuxde.net/wc)|
|dos2unix|windows格式文件转换为unix|--help|--help查看帮助|[dos2unix](http://man.linuxde.net/dos2unix)|
|diff|内容比较|参数太多请看链接|[链接](http://man.linuxde.net/diff)|  |
|grep|按关键字获取内容|-E，-v，-i|-E使用扩展的正则，-v排除接的关键字，-i忽略大小写|[grep](http://man.linuxde.net/grep)|
|tr|字符替换|-s，-t|-s连续重复的字符只显示一个字符。-t删除第一字符集比第二字符集多出的字符|[tr](http://man.linuxde.net/tr)|
|tee|将stderr、stdout重定向到文件|-a|-a以追加的方式写入文件中|[tee](http://man.linuxde.net/tee)|
|vim|文件编辑器|-b，-d，-R|-b以二进制模式打开文件，-d以diff模式打开文件，-R只读方式打开|[vim](http://man.linuxde.net/vim)|
|chmod|更改文件权限|-R|-R递归处理文件文件及子文件|[chmod](http://man.linuxde.net/chmod)|
|chown|更改文件所有者|-R|-R递归处理文件文件及子文件|[chown](http://man.linuxde.net/chown)|
|umask|设定文件默认权限值|-p，-S|-p输出的权限掩码可直接作为指令来执行。-S以符号方式输出权限掩码|[umask](http://man.linuxde.net/umask)|

### 压缩解压命令
|命令|功能说明|常用参数|参数说明|链接|
|-|-|-|-|-|
|tar|打包压缩。|-x, -v, -c, -f, -z, -j, -J|-x解压。-v显示stdout。-c创建压缩文件。-f指定压缩文件名。-z调用gzip程序。-j调用bzip2程序。-J调用xz程序|[tar](http://man.linuxde.net/tar)|
|unzip|解压zip文件|-l|-l列出压缩包文件|[unzip](http://man.linuxde.net/unzip)|
|gzip|打包压缩。|-d，-l，-1，-9|-d解压压缩文件。-l列出压缩包内容。-1快速创建压缩文件。-9压缩率最高且速度慢|[gzip](http://man.linuxde.net/gzip)|

### 系统资源管理
|命令|功能说明|常用参数|参数说明|链接|
|-|-|-|-|-|
|uname|打印系统信息|-a，-r|-a打印所有系统信息。-r打印内核释放版本。|[uname](http://man.linuxde.net/uname)|
|hostname|打印主机名|-f，-I|-f打印FQDN。-I打印出ip地址|[hostname](http://man.linuxde.net/hostname)|
|uptime|显示系统开机时间及系统负载情况|--help|列出该命令详细用法|[uptime](http://man.linuxde.net/uptime)|
|du|打印出文件或目录大小|-h，-s|-h以直观的单位大小显示。-s只打印出总的大小|[du](http://man.linuxde.net/du)|
|df|打印出磁盘挂载情况及使用率|-h，-T|-h以直观的单位大小显示。-T打印出磁盘格式类型|[df](http://man.linuxde.net/df)|
|top|动态显示linux进程情况|m，1|m以内存大小排序，倒序。1列出所有cpu情况。|[top](http://man.linuxde.net/top)|
|free|查看所有内存使用情况|-h，-t|-h，-T|-h以直观的单位大小显示。-t打印出所有的内存使用，包括swap|[free](http://man.linuxde.net/free)|
|date|打印当前时间|%Y%m%d%H%M%S|%Y四位数的年。%m两位数的月份。%d两位数的日。%H24小时制的时。%M分钟。%S秒。|[date](http://man.linuxde.net/date)|
|which|查找命令路径|-a|-a打印PATH变量中所有相关命令的路径。|[which](http://man.linuxde.net/which)|
|locate|从mlocate数据库中搜索文件|-d|-d指定mlocate数据库位置|[locate](http://man.linuxde.net/locate)|
|updatedb|更新mlocate数据库|-h|-h列出该命令帮助信息|[updatedb](http://man.linuxde.net/updatedb)|

### 用户管理
|命令|功能说明|常用参数|参数说明|链接|
|-|-|-|-|-|
|useradd|创建新用户|-d，-g，-G，-s，-m，-r，-n|-d指定用户目录路径。-g指定用户所属群组。-G指定用户所属的附加群组。-s指定用户的登录的shell。-m自动建立用户目录。-r创建系统用户。-n取消建立以用户名为名字的群组|[useradd](http://man.linuxde.net/useradd)|
|usermod|更改用户信息|-d，-g，-G，-s|-d更改用户目录。-g更改用户群组。-G更改用户附加群组。-s更改用户登录的shell|[usermod](http://man.linuxde.net/usermod)|
|userdel|删除用户|-f，-r|-f强制删除该用户。-r删除用户并同时删除该用户的所有文件|[userdel](http://man.linuxde.net/userdel)|
|passwd|更改用户密码|-d，-f，-S|-d删除密码。-f强制执行。-s查看密码信息|[passwd](http://man.linuxde.net/passwd)|
|id|查看用户信息|-g，-G，-n，-r，-u|-g所属群组ID。-G附加群组ID。-n显示群组名称。-r实际ID。-u用户ID|[id](http://man.linuxde.net/id)|
|su|切换用户|-l，-s|-l更改用户同时更改到用户的所有环境中。-s指定shell|[su](http://man.linuxde.net/su)|
|visudo|更改/etc/sudoers文件的内容|-c，-f|-c检查该文件。-f指定具体的sudoers文件|[visudo](http://man.linuxde.net/visudo)|
|sudo|使用其他用户执行命令|-b，-u，-l|-b在后台执行命令。-u指定用户，默认为root。-l查看目前用户可执行与不可执行的命令|[sudo](http://man.linuxde.net/sudo)|
|whoami|查看当前用户名称|--help|--help显示帮助|[whoami](http://man.linuxde.net/whoami)|
|who|查看当前登录系统的用户信息|-q|查看登录系统的帐号名称和总人数|[who](who)|
|w|查看已经登录的用户|-u，-f|-u查看当前进程和cpu时间时忽略用户名。-f显示用户从哪登录|[w](http://man.linuxde.net/w)|
|last|查看用户登录信息|-a|-a从哪登录系统的主机名或IP地址显示在最后一行|[last](http://man.linuxde.net/last)|
|lastlog|查看所有用户登录信息|-b，-t，-u|-b查看指定天数前的登录信息。-t查看指定天数以来的登录信息。-u指定用户|[lastlog](http://man.linuxde.net/lastlog)|

### 网络管理相关命令
|命令|功能说明|常用参数|参数说明|链接|
|-|-|-|-|-|
|telnet|登录主机方式|-a，-d，-K，-l|-a自动登录。-d启用debug。-K不自动登录。-l指定用户名|[telnet](http://man.linuxde.net/telnet)|
|ssh|远程登录|-i，-p|-i指定key文件。-p指定端口|[ssh](http://man.linuxde.net/ssh)|
|scp|远程文件复制|-i，-P，-r|-i指定key文件。-P指定端口。-r递归方式复制|[scp](http://man.linuxde.net/scp)|
|rsync|远程文件复制|-a，-v，-z，--progress，-e|-a启用文件同步。-v显示详情。-z启用压缩。--progress显示进度详情。-e使用ssh选项|[rsync](http://man.linuxde.net/rsync)|
|wget|下载文件|-c|-c启动断点续传|[wget](http://man.linuxde.net/wget)|
|ping|查看网络连接|-c|-c发送数据库的数量|[ping](http://man.linuxde.net/ping)|
|route|查看本机路由|-n|-n不显示主机名|[route](http://man.linuxde.net/route)|
|ifconfig|查看网卡IP信息|示例|ifconfig 192.168.11.10 netmask 255.255.255.0 eth0|[ifconfig](http://man.linuxde.net/ifconfig)|
|ip|设置主机网络设备，路由等|-s，-f，-r|-s显示详细信息。-f强制使用指定的协议族。-r显示主机名。|[ip](http://man.linuxde.net/ip)|
|netstat|查看主机的网络连接信息|-t，-u，-l，-n，-p|-t显示tcp连接。-u显示udp连接。-l以列表方式显示。-n不显示主机名。-p显示进程|[netstat](http://man.linuxde.net/netstat)|
|ss|查看主机的网络连接信息|-n，-a，-l，-m，-p，-t，-u|-n不显示主机名。-a显示所有socket。-l查看监听状态socket。-m显示socket内存使用。-p查看socket进程。-t查看tcp连接。-u查看udp链接|[ss](http://man.linuxde.net/ss)|
|lsof|查看进程打开的文件和端口|-a，-c，-p，-g，-d，-u|-a打开文件存在的进程。-c查看指定进程打开的文件。-p查看指定进程号打开的文件。-g查看gid号进程信息。-d查看该文件号的进程。-u指定拥护|[lsof](http://man.linuxde.net/lsof)|
|mail|命令行下收发邮件|-b，-c，-f，-I|-b指定密送收件人地址。-c抄送收件人地址。-f指定邮件文件中的邮件。-I使用交互模式|[mail](http://man.linuxde.net/mail)|
|dig|域名查询工具|-f，-b，-P，-t，-x|-b指定本机的某一个地址向DNS发送域名查询请求。-f域名查询请求存在与一个文件中供dig调用。-P DNS端口号。-t查询的DNS数据类型。-x反向域名查询|[dig](http://man.linuxde.net/dig)|
|traceroute|网络传输的全部路径|-d，-f，-g，-i，-I，-n，-p，-s，-t|-d开启debug。-f设置数据包的TTL的大小。-g设置源路由。-i指定网卡。-I使用ICMP。-n使用IP地址。-p设置UPD端口。-s设置本地的IP地址。-t设置TOS|[traceroute](http://man.linuxde.net/traceroute)|
|tcpdump|查看网络数据包信息|-a，-c，-d，-f，-i，-n，-w|-a将网络地址转换成名称。-c指定接收的数据包数目。-d数据包转换成可阅读的格式。-f指定数字显示网络地址。-i指定网卡。-n不把网络地址转换成名字。-w保存到指定的文件|[tcpdump](http://man.linuxde.net/tcpdump)|

### 磁盘管理
|命令|功能说明|常用参数|参数说明|链接|
|-|-|-|-|-|
|mount|挂载磁盘到目录|-a，-t，-r，-w|-a将/etc/fstab文件中还没有挂载的文件系统挂载起。-t挂载指定文件系统类型。-r以只读方式挂载。-w以读写方式挂载|[mount](http://man.linuxde.net/mount)|
|umount|卸载文件系统|-f，-l|-f强制卸载用于NFS中。-l懒惰模式|[umount](http://man.linuxde.net/umount)|
|dd|复制文件|bs，count，ibs，obs，if，of|bs字节数，count指定的区块数。ibs输入的字节数。obs输出的字节数。if输入的文件。of输出的文件|[dd](http://man.linuxde.net/dd)|
|fdisk|磁盘分区工具用于小于2T磁盘|-l，-b|-l列出本机所有磁盘，-b指定每个分区的大小|[fdisk](http://man.linuxde.net/fdisk)|
|parted|磁盘分区工具|-i，-s|-i使用交互模式。-s使用脚本模式|[parted](http://man.linuxde.net/parted)|
|mkfs|磁盘格式化|-t|-t指定文件系统类型|[mkfs](http://man.linuxde.net/mkfs)|
|mkswap|制作swap分区|-c|-c检查磁盘是否有损坏|[mkswap](http://man.linuxde.net/mkswap)|
|swapon|开始swap|-s|-s查看swap的使用情况|[swapon](http://man.linuxde.net/swapon)|
|swapoff|关闭swap|-a|-a关闭/etc/fstab中的所有swap|[swapoff](http://man.linuxde.net/swapoff)|
|echo|显示字符串或变量|-e|-e使用转义符|[echo](http://man.linuxde.net/echo)|

### 包管理
|命令|功能说明|常用参数|参数说明|链接|
|-|-|-|-|-|
|yum|redhat发行版及衍生版rpm包在线管理|-y，-v，-q|-y非交互模式全部选yes。-v verbose详细模式。-q安静模式|[yum](http://man.linuxde.net/yum)|
|rpm|系统rpm包管理器|-a，-e，-i，-l，-q|-a查询所有包。-e卸载包。-i查看包信息。-l查看包列表。-q查询包|[rpm](http://man.linuxde.net/rpm)|
|apt-get|debian发行版及衍生版deb包在线管理|-d，-u|-d仅下载不安装包。-u查看更新包列表|[apt-get](http://man.linuxde.net/apt-get)|
|apt|同apt-get作用|--help|--help查看帮助|[apt](http://man.linuxde.net/apt)|
|dpkg|系统deb包管理器|-l，-i，-r，-P|-l查看所有安装的包。-i安装包。-r删除包。-P删除包并删除该包的所有文件|[dpkg](http://man.linuxde.net/dpkg)|

### 其他系统相关
|命令|功能说明|常用参数|参数说明|链接|
|-|-|-|-|-|
|alias|设置命令别名|-p|-p显示已经设置的命令别名|[alias](http://man.linuxde.net/alias)|
|unalias|取消命令别名|-a|-a取消所有命令别名|[unalias](http://man.linuxde.net/unalias)|
|history|查看使用过的命令|-c，-w，-r，-a|-c清除历史命令。-w将当前历史命令写入文件中。-r将文件中的历史命令读到缓冲区。-a将缓冲区命令写入文件|[history](http://man.linuxde.net/history)|
|time|统计命令使用的时间|--help|--help显示帮助|[time](http://man.linuxde.net/time)|
|xargs|给其他命令传递参数的过滤器|-n，-d|-n指定列数。-d指定终止符|[xargs](http://man.linuxde.net/xargs)|
|exec|调用并执行其他命令|-c|-c执行指定的命令|[exec](http://man.linuxde.net/exec)|
|export|指定变量为环境变量|-f，-n，-p|-f变量名称中为函数名称|[export](http://man.linuxde.net/export)|
|unset|取消环境变量的定义|-f，-v|-f删除函数。-v删除变量|[unset](http://man.linuxde.net/unset)|
|chkconfig|检查设置系统服务|--add，--del，--level|--add增加指定的系统服务。--del删除指定的系统服务。--level指定服务在某个层级中开关|[chkconfig](http://man.linuxde.net/chkconfig)|
|systemctl|systemd的操作指令|enable，disable，status，start|集service命令和chkconfig命令于一身|[systemctl](http://man.linuxde.net/systemctl)|
|service|服务操作相关|start，stop，restart，status|启动。停止。重启。运行状态|[service](http://man.linuxde.net/service)|
|update-rc.d|debian系统服务操作相关同chkconfig类似|-f，remove，defaults，start，disable，enable|-f强制。删除。加入到默认启动。|[update-rc.d](http://man.linuxde.net/update-rc.d)|
|vmstat|查看虚拟内存状态|-a，-f，-d，-p|-a查看活动页。-f查看启动后创建的进程数。-d查看磁盘状态。-p查看分区状态|[vmstat](http://man.linuxde.net/vmstat)|
|mpstat|查看多cpu的状态|-P|-P指定cpu编号|[mpstat](http://man.linuxde.net/mpstat)|
|iostat|查看IO和cpu的状态|-c，-d，-p|-c显示cpu状态。-d设备利用率。-p块设备和被使用的其他分区状态|[iostat](http://man.linuxde.net/iostat)|
|sar|系统运行状态统计工具|-A，-b，-d，-P，-R，-x，-w|-A所有信息。-b I/O速率。-d块设备。-Pcpu状态。-R内存状态。-x指定进程状态。-w swap状态|[sar](http://man.linuxde.net/sar)|
|shutdown|关闭系统|-h，-r，-t|-h关机。-r重启。-t时间秒|[shutdown](http://man.linuxde.net/shutdown)|
|reboot|重启系统|-f，-w|-f强制重启。-w不真正关机|[reboot](http://man.linuxde.net/reboot)|
|logout|退出系统|--version|--version查看版本信息|[logout](http://man.linuxde.net/logout)|
|exit|退出系统|--version|--version查看版本信息|[exit](http://man.linuxde.net/exit)|
|bg|将作业放到后台执行|属于bash内置命令|无选项|[bg](http://man.linuxde.net/bg)|
|fg|将后台作业放到终端执行|同上|同上|[fg](http://man.linuxde.net/fg)|
|jobs|显示任务列表及状态|-l，-p，-n|-l进程号。-p作业对应的进程号。-n查看任务状态的变化|[jobs](http://man.linuxde.net/jobs)|
|kill|结束进程|-a，-u，-9|-a处理当前进程不限制命令和PID对应。-u指定用户。-9无条件结束进程|[kill](http://man.linuxde.net/kill)|
|killall|使用进程名结束进程|-l，-p，-i，-u|-p结束进程所属的进程组。-l忽略大小写。-i交互式结束需确认。-u指定用户|[killall](http://man.linuxde.net/killall)|
|pkill|按照进程名结束进程|-P，-g|-P指定父进程号。-g指定进程组|[pkill](http://man.linuxde.net/pkill)|
|crontab|定时任务管理|-e，-l，-r，-u|-e编辑定时任务。-l查看定时任务。-r删除定时任务。-u指定用户|[crontab](http://man.linuxde.net/crontab)|
|ps|进程状态|a u x，-e，-f|a显示所有进程。u用户为主显示进程状态。x显示所有进程。-ef显示所有进程|[ps](http://man.linuxde.net/ps)|
|pstree|树状的进程状态|-a，-u，-l|-a显示每个进程的完整指令。-u显示用户。-l长格式|[pstree](http://man.linuxde.net/pstree)|
|nohup|忽略进程的信号运行|--help|--help显示帮助|[nohup](http://man.linuxde.net/nohup)|