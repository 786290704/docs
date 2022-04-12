# PCM 代币经济模型

![](https://1397868517-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MHREX7DHcljbY5IkjgJ-3369173170%2Fuploads%2FTKK5IlnLXp426EcCWU9d%2Fcn-1129.png?alt=media\&token=d047e282-ac01-4b50-8ff0-c7207ec046cd)

### &#x20;<a href="#emission-rate" id="emission-rate"></a>

除此以外，还会以 9.09% 的比例，向[团队地址](broken-reference)铸造动态数量的 PCM。这意味着，如果你收获了 100 个PCM，那么就会有 9.09 个 PCM 被铸造出来，然后发送到团队地址。

所有铸造给团队地址的 PCM 都被每周销毁，从未进入流通。

### &#x20;<a href="#distribution" id="distribution"></a>

### &#x20;<a href="#other-deflationary-mechanics" id="other-deflationary-mechanics"></a>

* PCMSwap v2 的交易额的 **0.05%**
*
*
* ****
* ****
*
* ****
*
*
*

为了迅速落地，PCMSwap 以 MVP（最小可行产品）的形式推出，MasterChef 合约每区块恒定铸造 40 PCM。由于这个原因，早期的团队没有增加额外的功能，如更改 PCM 铸币速度与逻辑的能力。由于迁移到新的 MasterChef 需要大量的时间和精力，团队选择通过创建两个农场池来控制 PCM 的铸造速度：

*
* 销毁池 (PID - 138) —— 用于每区块 PCM 销毁

这些池子的工作方式与农场类似，在每次 PCM 减产投票后，大厨们可以通过它们，调整原本为每块 40 PCM 的产速以及比例。

因此，在销毁的那一天，当我们从这些销毁池中收获时，主页上显示的供应量可能会突然跃升几百万 PCM。

这个数字上的波动，只是因为我们需要收获所有在这一周内积累的，分配给销毁的 PCM 。

分配到 PID-137 和 PID-138 池的 PCM在每周销毁前需要被收获，这使得网站上显示的总供应量会突然跳升 \~600 万。这是因为待收获的 PCM 在销毁日，被收获之前，并不会算入总供应量中。一旦代币销毁交易完成，这 \~600 万就会算入那一周的销毁之中。

## 如何亲自确定 PCM  的流通总量？

若想亲自校验首页上显示的 PCM 总量是否正确，只需要：

1. 前往 BscScan 上 PCM  的代币页面，查看 [有多少 ](https://bscscan.com/token/0x0e09fabb73bd3ade0a17ecc321fd13a19e81ce82#balances)PCM [ 在销毁 (Burn) 地址中](https://bscscan.com/token/0x0e09fabb73bd3ade0a17ecc321fd13a19e81ce82#balances)。这个数量表示有多少 PCM 被销毁（从流通总量中移除，无法取回）
2. 然后，查看总量 (Total Supply) 并减去该数量。
3. 最后的数字即为 PCM  流通总量。
