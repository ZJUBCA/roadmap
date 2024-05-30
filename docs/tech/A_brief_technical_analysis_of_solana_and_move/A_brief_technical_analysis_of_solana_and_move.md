# Overview

-   Solana:以高性能著称，吞吐量高、延迟低、交易成本低、可扩展性强

-   Aptos:注重安全性和可扩展性，使用面向资源设计的move语言，灵活性、可组合性强

    ![img](./img/overview.png)

# Account model - Ethereum

-   在以太坊中，账户分为外部账户和合约账户
-   对于合约账户来说，合约代码和状态数据存储不分离

![img](./img/Account model-Ethereum.png)

-   这会带来系统性的跨合约调用安全性问题，如delegate call，本质是因为合约代码和数据存储不分离，用外部合约代码逻辑来修改本合约的数据存储本身就有很大风险
-   同时，合约升级非常麻烦（尽管有代理模式可以在一定程度上解决这个问题），但由于以太坊的账户模型设计，无法原生支持合约“原地”升级
-   EVM的设计是单核的，无法充分利用多核计算资源来提高交易处理并行度，因此性能非常拉胯

![img](./img/Account storage-Ethereum.png)

# Account model - Solana

-   在Solana中，万物皆“账户”
-   Solana的合约是无状态的，不存储任何数据/状态

![img](./img/Account model-Solana.png)

-   Solana的账户分为数据账户和程序账户
    -   数据账户由程序账户创建，用于存储和管理程序（合约）状态
    -   程序账户（合约账户）是存储可执行代码的无状态账户
    -   每个账户都有一个owner，这个owner是一个程序（合约）

![img](./img/AccountInfo-Solana.png)

-   AccountInfo组成：
    -   data:存储账户状态的字节数组，如果是程序账户，则存储可执行程序代码
    -   executable：标识该账户是否是一个程序（合约账户）
    -   lamports：账户余额
    -   owner:拥有该账户的程序的公钥（program ID）

# An example of account model difference

![img](./img/An example.png)

-   程序代码和数据存储解耦分离，使得合约升级变得更容易，也减少了跨合约调用的安全隐患
-   有一个小问题，假设你基于Solana构建了一个dapp，那么必定至少有一个数据账户用于存储状态数据，那这个数据账户的私钥存储在哪里？
-   程序衍生地址PDA(Program Derived Address)(借鉴以太坊将存储附加到程序的思想)

# PDA(Program Derived Address)

![img](./img/PDA.png)

-   PDA账户没有私钥，由控制程序为PDA账户进行签名，主要用于CPI（跨合约调用）
-   输入：program ID、seed，首先经过sha256哈希运算，看是否产生一个位于椭圆曲线上的公钥
-   若是，则加一个bump，从bump=255开始，逐次向下迭代，直到找到一个不在椭圆曲线上的地址
-   解决了数据账户私钥的存储问题，同时做到了程序代码和数据存储解耦分离
-   PDA还可以用来在独立的账户中存储用户的特定信息——通过指定seed(例如用户公钥+代币符号)

# Account model - Aptos

-   在Aptos中，万物皆“对象”，对象模型允许move将复杂类型表示为存储在单个地址内的一组资源，并提供允许细粒度资源控制和所有权管理的丰富功能模型。
    -   如move_to、move_from、borrow_from、borrow_from_mut等
-   Aptos上有三类账户：标准账户、资源账户和对象
    -   资源账户：没有私钥，供开发者存储资源或上链发布模块（合约以模块的形式发布）
    -   对象：存储在代表单个实体的单个地址内的一组复杂资源。
-   每个账户的状态由代码(move模块)和数据(move资源)组成
    -   move模块：包含代码，例如类型和过程声明，但它们不包含数据。
    -   move资源：包含数据但没有代码，每个资源值都有一个在已发布的模块中声明的类型。
-   更高的安全性、更强的资源可组合性

# Conclusion

![img](./img/High-performance Trilemma.png)

-   L1高性能三难问题：可靠性、效率和高性能
-   以太坊花了大量的数据冗余为最坏的情况做准备，带来的负面影响是性能极低
-   Solana选择减少数据冗余度，采用多核进行并行计算，提高出块率，但在极端环境下更容易出故障
-   Aptos的设计选择是在可靠性和性能之间折衷，与之而来的是硬件成本上升（更不去中心化）
-   开发者应充分考虑使用场景来选择底层基础设施，并将未来可能的跨链解决方案和潜在风险考虑在内

# Reference and relevant resources

-   Author:Ni1L
-   Online deck:https://docs.google.com/presentation/d/1IOflojh3PudmualIXS4uaQa-3PfEFvHc-usF5mAlGHI/edit?usp=sharing
-   Online video record:https://drive.google.com/file/d/1WPuzqxTw_Dw_ca_SCgzsB5f-HrT6H46T/view
-   Reference:
    -   https://ethereum.org/en/developers/docs/accounts/
    -   https://solana.com/docs
    -   https://aptos.dev/concepts/
    -   https://learn.aptoslabs.com/example/solana-to-aptos
    -   https://dl.acm.org/doi/abs/10.1145/3548606.3560552
    -   https://antiape.substack.com/p/cf40447d-d674-4454-9e09-f003517de6de?s=r
