仅供自定义插件的朋友使用！


2022-1-12更新配置文件,新增AX3600最新测试内核5.15，删除冲突及多余的插件

就算不精简插件云编译差不多才2小时左右完成所有的

全能插件版：
#OpenAppFilter
#IPv6
#简单mesh
#科学ssp（全组件）
#smartdns
#去广告plus—及—Adg广告拦截
#云音乐
#流控
#ttyd
#zerotier
#Turbo ACC
#访客网络
#openclash
#jd签到
#多拨&负载均衡#组播#等等！自行研究！
AX3600 拨号会重启与ipv6有冲突所以默认取消了。


适用于AX6和AX3600

本次config文件集成了基本上所有插件！

关于插件说明大家可参考恩山这个帖子 https://www.right.com.cn/forum/thread-344825-1-3.html 对照插件自定义删除config配置文件你们自己不需要的插件！

然后保存即可，编译出的固件就是你自定义想要的插件

驱动：默认NSS加速和sfe加速

主题：集成了所有主题，可对照config配置文件里主题随意删除！

脚本文件：目前1-2都是编辑添加，修改好的。

此次更新为Actions，自动拉取最新lede源码库，不需要任何修改，手动触发即可编译。

#SFE/NSS(on/off ecm)加速

#IPv6

#ttyd

#AdGuardhome

#酸酸乳plus（全组件）

#openclash小猫咪(与NSS冲突 二选一)

#全能推送

#上网时间控制

#动态DNS

#smartdns

#网络唤醒

#网易云解锁灰色歌曲

#KMS

#JD签到服务

#udpxy组播服务

#UPNP

#MWAN 3 分流助手

#IPSec VPN 服务器

#ZeroTier

#简单mesh

#QoS以及SQM QoS

#多线多拨

#负载均衡

#Turbo ACC 网络加速

#网络带宽监视器

enjoy

自定义环境变量与功能
详细信息
打开 work­flow 文件（.github/workflows/build-openwrt.yml），你会看到有如下一些环境变量，可按照自己的需求对这些变量进行定义。

env:
  REPO_URL: https://github.com/coolsnowwolf/lede
  REPO_BRANCH: master
  CONFIG_FILE: .config
  DIY_SH: diy.sh
  FREE_UP_DISK: false
  SSH_ACTIONS: false
  UPLOAD_BIN_DIR: false
  UPLOAD_FIRMWARE: true
  TZ: Asia/Shanghai
TIPS: 修改时需要注意:(冒号)后面有空格。
环境变量	功能
REPO_URL	源码仓库地址
REPO_BRANCH	源码分支
CONFIG_FILE	.config文件名
DIY_SH	DIY 脚本文件名
FREE_UP_DISK	释放磁盘空间。编译磁盘空间不足报错时使用。默认false
SSH_ACTIONS	SSH 连接 Actions 功能。默认false
UPLOAD_BIN_DIR	上传 bin 目录。即包含所有 ipk 文件和固件的目录。默认false
UPLOAD_FIRMWARE	上传固件目录。默认true
TZ	时区设置

