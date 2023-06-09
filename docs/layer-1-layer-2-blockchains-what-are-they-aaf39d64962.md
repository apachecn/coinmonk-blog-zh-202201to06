# 第一层和第二层区块链:它们是什么？

> 原文：<https://medium.com/coinmonks/layer-1-layer-2-blockchains-what-are-they-aaf39d64962?source=collection_archive---------46----------------------->

![](img/6b584e751e41fabbdca769425b0260ef.png)

# **简介**

如果你是密码和区块链世界的新手，那么你可能会以惊人的速度收到新单词。

DAOs，alpha，hodl，altcoins，第一层和第二层，等等。

这可能会令人望而生畏。更重要的是，为解释这些概念而写的文章对新手来说太难理解了。如果那是你，那么你一定要关注这个空间，因为我将会写文章以最简单的方式解释加密和区块链概念。

好了，让我们深入到第 1 层和第 2 层区块链。

那些是什么？人们所说的第 1 层和第 2 层区块链是什么意思？

简而言之，第 1 层区块链是任何网络中的基础区块链，第 2 层区块链是建立在第 1 层区块链之上(或旁边)的辅助区块链，用于提高第 1 层区块链的效率。

本质上，第 1 层区块链是加密空间中的主要区块链。它们就像房子的地基。它们是关于那个特定区块链的一切运作的主要架构。

第 1 层区块链是自我维持的，它可以在自己的网络上执行事务、验证和完成事务以及添加新的块。

另一方面，第二层区块链不能自我维持。它依靠第 1 层区块链来验证和完成事务，然后将这些事务作为新块添加到区块链中。

第一层区块链的例子有比特币和以太坊。第二层区块链的例子包括 Polygon 和比特币闪电网络。

这里有一个简单的方法来思考这个问题。

把第一层区块链想象成房子的地基。这是建造房子的第一步，也是最重要的一步。然而，你可以继续在地基之上建造地基之外的其他东西。

您可以将第 2 层区块链视为可以构建在原始基础之上的一切(第 1 层区块链)。

和所有的插图一样，这个也有它的局限性。因此，让我们以第 1 层和第 2 层区块链为例深入探讨一下。

# **比特币和比特币闪电网**

比特币是第一层区块链的一个很好的例子。比特币区块链是从零开始建立的，它没有建立在任何其他东西上。用我们之前的例子来说，这是一个基础网络。所有涉及比特币的交易都由比特币区块链自己执行、最终确定和验证。

另一方面，比特币闪电网络是建立在比特币区块链之上的次级区块链。比特币闪电网络通过自己处理其中一些交易，使主要比特币网络上的交易更快。交易可以在闪电网络上进行和验证，然后数据被发送回比特币网络，以检查结果的有效性，并将其添加到区块链中。

可以这样想:比特币区块链必须在短时间内处理大量任务。因此，为了更快地做事，它将一些交易交给闪电网络。当闪电网络完成任务处理后，它会将结果传回比特币区块链，后者随后会验证并记录结果。

这种安排可以在其他区块链中找到，也许最引人注目的是多边形，它是在区块链以太坊顶部建造的第二层区块链。

但是等一下，你可能会奇怪为什么区块链要建在其他区块链之上。第 2 层区块链有什么用？为什么不干脆再建一个区块链呢？欢迎来到缩放问题和区块链三难困境。

# **成长的烦恼**

维塔利克·布特林(以太坊的联合创始人之一)提出了一个广为人知的概念，即区块链三元悖论。

基本思想是区块链需要解决三件事，但这三件事不能同时解决。问题是可伸缩性、安全性和去中心化。

每个区块链都需要能够扩展，以便能够处理更多的事务—它还需要安全，以保护用户及其事务—最后，它需要去中心化，这意味着所有权是分布式的，而不是掌握在少数人手中。

区块链三难困境的含义是，你不能同时改善这三件事。

增加其中的任何一个或两个意味着你在减少其他的。提高安全性和可伸缩性会降低分散性，其他方面也是如此。

# **解决缩放问题**

第 2 层区块链是解决伸缩问题的典型方案。与更集中的平台相比，区块链今天的局限性之一是它们不能处理大量交易。

例如，比特币区块链每秒只能处理 7 笔交易。以太坊区块链速度更快，但每秒只能处理大约 15 笔交易。相比之下，支付公司 [Visa 每秒处理大约 1700 笔交易。](https://news.bitcoin.com/no-visa-doesnt-handle-24000-tps-and-neither-does-your-pet-blockchain/)

因此，区块链需要解决吞吐量问题，以便进行扩展，并有机会与集中式平台竞争。(吞吐量是网络上每次可以执行的事务数量。)

这个扩展问题的解决方案之一是构建第 2 层区块链来帮助主区块链更快地工作。

第 2 层解决方案的基本情况是，执行事务所需的所有处理能力以及正在执行的事务本身都发生在与主区块链相邻的网络上(或构建在主之上)。然后，最终结果被传输到主区块链进行验证和记录。

因此，闪电网络使用自己的处理能力来处理交易，然后将最终结果发送回比特币区块链进行验证和记录。第 2 层区块链通常被称为第 2 层扩展解决方案。这是因为他们试图通过在第 1 层区块链之上构建第 2 层区块链来解决扩展问题。

就区块链三元悖论而言，第二层区块链倾向于牺牲一定程度的去交易化，以实现更快的交易速度。

# **结束语**

现在，你可能想知道为什么最初的区块链没有被修改来解决这些问题。为什么要建立一个闪电网络，而不是改进比特币区块链本身？

事实上，有很多方法可以扩展第 1 层区块链。这些当然被称为第 1 层扩展解决方案。然而，第 1 层扩展解决方案有其局限性。它们很难实现，并且需要网络上所有用户的同意才能实现。如果不能达成协议，可能会导致社区分裂。

不涉及任何细节，一些第 1 层扩展解决方案包括:

1.  改变共识机制(例如，以太坊正在从工作证明转变为利益证明)。
2.  增加一个块中可以记录的事务数量。
3.  碎片。

我们将在另一篇文章中详细讨论第 1 层扩展解决方案。但是现在，当您在对话中听到第 1 层区块链或第 2 层区块链这两个术语时，您可以确信自己再也不会感到困惑了。

> 加入 Coinmonks [电报频道](https://t.me/coincodecap)和 [Youtube 频道](https://www.youtube.com/c/coinmonks/videos)了解加密交易和投资

# 另外，阅读

*   [XT.COM 评论](https://coincodecap.com/profittradingapp-for-binance) | [币安评论](https://coincodecap.com/xt-com-review)
*   [SmithBot 评论](https://coincodecap.com/smithbot-review) | [4 款最佳免费开源交易机器人](https://coincodecap.com/free-open-source-trading-bots)
*   [比特币基地僵尸程序](/coinmonks/coinbase-bots-ac6359e897f3) | [AscendEX 审查](/coinmonks/ascendex-review-53e829cf75fa) | [OKEx 交易僵尸程序](/coinmonks/okex-trading-bots-234920f61e60)
*   [如何在印度购买比特币？](/coinmonks/buy-bitcoin-in-india-feb50ddfef94) | [WazirX 审查](/coinmonks/wazirx-review-5c811b074f5b)
*   [CryptoHopper 替代品](/coinmonks/cryptohopper-alternatives-d67287b16d27) | [HitBTC 审查](/coinmonks/hitbtc-review-c5143c5d53c2)