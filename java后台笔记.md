- kafka 创建队列命令:<br>
bin/kafka-topics.sh --create --zookeeper 192.168.18.201:2181,192.168.18.202:2181,192.168.18.203:2181 --replication-factor 3 --partitions 1 --topic finance_voucher

- tomcat 日志搜索命令:<br>
cat -n catalina.out | grep '你要搜索的'
grep -rn "你要搜索的" 文件名

- rm删除目录及目录里的东西(-r 就是向下递归，不管有多少级目录，一并删除):<br>
rm -rf 目录名

- rm删除目录里的东西,但是不删除目录:<br>
1.先cd到该目录<br>
2.rm ./*<br>

### centos7 最小化系统必备软件:
<br>yum install -y net-tools
<br>yum install -y wget
<br>yum install -y vim-enhanced
<br>yum install -y sysstat #sar工具
<br>yum install -y psmisc #pstree工具,killall杀进程的
<br>yum install -y iptraf-ng #流量监控
<br>yum install -y bash-completion #systemctl命令补全
<br>yum install -y gcc gcc-c++   #任何编译安装必备
<br>yum install -y git  #装git
<br>yum install -y telnet
<br>yum install -y telnet-server
<br>yum install -y java (openjdk)

- 关闭centos7默认的firewall防火墙
<br>systemctl stop firewalld.service #停止firewall
<br>systemctl disable firewalld.service #禁止firewall开机启动

