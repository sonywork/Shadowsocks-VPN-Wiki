# Shadowsocks 配合 Proxifier 实现客户端代理

## 什么是 Proxifier

Proxifier 是一款功能非常强大的 socks5 客户端，可以让不支持通过代理服务器工作的网络程序能通过 HTTPS 或 SOCKS 代理或代理链。支持64位系统，支持XP，Vista，Win7，macOS, 支持socks4，socks5，http 代理协议，支持TCP，UDP 协议，可以指定端口，指定IP，指定域名,指定程序等运行模式，兼容性非常好，和SOCKSCAP 属于同类软件，不过SOCKSCAP 已经很久没更新了，不支持64位系统。有许多网络应用程序不支持通过代理服务器工作，Proxifier 解决了这些问题和所有限制，让您有机会不受任何限制使用你喜爱的软件。此外，它让你获得了额外的网络安全控制，创建代理隧道，并添加使用更多网络功能的权力。

## 使用方法

### Proxifier 下载

官网下载地址：[点击这里](http://www.proxifier.com/download.htm)

#### Windows 版本

软件分为 Standard Edition 和 Portable Edition 版本，请自行购买注册码

#### macOS 版本

请自行购买注册码

若系统为 10.11，请下载[Beta版 ](https://www.proxifier.com/distr/ProxifierMacBeta.zip)

若 Yosemite 下 Proxifier 不能运行，打开 终端 应用，运行下面的命令然后重启

```
sudo nvram boot-args="kext-dev-mode=1"
```

#### 详细使用方法：

因为 Windows 和 macOS 的使用方式是一样的，这里就只演示 macOS 下的使用方法

首先点击 `proxies` > `add`

在其中填写 `socks5` 的代理地址 `127.0.0.1:1080` 请确保与图中一致

![](https://ooo.0o0.ooo/2015/11/30/565c75c39e2fa.jpg)
![](https://ooo.0o0.ooo/2015/11/30/565c78968c9e6.jpg)

接下来填写代理规则

![](https://ooo.0o0.ooo/2015/11/30/565c75ed71e81.jpg)

中最重要的就是请将 Shadowsocks 客户端设置为全局模式

如图，点击*+* 添加 APP，再在 `Action` 中选择 `Direct`

![](https://ooo.0o0.ooo/2015/11/30/565c768b83f1d.jpg)

此时就可以添加其他 APP 了，比如让 Steam 和 CS:GO 走 Shadowsocks 以降低延迟，那么如图：

![](https://ooo.0o0.ooo/2015/11/30/565c75451538a.jpg)

确保选择的是走 `socks5` 就可以了
