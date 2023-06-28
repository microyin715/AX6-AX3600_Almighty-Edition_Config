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

### 自定义环境变量与功能

<details open="" style="box-sizing: border-box; display: block; color: rgba(0, 0, 0, 0.86); font-family: &quot;Droid Serif&quot;, -apple-system, system-ui, sans-serif; font-size: 18px; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: justify; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(255, 255, 255); text-decoration-style: initial; text-decoration-color: initial;"><div id="details-content"><p style="box-sizing: border-box; margin: 0.92em 0px;">打开 work­flow 文件（<code style="box-sizing: border-box; font-family: Menlo, Monaco, Consolas, &quot;Courier New&quot;, monospace; font-size: 1em; background: rgb(235, 237, 237); padding: 0px 3px; border-radius: 3px;">.github/workflows/build-openwrt.yml</code>），你会看到有如下一些环境变量，可按照自己的需求对这些变量进行定义。</p><pre class=" language-none line-numbers" style="box-sizing: border-box; font-family: Menlo, Monaco, Consolas, &quot;Courier New&quot;, monospace; font-size: 0.96em; position: relative; width: 820px; overflow: hidden; line-height: 1.5; border: 1px solid rgba(0, 0, 0, 0.05); border-radius: 5px; background: rgb(241, 243, 243); text-align: left; white-space: pre; word-spacing: normal; word-break: normal; overflow-wrap: normal; tab-size: 4; hyphens: none; counter-reset: linenumber 0;"><code class=" language-none" style="box-sizing: border-box; font-family: Menlo, Monaco, Consolas, &quot;Courier New&quot;, monospace; font-size: 1em; background: 0px 0px !important; padding: 10px 10px 10px calc(3em + 10px); border-radius: 3px; text-align: left; white-space: inherit; word-spacing: normal; word-break: normal; overflow-wrap: normal; tab-size: 4; hyphens: none; display: block; overflow: auto;">env:
  REPO_URL: https://github.com/coolsnowwolf/lede
  REPO_BRANCH: master
  CONFIG_FILE: .config
  DIY_SH: diy.sh
  FREE_UP_DISK: false
  SSH_ACTIONS: false
  UPLOAD_BIN_DIR: false
  UPLOAD_FIRMWARE: true
  TZ: Asia/Shanghai</code><span aria-hidden="true" class="line-numbers-rows" style="box-sizing: border-box; position: absolute; pointer-events: none; top: 10px; font-size: 17.28px; left: 0px; width: 3em; letter-spacing: -1px; border-right: 1px solid rgba(153, 153, 153, 0.2); user-select: none; background: rgb(241, 243, 243);"><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span><span style="box-sizing: border-box; pointer-events: none; display: block; counter-increment: linenumber 1;"></span></span></pre><blockquote style="box-sizing: border-box; margin: 0.92em 0px; border-width: 4px; border-left-style: solid; border-left-color: rgb(218, 218, 218); padding-left: 12px; color: rgba(0, 0, 0, 0.6);"><strong style="box-sizing: border-box; font-weight: 700; color: rgba(0, 0, 0, 0.98);">TIPS:</strong><span>&nbsp;</span>修改时需要注意<code style="box-sizing: border-box; font-family: Menlo, Monaco, Consolas, &quot;Courier New&quot;, monospace; font-size: 1em; background: rgb(235, 237, 237); padding: 0px 3px; border-radius: 3px;">:</code>(冒号)后面有空格。</blockquote><table style="box-sizing: border-box; width: 820px; max-width: 100%; border-collapse: collapse; border-spacing: 0px; margin-bottom: 1.5em; font-size: 0.96em;"><thead style="box-sizing: border-box; background-color: rgb(239, 239, 238);"><tr style="box-sizing: border-box;"><th style="box-sizing: border-box; text-align: left; padding: 4px 8px 4px 10px; border: 1px solid rgb(218, 218, 218);">环境变量</th><th style="box-sizing: border-box; text-align: left; padding: 4px 8px 4px 10px; border: 1px solid rgb(218, 218, 218);">功能</th></tr></thead><tbody style="box-sizing: border-box;"><tr style="box-sizing: border-box;"><td style="box-sizing: border-box; text-align: left; padding: 4px 8px 4px 10px; border: 1px solid rgb(218, 218, 218); vertical-align: top;"><code style="box-sizing: border-box; font-family: Menlo, Monaco, Consolas, &quot;Courier New&quot;, monospace; font-size: 1em; background: rgb(235, 237, 237); padding: 0px 3px; border-radius: 3px;">REPO_URL</code></td><td style="box-sizing: border-box; text-align: left; padding: 4px 8px 4px 10px; border: 1px solid rgb(218, 218, 218); vertical-align: top;">源码仓库地址</td></tr><tr style="box-sizing: border-box; background-color: rgb(239, 239, 238);"><td style="box-sizing: border-box; text-align: left; padding: 4px 8px 4px 10px; border: 1px solid rgb(218, 218, 218); vertical-align: top;"><code style="box-sizing: border-box; font-family: Menlo, Monaco, Consolas, &quot;Courier New&quot;, monospace; font-size: 1em; background: rgb(235, 237, 237); padding: 0px 3px; border-radius: 3px;">REPO_BRANCH</code></td><td style="box-sizing: border-box; text-align: left; padding: 4px 8px 4px 10px; border: 1px solid rgb(218, 218, 218); vertical-align: top;">源码分支</td></tr><tr style="box-sizing: border-box;"><td style="box-sizing: border-box; text-align: left; padding: 4px 8px 4px 10px; border: 1px solid rgb(218, 218, 218); vertical-align: top;"><code style="box-sizing: border-box; font-family: Menlo, Monaco, Consolas, &quot;Courier New&quot;, monospace; font-size: 1em; background: rgb(235, 237, 237); padding: 0px 3px; border-radius: 3px;">CONFIG_FILE</code></td><td style="box-sizing: border-box; text-align: left; padding: 4px 8px 4px 10px; border: 1px solid rgb(218, 218, 218); vertical-align: top;"><code style="box-sizing: border-box; font-family: Menlo, Monaco, Consolas, &quot;Courier New&quot;, monospace; font-size: 1em; background: rgb(235, 237, 237); padding: 0px 3px; border-radius: 3px;">.config</code>文件名</td></tr><tr style="box-sizing: border-box; background-color: rgb(239, 239, 238);"><td style="box-sizing: border-box; text-align: left; padding: 4px 8px 4px 10px; border: 1px solid rgb(218, 218, 218); vertical-align: top;"><code style="box-sizing: border-box; font-family: Menlo, Monaco, Consolas, &quot;Courier New&quot;, monospace; font-size: 1em; background: rgb(235, 237, 237); padding: 0px 3px; border-radius: 3px;">DIY_SH</code></td><td style="box-sizing: border-box; text-align: left; padding: 4px 8px 4px 10px; border: 1px solid rgb(218, 218, 218); vertical-align: top;">DIY 脚本文件名</td></tr><tr style="box-sizing: border-box;"><td style="box-sizing: border-box; text-align: left; padding: 4px 8px 4px 10px; border: 1px solid rgb(218, 218, 218); vertical-align: top;"><code style="box-sizing: border-box; font-family: Menlo, Monaco, Consolas, &quot;Courier New&quot;, monospace; font-size: 1em; background: rgb(235, 237, 237); padding: 0px 3px; border-radius: 3px;">FREE_UP_DISK</code></td><td style="box-sizing: border-box; text-align: left; padding: 4px 8px 4px 10px; border: 1px solid rgb(218, 218, 218); vertical-align: top;">释放磁盘空间。编译磁盘空间不足报错时使用。默认<code style="box-sizing: border-box; font-family: Menlo, Monaco, Consolas, &quot;Courier New&quot;, monospace; font-size: 1em; background: rgb(235, 237, 237); padding: 0px 3px; border-radius: 3px;">false</code></td></tr><tr style="box-sizing: border-box; background-color: rgb(239, 239, 238);"><td style="box-sizing: border-box; text-align: left; padding: 4px 8px 4px 10px; border: 1px solid rgb(218, 218, 218); vertical-align: top;"><code style="box-sizing: border-box; font-family: Menlo, Monaco, Consolas, &quot;Courier New&quot;, monospace; font-size: 1em; background: rgb(235, 237, 237); padding: 0px 3px; border-radius: 3px;">SSH_ACTIONS</code></td><td style="box-sizing: border-box; text-align: left; padding: 4px 8px 4px 10px; border: 1px solid rgb(218, 218, 218); vertical-align: top;">SSH 连接 Actions 功能。默认<code style="box-sizing: border-box; font-family: Menlo, Monaco, Consolas, &quot;Courier New&quot;, monospace; font-size: 1em; background: rgb(235, 237, 237); padding: 0px 3px; border-radius: 3px;">false</code></td></tr><tr style="box-sizing: border-box;"><td style="box-sizing: border-box; text-align: left; padding: 4px 8px 4px 10px; border: 1px solid rgb(218, 218, 218); vertical-align: top;"><code style="box-sizing: border-box; font-family: Menlo, Monaco, Consolas, &quot;Courier New&quot;, monospace; font-size: 1em; background: rgb(235, 237, 237); padding: 0px 3px; border-radius: 3px;">UPLOAD_BIN_DIR</code></td><td style="box-sizing: border-box; text-align: left; padding: 4px 8px 4px 10px; border: 1px solid rgb(218, 218, 218); vertical-align: top;">上传 bin 目录。即包含所有 ipk 文件和固件的目录。默认<code style="box-sizing: border-box; font-family: Menlo, Monaco, Consolas, &quot;Courier New&quot;, monospace; font-size: 1em; background: rgb(235, 237, 237); padding: 0px 3px; border-radius: 3px;">false</code></td></tr><tr style="box-sizing: border-box; background-color: rgb(239, 239, 238);"><td style="box-sizing: border-box; text-align: left; padding: 4px 8px 4px 10px; border: 1px solid rgb(218, 218, 218); vertical-align: top;"><code style="box-sizing: border-box; font-family: Menlo, Monaco, Consolas, &quot;Courier New&quot;, monospace; font-size: 1em; background: rgb(235, 237, 237); padding: 0px 3px; border-radius: 3px;">UPLOAD_FIRMWARE</code></td><td style="box-sizing: border-box; text-align: left; padding: 4px 8px 4px 10px; border: 1px solid rgb(218, 218, 218); vertical-align: top;">上传固件目录。默认<code style="box-sizing: border-box; font-family: Menlo, Monaco, Consolas, &quot;Courier New&quot;, monospace; font-size: 1em; background: rgb(235, 237, 237); padding: 0px 3px; border-radius: 3px;">true</code></td></tr><tr style="box-sizing: border-box;"><td style="box-sizing: border-box; text-align: left; padding: 4px 8px 4px 10px; border: 1px solid rgb(218, 218, 218); vertical-align: top;"><code style="box-sizing: border-box; font-family: Menlo, Monaco, Consolas, &quot;Courier New&quot;, monospace; font-size: 1em; background: rgb(235, 237, 237); padding: 0px 3px; border-radius: 3px;">TZ</code></td><td style="box-sizing: border-box; text-align: left; padding: 4px 8px 4px 10px; border: 1px solid rgb(218, 218, 218); vertical-align: top;">时区设置</td></tr></tbody></table><p style="box-sizing: border-box; margin: 0.92em 0px;"></p></div></details>

