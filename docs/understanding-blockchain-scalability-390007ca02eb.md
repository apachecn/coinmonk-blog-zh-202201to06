# 了解区块链可扩展性

> 原文：<https://medium.com/coinmonks/understanding-blockchain-scalability-390007ca02eb?source=collection_archive---------17----------------------->

![](img/07ac88f8b0061d4e06713176ba433ffe.png)

Source: [www.leewayhertz.com](https://www.leewayhertz.com/)

B [锁链](https://www.euromoney.com/learning/blockchain-explained/what-is-blockchain#:~:text=Blockchain%20is%20a%20system%20of,computer%20systems%20on%20the%20blockchain.)是一种存储数据的方法，因此很难或不可能更改、黑客攻击或欺骗数据。区块链是交易的数字账本，复制并分布在区块链的整个计算机系统网络中。链上的每个区块都包含几个交易，每当区块链上发生新的交易时，每个参与者对该交易的记录都会被添加到分类账中。尽管区块链在许多方面有益于现代世界，但它缺乏可扩展性。在许多真实的商业环境中，可伸缩性被认为是构建公共区块链的最大障碍。因此，随着使用区块链的用户数量的增长，可扩展性困难的数量也在增长。本文将讨论区块链的可扩展性及其解决方案。

# **什么是区块链可扩展性？**

在讨论区块链的可扩展性之前，我想解释一下可扩展性的科学含义。[可扩展性](https://www.iphos.com/it-scalability-rcy/#:~:text=IT%2Dscalability%20is%20the%20ability,sales%20with%20given%20increased%20resources.)是指计算机系统管理不断增加的工作量的能力(例如，数据库或搜索引擎)。由于数据量很大，区块链网络无法正常扩展或者可扩展性很低。区块链系统没有足够的努力来适应不断增长的工作负载、数据和资源(例如，计算能力、服务器或带宽)。区块链网络承受不断增加的事务负载和网络中节点数量的能力称为可扩展性。

然而，在区块链的背景下，“可扩展性”一词有着更广泛的含义。令人惊讶的是,“区块链”一词在学术上还没有得到彻底的定义。例如，在一篇关于区块链可扩展性的最有影响力的论文中，比特币在吞吐量、延迟、引导时间或每笔交易成本方面的任何增强都被称为“可扩展”，随后的区块链系统被称为可扩展。

> 当一个区块链系统被认为是可扩展的时，它实现了比其他当前系统更大的 TPS。TPS 代表每秒事务数，衡量事务吞吐量的速度。

几个区块链系统可以被归类为“可扩展的”，尽管它们的吞吐量差别很大。值得注意的是，在区块链中，“可扩展”一词是一个比较短语。当一个区块链系统被认为是可扩展的时，它通过改变特定的系统属性和调整其一致性过程来达到比其他当前系统更高的 TPS。

# **什么是区块链可扩展性解决方案？**

![](img/8de8714b07d77741fb72d36e9ce524e5.png)

Source: [https://applicature.com/](https://applicature.com/)

鉴于可扩展性是主流区块链采用的主要障碍，有效的区块链扩展解决方案是必要的。现在正在开发许多不同的解决方案来解决区块链可伸缩性的问题。令人惊讶的是，区块链可伸缩性问题的解决方案可以分为四类。每个解决方案类别都提供了独特的方法来解决困扰区块链的可扩展性难题。

## **第一层可扩展性解决方案**

“如何解决区块链的可伸缩性问题？”这个问题最常见的答案是会引导您找到[第 1 层](https://academy.binance.com/en/articles/what-is-layer-1-in-blockchain)解决方案。第一层或第 1 层解决方案需要对区块链核心网络的软件进行更改。因此，第 1 层解决方案通常被称为链上扩展解决方案。

第 1 层解决方案增强了区块链网络的基本特征和属性，例如增加块大小限制或减少块验证时间。分片、隔离见证(SEGWIT)和硬分叉是三种流行的第 1 层区块链扩展选项。

*   **分片**

分片是一种众所周知的链上可伸缩性技术。它专注于将区块链网络分解成更小、更易管理的碎片。然后，网络将彼此并行地执行碎片。网络的处理输出会随着每个碎片处理一部分组的事务处理而增加。通过将网络分成更小的比特，它可以充当其各部分的总和。分片有效地消除了对单个节点性能的依赖，从而实现更快、更高效的事务吞吐量。

*   **隔离见证**

隔离见证(SEGWIT)是第一层选项中对区块链可伸缩性的另一个重要贡献。SEGWIT 是比特币区块链网络中的一项协议增强，专注于改变数据存储的方式和结构。它有助于消除与每笔交易相关的签名数据，从而增加交易的容量和存储空间。值得注意的是，用于验证发送方所有权和现金可用性的数字签名占据了交易总空间的 70%左右。数字签名的移除可以为新事务的添加释放额外的空间。

*   **硬叉子**

硬分叉是一个过程，其重点是对区块链网络的属性进行结构性或根本性的更改。例如，硬分叉可能意味着增加块大小或减少创建块所需的时间。虽然硬分叉是第 1 层区块链可伸缩性解决方案的先决条件，但有争议的硬分叉是最有效的选择。有问题的硬分叉表明了更大的区块链网络中的分裂，社区的特定部分在特定主题上与核心社区相矛盾。在这种情况下，区块链社区的一个子集可能会选择对底层源代码进行根本性的修改。

## **第二层可扩展性解决方案**

对主要区块链网络的改变极大地影响了第一层或链上扩展技术的可行性。由于对如何处理区块链网络中的可扩展性困难的研究，出现了链外扩展方法。第二层或[第二层](https://academy.binance.com/en/glossary/layer-2)可扩展性解决方案是链外扩展选项。第 2 层解决方案是建立在主要区块链之上的补充协议，辅助协议将用于从主要区块链“卸载”交易。

因此，第 2 层解决方案可以显著应对空间和网络拥塞挑战。状态通道和场外链是第二层解决方案的常见示例。

*   **状态通道**

状态通道是区块链可伸缩性的第 2 层解决方案中的一个典型组成部分。通过各种方法，国家渠道使链外交易渠道和区块链网络之间的双向沟通。因此，它有可能显著提高交易速度和容量。必须指出的是，国有渠道不需要矿商的直接参与来验证交易。另一方面，状态信道充当网络附近的资源，其与智能契约或多重签名方法集成。当一个状态通道上的一个交易或一系列交易完成时，相关的区块链会记录该‘通道’的最终‘状态’以及任何相关的交易。

*   **侧链**

侧链也是第 2 层解决方案中的一个流行选择，用于确定如何解决您的区块链中的可扩展性问题。侧链作为大批量交易中紧挨着区块链的交易链运行。与主链相比，侧链使用不同的共有技术。

*   **血浆**

在第 2 层扩展解决方案领域，等离子也是一个突出的区块链可扩展性解决方案。它主要关注于利用从父区块链开始的子链，每个子链充当一个单独的区块链。结果，可以为涉及处理某种类型的交易的用例创建等离子体，同时确保在具有增强的安全性的可比较的环境中执行。

*   **闪电网**

闪电网络是区块链可扩展性的另一个著名的离链方法的例子。它通过主区块链网络上的私有、外链通道来利用智能合约功能。外链渠道可能会以较低的成本提供更快的交易。最重要的是，通过将交易从主链转移，Lightning Network 减轻了主链的负担。因此，用户不再需要支付开采费或长时间等待区块确认。

## **可扩展共识机制**

您对“如何解决区块链的可伸缩性问题”这一问题的解决方案的探索会引导你使用可扩展的共识技术。有几种共识技术可用于简化达成共识的过程。结果，可扩展的一致性算法可以提供更大的可扩展性和事务吞吐量。以下是可扩展共识流程的一些重要示例，可作为有效的区块链可扩展性方法:

*   **委托股权证明**

DPOS，或委托利害关系证明，是一种共识技术，类似于控制一个国家的民主进程。在这种情况下，令牌持有者可以为网络交易选择验证器。根据该系统，委托验证者的数量可以从 10 到 100 不等，并且有规律地变化。

*   **授权证明**

您还可以考虑将授权证明作为区块链可伸缩性选项中的一个可行选项。这是一种可扩展的共识方法，采用基于声誉的共识算法。被选择的节点负责使用权威证明共识技术来验证网络交易。

*   **拜占庭容错**

拜占庭容错(BFT)共识技术已经成为处理拜占庭将军问题的最可靠的工具之一。BFT 通常指的是一个分布式系统的特征，它表明尽管网络中有多个对立的参与者，但仍有必要保持一致。

## **可扩展分布式账本**

区块链技术只是更大的分布式账本技术(DLT)环境的一部分。除了区块链，还可以找到其他形式的分布式账本。有趣的事实是，这种分布式分类账并不使用与区块链相同的数据结构来将信息组织成一连串的区块链。

# 那么，为什么区块链很难规模化？

限制、交易费用、块大小和反应时间是决定区块链可伸缩性的主要因素。

**限制**

区块链可伸缩性的首要问题是局限性。在处理新交易的情况下，每个节点在分类帐中添加关于交易的信息。因此，不断增加的交易历史可能会颠覆整个系统。此外，区块链网络必须准确维护所有数据，以保护信任级别。此外，区块链在硬件方面也存在局限性。区块链可伸缩性问题中的大多数问题都是由硬件限制引起的。随着区块链网络的扩展，设置和维护运行节点所需的硬件变得不容易。

**交易费用**

导致区块链面临重大可扩展性挑战的下一个关键因素是高昂的交易费用。由于挖掘对更高计算能力的需求，区块链网络的日益流行导致了验证交易的过程更加复杂。用户必须支付特定的费用来验证他们的交易。随着区块链网络的不断扩大，用户渴望支付更高的交易费用来验证他们的交易。但是，还需要注意的是，许多其他事务会长时间留在队列中而没有得到处理。

**块大小**

对于理解为什么可扩展性是区块链的一个问题，区块大小也是一个值得注意的方面。区块链网络中事务数量的不断增加导致执行事务的过程非常耗时。例如，在最初的日子里，比特币区块链网络中的每个区块都有 1 Mb 的大小，它们包含近 2020 笔交易。另一方面，网络中事务数量的增长导致了块大小的增加，从而影响了可扩展性。

**响应时间**

区块链网络中的所有交易都应通过验证过程。通常，考虑到队列中的事务数量，事务必须等待很长时间进行验证。例如，比特币网络意味着需要将近 10 分钟来构建一个新的区块。交易验证的等待时间在高峰时段会增加。响应时间与高交易费用直接相关，这是导致区块链可伸缩性问题的显著因素之一。

# 结论

很明显，随着去中心化的增加，可伸缩性降低了。区块链应用程序的日益流行带来了严重的伸缩问题。因此，我们开发了区块链的扩展解决方案，以缓解急需的压力。随着区块链技术被多个用例所接受和部署，区块链的可伸缩性在不久的将来将继续成为人们着迷和好奇的来源。

> 加入 Coinmonks [电报频道](https://t.me/coincodecap)和 [Youtube 频道](https://www.youtube.com/c/coinmonks/videos)了解加密交易和投资

# 另外，阅读

*   [5 款最佳免费加密货币制图工具](https://coincodecap.com/crypto-charting-tools)
*   [最佳比特币保证金交易](/coinmonks/bitcoin-margin-trading-exchange-bcbfcbf7b8e3) | [萝莉点评](/coinmonks/lolli-review-e6ddc7895ad8) | [比特币保证金交易](https://coincodecap.com/bityard-margin-trading)
*   [创造并出售你的第一个 NFT](https://coincodecap.com/create-nft) | [密码交易机器人](https://coincodecap.com/best-crypto-trading-bots)
*   [如何在 CoinDCX 上购买柴犬(SHIB)币？](https://coincodecap.com/buy-shiba-coindcx)
*   [CBET 回顾](https://coincodecap.com/cbet-casino-review) | [库币 vs 比特币基地](https://coincodecap.com/kucoin-vs-coinbase) | [拜比特 vs 比特币基地](https://coincodecap.com/bybit-vs-coinbase)
*   [折叠 App 回顾](https://coincodecap.com/fold-app-review) | [本地比特币回顾](/coinmonks/localbitcoins-review-6cc001c6ed56) | [Bybit vs 币安](https://coincodecap.com/bybit-binance-moonxbt)