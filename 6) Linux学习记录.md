用VMware安装Ubuntu64位16.04后,想通过ssh访问.但是发现vm可以ping通主机,但是主机无法ping通vm.
<br>解决方法:打开主机的网络连接->VMnet8, 将VMnet8的ip段和网关改成vm里的网关一致即可.
