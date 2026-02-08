## 一.VPN简介

        虚拟专用网络（英文：Virtual Private Network），简称虚拟专网（VPN），其主要功能是在公用网络上建立专用网络，进行加密通讯。在企业网络中有广泛应用。VPN网关通过对数据包的加密和数据包目标地址的转换实现远程访问。VPN可通过服务器、硬件、软件等多种方式实现。

        简单来讲就是国外有些神奇的资源在国内是不允许访问的，只有搭个梯子跑到国外才能被访问，所以VPN也被称为梯子，机场，科学上网，安全访问👻

## 二.搭建

以下我提供的解决方式，不想自己搭建的话，你也可以去专业的机场网站儿上面购买。

1、首先你需要注册一个免费的 Cloudflare 账号。

[](https://dash.cloudflare.com/sign-up)

2、接着你需要准备好开源软件。

V2rayN

[GitHub - 2dust/v2rayN: A GUI client for Windows, Linux and macOS, support Xray and sing-box and others](https://github.com/2dust/v2rayN)

FIClash

[GitHub - chen08209/FlClash: A multi-platform proxy client based on ClashMeta,simple and easy to use, open-source and ad-free.](https://github.com/chen08209/FlClash)

3、在Cloudflare 上创建worker。

4、填写下面的代码，这个代码来自Github社区的开源项目，代码已经内置IP优选和代理功能，自带动态的UUID，可以大大减少手动配置过程，非常适合新手和特殊用户。

(1)

[edgetunnel/_worker.js at main · cmliu/edgetunnel](https://github.com/cmliu/edgetunnel/blob/main/_worker.js)

[connect.laoqian303.us.kg](https://connect.laoqian303.us.kg/qian1007)

(2)

[GitHub - yonggekkk/Cloudflare-vless-trojan: CF-workers/pages代理脚本【Vless与Trojan】：支持nat64自动生成proxyip，一键自建proxyip与CF反代IP，CF优选官方IP三地区应用脚本，自动输出美、亚、欧最佳优选IP](https://github.com/yonggekkk/Cloudflare-vless-trojan)

[far.laoqian303.us.kg](https://far.laoqian303.us.kg/2b2a9b9f-7d6d-49af-be3e-9329c19e3e84)

(3)

[GitHub - cmliu/edgetunnel: 在原版的基础上修改了显示 VLESS 配置信息转换为订阅内容。使用该脚本，你可以方便地将 VLESS 配置信息使用在线配置转换到 Clash 或 Singbox 等工具中。](https://github.com/cmliu/edgetunnel)

[connect.laoqian303.qzz.io](https://connect.laoqian303.qzz.io/2b2a9b9f-7d6d-49af-be3e-9329c19e3e84)

注意：创建的worker项目名称最好使用系统默认的，别自定义，以免被系统识别到特殊字符而被屏蔽。

## 三、优选订阅生成器

```
https://vless.fok.dedyn.io/sub?host=[你的Worker域名]&uuid=(你的UUID]
```

[优选订阅生成器](https://sub.laoqian303.us.kg/)