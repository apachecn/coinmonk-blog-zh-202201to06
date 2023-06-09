# power vs PoS——区块链共识机制的崩溃

> 原文：<https://medium.com/coinmonks/a-breakdown-of-blockchain-consensus-mechanisms-950bdace14a8?source=collection_archive---------61----------------------->

![](img/76b5a076913c7e7f4a41d82b15a78c61.png)

共识机制是密码世界中的一个常用词。你可能已经听过工作证明或股权证明。然而，大多数人不知道许多其他类型的共识机制。这是新协议的游戏规则改变者吗？

在本文中，我们将了解什么是共识机制，它如何应用于加密，当然，还有各种不同的类型。让我们开始吧。

# 共识机制

共识是指普遍同意。他们每天都在群体中接触，有时是为了卑微的决定和其他具有长期影响的决定。这种共识和协议的关系延续到密码。然而，这个解释还有更深一层的含义。

在加密中，共识机制是容错算法，用于对单个数据点和网络状态达成一致。这允许分布式系统(计算机)一起工作，保持安全，并避免操纵。

区块链上的共识算法被设计得非常复杂。你不希望任何人进来操纵结果，对吗？

这就引出了共识机制如何分类的话题。首先，让我们讨论两个主要的参与者:工作证明和利益证明。然后，我们将继续讨论其他一些你可能听说过也可能没有听说过的问题，如授权证明、能力证明、耗时证明和烧伤证明。

# 工作证明

在当今世界，工作证明模型通常与比特币联系在一起。然而，这个概念在 1993 年由辛西娅·德沃克和莫尼·诺尔首次提出。当时，它最初被设想为一种对抗电子邮件垃圾的方法。这是通过要求服务请求者的一些工作和计算机的处理时间来完成的。

比特币应用了简化版的工作证明协议。网络参与者或“矿工”竞相解决一个复杂而随意的难题——有点像猜随机数。一旦矿工破解了代码，他们就可以在这个链条上增加一笔比特币交易，并获得一定数量的 BTC 作为奖励。当参与者证明完成的工作允许他们向区块链添加新的交易时，这个循环会重复。

现在，这是一个淡化的版本。如果你已经在谷歌上搜索如何成为一名比特币矿工，你可能需要再想想。BTC 采矿需要惊人的计算能力、能源消耗和处理时间。当考虑到对环境的影响时，你可以看到战俘是如何带有一些负面含义的。这也是为什么其他网络选择采用不同的共识机制，如利害关系证明的原因。

# 利害关系证明

与它的对手不同，利害关系证明是一种低成本和节能的协议。这个想法产生于 2011 年，当时它被提出作为处理比特币交易的解决方案。虽然比特币并不适用，但此后许多加密货币都采用了利益一致算法的证明。最值得注意的是以太坊 2.0、Cardano、Solana 和 Polygon。

在赌注证明协议中，加密货币的所有者可以“赌”他们的硬币。这可能导致被选择来验证新的事务块。被选中来完成这项任务确实需要一些技术支持，但是你已经掌握了要点。在 PoS 共识机制中负责验证交易的网络参与者被称为“验证者”。

验证器可以(也应该)位于全球各地，确保去中心化。所有者必须“下注”的具体金额因硬币而异，但被下注的硬币仍被禁止交易。您可以在他们的网站上找到大多数硬币特定的赌注要求。

当然，任何共识机制都不可能是完美的。

PoS 协议最大的问题之一是 51%攻击。当一个人(或一个团体)获得了区块链 51%的多数控制权时，就会出现这种情况。获得这种级别的控制成本很高，肯定会影响所持有的加密货币的价值，但这并非不可能。

# 权威证明

这种下一个共识机制自我标榜为处理交易的有效替代方案，不依赖于计算能力或资金。这是权威的证明。

这一概念最早是由以太坊(Ethereum)联合创始人、波尔卡多(Polkadot)创始人加文·伍德(Gavin Wood)在 2017 年提出的。在 PoA 中，网络参与者用他们的真实身份进行交易。该算法利用了将你的声誉置于危险之中，这是诚实行事的核心动机。

虽然这种方法能够实现更快的交易，但 PoA 区块链往往缺乏分散性。主要是因为参与者必须向权威或实体的中央来源证明他们的身份。因此，PoA 算法对于有物流问题的大型企业来说是一个更可行的解决方案。

# 能力证明

一种不太流行的共识算法是容量证明，或者像一些人所说的那样——空间证明。这允许贡献节点使用其硬盘驱动器上的存储空间来挖掘网络上的加密货币并为区块链产生块。可用硬盘空间越多，维护公共分类账的能力就越强。

关于 PoC 的研究最早出现在 2015 年 Stefan Dziembowski 的一篇论文中。虽然这种算法的用例没有其他算法普遍，但在希格诺(以前称为 Burstcoin)、Chia 和 Arweave 中可以找到这种概念的变体。

基于存储的网络的缺点是集中化的可能性。这是因为机构或富裕的个人可以利用他们的购买力获得更多的存储空间，并最终主导网络。

# 经过时间的证明

经过时间算法的证明反映了 PoW 和 PoA 协议的相似质量。它被用于许可的区块链来决定采矿权和新区块的增加。与 PoA 一样，参与者必须证明自己的身份才能加入网络。然而，PoET 还结合了基于时间抽签的协议的概念。

英特尔公司在 2016 年初发布了这个想法。它利用时间的概念，以便在网络上实现公平和平等的共识。PoET 算法包含两个部分。首先，节点必须随机选择一个等待时间或“计时器对象”。第二，首先完成所选等待时间的参与者是“获胜者”,并且有资格向网络添加新的块。

鉴于这是一个许可的封闭网络，PoET 协议引起了人们对集中化的关注。该机制还依赖于英特尔的工具，这引发了更多关于兼容性的担忧。尽管如此，PoET 仍然在公平和效率方面提供了坚实的优势。

# 燃烧证明

我们列表中的最后一个共识机制是烧伤证明。在 PoB 模式下，网络参与者通过将硬币发送到无法运行的地址来“烧毁”硬币。焚烧硬币会使其永久退出流通。这种做法经常被用于通货膨胀，但 PoB·区块链用它来验证交易和赚取采矿奖励。

伊安·斯图瓦特在 2012 年首次提出了刻录密码的概念。该协议有一些显著的优点，包括稀缺性、低能耗，并鼓励长期项目参与。

另一方面，一些人认为焚烧硬币不环保，被视为浪费资源。该算法也没有被证明能够在更大规模上工作，需要更多的测试来确保安全性。

在 crypto 中使用的共识机制的类型不胜枚举。随着事情的继续发展和新计划的出现，我们很可能会在未来看到许多新的协议。有没有哪种共识机制不在这个名单上？请在评论中分享。

下次见——神秘金发女郎。

> 加入 Coinmonks [电报频道](https://t.me/coincodecap)和 [Youtube 频道](https://www.youtube.com/c/coinmonks/videos)了解加密交易和投资

# 另外，阅读

*   [币安期货交易](https://coincodecap.com/binance-futures-trading)|[3 commas vs Mudrex vs eToro](https://coincodecap.com/mudrex-3commas-etoro)
*   [如何购买 Monero](https://coincodecap.com/buy-monero) | [IDEX 评论](https://coincodecap.com/idex-review) | [BitKan 交易机器人](https://coincodecap.com/bitkan-trading-bot)
*   [尤霍德勒 vs 科恩洛 vs 霍德诺特](/coinmonks/youhodler-vs-coinloan-vs-hodlnaut-b1050acde55a) | [Cryptohopper vs 哈斯博特](https://coincodecap.com/cryptohopper-vs-haasbot)
*   [顶级付费加密货币和区块链课程](https://coincodecap.com/blockchain-courses)
*   [MXC 交易所评论](/coinmonks/mxc-exchange-review-3af0ec1cba8c) | [Pionex vs 币安](https://coincodecap.com/pionex-vs-binance) | [Pionex 套利机器人](https://coincodecap.com/pionex-arbitrage-bot)
*   [如何在印度购买比特币？](/coinmonks/buy-bitcoin-in-india-feb50ddfef94) | [瓦济克斯评论](/coinmonks/wazirx-review-5c811b074f5b)