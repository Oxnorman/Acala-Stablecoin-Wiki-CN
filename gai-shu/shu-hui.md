# 赎回

## 关闭Acala Dollar金库&#x20;

有两种方法可以关闭Acala Dollar金库&#x20;

* **偿还所有**铸造的Acala Dollar来关闭金库
* **使用可用的抵押品来偿还**，当你手头没有足够的Acala Dollar来偿还贷款时，就可以用这个方法。系统会自动将你的抵押品通过AcalaSwap兑换成Acala Dollar，一次性偿还债务。

## Extrinsics

1. 偿还确切的金额

```
honzon.adjustLoan(currency_id, collateral_adjustment, debit_adjustment)
```

&#x20; 2.用可用的抵押品来偿还

```
honzon.closeLoanHasDebitByDex(currency_id, maybe_path)
```

\[honzon协议 [代码](https://github.com/AcalaNetwork/Acala/tree/master/modules/honzon)]
