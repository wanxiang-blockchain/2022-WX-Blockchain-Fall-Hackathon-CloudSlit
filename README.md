# 2022-WX-Blockchain-Fall-Hackathon-CloudSlit

- [2022-WX-Blockchain-Fall-Hackathon-CloudSlit](#2022-wx-blockchain-fall-hackathon-cloudslit)
- [灵感](#灵感)
- [它的作用](#它的作用)
- [我们如何建造它](#我们如何建造它)
  - [第一部分:CloudSlit-Fullnode（数据的私人检索网络全节点 - Dao Tools）](#第一部分cloudslit-fullnode数据的私人检索网络全节点---dao-tools)
  - [第二部分:CloudSlit-Provider（去中心化的数据私人检索安全网络隧道提供商 - Network Miner）](#第二部分cloudslit-provider去中心化的数据私人检索安全网络隧道提供商---network-miner)
  - [第三部分:CloudSlit-Contracts](#第三部分cloudslit-contracts)
  - [第五部分：CloudSlit-verifier(去中心化网络质量校验者)](#第五部分cloudslit-verifier去中心化网络质量校验者)
  - [第五部分:CloudSlit-Client（数据的私人检索网络客户端）](#第五部分cloudslit-client数据的私人检索网络客户端)
- [我们遇到的挑战](#我们遇到的挑战)
- [我们引以为豪的成就](#我们引以为豪的成就)


# 灵感

目前可用于具有隐私保证的交互式(低延迟)通信的选项非常有限，并且迄今为止开发的解决方案都集中在单一源数据发布者的传统web模型上，并且在延迟和威胁模型方面，它都具有缺陷。

CloudSlit使用区块链、web3和数据的私人检索安全网络技术来增强和改善用户私有化网络安全/隐私的平衡。

为了保护web2下公众的网络安全，出现了非常流行的零信任安全架构。我们团队一直在做零信任安全方向的开源产品，但是我们发现很多零信任网络安全公司虽然提供零信任安全平台，但是他们垄断用户的网络接入节点，集中存储用户的核心安全配置文件。因此，我们正在考虑是否可以使用web3技术来实现数据的私人检索安全网络。我们设计了CloudSlit项目，为用户提供去中心化的私人数据检索安全网络平台，帮助用户掌握自己的安全数据。

# 它的作用

CloudSlit旨在构建全球web3去中心化的数据的私人检索安全网络体系，帮助用户夺回web2下被巨头侵蚀的隐私安全信息，让目前全球火热的零信任安全网络技术结合web3更好地帮助用户掌握自己的安全隐私数据，给用户良好的数据的私人检索安全网络产品和平台体验。


# 我们如何建造它

CloudSlit项目的设计部分包括分散式全节点、网络矿工提供商、智能合约、网络质量校验者、网络客户端程序。具体设计介绍如下:

## 第一部分:[CloudSlit-Fullnode](https://github.com/wanxiang-blockchain/2022-WX-Blockchain-Fall-Hackathon-CloudSlit/tree/main/codes/fullnode)（数据的私人检索网络全节点 - Dao Tools）

任何人都可以运行Fullnode，它托管去中心化网络的元数据，并提供元数据联网和事务匹配平台。它集成了来自所有提供者的元数据，提供者每隔几秒钟使用基于[libp2p的pubsub](https://github.com/libp2p/go-libp2p)向Fullnode保持心跳，以证明他们在线。

用户可以找到资源和节点来构建自己的安全匿名网络隧道。他们只需要支付一些代币，提供者节点就可以得到这些代币作为奖励。

对于所有用户和Dao的数据，我们使用Filecoin的web3.storage对用户数据进行去中心化存储。

<img width="929" alt="image" src="https://user-images.githubusercontent.com/34047788/190649560-9bb3d443-3a3e-4747-8805-931c79db55b0.png">


## 第二部分:[CloudSlit-Provider](https://github.com/wanxiang-blockchain/2022-WX-Blockchain-Fall-Hackathon-CloudSlit/tree/main/codes/provider)（去中心化的数据私人检索安全网络隧道提供商 - Network Miner）

我们的节点通过libp2p的kademlia DHT和IPFS网络通过对等点发现和路由实现自动组网，通过libp2p的PubSub函数实现多个节点之间的数据同步。
对于所有用户和Dao数据，我们使用Filecoin的web3.storage对用户数据进行分散存储。

<img width="952" alt="image" src="https://user-images.githubusercontent.com/34047788/190649367-aea3230f-6c87-4b74-b692-e328ed33a78f.png">


## 第三部分:[CloudSlit-Contracts](https://github.com/wanxiang-blockchain/2022-WX-Blockchain-Fall-Hackathon-CloudSlit/tree/main/codes/contract)

我们为去中心化可信带宽市场提供了完整的智能合约，我们的智能合约部署在**万纳链**节点上，我们在智能合约中提供了许多方法来确保安全的交易流程和安全的交易环境。

我们的万纳链RPC地址为http://66.42.43.202:6791

合约地址是0x4E9bfAB50AE5aA47838921450BBc1b12a81798ba

## 第五部分：[CloudSlit-verifier](https://github.com/wanxiang-blockchain/2022-WX-Blockchain-Fall-Hackathon-CloudSlit/tree/main/codes/verifier)(去中心化网络质量校验者)
我们为去中心化可信带宽市场提供了verifier组件，任何人都可以运行网络检验者，对于正在进行的订单进行网络质量的监控，对于非法及恶劣网络提供者进行检测并惩罚。

<img width="935" alt="image" src="https://user-images.githubusercontent.com/34047788/190649698-9a48853b-aae4-4951-9ffe-f18ae23e8fc9.png">



## 第五部分:[CloudSlit-Client](https://github.com/wanxiang-blockchain/2022-WX-Blockchain-Fall-Hackathon-CloudSlit/tree/main/codes/client)（数据的私人检索网络客户端）

客户端软件用户连接到提供商以建立零信任网络安全隧道。

<img width="932" alt="image" src="https://user-images.githubusercontent.com/34047788/190649859-ee288f05-3581-4323-b672-de9546f8758d.png">



# 我们遇到的挑战

1.建立一个稳定的分散网络

2.构建一个去中心化的pubsub信令机制，满足网络矿工和全节点之间网络隧道动作的协调。

3.构建用户安全规则数据的分散存储和加密解密。

# 我们引以为豪的成就

我们已经能够满足选择去中心化网络隧道矿工的用户，创建智能合约订单，支付订单，自动构建数据的私人检索双向网络隧道，享受全栈去中心化数据的私人检索网络安全隧道体验，这是我们最大的喜悦。