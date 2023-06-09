# DLT 互操作性和更多⛓️#5⛓️——通用原子互换:全区块链硬币的安全交换

> 原文：<https://medium.com/coinmonks/dlt-interoperability-and-more-%EF%B8%8F-5-%EF%B8%8F-universal-atomic-swaps-secure-exchange-of-coins-across-8c7b87b20509?source=collection_archive---------10----------------------->

# 在这个系列中，我们分析了关于区块链和互操作性(以及两者)的论文。

这一版涵盖了最近一篇关于原子交换的论文

![](img/fb3b4268dfa910a53be2336e5a97e926.png)

Photo by [Maxim Hopman](https://unsplash.com/@nampoh?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com?utm_source=medium&utm_medium=referral)

➡️ **书名** : **通用原子互换:全区块链硬币的安全交换**➡️**作者**:斯里·阿拉文达、克里希南·塔亚加拉詹、朱利奥·马拉沃尔塔、佩德罗·莫雷诺-桑切斯

来源:[https://eprint.iacr.org/2021/1612](https://eprint.iacr.org/2021/1612)

➡️ **背景:**

研究互操作性很重要，因为它允许区块链(默认情况下最初构建为孤岛)一起通信。不同区块链的交流创造了网络效应，类似于互联网的兴起，导致数十亿美元产业的产生。
然而，互操作性很难被认为是一个已解决的挑战，原因有几个，我们将在以后的文章中研究。这篇论文提供了这一学科的最新发展水平。

作者认为对原子交换协议很重要的属性:

1.  *非保管*，在兑换过程中脱离受托保管用户硬币的第三方；

像 ODAP 这样的几个协议允许在保管模式下进行安全的资产交换。这种模式对于在集中世界中注册的机构和企业来说可能是足够的。

*2。通用*，即兼容所有(当前和未来)加密货币；

作者寻找一种可以适应各种加密货币的通用协议。这是一个有趣的特性，因为执行分散的资产转移(关于资产转移和资产交换的含义，请参见我们的论文[您需要分布式账本技术互操作性解决方案吗？](https://www.techrxiv.org/articles/preprint/Do_You_Need_a_Distributed_Ledger_Technology_Interoperability_Solution_/18786527/1))通常需要处理每个区块链的复杂性。发现区块链支持任意资产转移的根本技术需求(或者更正式地说，一个理想的功能)确实非常有趣。

*3。多资产*，支持单次原子互换多枚硬币。

它应该允许在一个会话中组合多个单一资产转让。这可以提高 1-n 甚至 n-n 转移的效率，这也是我们正在研究的事情(见 [Hermes](https://www.sciencedirect.com/science/article/abs/pii/S0167739X21004337) 和我们即将发表的论文)。

➡️ **投稿:**

*   作者提供了一个资产转移协议，该协议满足以下性质:非托管、通用和多资产。该协议具有最低的技术要求(只要求底层区块链具有验证签名的能力)，可以进行不同加密货币的 n-n 转移。
*   作者为区块链支持 Schnorr/ECDSA 的案例提供了一个实现(非开源)和一个评估(本文不涉及)

💪**优点:**

*   在我看来，作者很好地介绍了什么是散列时间锁契约以及如何实现原子交换。
*   作者可以找到一种不需要链上脚本(例如，智能合约)来实现原子交换的方法。这通常并不简单，因为 HTLCs(和其他原子交换机制，如 Hermes)需要跟踪时间来实现超时。超时允许从崩溃故障中恢复并避免死锁(当用户故意不想完成传输时)。然后，这种方案依赖于希望进行资产交换的各方共同拥有一个地址。
*   这个方案很简单，尽管很复杂。首先，双方创建一个共同管理的帐户，每个人在该帐户上都有一份份额(特别是在帐户的私钥上)。然后，双方签署退款交易，该交易在超时后触发。然后，秘密创造阶段发生了。在 HTLCs 中，它是一个秘密的散列；在这个方案中，通过两方计算得到的“锁定”版本的签名充当秘密。解锁资产的一个签名依赖于另一个签名(“秘密”)，在某种程度上，当一个资产被赎回时，下一个也可以被赎回。
*   该协议所做的假设是对手不能阻止一方离线执行计算(即离线)，类似于 HTLCs 中的假设。然而，在这种情况下，对于所提出的协议，要付出的代价是本地计算相对于链上计算(在 HTLCs 的情况下，招致交易费用)。

> 加入 Coinmonks [电报频道](https://t.me/coincodecap)和 [Youtube 频道](https://www.youtube.com/c/coinmonks/videos)了解加密交易和投资

**😞局限性:**

*   的确，原子交换可以用 HTLCs 实现，但是有一些攻击会妨碍原子性。特别是，当 Bob 收到一个秘密 r 来解锁目标链上的散列锁时，执行解锁的事务可能会不成功。如果是这样的话，我们就有了这样一种情况，Alice 获得了她的资产，但是 Bob 没有，这违反了原子性属性(通过扩展可以认为是跨链的一致性属性)。
*   由于在虚拟的端到端资产转移中，只测试了允许锁定资产的关键功能的性能，因此实现和评估都是短暂的。没有提供设置阶段的开销(就计算工作量而言)。

**🔥兴趣点:**

*   “原子互换必须保持*可替代性*，也就是说，分类账的观察者(除了爱丽丝和鲍勃)不应该将作为原子互换一部分执行的转移与此类分类账中的标准资产转移区分开来。”。在跨链资产交换(资产转移)中，不会保留此属性，因为转移的资产是该资产在来源区块链中的表示。然而，资产交换(这是本文的研究对象)保留了该属性(通常由 HLTCs 实现)
*   如果作者说“即使在现有的加密货币中，原子互换(以及随之而来的安全交换)也仅限于少数加密货币的组合，或者要求人们接受强信任假设”，这将是有趣的
*   我不知道作者所说的“作为这种普遍性的副产品，这种原子互换交易与标准的一对一交易*相同*，从而增加了互换硬币的可替代性”是什么意思
*   作者认为，要使协议具有普遍性，他们应该能够提供“用于认证交易的签名验证脚本”。它假设一个通用的两方计算(2PC)协议和一个可验证的定时签名的存在。鉴于这些假设，我不确定这是否是一个通用协议的合适定义，我希望作者能对此进行更多的讨论。
*   我想我发现了一个错别字:“事务 tx 的超时 t 意味着事务仅在时间 t 到期后被网络中的节点接受”->“事务 tx 的超时 t 意味着事务仅在时间 t 之前被网络中的节点接受”
*   该协议似乎比简单的 HTLC 复杂得多。它要求用户控制一个联合地址，作为原子交换的基础。事实上，这种方案看起来类似于支付渠道，在那里签署了承诺，在一方离线的情况下将资金返还给原始所有者(也因为大多数处理似乎发生在链外)。设置阶段(即设置联合账户)没有提供所需资源的足够细节(在时间和交易成本方面)。

**🚀它与我们在 Técnico Lisboa、INESC-ID 和 Blockdaemon 的工作有何关系？(观点是我自己的，不一定反映我雇主的意见)**

*   实现安全、可扩展的互操作性是我们 Blockdaemon 工作的重要组成部分。研究执行原子交换的更便宜的方法对于支持不断增长的区块链生态系统是有意义的，该生态系统将互操作性作为一个重要因素。

🚀这对我们的工作有什么启示？

*   鉴于上述任务，有研究通用原子交换的应用。这已经应用于几个研究领域，允许我们推理攻击者如何利用 n-n 原子交换。
*   多资产互换对于防止前期交易和后期交易非常重要，因为对于大额交易，在交易过程中操纵资产价格 a1-> a2-> a…-> a 可能会导致进行交易的用户遭受损失。