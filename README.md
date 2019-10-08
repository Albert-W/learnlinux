# Learn Linux 
It's a project to demonstrate how the linux bash works. 

### Install bash kernel for jupyter notebook
```bash
pip install bash_kernel
python -m bash_kernel.install
```
### Start jupyter notebook
```bash
jupyter notebook 
# In the notebook interface, select Bash from the 'New' menu
```

### Centos VS Ubuntu Commands Comparison 

|                                                                | ubuntu                                                                            | centos7                                                                                |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| 系统信息                                                       |                                                                                   |                                                                                        |
| 版本                                                           | lsb_release -ahead -n 1 /etc/issuecat /etc/issue                                  | cat /etc/redhat-release                                                                |
| 内核/操作系统/CPU信息                                          | uname -a                                                                          |                                                                                        |
| 包含GCC的版本信息                                              | cat /proc/version                                                                 |                                                                                        |
| CPU信息                                                        | cat /proc/cpuinfolscpu                                                            |                                                                                        |
| 计算机名                                                       | hostname                                                                          |                                                                                        |
| 环境变量                                                       | env                                                                               |                                                                                        |
| 查看系统位数                                                   | file /bin/lsgetconf LONG_BIT                                                      |                                                                                        |
| 显示当前shell                                                  | echo $SHELL                                                                       |                                                                                        |
| 资源信息                                                       |                                                                                   |                                                                                        |
| 内存使用量和交换区使用量                                       | free -h                                                                           |                                                                                        |
| 各分区使用情况                                                 | df -h                                                                             |                                                                                        |
| 指定目录的大小                                                 | du -sh ./miniconda3/                                                              |                                                                                        |
| 内存总量                                                       | grep MemTotal /proc/meminfo                                                       |                                                                                        |
| 空闲内存量                                                     | grep MemFree /proc/meminfo                                                        |                                                                                        |
| 系统运行时间、用户数、负载                                     | uptime                                                                            |                                                                                        |
| 系统负载磁盘信息                                               | cat /proc/loadavg                                                                 |                                                                                        |
| 挂接的分区状态                                                 | mount \| column -t输出显示为表格                                                  |                                                                                        |
| 网络信息                                                       |                                                                                   |                                                                                        |
| 所有网络接口的属性，mtu                                        | ifconfig                                                                          |                                                                                        |
| 查看防火墙设置                                                 | iptables -L                                                                       |                                                                                        |
| 路由表                                                         | route                                                                             |                                                                                        |
| 网卡信息文件                                                   | 无                                                                                | cat /etc/sysconfig/network-scripts/ifcfg-eth0                                          |
| 主机名文件                                                     | cat /etc/sysconfig/network                                                        |                                                                                        |
| 查看DNS服务器                                                  | cat /etc/resolv.conf                                                              |                                                                                        |
| 监听网卡docker0收发包                                          | sudo tcpdump -i docker0                                                           |                                                                                        |
| 查看收发包                                                     | ping www.google.com                                                               | sudo ping www.google.com                                                               |
| 查看端口                                                       | netstat -alsof -i                                                                 |                                                                                        |
| 用户与组                                                       |                                                                                   |                                                                                        |
| 活动用户                                                       | w                                                                                 |                                                                                        |
| 当前用户信息                                                   | id                                                                                |                                                                                        |
| 用户登录日志                                                   | last                                                                              |                                                                                        |
| 用户所在组信息                                                 | groups                                                                            |                                                                                        |
| 系统所有用户                                                   | cut -d: -f1 /etc/passwd                                                           |                                                                                        |
| 所有用户详细                                                   | cat /etc/passwdlslogins                                                           |                                                                                        |
| 系统所有组                                                     | cut -d: -f1 /etc/group                                                            |                                                                                        |
| 当前用户的计划任务                                             | crontab -l                                                                        |                                                                                        |
| 激活root用户                                                   | passwd                                                                            |                                                                                        |
| 添加一个新用户                                                 | useradd youname                                                                   |                                                                                        |
| 设定登录密码                                                   | sudo passwd youname                                                               |                                                                                        |
| 添加用户到sudoers file                                         |                                                                                   | chmod u+w /etc/sudoersvi /etc/sudoers添加 youuser ALL=(ALL) ALLchmod u-w /etc/sudoers  |
| 切换到root用户                                                 | su root                                                                           |                                                                                        |
| 切换用户和home目录                                             | su - postgres                                                                     |                                                                                        |
| 添加新组                                                       | sudo groupadd docker                                                              |                                                                                        |
| 添加用户到组                                                   | sudo usermod -aG docker $USER                                                     |                                                                                        |
| 切换群组                                                       | newgrp - docker                                                                   |                                                                                        |
| 添加所有权                                                     | sudo chown -R $USER ~/.npm                                                        |                                                                                        |
| 添加执行权限                                                   | chmod u+x getdocker.sh                                                            |                                                                                        |
| 全部修改权限                                                   | chmod 600 *                                                                       |                                                                                        |
| 软件操作                                                       |                                                                                   |                                                                                        |
| 软件包后缀                                                     | *.deb                                                                             | *.rpm                                                                                  |
| 软件源配置文件                                                 | /etc/apt/sources.list                                                             | /etc/yum.conf                                                                          |
| 升级系统版本                                                   | sudo do-release-upgradesudo apt dist-upgrade                                      | sudo yum update                                                                        |
| 更新软件源                                                     | sudo apt update                                                                   | 每次运行yum时自动更新                                                                  |
| 更新已经安装的软件                                             | sudo apt upgrade                                                                  | sudo yum update                                                                        |
| 升级某个包                                                     | sudo upgrade package                                                              | sudo yum update package                                                                |
| 安装软件                                                       | sudo apt install package                                                          | sudo yum install package                                                               |
| 安装本地软件                                                   | dpkg -i pkg.debpkg --install pkg.deb                                              | yum install pkg.rpmrpm -i pkg.rpm                                                      |
| 源码安装                                                       | $ tar -xvf ruby-2.6.5.tar.gz$ cd ruby-2.6.5$ ./configure$ make$ sudo make install |                                                                                        |
| 删除源码安装                                                   | sudo make uninstallwhereis ruby \| xargs -n 1 sudo rm -rf                         |                                                                                        |
| 删除已安装的软件（保留配置文件）                               | sudo apt remove xxxxx                                                             | sudo yum erase package                                                                 |
| 删除已安装软件（不保留配置文件)。                              | sudo apt --purge remove xxxxx                                                     |                                                                                        |
| 批量卸载                                                       | dpkg -l \| grep docker \| awk '{print $2}' \| xargs -n1 sudo apt -y remove        | yum list installed \| grep docker \| awk '{print $1}' \| xargs -n1 sudo yum -y remove  |
| 删除为了满足其他软件包的依赖而安装的，但现在不再需要的软件包。 | sudo apt autoremove                                                               |                                                                                        |
| 将已经删除了的软件包的.deb安装文件从硬盘中删除掉。             | sudo apt autoclean                                                                | sudo yum clean                                                                         |
| 查看已安装的软件                                               | apt list --installeddpkg -l                                                       | yum list installedrpm -qa                                                              |
| 获取某软件包的信息                                             | apt-cache show package                                                            | yum search package                                                                     |
| 获取某个已安装软件包的信息                                     | dpkg --status package                                                             | yum info packagerpm -qi package                                                        |
| 搜索某个文件是由哪个软件包安装的                               | dpkg -S /file/namedpkg --search /file/name                                        | rpm -qf /file/name                                                                     |
| 搜索所有提供某个文件的软件包                                   | apt-file search /file/name                                                        | yum provides /file/name                                                                |
| 服务管理                                                       |                                                                                   |                                                                                        |
| 启动服务                                                       | /etc/init.d/apache start                                                          | systemctl start postgresql-11                                                          |
| 停止服务                                                       | /etc/init.d/apache stop                                                           | systemctl stop postgresql-11                                                           |
| 开机启动                                                       | update-rc.d apache defaults                                                       | systemctl enable postgresql-11                                                         |
| 禁止开机启动                                                   | update-rc.d apache purge                                                          | systemctl disable postgresql-11                                                        |
| 开机启动状态                                                   |                                                                                   | systemctl status postgresql-11chkconfig --list\|grep httpd                             |
| 进程管理                                                       |                                                                                   |                                                                                        |
| 查看当前进程                                                   | ps                                                                                |                                                                                        |
| 查看所有进程                                                   | ps -efps aux                                                                      |                                                                                        |
| 找到所有httpd                                                  | ps aux \| grep httpd                                                              |                                                                                        |
| 查看进程树                                                     | pstree                                                                            | 无                                                                                     |
| 查看进程占用的目录                                             | pwdx  PID                                                                         |                                                                                        |
| 实时显示进程状态                                               | top                                                                               |                                                                                        |
| 形象化查看系统状态                                             | htop                                                                              |                                                                                        |
| 重启2235进程                                                   | kill -1 2235                                                                      |                                                                                        |
| 强制杀死2236                                                   | kill -9 2236                                                                      |                                                                                        |
| 杀死所有包含httpd的进程                                        | killall -9 httpd                                                                  |                                                                                        |
| 暂停当前进程                                                   | ctrl+z                                                                            |                                                                                        |
| 终止                                                           | ctrl+c                                                                            |                                                                                        |
| 后台启动                                                       | vi test &                                                                         |                                                                                        |
| 脱离shell启动                                                  | nohup wget site.com/file.zip                                                      |                                                                                        |
| 显式后台进程                                                   | jobs -l                                                                           |                                                                                        |
| 把工作号为1的后台任务置前台                                    | fg 1                                                                              |                                                                                        |
| 文件命令                                                       |                                                                                   |                                                                                        |
| 切换目录                                                       | cd     homecd -   lastcd ..  parent                                               |                                                                                        |
| 当前目录                                                       | pwd                                                                               |                                                                                        |
| 创建多级目录                                                   | mkdir -p A/B                                                                      |                                                                                        |
| 强制删除目录或文件                                             | rm -rf /dir                                                                       |                                                                                        |
| 查看目录树                                                     | sudo apt install treetree .                                                       |                                                                                        |
| 查看两级目录                                                   | tree -L 2                                                                         |                                                                                        |
| 查看当前目录                                                   | ll='ls -alF'                                                                      | ll='ls -al --color=auto'                                                               |
| 查看别名                                                       | alias                                                                             |                                                                                        |
| 设置别名（临时生效）                                           | alias ll='ls -alh --color=auto'                                                   |                                                                                        |
| 设置别名永久生效                                               | echo "alias ll='ls -alh --color=auto'" >> ~/.bashrc && source ~/.bashrc           |                                                                                        |
| 复制文件夹                                                     | cp -avr A B结果B/A                                                                |                                                                                        |
| Rename folder.                                                 | mv A B结果B                                                                       |                                                                                        |
| move folder                                                    | mv A/B C/D结果A, C/D/Bmv C/D/B C/结果 C/B, D                                      |                                                                                        |
| 当前目录所有文件移动到上一级目录                               | mv * ../                                                                          |                                                                                        |
| 显示追加的内容                                                 | tail -f /var/log/auth.log                                                         |                                                                                        |
| 解压                                                           | tar -xvf ruby-2.6.5.tar.gz                                                        |                                                                                        |
| 查找命令                                                       |                                                                                   |                                                                                        |
| 显示builtin commands                                           | help                                                                              |                                                                                        |
| Display information about builtin commands.                    | help cd                                                                           |                                                                                        |
| Display information about command type.                        | type grep                                                                         |                                                                                        |
| locate the binary, source, and manual page files for a command | whereis grep                                                                      |                                                                                        |
| shows the full path of (shell) commands.                       | which greptype -p grep                                                            |                                                                                        |
| read from info file.                                           | info python                                                                       | info yum                                                                               |
| find file from database                                        | sudo updatedblocate                                                               | N/A                                                                                    |
| find file from directore tree, not commands.                   | find A                                                                            |                                                                                        |
| 执行命令                                                       |                                                                                   |                                                                                        |
| excute last command.                                           | !!                                                                                |                                                                                        |
| sudo 执行上条                                                  | sudo !!                                                                           |                                                                                        |
| 显示最近的30条指令                                             | history\|tail -30                                                                 |                                                                                        |
| excute #331 command of history list.                           | !331                                                                              |                                                                                        |
| 执行最近的以doc开头的指令                                      | !doc                                                                              |                                                                                        |
| 其他管道命令                                                   |                                                                                   |                                                                                        |
| 换行打印                                                       | echo -e '1 2 3 4 \n 5 6 7 8'                                                      |                                                                                        |
| 每次取3个参数                                                  | echo -e '1 2 3 4 \n 5 6 7 8'\|xargs -n3                                           |                                                                                        |
| 取第2列输出                                                    | echo -e '1 2 3 4 \n 5 6 7 8'\| awk '{print $2}'                                   |                                                                                        |
|                                                                |                                                                                   |                                                                                        |