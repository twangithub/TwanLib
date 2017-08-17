## mac osx 的虚拟机安装 以及 Ios免证书开发

### mac osx 的安装

mac osx的下载地址,安装教程: [https://techsviewer.com/how-to-install-mac-os-x-el-capitan-on-vmware-on-pc/](https://techsviewer.com/how-to-install-mac-os-x-el-capitan-on-vmware-on-pc/)

> tips:

1. 安装时, 在选择登录apple时可以先不登录.我试几次都是一直在等待状态.
2. 安装后,这个系统装也许并不是最新的,不要紧,该系统跟正常的max os一样, 放心的升级.没有任何问题

### IOS免证书开发注意事项

下面这些记录,务必记住,特别是推送

- 第一次真机运行项目时，Xcode会弹出一个框（Could not launch “YourAppName”），手机没有信任该开发者的应用，在信任该开发者之前将不会运行。需要在手机里进行设置：
***设置 -> 通用 -> 描述文件与设备管理 -> 开发者应用 -> 信任“开发者账号”***

- 如果你的项目使用了通知功能,请一定关掉(先把Automatically manage signing 的勾去掉才会出现推送等特性.因为自己的appleid没交费不会显示这些特性): ***真机测试前必须关闭App的推送特性(Target->Capabilities->Push Notifications)。***
还有一些功能也不能用.[参考apple官方地址](https://developer.apple.com/support/app-capabilities/)

- 免费的真机调试账号，Provisioning Profile期限只有十天左右（付费有一年的时间），超过这个期限，打开App就是闪退。
解决办法：删掉Provisioning Profile，重新配置一次。如果勾选了Automatically manage signing,Xcode会自动更新证书和配置文件，重新安装即可！

- 真机调试时,请务必保持xcode sdk和 iPhone sdk 版本一致, xcode的错误提示太难懂.
