# luci-app-socat

Web UI AT-commands using socat for OpenWrt.

![GitHub release (latest by date)](https://img.shields.io/github/v/release/4IceG/luci-app-socat?style=flat-square)
![GitHub stars](https://img.shields.io/github/stars/4IceG/luci-app-socat?style=flat-square)
![GitHub forks](https://img.shields.io/github/forks/4IceG/luci-app-socat?style=flat-square)
![GitHub All Releases](https://img.shields.io/github/downloads/4IceG/luci-app-socat/total)


需要用到socat命令和atinout命令
兼容2个命令。

优先使用atinout命令，如果找不到，则使用socat命令。
（PS：atinout的速度，比socat快）

举例：
root@GL-MT3000:/usr/bin# echo -ne "ati\n" | /usr/bin/atinout - /dev/ttyUSB0 -
ati
Quectel
EC200D
Revision: EC200DCNLAR02A01M64

OK
root@GL-MT3000:/usr/bin# echo -ne "ati\n" | socat - /dev/ttyUSB0,,crnl
ati
Quectel
EC200D
Revision: EC200DCNLAR02A01M64

OK
