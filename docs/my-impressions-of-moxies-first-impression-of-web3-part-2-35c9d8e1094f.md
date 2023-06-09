# 我的印象莫邪对 web3 的第一印象(下)

> 原文：<https://medium.com/coinmonks/my-impressions-of-moxies-first-impression-of-web3-part-2-35c9d8e1094f?source=collection_archive---------14----------------------->

![](img/da686e0e4f37ef306cb801236b6ec213.png)

Photo by [Shubham Dhage](https://unsplash.com/@theshubhamdhage?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/s/photos/decentralized?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)

我的分析的第一部分通过莫邪最初的论文阐述了中央集权的出现。第二部分在这里分析了更多莫邪的[印象](https://moxie.org/2022/01/07/web3-first-impressions.html)。第三部分是这里的。

莫邪描述了通过建立两个基于 NFT 的 dapps 进行的实验:

> 两者都让我感受到了这个空间是如何运作的。需要澄清的是，这些应用本身并没有什么特别的“分布式”:它们只是普通的 react 网站。“分布式”指的是状态和更新状态的逻辑/权限所在的位置:在区块链，而不是在“集中式”数据库中……我对加密货币世界一直感到奇怪的一点是，它缺乏对客户端/服务器接口的关注。

我认为这是区块链最容易被误解的地方(可能在某种程度上是由于虚假广告)——它浓缩成了数据库层的替代品。数据驻留在共享的、可公开访问的区块链上，而不是集中式数据库。

但是界面层不会神奇地变成“分布式的”——最终它将是一个普通的 react 网站，或者一些类似的变种。一个中心实体(读作:开发人员)将需要部署您所使用的接口。并且需要一个中央实体(如 Infura)将该接口直接连接到区块链。

我将扩展莫邪早些时候的观点，即没有人希望进一步运行自己的服务器:没有人，我是说*没有人*希望为他们使用的每个应用程序构建自己的界面，或者运行自己的区块链节点——尽管要明确的是，任何人都可以这样做。

因此，我认为这是莫邪对 web3 最强烈的批评——缺乏对客户机/服务器接口的关注。

我们知道区块链本身是安全的，但是你用来和区块链联系的东西呢？比如让[用户签署欺诈交易](https://ethresear.ch/t/proposal-minimizing-fraudulent-transactions-in-metamask-e-g-via-front-end-hacks/11416)的 Metamask 克隆。或者 Infura [节点](https://coinmarketcap.com/alexandria/article/ethereums-infura-iating-outage-revives-decentralization-concerns)的潜在问题。

但我们也要清楚，这并不是区块链的具体过错，它只是将这个问题模块化成了不同的部分。同样的批评也适用于任何现存的 web2 应用程序——现有堆栈的任何一层都可能受到损害。

不同的是，区块链至少关闭了一个漏洞载体，即后端——防止了类似 Okta 的[这样的灾难，所有这些都源于一个拥有数据库访问权限的工程师。一旦数据成功到达区块链，您就安全了。因此，尽管不完美，但 T2 仍然比现状要好。](https://www.theverge.com/2022/3/22/22990637/okta-breach-single-sign-on-lapsus-hacker-group)

对我来说，问题不在于区块链还没有解决这个问题，而是，正如莫邪所说，福音传道者“经常掩盖客户最终无法参与那些(无领袖共识)机制的现实”。

有责任清楚宣传的是什么。

莫邪还指出了这些集中式实体的出现，如 [Infura](https://infura.io/) 和 [Alchemy](https://www.alchemy.com/) ，它们有助于通过服务器上远程运行的节点与区块链进行交互。Dan Finlay 已经解决了关于这些 API“没有使用任何东西来验证区块链状态或真实性”的批评，所以这一点似乎被夸大了。

但是，即使它是有效的——仅仅因为这些特定的客户端 API 是不充分的，这并不意味着区块链本身存在根本性的问题。这些实体仅仅是区块链的接口。

这只是意味着他们还没有足够的竞争，意味着*仍然有*一个颠覆性的机会(即使与这些颠覆者相比，他们只是在建立[MVP](https://economictimes.indiatimes.com/definition/minimum-viable-product))，意味着——你猜对了，我们仍然他妈的早，而标准还没有赶上宣传。

[维塔利克反驳](https://www.reddit.com/r/ethereum/comments/ryk3it/my_first_impressions_of_web3/hrrz15r/)，我同意:

> 在我看来，莫邪在文章的后半部分对生态系统现状的批评是正确的……但是他们忽略了区块链生态系统的发展方向。

这是一个当前版本的实现问题，*而不是*一个基本的协议问题(在某种程度上，Vitalik 承认在依赖链中，“为了拥有轻客户端，我们需要有一个轻客户端友好链，这是对协议的一个深刻改变，因此实现它的唯一现实机会是切换到 PoS”)。

这个主题还在继续，因为接下来是莫邪评论的一大支柱，其中心是 NFT 实现*当前的形式*——即“NFT 通常不将数据存储在链上。对于大多数图像的大多数 NFT 来说，这太昂贵了。”本质上，“那个(NFT)URL 经常只是指向一些运行 Apache 的副总裁”。他继续详细展示了他如何能够通过利用这一方面来操纵 NFT 的完整性——使 NFT“根据谁在查看它而改变，因为提供图像的 web 服务器可以根据请求者的 IP 或用户代理选择提供不同的图像。”

我 100%同意这一批评的内容——非功能性测试在目前的状态下根本不够，而且经常是骗局。他是对的——你所竞拍的并不完全是你所得到的。但同样，我觉得这集中于当前实施的弱点，将其问题与区块链或更广泛的非功能性测试固有的问题混为一谈。它只是见树不见林——在这种情况下，甚至不承认更合适的实现可以在链上存储其所有数据(如 URL ),具有[持久性](https://arweave.news/nft-arweave-ethereum/),消除了他提到的一些问题。

它完全忽略了 NFTs 的潜在未来使用案例，这可以彻底改变数字所有权的性质。它错过了生态系统的发展方向。

莫邪还指责了 web3 对平台的依赖。这是我们最不同意的地方:

> 像以太坊这样的技术已经建立了许多与 web1 相同的隐含陷阱。为了使这些技术变得可用，空间正在围绕…平台进行整合。又来了。[…]
> 
> 在集中式平台上快速迭代已经超过了分布式协议，并将控制整合到平台中。[…]
> 
> 一旦一个分布式生态系统为了方便而集中在一个平台上，它就变成了两个世界中最糟糕的:集中控制，但仍然足够分散，最终会陷入困境。

我再次同意他断言的内容，但却得出了完全相反的结论。在他的分析中隐含着对平台的批评，平台本身就是对控制的巩固。他将 web2 的弱点误解为依赖于平台，而不是它们真正的弱点，即依赖于*集中式*平台。平台部分不是问题，是集中部分才是问题！

平台本身是有益的。正如马克·安德里森所说:

> “平台”是一个可以由外部开发人员(用户)编程并定制的系统，以这种方式适应无数的需求和利基，这些需求和利基是平台的原始开发人员不可能想到的，更不用说有时间适应了[……]有平台总是比没有平台好，就这样。平台是好的，就这样。

正如[比尔·盖茨通过 Chamath Palihapitiya](https://semilshah.com/2015/09/17/transcript-chamath-at-strictlyvcs-insider-series/) 解释的那样:

> 一个平台是当每个使用它的人的经济价值**超过创造它的公司的价值**。然后是一个平台。

查马斯补充道:

> 如果你把这个简单的方法应用到任何一家声称自己是平台的公司，世界上只有 3 个平台！[……]所以，我认为，这些不是“平台”，这些是 API，这些是开发人员工具，这很好，它是通向某些东西的桥梁，但它不是平台，所以**让我们停止称它为平台，让我们称它为它是什么，它是一堆端点**。

这正是 OpenSea、Infura 或 Alchemy 的含义:一堆端点。*以太坊*就是平台。以太坊是生态系统围绕其旋转的东西。

我反过来想这个。当 crypto 围绕一个平台集中时，它不再像围绕 AWS(它控制你的数据和服务器)，围绕 Twitter(它控制你的追随者列表)，或围绕脸书(它控制你的网络)那样集中。它们都非常方便，但代价是对数据的完全所有权。

相反，有了区块链，我觉得你得到了两个世界最好的东西——集中平台的便利性，而没有锁定。

正如 SBF 承认的那样，crypto 中确实存在集中式应用(比如 FTX)——但现在你有权带着你的资产完好无损地退出:

莫邪对此不屑一顾:

> 区块链的支持者可能会说，如果出现这种类型的集中式平台也没关系，因为国家本身就在区块链上，所以如果这些平台行为不当，客户可以直接转移到其他地方。**然而，我认为这是一种非常简单的观点，认为平台是由动态变化形成的。** […]
> 
> 我可以建立自己的 NFT 市场，但如果 OpenSea 协调人们使用的钱包中所有 NFT 的视图(以及生态系统中的所有其他应用程序)，它不会提供任何额外的控制。

除了在这种情况下，OpenSea only *目前*协调钱包中所有 NFT 的视图——同样是出于方便——因为还没有开发出更好的解决方案。尽管至少这实际上仍然是可能的，因为数据在开放的区块链上，而 OpenSea 仅仅是制作了接口。

相比之下，OpenSea 的“web2”版本拥有存储 NFT 的中央数据库。在这种情况下，物理上不可能“简单地移动到别处”，甚至忽略平台动态。

现在数据是公开的，可审计的；真相的地面来源仍然可以在没有 OpenSea 同意的情况下提取。OpenSea 仅仅拥有控制的幻觉。事实上，多亏了区块链，这种控制是通过公众共识实现的。

完美吗？不要！但是为什么*需要*完善才算是进步呢？

期望区块链同时放松“让平台成为现在这个样子的动力”也太过分了这就像期待我的 [Ultraboosts](https://www.adidas.com/us/blog/439874-what-is-adidas-boost-technology) 来解决我跑步缺乏动力的问题。

然而，以太坊仍然间接地解决了这个问题，通过从这些纯粹的端点剥离控制——它自己承担了防止这些实体自己这样做的平台。

莫邪的含蓄论点听起来像许多反对任何东西的类似风格的论点——如果它不是 100%，如果它不是一个完美的解决方案，它就是失败的。它遵循相同的逻辑:

*   哦，我们不能通过做 X，Y，Z 来解决气候的逆转，所以让我们放弃吧。
*   哦，我们不能完全阻止枪支暴力，所以让我们接受大规模枪击事件将会发生。
*   口罩不能 100%阻止病毒，所以我们不要戴口罩。

他没有庆祝某种程度的权力下放，而是对缺乏理想的权力下放吹毛求疵。

然而，我仍然附和他的终极担忧:“web3 社区期待着一些不同于我们已经看到的结果”。他的许多陈述在本质上是事实正确的。

但我们也不要纯粹根据 dapps 的现状来评判 web3。这就像在 1995 年因为一些劣质网站和低带宽、刺耳的 AOL 连接而对互联网的变革性吹毛求疵。某些网站没有正确地散列它们的密码就意味着网上交易根本不安全吗？

这很愚蠢——我们需要将实现与协议的潜在优势分开，尤其是协议的发展方向。

这太长了。未完待续… [第三部分](https://blog.yanbman.com/my-impressions-of-moxies-first-impression-of-web3-part-3-6fb0bdebfdaf)。

> 加入 Coinmonks [电报频道](https://t.me/coincodecap)和 [Youtube 频道](https://www.youtube.com/c/coinmonks/videos)了解加密交易和投资

# 另外，阅读

*   [币安期货交易](https://coincodecap.com/binance-futures-trading)|[3 commas vs Mudrex vs eToro](https://coincodecap.com/mudrex-3commas-etoro)
*   [如何购买 Monero](https://coincodecap.com/buy-monero) | [IDEX 评论](https://coincodecap.com/idex-review) | [BitKan 交易机器人](https://coincodecap.com/bitkan-trading-bot)
*   [CoinDCX 评论](/coinmonks/coindcx-review-8444db3621a2) | [加密保证金交易交易所](https://coincodecap.com/crypto-margin-trading-exchanges)
*   [红狗赌场评论](https://coincodecap.com/red-dog-casino-review) | [Swyftx 评论](https://coincodecap.com/swyftx-review) | [CoinGate 评论](https://coincodecap.com/coingate-review)
*   [Bookmap 评论](https://coincodecap.com/bookmap-review-2021-best-trading-software) | [美国 5 大最佳加密交易所](https://coincodecap.com/crypto-exchange-usa)