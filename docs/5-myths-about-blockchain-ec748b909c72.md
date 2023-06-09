# 关于区块链的 5 个神话

> 原文：<https://medium.com/coinmonks/5-myths-about-blockchain-ec748b909c72?source=collection_archive---------57----------------------->

![](img/ad8b3a20b4dd0831ba4c275db83546ed.png)

诚然，我掌握区块链技术有点晚——就在 2018 年，我和我的团队开始涉足密码相关业务。OpenZeppelin 帮了大忙。渴望密码的客户提供了更多帮助。

开发环境碰巧有点“矮胖”，交易缓慢，费用高，以及大量等等…我的意思是…不是一见钟情！用户和开发者的体验都没有让我们满意。尽管如此，Zelle transfer 或 SEPA transaction easy 背后的加密用户体验，更不用说 PayPal 或 Stripe 等支付处理器的便利性了。但是，DeFi 是一个不同的世界，它的规则已经改变了全球金融规则——也许是永远改变了；因此，我们调整自己，将金融与技术相结合，并接受与资金管理工具和平台更复杂的互动。作为这种新的复杂性的交换，我们获得了更多的隐私、新的投资模式、先进的金融工具、更多的自由，以及——最后——将我们的手放在最时尚和最热门的技术上的智力满足感(与 AI 进行辩论，AI 是另一个被高度误解的工业 4.0 r-evolution 的孩子)。

最后这一点引发了与一群拥有区块链商业理念的客户和潜在客户的几次对话，有些想法很疯狂，有些则潜力巨大(如果开发得当)。

作为一个全球性的“特质联盟”，我和我的团队发现了一个关于区块链发展的明显错误信息，以及对这种技术提供的功能能力和潜在可能性的普遍高估。我们感受到的是一种“*神话*”的感觉，而不是信息，有时这给我们带来了非常困难的时刻，让我们与客户进行尴尬的对话，客户在开始他们的项目时，对使用账本和智能合同能做什么以及不能做什么有着完全不同的假设。

在几次问答会议后，我列出了一个很小的清单，列出了围绕区块链工业的**五大神话**，这些神话最终可能会破坏一些项目，如果设计和领导得当，这些项目可能会有巨大的潜力。当然，**我的文章并不打算完整详细地描述这种技术是如何工作的**——比我更熟练、更有能力写下自己想法的人已经发表了大量更准确的技术文章；我更谦虚的目标是让非技术人员容易理解区块链范式的局限性，以避免时间和金钱的浪费，同时增加成功开发基于分类帐的项目的机会。该列表(当然还有待扩充)由以下主题组成:

***1)为什么把你的结婚照存在区块链里不是个好主意***

2)你的密码不在你的钱包里

***3)智能合约并不那么智能***

***4)隐私不是神话——但也不是被授予的***

***5)分权化成为神话***

# 第一个误区:为什么把你的结婚照保存在区块链里是个坏主意。

作为第一个炒作的话题，我们无疑有相同的区块链技术本身的主要核心和一切开始的地方:账本。众所周知，分类账是一种分散分布在节点网络(DLT)上的“数据库”，由通过索引代码(哈希)链接的逻辑块组成，每个逻辑块引用前一个逻辑块。当前的区块链诞生于比特币，它旨在作为一个数字账本，以最简单的方式记录来自两个不同来源(钱包)的移动，这意味着底层逻辑是——很可能——通过从一个地址减去特定金额并向第二个地址添加相同金额来记录交易。

举个例子，在当前的账本状态下(姑且称之为状态 1)，爱丽丝钱包里有 1 个 BTC，鲍勃 0；如果执行了一个事务，Alice 将她的 BTC 发送给 Bob，我们的后续状态(状态 2)将反映事务的输出(Alice 的钱包中有 0，Bob 现在有 1 个 BTC)。

根据设计，**分类账不打算存储业务对象和复杂信息**，在其存储级别—作为其物理对应账簿分类账，**仅仅是具有键/值对格式的交易日志**。像以太坊这样的“国家计算机”中的信息存储在链上(在区块链)和链下。在链上，我们有区块链层和一个以块存储的简单交易日志，而链外是“世界状态”数据库，它维护钱包余额的当前“快照”(以及其他非永久或短暂的信息)。

交易信息和智能合约输出最初注册在世界状态数据库中，后来永久写入区块链中(可以认为是第一批只能刻录一次的 CD)。以太坊通常使用 LevelDB 作为数据库来管理区块链和世界状态，而 Hyperledger Fabric 可以使用 LevelDB 或类似 CouchDB 的 JSON 数据库。与存储在区块链中的信息的一个主要区别是，世界状态中的数据可以更新和删除。每当我们从智能契约或链码中获取信息时，我们通常从世界状态中检索这些信息。但是，即使像 CouchDB 这样的中等先进的数据库也可能缺乏数据操作的特性，并且在一些情况下会添加第三层(例如，我们在 Hyperledger Fabric 中使用 MongoDB 来报告数据操作)。因此，在 Hyperledger Fabric 环境中，我们可以有一个由区块链(链上数据)和 CouchDB(不太频繁的 LevelDB)组成的分类帐，以及 MongoDB 中用于更深层次数据操作的第三层(CouchDB 和 MongoDB 都被认为是链外数据库)。

希望画面足够清晰，也应该同样清晰:

a) *在类似“状态计算机”的上下文中，关于链上和链外数据的对话没有什么意义*，因为无论何时我们获取和读取数据，都是来自 LevelDB/CouchDB/RocksDB 等，按照区块链的命名法，它们被认为是链外数据库(因此，仅仅是这个简单的差异就可能引起许多混乱)。

b) *存储在区块链级的信息非常简单*，引用一个事务日志；就灵活性和存储容量而言，区块链不是为管理复杂的业务对象而构建的——也不是区块链顶级的外链世界状态数据库。这就是为什么 DeFi 协议，基本上是链式金融交易，在区块链上有自己的自然环境，实际上是真实世界区块链服务实现的 99.99%。

c) *存储在区块链和世界州的数据是基本的*并涉及交易；*以 SQL 方式检索复杂数据和操作超出了当前分类帐实现的范围*(有一些基于 SQL-99 的区块链数据库，甚至 PostgreSQL 也在某些上下文中使用，但它们仍然不是主流)。由于需要增加我们产品的复杂性，在许多情况下，需要部署第三级数据存储和操作——通常是 NoSQL 数据库，如 Elastics 和 MongoDB。

d)最后但同样重要的是:**存储在区块链的数据极其昂贵！**天然气费用由固定成本和可变成本组成；最后一个取决于几个触发因素，包括事务中要处理的信息的大小。事实上，在以太坊中存储一千字节的数据将花费 640，000 汽油:当前的汽油费(在这篇文章发表之日)是 20 gwei，或 0.00000002 ETH，所以 0.0128 ETH，或(在这篇文章的当前成本下)**每千字节 38.4 美元！**这意味着几乎**每兆字节 40，000 美元**(一个简单的 PDF 合同的大小)——此外，在区块链上写那兆字节需要几乎 14 分钟。

分类账是处理交易信息的一种不可思议的方式，并按预期完成了工作。强迫 DLT 范式像大型 SQL 或 NoSQL 数据库一样注册和操作数据是不可行的。每当出现这种信息管理情况时，除了区块链部署之外，还必须实施传统的数据库来正确处理数据。

> 加入 Coinmonks [电报频道](https://t.me/coincodecap)和 [Youtube 频道](https://www.youtube.com/c/coinmonks/videos)了解加密交易和投资

# 另外，阅读

*   [如何在 Uniswap 上交换加密？](https://coincodecap.com/swap-crypto-on-uniswap) | [A-Ads 审查](https://coincodecap.com/a-ads-review)
*   [WazirX vs CoinDCX vs bit bns](/coinmonks/wazirx-vs-coindcx-vs-bitbns-149f4f19a2f1)|[block fi vs coin loan vs Nexo](/coinmonks/blockfi-vs-coinloan-vs-nexo-cb624635230d)
*   [本地比特币评论](/coinmonks/localbitcoins-review-6cc001c6ed56) | [加密货币储蓄账户](https://coincodecap.com/cryptocurrency-savings-accounts)
*   什么是融资融券交易
*   [支持卡审核](https://coincodecap.com/uphold-card-review) | [信任钱包 vs MetaMask](https://coincodecap.com/trust-wallet-vs-metamask)