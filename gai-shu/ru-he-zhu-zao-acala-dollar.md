# 如何铸造Acala Dollar

你可以使用&#x20;

* [Acala DApp](https://apps.acala.network/vault)（协议的前端应用）从Polkadot/Acala网络的抵押资产中创建Acala Dollar（aUSD）。&#x20;
* [Karura DApp](https://apps.karura.network/vault)（协议的前端应用），从Kusama/Karura网络的抵押资产中创建Acala Dollar on Karura（kUSD）。&#x20;
* [Polkawallet](https://polkawallet.io) - 一个移动应用程序，用于在以上两个生态系统中创建Acala Dollar。&#x20;

用户可以通过这个应用程序创建一个基于Acala Dollar的贷款，或存入抵押资产，铸造和偿还Acala Dollar，跟踪抵押资产价格，发送和接收代币，兑换Acala Dollar。&#x20;

## 前提条件&#x20;

在使用Web App铸造Acala Dollar之前，你需要准备好以下事情：&#x20;

1. **下载并使用Polkadot钱包**：遵循[这里](https://guide.acalaapps.wiki/general/installing-polkadot.js)的指南操作&#x20;
2. **钱包里有抵押资产**
3. **将抵押资产桥接到Acala（或Karura）网络**&#x20;

* [Acala's DOT桥接指南](https://app.gitbook.com/s/X0fjyKavAAozAGhuu7sU/ru-men/acala-wang-luo/acalas-dot-qiao)&#x20;
* [Karura's Inter-Kusama 转账指南](https://app.gitbook.com/s/X0fjyKavAAozAGhuu7sU/ru-men/karura-wang-luo/karura-de-nei-bu-zhuan-zhang)&#x20;

&#x20;  4\. **钱包存有交易费代币：**使用指南[这里](https://app.gitbook.com/s/X0fjyKavAAozAGhuu7sU/le-jie-acala/ling-huo-de-shou-xu-fei)&#x20;

## 铸造Acala Dollar&#x20;

任何人都可以通过存入被接受的储备资产（抵押资产）来铸造Acala Dollar，例如，用DOT来创建一个金库/贷款，即所谓的抵押债仓（CDP）。&#x20;

在铸造Acala Dollar时，你需要输入这些参数

* 选择抵押品的类型，例如：DOT&#x20;
* 要存入的抵押品的数量 &#x20;
* 要铸造的Acala Dollar的数量

请注意：该协议并不直接记录Acala Dollar的铸币量，而是记录一个借方单位，包含Acala Dollar铸币量加上累计稳定费等。&#x20;

进一步了解关键参数，请点击这里

### Extrinsics

这是用于铸造Acala Dollar的Extrinsics（交易）

&#x20; `1 honzon.adjustLoan(currency_id, collateral_adjustment, debit_adjustment)`&#x20;

## 更新Acala Dollar金库/贷款&#x20;

一旦你铸造了Acala Dollar并创建了金库，你可以通过以下方式更新它：

1. **铸造更多的Acala Dollar**，如果金库里有足够的抵押品的话&#x20;
2. **偿还已经铸造的Acala Dollar（欠款）**，这将增加当前的抵押品比例且减少需要支付的稳定费用&#x20;
3. **提取抵押品**，只有未使用的抵押品才能被提取出来&#x20;
4. **存入抵押品**，以增加抵押品比率（会使得在相关资产价格大幅波动的情况下，依然保持安全），可有选择地铸造更多的Acala Dollar&#x20;

### Extrinsics&#x20;

这是用于更新Acala Dollar金库的Extrinsics（交易）。同样的Extrinsics也被用来铸造Acala Dollar（新开一个金库）。

```
honzon.adjustLoan(currency_id, collateral_adjustment, debit_adjustment)
```
