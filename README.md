# 2022-WX-Blockchain-Fall-Hackathon-CloudSlit

# Inspiration

The options currently available for interactive (low-latency) communication with privacy guarantees are very limited, and the solutions developed to date have focused on the traditional web model of a single-source data publisher, and in terms of the latency and threat models it incurs All have flaws. 

CloudSlit uses blockchain, web3, and zero-trust security network technologies to enhance and improve the balance of user privatization network security/privacy. 

In order to protect the network security of the public under web2, a very popular zero-trust security architecture has emerged. Our team has been working on open-source products in the direction of zero-trust security, but we found that although many zero-trust network security companies provide zero-trust security platforms, they monopolize users' network access nodes and centrally store users' core security configuration files. Therefore, we are thinking about whether we can use web3 technology to enable zero trust security network. We designed the CloudSlit project to provide users with a decentralized zero-trust secure network platform to help users master their own secure data.

# What it does

CloudSlit aims to build a global web3 decentralized zero trust security network system to help users regain the private security information eroded by giants under web2, so that the current global hot zero trust security network technology can better help users master their own security privacy data in combination with web3, and give users a good zero trust security network products and platform experience.

# How we built it

The design part of the CloudSlit project includes decentralized full nodes, network miner providers, smart contracts, and network client programs. The specific design introduction is as follows:

### Part one: [CloudSlit-Fullnode](https://github.com/CloudSlit/cloudslit/tree/main/fullnode)（Zero Trust Secure Data Management Platform - Dao Tools）

Anyone can run a Fullnode, which hosts the metadata of the decentralized network, and provides a metadata networking and transaction matching platform.It integrates metadata from all Providers and Providers  keep heartbeat to Fullnode every few seconds using pubsub based on [libp2p](https://github.com/libp2p/go-libp2p) to prove they are online.

Users can find resources and nodes to build their own secure and anonymous network tunnel.They just need to pay a few tokens and the Provide who provides node can get these token as rewards.

For all users and Dao's data, we use Filecoin's web3.storage decentralized storage of user data.

![https://user-images.githubusercontent.com/52234994/179184171-f881f3ee-e7ca-45ad-94e1-813b9964e524.png](https://user-images.githubusercontent.com/52234994/179184171-f881f3ee-e7ca-45ad-94e1-813b9964e524.png)

### Part two: [CloudSlit-Provider](https://github.com/CloudSlit/cloudslit/tree/main/provider)（Decentralized Zero Trust Secure Network Tunnel Provider - Network Miner）

Our nodes realize automatic networking through peer discovery and routing through libp2p kademlia DHT and IPFS networks, and realize data synchronization between multiple nodes through libp2p's PubSub function.
For all user and Dao data, we use Filecoin's web3.storage for decentralized storage of user data.

![https://user-images.githubusercontent.com/52234994/179186444-81e0f4de-a2c1-4607-bf66-275d20c2fe0c.png](https://user-images.githubusercontent.com/52234994/179186444-81e0f4de-a2c1-4607-bf66-275d20c2fe0c.png)

### Part three: [CloudSlit-Contract](https://github.com/CloudSlit/cloudslit/tree/main/contract)

We develop smart contracts based on the OpenZeppelin library, follow the ERC20 token standard and use OpenZeppelin Upgrades to write upgradeable contracts.
Our smart contracts are deployed on the Ethereum testnet. We provide many methods in smart contracts to ensure a secure transaction process and a secure transaction environment.

### Part four: [CloudSlit-Client](https://github.com/CloudSlit/cloudslit/tree/main/client)（Zero Trust Secure Network Access Client）

The client software user connects to the provider to establish a zero trust network security tunnel.

![https://user-images.githubusercontent.com/52234994/179190148-ebd19f1d-90f0-4377-a57d-7c4942d5e0b3.png](https://user-images.githubusercontent.com/52234994/179190148-ebd19f1d-90f0-4377-a57d-7c4942d5e0b3.png)

# Challenges we ran into

1. Build a stable decentralized network
2. Build a decentralized pubsub signaling mechanism to meet the coordination of network tunnel actions between miners and full nodes.
3. Build decentralized storage and encryption and decryption of user security rules data.

# Accomplishments that we're proud of

We have been able to satisfy users who choose decentralized network tunnel miners, create smart contract orders, pay orders, automatically build zero-trust two-way network tunnels, and enjoy full-stack decentralized zero-trust network security tunnel experience, which is our greatest joy and pride.

CloudSlit helps users regain control of their zero-trust security data and helps users experience the advantages of web3.

CloudSlit has gained a lot of downloads since it was open sourced.

![https://res.cloudinary.com/malloc/image/upload/v1659597089/cloudslit/Untitled_paimfj.png](https://res.cloudinary.com/malloc/image/upload/v1659597089/cloudslit/Untitled_paimfj.png)

# What we learned

1. Decentralized networking technology based on IPFS libp2p
2. Decentralized data storage technology based on web3.storage.
3. Based on the core program logic of smart contracts.

# What's next for

1. Optimize smart contracts to reduce gas costs.
2. Build more CloudSlit network miner nodes to enrich CloudSlit's decentralized network.
3. Build a user community and let more interested users participate in the use.
4. The open source community that builds the program, returns control of the program to the open source community.