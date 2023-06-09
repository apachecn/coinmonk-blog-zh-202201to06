# 确保物联网设备的安全性

> 原文：<https://medium.com/coinmonks/ensuring-security-for-iot-devices-8a05b51342c5?source=collection_archive---------30----------------------->

![](img/b9ee3a114b10695d997550baacbb8f15.png)

Photo by FLY:D on Unsplash

安全性通常是物联网设备管理中被忽视的一个方面。为物联网设备提供安全性变得越来越昂贵，而且成本会越来越高。根据 Gartner 2018 年 3 月发布的报告，2018 年物联网安全支出将达到 15 亿美元，高于 2017 年的 12 亿美元，增长 28%。物联网设计师面临的一些常见挑战是常用传感器缺乏任何安全性。虽然这些传感器提供的信息相对无害，但当这些信息在用户环境中发送时，就会成为威胁，导致用户数据易受攻击。因此，用户上下文的所有方面，如密码、指纹识别、公共接口访问，都应该能够抵御常见的安全攻击。

物联网系统的安全性可以大致分为物联网硬件的安全性和物联网网络的安全性，即物联网硬件和云之间的通信网络。在接下来的章节中，将分析这两个类别的安全性，并讨论可能的安全措施。

## 物联网硬件常见的安全攻击

物联网硬件/设备最脆弱的部分是传感器/执行器。大多数传感器/致动器不具备处理安全性的能力。他们通常没有足够的内存和 CPU 资源来实现传统的安全机制。关于传感器/致动器的假设是黑客对它们不感兴趣，或者它们不容易受到攻击，并且简单的密码/认证机制足以防止安全黑客攻击。物联网设备中的大多数传感器使用无法更改或太容易更改的默认密码。然而，近年来，这些设备最容易受到安全黑客的攻击。事实上，大多数黑客瞄准这些设备来影响自我折磨的行为。由于大量物联网设备部署在交通、公用电网、家庭自动化和通信系统中，对物联网设备的安全攻击会严重破坏现代生活方式。

## 在传感器/执行器中实现安全性的挑战

在传感器/致动器中实现安全性面临以下挑战:

1.  复制:这些设备是大规模生产的，一旦黑客可以对一个设备进行成功的攻击，同样的攻击就可以对所有设备进行复制。
2.  关于实现安全性的假设:大多数实现者假设传感器/执行器不会成为安全攻击的目标，或者不会容易受到这种攻击。因此，他们没有实施足够的安全措施。
3.  安全补丁不容易应用:大多数传感器/致动器是嵌入式设备，并且安全补丁不容易应用。
4.  专有协议:大多数传感器/执行器本质上都是专有的，因此不受安全工具的保护。
5.  易于访问:因为传感器/致动器通常由默认密码保护；访问这些设备非常容易。

## 物联网硬件的安全措施

没有一种适用于所有物联网设备的解决方案。但是，这些安全措施有助于防范常见的安全攻击:

1.  安全引导:固件被加密签名，以防止任何固件更改。
2.  安全代码更新:一种确保可以轻松应用安全补丁的方法。该功能与安全引导一起将确保恶意软件不会被引入。
3.  数据和通信安全:设备上的数据和通信可以加密。
4.  认证:所有与设备的通信都应该使用强认证机制进行认证。
5.  嵌入式防火墙:嵌入式防火墙将确保只与已知的可信主机进行通信。这样黑客就无法轻易发动攻击。
6.  入侵检测:必须检测和报告无效登录和其他恶意活动。
7.  设备篡改机制:这种实现将防止任何自我折磨的活动。

## 物联网网络常见的安全攻击

物联网网络组件包括物联网网关、物联网平台、物联网服务器、数据中心和通信协议。这些组件应该防范这些常见的安全攻击:

1.  欺骗:攻击者可以欺骗传感器来访问物联网网关/平台。
2.  中间人攻击:攻击者可以读取物联网网关和物联网平台之间交换的信息。具有足够安全性的内置通信协议可以防止这种攻击。
3.  窃听:与中间人攻击类似，攻击者可以读取物联网服务器和物联网应用程序之间交换的信息。该信息可以被调节以改变来自应用/致动器的结果。
4.  隐私:隐私已成为最终用户关注的问题，因为消费者数据可能会在消费者不知情或未同意的情况下被使用。这些数据可用于跟踪他/她的购买习惯、病史、旅行记录、财务状况等信息。
5.  DDoS 攻击:通过向物联网平台和物联网服务器发送无效请求，可以发起拒绝服务攻击。

## 物联网网络的安全措施

1.为物联网设备分配唯一的 id:为每个设备分配唯一的 id 可以防止欺骗等攻击。一旦分配了唯一的 id，就可以配置物联网设备的发现和检测。

2.静态和传输中的数据加密:物联网网络数据在静态和传输中都必须加密。静态数据的加密是设备本地的，使用本地磁盘加密可以轻松实现。到目前为止，非对称加密已经非常可靠地用于传输中的数据加密。如果使用公钥来加密数据，那么只能使用私钥来解密数据。如果私钥用于加密数据，那么只有公钥可以用于解密数据。由于加密功能的不对称性，一个发送方无法读取另一个发送方的消息，即使双方都拥有对方的公钥。

3.数据所有权/隐私:数据所有权应始终属于最终客户。最终客户应该是决定如何以及何时使用其数据的最终权威。

## 结论

如果不将安全性作为物联网系统设计的组成部分，就不可能使物联网系统安全。安全性必须从一开始就内置，因为大多数安全措施由于设计挑战、复杂性以及有时无法更改而无法在后期引入。

> 加入 Coinmonks [电报频道](https://t.me/coincodecap)和 [Youtube 频道](https://www.youtube.com/c/coinmonks/videos)了解加密交易和投资

# 另外，阅读

*   [OKEx vs KuCoin](https://coincodecap.com/okex-kucoin) | [摄氏替代品](https://coincodecap.com/celsius-alternatives) | [如何购买 VeChain](https://coincodecap.com/buy-vechain)
*   [币安期货交易](https://coincodecap.com/binance-futures-trading)|[3 comas vs Mudrex vs eToro](https://coincodecap.com/mudrex-3commas-etoro)
*   [如何购买 Monero](https://coincodecap.com/buy-monero) | [IDEX 评论](https://coincodecap.com/idex-review) | [BitKan 交易机器人](https://coincodecap.com/bitkan-trading-bot)
*   [CoinDCX 评论](/coinmonks/coindcx-review-8444db3621a2) | [加密保证金交易交易所](https://coincodecap.com/crypto-margin-trading-exchanges)
*   [红狗赌场点评](https://coincodecap.com/red-dog-casino-review) | [Swyftx 点评](https://coincodecap.com/swyftx-review) | [CoinGate 点评](https://coincodecap.com/coingate-review)