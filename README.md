* [ShadowsocksR\-install](#shadowsocksr-install)
  * [一、SSR安装](#%E4%B8%80ssr%E5%AE%89%E8%A3%85)
      * [适用环境：](#%E9%80%82%E7%94%A8%E7%8E%AF%E5%A2%83)
      * [默认配置：](#%E9%BB%98%E8%AE%A4%E9%85%8D%E7%BD%AE)
      * [使用方法：](#%E4%BD%BF%E7%94%A8%E6%96%B9%E6%B3%95)
      * [卸载方法：](#%E5%8D%B8%E8%BD%BD%E6%96%B9%E6%B3%95)
      * [状态查看：](#%E7%8A%B6%E6%80%81%E6%9F%A5%E7%9C%8B)
      * [使用命令：](#%E4%BD%BF%E7%94%A8%E5%91%BD%E4%BB%A4)
      * [配置文件：](#%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6)
  * [二、网络加速安装](#%E4%BA%8C%E7%BD%91%E7%BB%9C%E5%8A%A0%E9%80%9F%E5%AE%89%E8%A3%85)
      * [使用方法：](#%E4%BD%BF%E7%94%A8%E6%96%B9%E6%B3%95-1)
  * [三、SSR 客户端](#%E4%B8%89ssr-%E5%AE%A2%E6%88%B7%E7%AB%AF)
      * [功能介绍和使用方法：](#%E5%8A%9F%E8%83%BD%E4%BB%8B%E7%BB%8D%E5%92%8C%E4%BD%BF%E7%94%A8%E6%96%B9%E6%B3%95)
      * [客户端下载：](#%E5%AE%A2%E6%88%B7%E7%AB%AF%E4%B8%8B%E8%BD%BD)
  * [四、参考资料](#%E5%9B%9B%E5%8F%82%E8%80%83%E8%B5%84%E6%96%99)
  
# ShadowsocksR-install
## 一、SSR安装
#### 适用环境：  
  - 系统支持：CentOS6+ / Debian6+ / Ubuntu14+
  - 内存要求：≥128M 
  - KVM

#### 默认配置：
  - 服务器端口：默认或自己设定
  - 密码：默认或自己设定
  - 加密方式：建议 aes-256-cfb
  - 协议（Protocol）：建议 origin
  - 混淆（obfs）：建议 plain
  
#### 使用方法：  
#### 脚本1(推荐)：
使用root用户登录，运行以下命令：  
```bash
wget -N --no-check-certificate https://raw.githubusercontent.com/ToyoDAdoubi/doubi/master/ssr.sh
chmod +x ssr.sh 
bash ssr.sh
```
#### 脚本2：  
使用root用户登录，运行以下命令：  
```bash
wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocksR.sh
chmod +x shadowsocksR.sh
./shadowsocksR.sh 2>&1 | tee shadowsocksR.log
```
###### 卸载方法：   
使用 root 用户登录，运行以下命令：
```bash
./shadowsocksR.sh uninstall
```

###### 状态查看：
安装完成后即已后台启动 ShadowsocksR ，运行：
```bash
/etc/init.d/shadowsocks status
```
可以查看 ShadowsocksR 进程是否已经启动。 
本脚本安装完成后，已将 ShadowsocksR 自动加入开机自启动。

###### 使用命令：
  - 启动：/etc/init.d/shadowsocks start
  - 停止：/etc/init.d/shadowsocks stop
  - 重启：/etc/init.d/shadowsocks restart
  - 状态：/etc/init.d/shadowsocks status
  
###### 配置文件：
  - 配置文件路径：/etc/shadowsocks.json
  - 日志文件路径：/var/log/shadowsocks.log
  - 代码安装目录：/usr/local/shadowsocks

## 二、网络加速安装
#### 使用方法：
使用root用户登录，运行以下命令：
```bash
wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh"
chmod +x tcp.sh
tcp.sh
```
三选一，推荐锐速或BBRplus（请先安装内核）  
![](https://s1.ax1x.com/2018/12/24/F6XveP.png)

安装完成后，脚本提示如下：
```bash
Congratulations, ShadowsocksR server install completed!
Your Server IP        :your_server_ip
Your Server Port      :your_server_port
Your Password         :your_password
Your Protocol         :your_protocol
Your obfs             :your_obfs
Your Encryption Method:your_encryption_method

Welcome to visit:https://shadowsocks.be/9.html
Enjoy it!
````

## 三、SSR 客户端
#### 功能介绍和使用方法：
  - [大概是萌新也看得懂的SSR功能详细介绍&使用教程](https://lolico.moe/tutorial/shadowsocksr.html)
  
#### 客户端下载：
  - [Windows](https://github.com/shadowsocksrr/shadowsocksr-csharp/releases)
  - [OS X](https://github.com/shadowsocks/shadowsocks-iOS/wiki/Shadowsocks-for-OSX-Help)
  - [Linux](https://github.com/shadowsocks/shadowsocks-qt5)
  - [Android](https://github.com/shadowsocks/shadowsocks-android)
  - [iOS](https://github.com/shadowsocks/shadowsocks-iOS/wiki/Help)
  - [OpenWRT](https://github.com/shadowsocks/openwrt-shadowsocks)

## 四、参考资料
- [Shadowsocks非官方网站](https://shadowsocks.be/9.html)
- [Linux网络优化加速一键脚本](https://www.94ish.me/1635.html)
