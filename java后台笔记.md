- kafka 创建队列命令:<br>
bin/kafka-topics.sh --create --zookeeper 192.168.18.201:2181,192.168.18.202:2181,192.168.18.203:2181 --replication-factor 3 --partitions 1 --topic finance_voucher

- tomcat 日志搜索命令:<br>
cat -n catalina.out | grep '你要搜索的'
<br>grep -rn "你要搜索的" 文件名

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

##### 安装oh-my-zsh
1.安装zsh包
yum -y install zsh

2.切换默认shell为zsh
chsh -s /bin/zsh

(重启或者关闭当前终端)

4.安装on my zsh
curl
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
wget
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"

git clone git://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions
source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh
git clone git://github.com/joelthelion/autojump.git

5.查看oh my zsh主题
ls ~/.oh-my-zsh/themes

6.修改主题
vim ~/.zshrc (默认的主题是ZSH_THEME="robbyrussell")
1.ZSH_THEME="ys"
2.同时修改plugins=(git git-flow grails rvm history-substring-search github gradle svn node npm zsh-syntax-highlighting sublime autojump)

7.使配置立即生效
$ source ~/.zshrc




