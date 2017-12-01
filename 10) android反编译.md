1. android 经典的root权限漏洞监测工具 https://labs.duo.com/xray/
2. apktool 官网 https://ibotpeaches.github.io/Apktool/
>> 利用apktool Decoding 反编译为Smali 语言:<br>
   apktool d demo.apk -o demo<br>
   d 表示decode ,反编译，与之对应的是building,编译。<br>
   eg: apktool d E:\smali\app-release.apk -o E:\smali\1.apk<br>
   demo.apk 是要反编译的目标apk, -o 表示输出地址 ，如果没有 -o 参数，默认在当前文件夹。<br>
