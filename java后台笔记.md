- kafka 创建队列命令:<br>
bin/kafka-topics.sh --create --zookeeper 192.168.18.201:2181,192.168.18.202:2181,192.168.18.203:2181 --replication-factor 3 --partitions 1 --topic finance_voucher

- tomcat 日志搜索命令:<br>
cat -n catalina.out | grep '你要搜索的'

- rm删除目录及目录里的东西(-r 就是向下递归，不管有多少级目录，一并删除):<br>
rm -rf 目录名

- rm删除目录里的东西,但是不删除目录:<br>
1.先cd到该目录<br>
2.rm ./*<br>

### centos7 最小化系统必备软件:
<br>yum install -y net-tools
<br>yum install -y wget
<br>yum install -y vim-enhanced
<br>yum install sysstat #sar工具
<br>yum install psmisc #pstree工具
<br>yum install iptraf-ng #流量监控
<br>yum install -y bash-completion #systemctl命令补全
<br>yum install gcc gcc-c++ -y  #任何编译安装必备
<br>yum install psmisc -y    #killall杀进程的
<br>yum install git -y #装github不然无法clone
<br>yum install telnet
<br>yum install telnet-server
<>yum install java -y

<br>#替换成阿里的源
<br>cd /etc/yum.repo.d
<br>#备份一下官方源
<br>mv CentOS-Base.repo CentOS-Base.repo.bak
<br>#将阿里源文件下载下来
<br>wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo
<br>#重建源数据缓存
<br>yum makecache


