# Sharding

+ https://github.com/SebastianElvis/sharding-bib
+ MIT 6.852
+ ethz
    * https://disco.ethz.ch/courses/ss04/distcomp/
    * https://disco.ethz.ch/courses/ss03/distcomp/
    * https://disco.ethz.ch/courses/podc/
    * https://disco.ethz.ch/courses/distsys/
+ MIT 6.S974
    * theoretical
+ MIT 6.824
    * distributed system
+ talent-plan

## 1% Attack

+ 状态分片（智能合约状态同步&数据可用性相关）、交易分片（需要防止双花） 涉及 跨分片通信 和  状态交换，这里不进行讨论
+ 网络分片
    * 节点越多，速度越快吗？不是的
        - 每个节点都要验证所有的交易
        - 不可能三角: security, scalability, decentralization
            + 牺牲一定的 安全性，换取一定的 scalability?
                * 分片! 每个节点只需要验证部分交易
                    - 超级节点 vs 校对节点(collator)
+ PoW
    * security & reliability 好，但 scalability 差
    * 如果进行分片，比如分 100 片，那么分片上的算力只占 全网 1%，也就是说只需要 1% 的算力，就能完全控制该分片(1% 攻击)
        - 其实也有方案解决这个问题，monoxide 连弩挖矿，此处略过
+ PoS
    * 为什么 PoS 不会遇到这个问题
        - 将节点随机分配到分片，防止作恶者将算力汇集到某一分片
            + 无法选择被分配到哪个分片
            + 无法提前知道会被分配到哪一个分片
    * 这算是 ETH 为了分片想转 PoS 的一个原因