- 当前Activity     -   用于获取应用包名及当前显示的activity
- 开发助手          -   用于快速获取本机信息以及界面调试信息
- F-Droid          -   android应用市场,该市场里的大部分app都有在github开源
- apkpure          -   Android应用市场,该市场可以下载play商店里的应用, apkpure.com
- Termux           -   android终端
- MyAndroidTools   -   可以对各个app的服务,活动,广播,进程,日志,数据库等进行分析
- LBE加速          -   常用来卸载顽固应用
- ML Manager       -   提取系统里的apk,可以看到包名
- vysor            -   在桌面上控制手机的一切
- Native Libs Monitor -  so库分析
- Pixel Ruler      -   测量空间大小,单位有sp,dp,px

## android apk 安装注意事项
- 如果apk保护so文件,那么就表示并不一定在所有的android手机上顺利安装. 目前市面上几乎都是ARM架构的.如果so没有编译出比如X86平台的so,那么在X86架构上的手机就无法安装(虽然很少还是有的, 注意Androidstudio的模拟器为了性能提升采用X86的架构.所以很多的apk在这个模拟器上无法安装,除非这个apk没有使用so或者编译出了基于X86的是so.) 这也是为什么Genymotion采用虚拟机的原因了. 电脑的cpu架构都是X86的.直接运行ARM架构的apk将会非常慢,几乎用不了.
