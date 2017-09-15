> adb shell 命令的官方网站
  https://developer.android.com/studio/command-line/shell.html#othershellcommands

- 输出所有已经安装的应用 :  adb shell pm list packages -f [ | grep "mingcheng" ]
  <BR>如果提示grep无法使用, 将grep 用 find 或者 findstr替换
- 列出除了系统应用的第三方应用包名 :  adb shell pm list packages -3
- 列出系统应用的所有包名 :  adb shell pm list packages -s
- 查看设备型号 :  adb shell getprop ro.product.model  (如 xt1085)
- 手机截图 :  adb shell screencap /sdcard/screen.png
- 手机录像 :  adb shell screenrecord /sdcard/demo.mp4

- 如何只克隆git仓库中的一个分支？ : git clone -b <branch> <remote_repo>   例如： git clone -b 指定的分支名字 git地址


## 刷机常用
### 重启命令

- 正常重启 adb reboot

- 重启到 bootloader (刷机模式):  adb reboot bootloader

- 重启到 recovery (恢复模式):    adb reboot recovery

### fastboot
> fastboot 命令不多(以下为刷机常用):
1. 通过fastboot刷入系统镜像经常失败( recovery的sideload刷机也经常失败),所以如果没有recovery,则进入fastboot后,先装recovery,强烈建议使用twrp的rec,其他的都不好用,一路踩坑经验.
2. 重启bootloader : fastboot reboot-bootloader
3. 如果fastboot都无法进入,则成砖
     
> fastboot 刷入recovery步骤: 
1. 擦除(相当于recovery下的wipe): fastboot -w 
2. 列出设备: fastboot devices 
3. 刷入recovery: fastboot flash recovery (recovery.img-即本地路径) . 
4. 重新启动,正常开机 : fastboot reboot 
5. 每个型号的手机不同,按不同的键进入recovery (如果进不了rec,表示该rec不能用,换一个合适的)

### recovery
> recovery装好后,就可以利用adb命令. 在recovery的环境下直接传输文件
- 通过adb推送本地文件到手机sdcard : adb push 本地文件路径  /sdcard/

 ## 端口占用问题
 
 > 以adb的5037端口为例:
 1. C:\Users\Administrator>netstat -aon|findstr 5037 
    <br>找到一行有listening 的字样,表示被占用 .如: TCP 127.0.0.1:5037 0.0.0.0:0 LISTENING 996
    
 2. 通过PID查看所有进程 :  C:\Users\Administrator>tasklist /fi "pid eq 996"
 
 3. 杀死占用端口的进程 :   C:\Users\Administrator>taskkill /pid 996 /f

 ## git常用 
 > 提交步骤:
 1. 打开 Gitbash
 2. 使用 cd 命令用于切换到对应仓库的目录，cd .. 用于切换到上级目录，ls 用于查看当前目录下面的文件/夹
 3. 当修改了一段代码后，使用 git status 查看当前改动
 4. 如果需要把所有改动提交上去，使用 git add . 提交到缓冲区（此时文件并没有提交到远程仓库）
 5. 填写提交说明，使用 git commit -m '此处填写修改的内容' 命令
 6. 使用 git pull origin master 获取远程仓库master分支的最新改动。（如果远程仓库有更新，没有执行此步骤，无法进行下一步）
 7. 使用 git push origin master 提交改动到远程仓库
 8. github 的 Demo 默认使用 gh-pages 分支，Demo 地址是：http://用户名.github.io/仓库名/ 可以使用 git checkout gh-pages 切换到该分支(默认没有这     个分支，需要使用git checkout -b gh-pages创建该分支)。
