- kafka 创建队列命令:<br>
bin/kafka-topics.sh --create --zookeeper 192.168.18.201:2181,192.168.18.202:2181,192.168.18.203:2181 --replication-factor 3 --partitions 1 --topic finance_voucher

- tomcat 日志搜索命令:<br>
cat -n catalina.out | grep '你要搜索的'

- rm删除目录及目录里的东西(-r 就是向下递归，不管有多少级目录，一并删除):<br>
rm -rf 目录名

- rm删除目录里的东西,但是不删除目录:<br>
1.先cd到该目录<br>
2.rm ./*<br>

