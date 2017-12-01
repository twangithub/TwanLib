1. android 经典的root权限漏洞监测工具 https://labs.duo.com/xray/
2. apktool 官网 https://ibotpeaches.github.io/Apktool/
>> 利用apktool Decoding 反编译为Smali 语言:<br>
   apktool d demo.apk -o demo<br>
   d 表示decode ,反编译，与之对应的是building,编译。<br>
   eg: apktool d E:\smali\app-release.apk [-o E:\smali\demo]<br>
   demo.apk 是要反编译的目标apk, -o 表示输出地址 ，如果没有 -o 参数，默认在当前文件夹。<br>
   
- 破解一个so文件步骤.
1.apktool d demo.apk -o E:\test<br>
2.利用ida , urltaedit 等修改so<br>
3.apktool b e:\test<br>
4.利用android逆向助手将dist目录的apk签名<br>
