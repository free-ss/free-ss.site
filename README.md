# free-ss.site
------
## 网站地址
### 主站
+ https://free-ss.site/
### 注意事项
+ 禁止使用免费账号进行黑客攻击，BT下载，滥发垃圾邮件。这些账号来之不易，请珍惜使用。
+ 主站不更换，为永久地址，请尽量使用主站来访问。
+ 镜像站已关闭，太累没有时间管了。
------
## 使用方法
### V账号使用方法
1. [V2fly介绍](https://www.v2fly.org/)
2. [工具下载](https://www.v2fly.org/awesome/tools.html)
3. 通过导入剪切板或扫描二维码的方式，导入账号
------
## 账号来源与特点
### V账号
1. 来源于网站， free-ss.site 保障其隐私性和安全性
2. 每天8点或20点自动更换UID
3. 已限制不能访问中国大陆的网站
4. 下载速度有一定的限制，月底若流量耗尽将停止使用
### S账号
1. 虽然后台有黑科技，扫描出一大堆S账号，但公布后存活期太短，感觉没必要公布出来了。
------
## 技术细节
+ 主要有四部分：网站、爬虫、检测、扫描。
### 网站
1. VPS 使用 Vultr 美国新泽西节点。
2. CDN 使用 Cloudflare 的节点进行加速。
3. 操作系统使用 Archlinux。
4. 运行环境为 Nginx, PHP。
5. 部署了简单的反爬技术，主要用于防止恶意使用。
### 爬虫
1. 每天自动爬取V账号的节点中的UID。
2. S账号来源广泛，为了防止恶意使用，暂不公布爬取细节。
### 检测
1. V账号比较稳定，不需要设置检测点。所有检测点仅检测S账号。
### 扫描
1. 有些节点根本不是爬虫爬取而来的，而是根据一定的规则直接扫描出来的。这个属于 free-ss.site 的黑科技，暂不公布具体细节。
