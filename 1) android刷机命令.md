## 1.常用命令
> adb shell 命令的官方网站
  https://developer.android.com/studio/command-line/shell.html#othershellcommands

- 输出所有已经安装的应用 :  adb shell pm list packages -f [ | grep "mingcheng" ]
  <BR>※如果提示grep无法使用, 将grep 用 find 或者 findstr替换
  <BR>※grep命令只有先执行adb shell , 才能使用 grep
- 列出除了系统应用的第三方应用包名 :  adb shell pm list packages -3
- 列出系统应用的所有包名 :  adb shell pm list packages -s
- 查看设备型号 :  adb shell getprop ro.product.model  (如 xt1085)
- 手机截图 :  adb shell screencap /sdcard/screen.png
- 手机录像 :  adb shell screenrecord /sdcard/demo.mp4
- 当前activity的包名和activity名称 :  dumpsys activity top
- 关机命令 :  adb shell reboot -p
- 查看应用的包信息 : dumpsys package 包名
- 强制关闭某个应用 : adb shell am force-stop 包名
    
    
#### 有没有我删不掉的流氓应用, 没有!!!, 终极杀器,深入Linux:
> 1.在cmd中获取root权限    执行adb root

> 2.进入adb shell   执行adb shell

> 3.获取su   执行su

> 4.查看system物理路径,以及是否可读   执行mount | grep /system

> 5.挂载system为可读写   执行mount -o remount,rw [路径] /system

> 6.删除目录及文件   执行rm -rf 目录名称

> 7.挂载system为只读   执行mount -o remount,ro [路径] /system(如果这一步无法实现,直接重启系统,会自动恢复RO只读)




## 2.刷机常用
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

> fastboot 危险命令(禁用):
1. !!! fastboot flash bootloader bootloader.img  该命令意思是重新输入bootloader分区,请务必注意, 如果你刷入了一个不匹配的bootloader.img, 那么你的手机100%成砖,只能换主板了.别无他法 !!!
2. fastboot erase bootloader (自毁命令)该命令意思是擦除BootLoader分区.一旦执行,宣告手机成砖.

### recovery
> recovery装好后,就可以利用adb命令. 在recovery的环境下直接传输文件
- 通过adb推送本地文件到手机sdcard : adb push 本地文件路径  /sdcard/

 ## 3.端口占用问题
 
 > 以adb的5037端口为例:
 1. C:\Users\Administrator>netstat -aon|findstr 5037 
    <br>找到一行有listening 的字样,表示被占用 .如: TCP 127.0.0.1:5037 0.0.0.0:0 LISTENING 996
    
 2. 通过PID查看所有进程 :  C:\Users\Administrator>tasklist /fi "pid eq 996"
 
 3. 杀死占用端口的进程 :   C:\Users\Administrator>taskkill /pid 996 /f

 
