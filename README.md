> beta.gs

一键 DD 脚本，支持性好，更智能更全面，支持国内外各种 VPS 重装，特别是对国内各种访问国外资源慢的 VPS 安装有奇效。

* * *

更新说明：  
20230313: 新增强制 CN 模式，Using CN Mode 选择 Y 将默认为国内主机安装，国外主机请选择 N  
20220724：更新及增加大量系统镜像，41 合 1 脚本，请注意看说明。  
20220703：新增自定义 SSH 端口（9-16）  
20220613：新版自定义密码支持特殊字符.!$@#&%  
20220428：修复 MoeClub 新版 DD 过程中卡住的 BUG，修复 Centos7 下出现 Error! Not Found grub. 的错误提示，新增支持 xz 压缩格式的 DD 系统镜像包。  
20220406：CN 系统镜像已失效，国内主机使用一键脚本 1-25 选项需要较长时间，推荐使用 99 的自定义系统镜像。  
20211120：更新 MoeClub 新版, 依赖更少, 支持原版自定义密码安装, 体验版可能有 Bug.  
20210909：支持 debian11.  
20210511：发现很多人不知道怎么 DD 甲骨文, 使用支持 uefi 的镜像包即可, ARM 机器选择带 ARM 镜像.  
20210509：更新部分 windows 镜像, 修正一处小问题.  
20210127：更换部分 windows 镜像.  
20210109：更新支持 Ubuntu20.04 安装, 更新几个 windows 镜像.  
20200708：更新自动为 CN 主机使用国内镜像源.

* * *

安装重装系统的前提组件:  
Debian/Ubuntu:

```
apt-get install -y xz-utils openssl gawk file wget screen && screen -S os
```

RedHat/CentOS:

```
yum install -y xz openssl gawk file glibc-common wget screen && screen -S os
```

如果出现异常，请刷新 Mirrors 缓存或更换镜像源。  
RedHat/CentOS:

```
yum makecache && yum update -y
```

Debian/Ubuntu:

```
apt update -y && apt dist-upgrade -y
```

使用:

```
wget --no-check-certificate -O NewReinstall.sh https://raw.githubusercontent.com/fcurrk/reinstall/master/NewReinstall.sh && chmod a+x NewReinstall.sh && bash NewReinstall.sh
```

如为 CN 主机 (部分主机商已不能使用)，可能出现报错或不能下载脚本的问题，可执行以下命令开始安装.

```
wget --no-check-certificate -O NewReinstall.sh https://cdn.jsdelivr.net/gh/fcurrk/reinstall@master/NewReinstall.sh && chmod a+x NewReinstall.sh && bash NewReinstall.sh
```

点击使用[旧版脚本](https://git.beta.gs/index.php/8.html)

  

![](https://git.beta.gs/usr/uploads/2022/07/366941637.png)  
输入 Y 确认 DD 后主机自动获取 IP，N 则自行设置 IP 输入 N 后会自动检测出主机现用 IP，如果正确可以按 Y 确认使用，如不正确则按 N 自行按正确的输入。  
![](https://git.beta.gs/usr/uploads/2022/07/1245303289.png)  
41 合 1 的系统一键 DD 选择界面，输入 99 则使用自定义镜像。 以上系统密码不为默认密码的均为网络收集，如有疑虑使用自己的自定义镜像。

41 合一系统密码：  
1、CentOS 7.7 (已关闭防火墙及 SELinux，默认密码 Pwd@CentOS)  
2、CentOS 7 (默认密码 cxthhhhh.com)  
3、CentOS 7 (支持 ARM64、UEFI，默认密码 cxthhhhh.com)  
4、CentOS 8 (默认密码 cxthhhhh.com)  
5、Rocky 8 (默认密码 cxthhhhh.com)  
6、Rocky 8 (支持 UEFI，默认密码 cxthhhhh.com)  
7、Rocky 8 (支持 ARM64、UEFI，默认密码 cxthhhhh.com)  
8、CentOS 9 (默认密码 cxthhhhh.com)  
9、CentOS 6 (官方源原版，默认密码 Minijer.com)  
10、Debian 11 (官方源原版，默认密码 Minijer.com)  
11、Debian 10 (官方源原版，默认密码 Minijer.com)  
12、Debian 9 (官方源原版，默认密码 Minijer.com)  
13、Debian 8 (官方源原版，默认密码 Minijer.com)  
14、Ubuntu 20.04 (官方源原版，默认密码 Minijer.com)  
15、Ubuntu 18.04 (官方源原版，默认密码 Minijer.com)  
16、Ubuntu 16.04 (官方源原版，默认密码 Minijer.com)  
17、Windows Server 2022 (默认密码 cxthhhhh.com)  
18、Windows Server 2022 (支持 UEFI，默认密码 cxthhhhh.com)  
19、Windows Server 2019 (默认密码 cxthhhhh.com)  
20、Windows Server 2016 (默认密码 cxthhhhh.com)  
21、Windows Server 2012 (默认密码 cxthhhhh.com)  
22、Windows Server 2008 (默认密码 cxthhhhh.com)  
23、Windows Server 2003 (默认密码 cxthhhhh.com)  
24、Windows 10 LTSC (默认密码 Teddysun.com)  
25、Windows 10 LTSC (支持 UEFI，默认密码 Teddysun.com)  
26、Windows 7 x86 Lite (默认密码 nat.ee)  
27、Windows 7 x86 Lite (阿里云专用，默认密码 nat.ee)  
28、Windows 7 x64 Lite (默认密码 nat.ee)  
29、Windows 7 x64 Lite (支持 UEFI，默认密码 nat.ee)  
30、Windows 10 LTSC Lite (默认密码 nat.ee)  
31、Windows 10 LTSC Lite (阿里云专用，默认密码 nat.ee)  
32、Windows 10 LTSC Lite (支持 UEFI，默认密码 nat.ee)  
33、Windows Server 2003 Lite (C 盘默认 10G，默认密码 WinSrv2003x86-Chinese)  
34、Windows Server 2008 Lite (默认密码 nat.ee)  
35、Windows Server 2008 Lite (支持 UEFI，默认密码 nat.ee)  
36、Windows Server 2012 Lite (默认密码 nat.ee)  
37、Windows Server 2012 Lite (支持 UEFI，默认密码 nat.ee)  
38、Windows Server 2016 Lite (默认密码 nat.ee)  
39、Windows Server 2016 Lite (支持 UEFI，默认密码 nat.ee)  
40、Windows Server 2022 Lite (默认密码 nat.ee)  
41、Windows Server 2022 Lite (支持 UEFI，默认密码 nat.ee)  
99、自定义镜像

* * *

注意：
---

### 系统名称后带 Lite 的均为精简版，没有的是完整版.

### [X64-Legacy-cxthhhhh] 代表系统为 AMD64 位，支持传统 BIOS 启动，cxthhhhh 定制的系统镜像.

### ARM64 代表系统支持 ARM64 位

### UEFI 代表系统支持最新的 UEFI 启动，如甲骨文全部都是这种

### aliyun 代表阿里云专用系统镜像

### cxthhhhh、teddysun、nat.ee 均为三位制作系统镜像的大佬代称

### 系统密码会在选择相应序号后提示，请注意记录。

经测试在谷歌云原版系统基础上 DD 会出现自动获取的子网掩码为 255.255.255.255, 如出现这种情况需要手工输入改正为正确的如 255.255.255.0, 否则会安装完成主机可能会离线。

阿里云因使用了特殊的驱动，DD 安装 Windows 系统选择阿里云专用版。

Oracle Cloud（甲骨文云）可选择支持 UEFI 的镜像，注意基础系统最好选择 Ubuntu，如原系统是 CentOS 可能无法成功，注意如是 ARM 机器注意选择同时支持 ARM64 和 UEFI 的镜像。

9-16 项安装原版系统，可自定义密码，密码要求 8-16 位，以英文字母或数字开头，可以是大小写英文字母、数字及 7 个特殊字符.!$@#&% 的任意组合。

报错 Error! grub.cfg. 解决办法

```
mkdir /boot/grub2 && grub-mkconfig -o /boot/grub2/grub.cfg
```

特别感谢：Vicer、cxt、hiCasper 等各位技术大佬的脚本，站长只是脚本的 "搬运工"。

版权申明：以上所有脚本、系统均为网络收集，站长不对资源的安全及版权纠纷负责，如有侵犯您的权益欢迎联系。  
[站长邮箱：minijer#beta.gs(# 换成 @)](mailto:minijer@beta.gs)
