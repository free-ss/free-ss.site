# free-ss.site
------
## 网站地址
### 主站
+ https://free-ss.site/
### 镜像站
+ https://free-ss.tw/
### 注意事项
+ 主站不更换，为永久地址，请尽量使用主站来访问。
+ 镜像站为临时地址，人工确认被墙后，会手动更换。
+ 所有站点都需要输入完整的地址 https:// + 域名，注意是 https:// ，不是 http://
------
## 使用方法
### V账号使用方法
1. [官网介绍](https://v2ray.com/)
2. Windows
    > 方法一：下载[核心程序](https://github.com/v2ray/v2ray-core/releases)，下载网站上的配置文件 config.json，覆盖到程序目录的同名文件，双击 v2ray.exe 运行。<p>
    > 方法二：下载[界面程序](https://github.com/2dust/v2rayN/releases)，双击 v2rayN.exe 运行，然后扫描网站上的二维码。
3. Android
    > 下载[安装程序](https://github.com/2dust/v2rayNG/releases)，运行后扫描网站上的二维码。
4. Linux
    > 下载[核心程序](https://github.com/v2ray/v2ray-core/releases)，下载网站提供的配置文件，命令行下运行 v2ray -config config.json
### S账号使用方法
1. [官网介绍](https://shadowsocks.org/)
2. Windows
    > 下载[安装程序](https://github.com/shadowsocks/shadowsocks-windows/releases)，运行后扫描网站上的二维码。
3. Android
    > 下载[安装程序](https://github.com/shadowsocks/shadowsocks-android/releases)， 运行后扫描网站上的二维码。
4. Linux
    > [安装、配置与运行](https://github.com/shadowsocks/shadowsocks-libev)
### 浏览器插件
    推荐使用 [SwitchyOmega](https://www.switchyomega.com/)
------
## 账号来源与特点
### V账号
1. 来源于网站， free-ss.site 保障其安全性
2. 每天早上8点钟自动更换UID
3. 已限制不能访问中国大陆的网站
4. 下载速度有一定的限制，月底流量耗尽将停止使用
### S账号
1. 来源于第三方，free-ss.site 不保障其安全性
2. 账号有效期不固定，free-ss.site 每5分钟检测其是否可用
3. 其他限制未知
------
## 问答
1. V/T/U/M 是什么意思？
    > V 表示美国 Vultr 检测点，T 表示中国电信(China Telecom)检测点，U 表示中国联通(China Unicom)检测点，M 表示中国移动(China Mobile)检测点。检测点分数越高越好，最高为10分。当分数降为0分时，网站将不显示该账号。↑ 表示分数正在上升，↓ 表示分数正在下降。
2. 为什么没有订阅地址？
    > 一、防止恶意使用：主要防止有人把订阅地址设置在路由器上，定期自动更换失效的账号从而实现24小时不间断下载。二、防止GFW订阅：如果有订阅，大家方便了，但GFW也能自动订阅自动封锁了。
3. 为什么没有SSR账号？
    > SSR各个协议与插件太多太混乱，检测程序兼容各个协议与插件需要耗费太多的资源，然而重要的是SSR目前却没有人继续维护了。SSR各个分支代码质量参差不齐，内存占用比shadowsocks-libev大了很多倍，而且不稳定。各个检测点若检测SSR账号，会影响其稳定性。
