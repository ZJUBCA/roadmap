# Consortium Blockchain-roadmap 2023

联盟链学习路线总结，不断更新。

—— By 浙江大学区块链协会（Zhejiang University BlockChain Association, ZJUBCA）

## 第一层

- **基本概念**：
  - 什么是公有链、联盟链和私有链？(万向区块链实验室动画教程) [🔗](https://v.qq.com/x/page/a0328vol40v.html)
  - Blockchain Consortium: Advantages And Disadvantages[🔗](https://dataconomy.com/2023/01/blockchain-consortium-advantages/)
  - A Complete Guide to Consortium Blockchain And Its Features[🔗](https://www.analyticsvidhya.com/blog/2023/01/a-complete-guide-to-consortium-blockchain-and-its-features/)
  - Everything You Need To Know About Consortium Blockchain[🔗](https://www.blockchain-council.org/blockchain/everything-you-need-to-know-about-consortium-blockchain/)
- **解读与讨论**：
  - 联盟链战国：五大巨头横向对比 [🔗](https://www.infoq.cn/article/5-consortium-blockchain-comparison/)
  - 基于联盟链技术的隐私保护金融应用研究报告 [🔗](https://www.bfia.org.cn/upload/file/20221201/1669860599908060153.pdf)
  - 研报：连通公链和联盟链的研究 [🔗](https://www.8btc.com/article/6582723)
  - 安全问题成短板，联盟链发展背后的安全如何保障？[🔗](https://www.chainnews.com/articles/576303926328.htm)
  - 联盟链智能合约安全浅析 [🔗](https://paper.seebug.org/1317/)
  - 怎样让你的区块链更加安全可控[🔗](https://fisco-bcos-documentation.readthedocs.io/zh_CN/latest/docs/articles/1_conception/safe_and_controllable.html)
  - 盘点国内联盟链及现状 [🔗](https://zhuanlan.zhihu.com/p/519283107)

## 第二层

- **技术原理**

  - 共识机制

    - 区块链共识机制浅谈：[🔗](https://blog.csdn.net/jeffrey__zhou/article/details/56672948)
    - [区块链] 共识算法之争（PBFT，Raft，PoW，PoS，DPoS，Ripple）:[🔗](https://www.cnblogs.com/X-knight/p/9157814.html)
    - 深度分析 Raft 的主要特点：[🔗](https://mp.weixin.qq.com/s/yxJNsFzhpShzRvU9djhTjQ)
    - Paxos，Raft，Zab 一致性协议-Raft 篇：[🔗](https://mp.weixin.qq.com/s/5EZ2_vIzHEymJPxeSZtlmg)
    - 深入剖析区块链的共识算法 Raft & PBFT：[🔗](https://mp.weixin.qq.com/s/ITCaMKdYrdlvQ0IGW3qpKg)

  - 密码学相关

    - RSA、ECC、国密等加密算法
    - 数字签名
    - 零知识证明
    - 多方安全计算

  - 网络通信

    - 联盟链网络专栏(Hyperledger Fabric)：[🔗](https://hyperledger-fabric.readthedocs.io/zh_CN/latest/network/network.html)
    - 【网络专栏】联盟链的通信安全如何保障？：[🔗](https://tech.hyperchain.cn/wang-luo-zhuan-lan-lian-meng-lian-de-tong-xin-an-quan-ru-he-bao-zhang/)

  - 存储相关

    - IPFS：[🔗](https://docs.ipfs.tech/)
    - 传统数据库如 mysql、CouchDB、MongoDB 等

  - 智能合约

    - 智能合约初探：概念与演变：[🔗](https://fisco-bcos-documentation.readthedocs.io/zh_CN/latest/docs/articles/3_features/35_contract/smart_contract_concept_and_evolution.html)
    - 联盟链的智能合约多采用 go、java 等语言编写，不同联盟链框架对合约语言的支持不同，可根据需要进一步学习

- **源码分析**

  - 《Hyperledger Fabric 源代码分析与深入解读》
  - Hyperledger Fabric v2.x 最新资料汇总[🔗](https://hello2mao.github.io/2020/04/22/hyperledger-fabric-v2.x-info/)
  - Fabric2.2 中的 Raft 共识模块源码分析[🔗](https://www.cnblogs.com/GarrettWale/p/16131853.html)
  - 深入浅出 FISCO BCOS[🔗](https://fisco-bcos-documentation.readthedocs.io/zh_CN/latest/docs/articles/index.html)
  - FISCO BCOS 核心模块设计解析[🔗](https://fisco-bcos-documentation.readthedocs.io/zh_CN/latest/docs/design/index.html)

## 第三层

- **联盟链实例**
  - Hyperledger Fabric
    - Hyperledger Fabric 是由 Linux 基金会支持的开源项目，提供了一种可扩展、可定制和安全的联盟链技术。
    - 官网：[🔗](https://www.hyperledger.org/use/fabric)
    - paper:[🔗](https://arxiv.org/pdf/1801.10228.pdf)
    - 官方文档：[🔗](https://hyperledger-fabric.readthedocs.io/en/release-2.5/)
    - 中文文档：[🔗](https://hyperledgercn.github.io/hyperledgerDocs/)
    - 中文视频 Tutorial：[🔗](https://wiki.hyperledger.org/display/TWGC/Fabric+Video+Tutorial)
    - FAQ：[🔗](https://github.com/Hyperledger-TWGC/FAQ)
    - 博客(Hyperledger Fabric 2.0 系列)：[🔗](https://blog.csdn.net/qq_28540443/article/details/104265844)
    - 电子书《区块链技术指南》:[🔗](https://github.com/yeasy/blockchain_guide)
    - 电子书《Hyperledger 源码分析之 Fabric》:[🔗](https://github.com/yeasy/hyperledger_code_fabric)
  - R3 Corda(金融行业)
    - R3 Corda 是一种用于金融行业的联盟链技术，提供了一种可扩展、安全和隐私保护的方法。
    - 官网：[🔗](https://r3.com/products/corda/)
    - white paper：[🔗](https://r3.com/blog/corda-technical-whitepaper/)
    - 官方文档：[🔗](https://docs.r3.com/)
    - 中文文档：[🔗](https://cncorda.readthedocs.io/zh_CN/latest/index.html)
    - developer training:[🔗](https://training.corda.net/)
    - FAQ:[🔗](https://docs.r3.com/en/platform/corda/4.9/enterprise/notary/faq/toctree.html)
  - FISCO BCOS(国内金链盟)
    - FISCO BCOS 是由国内企业主导研发、对外开源、安全可控的企业级金融联盟链底层平台，由金链盟开源工作组协作打造，并于 2017 年正式对外开源。
    - 官网：[🔗](https://www.fisco.com.cn/fisco_20.html)
    - white paper:[🔗](https://github.com/FISCO-BCOS/whitepaper)
    - 中文文档：[🔗](https://fisco-bcos-documentation.readthedocs.io/zh_CN/latest/)
    - 英文文档：[🔗](https://fisco-bcos-documentation.readthedocs.io/en/latest/index.html)
    - 博客：[🔗](https://www.wanghaoyi.com/fisco-bcos-learning.html)
    - FAQ：[🔗](https://fisco-bcos-documentation.readthedocs.io/en/latest/docs/faq/faq.html)
  - Quorum(基于以太坊代码库)
    - Quorum 是由美国金融机构摩根大通推出的企业级分布式账本和智能合约平台，可看作企业版的以太坊。它是基于以太坊分布式账本协议开发而成，为金融服务行业提供以太坊许可链方案，以便支持交易与合约的隐私性。
    - 官网：[🔗](https://quorum.com/)
    - white paper:[🔗](https://github.com/ConsenSys/quorum/blob/master/docs/Quorum%20Whitepaper%20v0.2.pdf)
    - 官方 Tutorial：[🔗](https://docs.goquorum.consensys.net/)
- **应用实例**
  - 金融服务：
    - 项目：taXchain - A blockchain network to exchange digitized tax forms(Hyperledger Fabric)[🔗](https://www.hyperledger.org/learn/publications/taxchain-case-study)
    - 项目：fragmos chain - Digitizing interactions between OTC derivatives market participants(R3 Corda)[🔗](https://r3.com/case-studies/fragmos-chain/)
    - 项目：Spunta - Revolutionizing the interbank reconciliation process in Italy(R3 Corda)[🔗](https://r3.com/case-studies/spunta/)
    - 项目：广东国税税链项目（蚂蚁链）[🔗](https://guangdong.chinatax.gov.cn/gdsw/gzsw_swxw/2021-10/08/content_323f08675f604b629f233b5f38707d91.shtml)
    - 项目：浙江区块链电子票据平台（蚂蚁链）[🔗](https://www.zjzwfw.gov.cn/col/col1228922696/)
  - 供应链管理：
    - 项目：KrypC - Managing the Metal and Mining Industry’s Supply Chain(Hyperledger Fabric)[🔗](https://www.hyperledger.org/learn/publications/krypc-minehub-case-study)
    - 项目：gavea - Automating the commodity trading process(R3 Corda)[🔗](https://r3.com/case-studies/gavea/)
    - 项目：axedra - Connecting and digitizing the precious metals industry(R3 Corda)[🔗](https://r3.com/case-studies/axedras/)
  - 电子政务：
    - 项目：澳门智慧城市-证书电子化（FISCO BCOS）
    - 项目：山东省荣成市区块链政务诚信管理系统（FISCO BCOS)
    - 项目：安徽区块链电子证照应用（蚂蚁链）[🔗](https://sft.ah.gov.cn/public/7061/53866131.html)
  - 智慧医疗：
    - 项目：LedgerDomain - The Right Rx for the Pharmaceutical Supply Chain(Hyperledger Fabric)[🔗](https://www.hyperledger.org/learn/publications/ledgerdomain-case-study)
    - 项目：武汉市中心医院/上海华山医院-区块链医疗电子处方（蚂蚁链）[🔗](https://developer.aliyun.com/article/697162)
  - 版权保护：
    - 项目：人民版权-区块链版权保护平台（FISCO BCOS）[🔗](https://www.peoplec.cn/)
    - 项目：雀凿数字版权服务平台（蚂蚁链）[🔗](https://www.mydcs.com/pages/index?channelCode=WBLT)
  - 其他：
    - 项目：Sony Global Education - a Next-Generation Credentials Platform(Hyperledger Fabric)[🔗](https://www.hyperledger.org/wp-content/uploads/2017/12/Hyperledger_CaseStudy_Sony.pdf)
    - 项目：绿色出行普惠平台-绿色碳交易积分区块链（FISCO BCOS)
