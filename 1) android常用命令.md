- 输出所有已经安装的应用 :  adb shell pm list packages -f [ | grep "mingcheng" ]

- 如何只克隆git仓库中的一个分支？ : git clone -b <branch> <remote_repo>   例如： git clone -b 指定的分支名字 git地址


## 刷机常用
- 通过adb推送本地文件到手机sdcard : adb push 本地文件路径  /sdcard/

- 正常重启 adb reboot

- 重启到 bootloader (刷机模式):  adb reboot bootloader

- 重启到 recovery (恢复模式):    adb reboot recovery

- fastboot 命令不多(以下为刷机常用).  
     i) 通过fastboot刷入系统镜像经常失败( recovery的sideload刷机也经常失败),所以如果没有recovery,则进入fastboot后,先装recovery,
        强烈建议使用twrp的rec,其他的都不好用,一路踩坑经验.
        
     i) 重启bootloader : fastboot reboot-bootloader
     i) 如果fastboot都无法进入,则成砖
     
  fastboot 刷入recovery步骤:
  1) 擦除(相当于recovery下的wipe): fastboot -w
  2) 列出设备: fastboot devices
  3) 刷入recovery: fastboot flash recovery (recovery.img-即本地路径) .
  4) 重新启动,正常开机 : fastboot reboot
  5) 每个型号的手机不同,按不同的键进入recovery
 
  
