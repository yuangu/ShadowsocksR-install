# ShadowsocksR-install
## 一、SSR安装
#### 适用环境：  
  - 系统支持：CentOS，Debian，Ubuntu  
  - 内存要求：≥128M 

#### 默认配置：
  - 服务器端口：自己设定（如不设定，默认从 9000-19999 之间随机生成）
  - 密码：自己设定（如不设定，默认为 teddysun.com）
  - 加密方式：自己设定（如不设定，默认为 aes-256-cfb）
  - 协议（Protocol）：自己设定（如不设定，默认为 origin）
  - 混淆（obfs）：自己设定（如不设定，默认为 plain）
  
#### 使用方法：  
使用root用户登录，运行以下命令：  
```bash
wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocksR.sh
chmod +x shadowsocksR.sh
./shadowsocksR.sh 2>&1 | tee shadowsocksR.log
```
#### 卸载方法：   
使用 root 用户登录，运行以下命令：
```bash
./shadowsocksR.sh uninstall
```

#### 安装完成后即已后台启动 ShadowsocksR ，运行：
```bash
/etc/init.d/shadowsocks status
```

  可以查看 ShadowsocksR 进程是否已经启动。 
  本脚本安装完成后，已将 ShadowsocksR 自动加入开机自启动。

#### 使用命令：
  - 启动：/etc/init.d/shadowsocks start
  - 停止：/etc/init.d/shadowsocks stop
  - 重启：/etc/init.d/shadowsocks restart
  - 状态：/etc/init.d/shadowsocks status
  
#### 配置文件
  - 配置文件路径：/etc/shadowsocks.json
  - 日志文件路径：/var/log/shadowsocks.log
  - 代码安装目录：/usr/local/shadowsocks

## 二、网络加速安装
#### 使用方法：
使用root用户登录，运行以下命令：
```bash
wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh"
chmod +x tcp.sh
./tcp.sh
```
三选一，推荐锐速（请先安装内核）  
![](https://www.94ish.me/usr/uploads/2017/11/557206173.png)

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

## SSR 客户端
#### 功能介绍和使用方法
  - [大概是萌新也看得懂的SSR功能详细介绍&使用教程](https://lolico.moe/tutorial/shadowsocksr.html)
  
#### 客户端下载：
  - [Windows](https://github.com/shadowsocksrr/shadowsocksr-csharp/releases)
  - [OS X](https://github.com/shadowsocks/shadowsocks-iOS/wiki/Shadowsocks-for-OSX-Help)
  - [Linux](https://github.com/shadowsocks/shadowsocks-qt5)
  - [Android](https://github.com/shadowsocks/shadowsocks-android)
  - [iOS](https://github.com/shadowsocks/shadowsocks-iOS/wiki/Help)
  - [OpenWRT](https://github.com/shadowsocks/openwrt-shadowsocks)

## 参考资料
- [Shadowsocks非官方网站](https://shadowsocks.be/9.html)
- [Linux网络优化加速一键脚本](https://www.94ish.me/1635.html)
