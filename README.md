# free-ss.site
------
## 网站地址
### 主站
+ https://free-ss.site/
+ 直连主站的设置方法：https://free-ss.site/v/direct_access.png
### 注意事项
+ 禁止使用免费账号进行黑客攻击，BT下载，滥发垃圾邮件。这些账号来之不易，请珍惜使用。
+ 主站不更换，为永久地址，请尽量使用主站来访问。
+ 镜像站为临时地址，人工确认被墙后，会手动更换。
------
## 使用方法
### V账号使用方法
1. [V2Ray介绍](https://v2ray.com/)
2. Windows系统使用方法
    > 方法一：下载[核心程序](https://github.com/v2ray/v2ray-core/releases) v2ray-windows-64.zip 或 v2ray-windows-32.zip，下载网站上的配置文件 config.json，覆盖到程序目录的同名文件，双击 v2ray.exe 运行。<p>
    > 方法二：下载[界面程序](https://github.com/2dust/v2rayN/releases) v2rayN-Core.zip，双击 v2rayN.exe 运行，然后扫描网站上的二维码。
3. Android系统使用方法
    > 下载[安装程序](https://github.com/2dust/v2rayNG/releases) app-universal-release.apk，运行后扫描网站上的二维码。
4. Linux系统使用方法
    > 下载[核心程序](https://github.com/v2ray/v2ray-core/releases) v2ray-linux-64.zip 或 v2ray-linux-32.zip，下载网站提供的配置文件 config.json，覆盖到程序目录的同名文件，同目录下用命令行下运行 ./v2ray -config config.json
### S账号使用方法
1. [Shadowsocks介绍](https://shadowsocks.org/)
2. Windows系统使用方法
    > 下载[安装程序](https://github.com/shadowsocks/shadowsocks-windows/releases) Shadowsocks-x.x.x.zip，运行后扫描网站上的二维码。
3. Android系统使用方法
    > 下载[安装程序](https://github.com/shadowsocks/shadowsocks-android/releases) shadowsocks--universal-x.x.x.apk，运行后扫描网站上的二维码。
4. Linux系统使用方法
    > 参考[说明文档](https://github.com/shadowsocks/shadowsocks-libev) 进行安装、配置与运行
### 浏览器插件
    > 推荐使用[SwitchyOmega](https://proxy-switchyomega.com/)
------
## 账号来源与特点
### V账号
1. 来源于网站， free-ss.site 保障其隐私性和安全性
2. 每天8点或20点自动更换UID
3. 已限制不能访问中国大陆的网站
4. 下载速度有一定的限制，月底若流量耗尽将停止使用
### S账号
1. 来源于第三方，free-ss.site 不保障其隐私性和安全性
2. 账号有效期不固定，free-ss.site 每5分钟检测其是否可用
3. 其他限制未知
------
## 问答
1. V/T/U/M 是什么意思？
    > V 表示美国 Vultr 检测点，T 表示中国电信(China Telecom)检测点，U 表示中国联通(China Unicom)检测点，M 表示中国移动(China Mobile)检测点。检测点分数越高越好，最高为10分。当分数降为0分时，网站将不显示该账号。↑ 表示分数正在上升，↓ 表示分数正在下降。
    > 注意，这些分数仅表示各账号在过去一小时内的可用性，并不能反应各个账号的速度以及延迟。也就是说，分数最高的账号不一定是速度最快的，而是最近一小时内表现最稳定的。分数值降低的可能原因有：账号失效、服务器繁忙暂停响应、检测点线路丢包等等。
    > 当观察到VTUM分数全都在下降，而且最后检测可用的时间大于10分钟，说明这个账号已经失效了。当观察到V分数在上升，TUM分数都在下降，说明这个账号已经被墙了。
2. 为什么没有订阅地址？
    > 一、防止恶意使用：主要防止有人把订阅地址设置在路由器上，定期自动更换失效的账号从而实现24小时不间断下载。二、防止GFW订阅：如果有订阅，大家方便了，但GFW也能自动订阅自动封锁了。
3. 为什么没有SSR账号？
    > SSR各个协议与插件太多太混乱，检测程序兼容各个协议与插件需要耗费太多的资源，然而重要的是SSR目前却没有人继续维护了。SSR各个分支代码质量参差不齐，内存占用比shadowsocks-libev大了很多倍，而且不稳定。各个检测点若检测SSR账号，会影响其稳定性。
------
## 技术细节
+ 主要有四部分：网站、爬虫、检测、扫描。
### 网站
1. VPS 使用 Vultr 美国新泽西节点。
2. CDN 使用 Cloudflare 的节点进行加速。
3. 操作系统使用 Archlinux。
4. 运行环境为 Apache, PHP, MariaDB。
5. 部署了简单的反爬技术，主要用于防止恶意使用和自动订阅。
6. 使用了站库分离与页面静态化技术，主要用于防止CC攻击。
### 爬虫
1. 每天自动爬取V账号的节点中的UID。
2. S账号来源广泛，为了防止恶意使用，暂不公布爬取细节。
### 检测
1. V账号比较稳定，不需要设置检测点。所有检测点仅检测S账号。
2. Vultr检测点线路干扰比较小，使用 shadowsocks-libev 进行真实的发包检测。主要检测账号是否存活。
3. 电信联通移动检测点线路干扰比较大，使用建立 socket 连接的方式来检测TCP端口，不发送真实的Shadowsocks封包。主要检测账号是否被墙，以及各运营商的线路情况。（存活与被墙是两个不同的概念，仔细想想它们的区别）
4. [检测程序细节](https://github.com/free-ss/free-ss.site/blob/master/%E6%A3%80%E6%B5%8B%E7%A8%8B%E5%BA%8F%E4%BB%8B%E7%BB%8D.md)
### 扫描
1. 有些节点根本不是爬虫爬取而来的，而是根据一定的规则直接扫描出来的。这个属于 free-ss.site 的黑科技，暂不公布具体细节。
