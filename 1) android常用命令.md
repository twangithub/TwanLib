- 输出所有已经安装的应用 :  adb shell pm list packages -f [ | grep "mingcheng" ]

- 如何只克隆git仓库中的一个分支？ : git clone -b <branch> <remote_repo>   例如： git clone -b 指定的分支名字 git地址

- 通过adb推送本地文件到手机sdcard : adb push 本地文件路径  /sdcard/

- 正常重启 adb reboot

- 重启到 bootloader (刷机模式):  adb reboot bootloader

- 重启到 recovery (恢复模式):    adb reboot recovery
