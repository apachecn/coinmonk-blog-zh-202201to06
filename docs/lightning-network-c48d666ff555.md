# ⚡⚡闪电网络

> 原文：<https://medium.com/coinmonks/lightning-network-c48d666ff555?source=collection_archive---------53----------------------->

![](img/b29b55f99d8154b12ce9e71a4d7a5f66.png)

**让区块链的交易变得可扩展和即时**

> **目的**

**比特币是世界上最受欢迎、最有价值的数字货币，任何人都可以在不需要可信中介或存管机构的情况下汇款。比特币有一个复杂的脚本系统，允许用户为资金编写指令。然而，比特币的去中心化设计也有一些缺点。**

**比特币区块链上的交易可能需要长达**小时才能恢复。****

**小额支付，或者几美分或更少的支付，很少被确认，而且费用使得这种交易在今天的网络上不可行。**

**这些问题由**闪电网络**解决。这是最早使用比特币内置脚本创建**多方智能合约(可编程货币)的方式之一。**有了比特币，闪电网络在多方金融计算领域处于技术进步的前沿。闪电网络解决了这些问题。它是首批**多方智能合约**实现之一。**

**比特币的内置脚本可以用来创造可编程货币。闪电网络处于技术进步的最前沿。**

**![](img/279db78c72c6ff957ce3ed17cff41672.png)**

> ****工作****

**Lightning Network 是一个分散式系统，用于**即时、大量的小额支付**，消除了将资金委托给第三方的风险。**

**闪电网络是第二层，旨在解决比特币和其他区块链的可扩展性问题。闪电 mainnet 于**2018 年 3 月**上线。今天，我们将看看闪电网络是什么，它是如何工作的，以及它将如何在比特币的未来发挥作用。**

**闪电网络是一种运行在区块链之上的网络，允许快速的点对点交易。不限于比特币；其他加密货币，如莱特币，也采用了它。**

**你可能想知道我们说“**坐在区块链顶上”是什么意思。“闪电网络是一种链外或第二层解决方案。它使任何人都可以进行交易，而不必在区块链上登记每一笔交易。****

****闪电网络不同于比特币网络，它有自己的节点和软件，**但它仍然与主链通信。要进入或退出 Lightning 网络，必须创建**唯一区块链交易**。**

**在您的第一笔交易中，您实际上是在与另一个用户创建智能合同。我们将在稍后讨论具体细节；现在，把智能合约想象成一个与其他用户共享的私有账本。这个分类账可以容纳大量的交易。它们只对你和你的交易对手可见，但因为对系统中的一些奇怪元素来说，你们都不能作弊。**

**渠道是**小账本**的一种。假设**爱丽丝**和**鲍勃**各自在智能合约中输入 5 BTC。他们现在在他们的频道上都有 5 BTC 的余额。艾丽丝可能会用这个分类账来支付鲍勃**1 BTC。鲍勃现在有 6 个 BTC 站在他这边，而爱丽丝有 4 个。然后，在稍后的时间，**鲍勃**可以将 2 BTC 还给**爱丽丝**，从而将余额带到**爱丽丝**方的 6 BTC 和**鲍勃**方的 4 BTC。他们可以继续这样做一段时间。****

**任何一方都可以在任何时候向区块链广播信道的当前状态。此时，通道两端的余额被分配给相应的链上交易方。**

**闪电交易，顾名思义，极其迅速。没有需要处理的批量确认——只要您的互联网连接允许，付款就可以尽快完成。**

**![](img/4cb7dc5c42443cebef665b1c3c209a98.png)**

> ****为什么需要雷电网络？****

**到目前为止，**闪电网络**(或简称 LN)看起来是扩展比特币区块链最实用的方法。在这样一个大的生态系统中协调修改是困难的——有可能出现硬分叉和潜在的灾难性错误。当风险如此之大时，实验是极其危险的。**

**当你把实验移出区块链时，你会有更多的灵活性。如果出了问题，对比特币网络本身没有任何影响。第二层解决方案没有任何使该协议运行了十多年的安全假设。**

**也没有责任抛弃以前的做事方法。**对于最终用户，链上交易继续正常运行，但他们现在也可以选择链外交易。****

**使用闪电网络有各种好处。我们将在下面讨论一些更重要的问题。**

> ****可扩展性问题****

**可扩展性是指应对需求增长的能力，或者——如比特币网络所定义的——在区块链中填充更多交易以实现最大用户增长的能力。目前，世界上大约有 2200 万个比特币钱包。即使我们假设每个人都有多个钱包地址，这也只代表了世界人口的很小一部分。比特币旨在成为一种数字现金货币，也是一种全球通用的货币。因此，网络必须在其开发的早期和广泛部署之前解决这个可扩展性问题。**

> ****链外解决方案****

**一种非链解决方案指出，比特币交易的主要部分将被记录在并行运行的辅助网络上，而不是主公共账本上。这可以通过利用**多签名钱包(Multi-Sig wallets)技术来实现。**多签名钱包旨在为一个或多个用户提供额外的安全保障，这些用户希望在不需要信任的情况下保存资金。这类似于联合银行账户，提款需要双方签字。**

**为了使用多签名钱包中的钱，钱包中涉及的每个人的私钥的数字签名是必要的。您可以建立一个多签名钱包，它需要 3 个密钥中的 2 个，甚至 15 个密钥中的 15 个。**

**![](img/0aebeafa0096d5b568e60f9e72692171.png)**

# ****弊端****

> ****流动性****

**对闪电网络最严重的指控之一是它限制了你的交易能力。**你不能在一个渠道上花费超过你已经承诺的费用。如果您花光了所有资金，您必须关闭该渠道，以便远程余额包含该渠道的所有资金。你也可以等到有人通过它付钱给你，但这并不理想。****

**您的路径也可能受到通道总容量的限制。想想爱丽丝>鲍勃>弗兰克。如果爱丽丝和鲍勃具有 5 个 BTC 的信道容量，但是鲍勃和弗兰克只有 1 个 BTC 的信道容量，则爱丽丝永远不能发送超过 1 个 BTC。即便如此，为了实现这个功能，全部的平衡必须在 Bob -> Frank 频道的 Bob 一边。这可能会严重限制可以通过 LN 渠道传递的现金数量，影响有效性。**

> ****集中的集线器****

**由于上一节强调的问题，一些人担心该网络将允许形成巨大的“枢纽”也就是说，拥有大量现金的庞大、人脉广泛的实体。任何大额支付都必须通过这些机构之一进行。**

**显然，这不会是一个**好形势**。这会破坏系统，因为这些实体的崩溃会严重破坏对等关系。因为只有少数几个地方进行交易，所以审查的可能性也增加了。**

# ****把所有的放在一起****

**尽管它仍处于测试阶段，但自 2018 年**mainnet 发布以来，闪电网络已经取得了巨大的增长。****

****仍然有重大的可用性问题需要克服，因为操作一个闪电节点现在需要相当多的技术知识。然而，考虑到正在进行的工作数量，随着时间的推移，进入的障碍可能会减少。****

****如果缺陷得到修复，闪电网络可能成为比特币生态系统的重要组成部分，大幅提高可扩展性和交易速度。****

******Lightning** **网络**和**非链解决方案**对于网络的可扩展性和将比特币转化为可用于所有类型日常购买的真正数字现金至关重要。****

# ****加入我们的社区****

> ****WHATSAPP****

****[](https://chat.whatsapp.com/FTKme4XzkOU73ZDv99Oatj) [## BLOCKENTHU

### WhatsApp 群邀请

chat.whatsapp.com](https://chat.whatsapp.com/FTKme4XzkOU73ZDv99Oatj) 

> 电报

[](https://t.me/blockenthu) [## ⚡·布洛克登胡·⚡

### 可以马上查看并加入@blockenthu。

t.me](https://t.me/blockenthu) 

> INSTAGRAM

[https://www.instagram.com/blockenthu/](https://www.instagram.com/blockenthu/)

> 商务化人际关系网

[](https://www.linkedin.com/company/blockenthu/) [## Blockenthu | LinkedIn

### LinkedIn 上有 384 名粉丝。“面向大众的 Web 3.0 福利”加密和区块链| BlockEnthu 是社区…

www.linkedin.com](https://www.linkedin.com/company/blockenthu/) 

使用印度最安全的加密交换#COINDCX。

[](https://coindcx.com/) [## CoinDCX -加密交易所|购买、出售和交易比特币和顶级替代币

### CoinDCX 是印度最大、最安全的加密货币交易所，在这里你可以买卖比特币和其他…

coindcx.com](https://coindcx.com/) 

#区块链# BLOCKENTHU # CRYPTO # coincxpath breaker # coincx #比特币#lightningnetwork #

> 加入 Coinmonks [电报频道](https://t.me/coincodecap)和 [Youtube 频道](https://www.youtube.com/c/coinmonks/videos)了解加密交易和投资

# 另外，阅读

*   [3 商业评论](/coinmonks/3commas-review-an-excellent-crypto-trading-bot-2020-1313a58bec92) | [Pionex 评论](https://coincodecap.com/pionex-review-exchange-with-crypto-trading-bot) | [Coinrule 评论](/coinmonks/coinrule-review-2021-a-beginner-friendly-crypto-trading-bot-daf0504848ba)
*   [莱杰 vs Ngrave](/coinmonks/ledger-vs-ngrave-zero-7e40f0c1d694) | [莱杰 nano s vs x](/coinmonks/ledger-nano-s-vs-x-battery-hardware-price-storage-59a6663fe3b0) | [币安评论](/coinmonks/binance-review-ee10d3bf3b6e)
*   [Bybit Exchange 评论](/coinmonks/bybit-exchange-review-dbd570019b71) | [Bityard 评论](https://coincodecap.com/bityard-reivew) | [Jet-Bot 评论](https://coincodecap.com/jet-bot-review)
*   [3 commas vs crypto hopper](/coinmonks/3commas-vs-pionex-vs-cryptohopper-best-crypto-bot-6a98d2baa203)|[赚取加密利息](/coinmonks/earn-crypto-interest-b10b810fdda3)
*   最好的比特币[硬件钱包](/coinmonks/hardware-wallets-dfa1211730c6) | [BitBox02 回顾](/coinmonks/bitbox02-review-your-swiss-bitcoin-hardware-wallet-c36c88fff29)
*   [BlockFi vs 摄氏](/coinmonks/blockfi-vs-celsius-vs-hodlnaut-8a1cc8c26630) | [Hodlnaut 点评](/coinmonks/hodlnaut-review-best-way-to-hodl-is-to-earn-interest-on-your-bitcoin-6658a8c19edf) | [KuCoin 点评](https://coincodecap.com/kucoin-review)****