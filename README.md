
分析完yearn的ETH Vault合约代码，并找来其中一个策略(Strategy)合约代码分析。yearn被业界叫做收益聚合器(yield aggregator)或者机枪池，我觉得Vault(本意为储蓄罐)更像是主动管理的公募基金，两者有不少类似地方： 
 1）治理人决定储蓄罐资产的投资标的和投资比例，而公募基金是由所在的基金经理来管理
 2） 购买公募基金，通过法币申购获取的对应基金份额，赎回时根据份额和净值换回法币。存入币到Vault获取对应份额的yToken，赎回时根据yToken份额返回对应币的数量,3) 治理人定期生成Valut报告 ，基金经理生成季度投资报告
 3） 用户发起赎回时，先从Vault本币余额赎回，如果本币余额不够，则从投资策略里赎回。公募基金也差不多类似逻辑，先用公募基金的现金给用户赎回，如果现金不够，则需要将底层资产卖出，再给用户赎回

| 合约名称 | 地址 | 文件 |
| --- | --- | --- |
| Yearn multiSig | 0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52 | contracts/yearn multisig.sol |
| Yearn WETH Vault | 0xa258C4606Ca8206D8aA700cE2143D7db854D168c | contracts/yearn WETH yVault.vy |
| Yearn WETH Vault-Strategy-Lido | 0x120FA5738751b275aed7F7b46B98beB38679e093 | contracts/yearn StrategystETHAccumulator_v2.sol |
| Yearn V2 registry| 0xa258C4606Ca8206D8aA700cE2143D7db854D168c | contracts/yearn v2 registry.vy |


