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
<br>yum install net-tools vim lrzsz 
<br>yum install sysstat #sar工具
<br>yum install psmisc #pstree工具
<br>yum install iptraf-ng #流量监控
<br>yum install -y bash-completion #systemctl命令补全
<br>
<br>yum -y install lshw pciutils gdisk system-storage-manager
<br>yum -y bash-completion zip unzip bzip2 tree tmpwatch pinfo man-pages
<br>yum -y nano vim-enhanced tmux screen
<br>yum -y net-tools psmisclsof sysstat
<br>yum -y yum-plugin-security yum-utils createrepo
<br>yum -y get wget curl eliks lynx lftp mailx mutt reync 
<br>yum -y libaio make cmake gcc-c++ gcc zib zlib-devel open openssl-devel pcre pcre-devel

