# Student 1951 - Lesson 1 Submission

This folder contains screenshots of the completed work for Lesson 1 from liumeng.


---------------------------------

## 1. 安装三种不同的钱包，创建测试账户。

### 1.1 MetaMask

> Ethereum: 0xDAA5A34D500799935C065282D24853e467D0497c

![1.1.metamask.png](assets/1.1.metamask.png)

### 1.2 Talisman

> Ethereum: 0xA75Aab290Be63b6e22A3fD98E2a4d928D758d689

![1.2.talisman.png](assets/1.2.talisman.png)

### 1.3 SubWallet

> Ethereum: 0x4A622DaB8485AbaF718Fa40073747EE13d7110df
> Paseo testnet: 15qdkk1xcCxFwC9xB1BN436cDxUQ8pM3m2GKRfG1VnbxmRJF

![1.3.subwallet.png](assets/1.3.subwallet.png)

---------------------------------

## 2. 本地编译Polkadot SDK，启动节点和RPC服务

- 编译：
	- cargo build --release -p pallet-revive-eth-rpc
	- cargo build --release --bin substrate-node
- 启动：
	- target/release/substrate-node --dev --tmp
	- target/release/eth-rpc

![ 2.1.substrate_node.png ](assets/2.1.substrate_node.png)

![ 2.2.eth_rpc.png ](assets/2.2.eth_rpc.png)

---------------------------------

## 3. https://faucet.polkadot.io/?parachain=1110 得到测试token

![ 3.faucet_got_token.png ](assets/3.faucet_got_token.png)


### 3.1 metamask wallet 领取testnet token:
metamask - settings - network - Add a custom network - Default RPC URL: 
    https://testnet-passet-hub-eth-rpc.polkadot.io

把Ethereum的地址输入上述水龙头，获得token

Tokens: 4,999.989 

![ 3.1.metamask_wallet_got_token.png ](assets/3.1.metamask_wallet_got_token.png)


### 3.2 talisman wallet 领取testnet token:

receive - network - paseo / Paseo Asset Hub - copy address - 到上述水龙头获取testnet token

talisman中不显示该token余额，因为创建的account是polkadot的

把talisman钱包的助记词导入metamask，选择新导入的wallet - receive - network选择刚才添加的testnet - 复制地址，到上述水龙头获取testnet token，可以查询到Tokens: 4,999.989 PAS

又在talisman创建一个eth account:eth_account1此时可以看到余额了：5000 PAS
eth_account1: 0xA75Aab290Be63b6e22A3fD98E2a4d928D758d689

在线查询： https://paseo.subscan.io/

输入地址，查询结果最底部有一条信息：Crosschain Transfer (1)

可以查询到Tokens: 4,999.989 PAS


![ 3.2.talisman_wallet_got_token.png ](assets/3.2.talisman_wallet_got_token.png)


### 3.3 subwallet wallet 领取testnet token:

got address - paseo testnet - copy address - 到上述水龙头获取testnet token

但是subwallet不显示，需要添加token: PAS，等一会儿就显示了

在线查询： https://paseo.subscan.io/

输入地址，查询结果最底部有一条信息：Crosschain Transfer (1)

可以查询到Tokens: 4,999.989 PAS

![ 3.3.subwallet_wallet_got_token.png ](assets/3.3.subwallet_wallet_got_token.png)


### 3.4 注意

#### 3.4.1 这里有两种地址格式

metamask提供的的地址格式是eth address，和substrate address的不同：

- The Polkadot Faucet at faucet.polkadot.io often requires a Substrate (SS58) address, but MetaMask gives you an Ethereum (H160) address (starting with 0x).

- Since you are working with pallet-revive (the new EVM-compatible layer for Polkadot), you actually have two ways to query balances: the Ethereum way (for MetaMask) and the Substrate way (for SubWallet/Talisman).

#### 3.4.2 用任何一种钱包，创建account的时候，尽量选择eth

#### 3.4.3 faucet领水时选择的testnet和代码中的rpc-url必须匹配

---------------------------------

## 4. 分别在钱包中和运行程序 [https://github.com/papermoonio/2026-h1-building-production-grade-dApps/blob/main/course/lesson-1/src/index.ts](https://github.com/papermoonio/2026-h1-building-production-grade-dApps/blob/main/course/lesson-1/src/index.ts) 确认token领取成功

### 4.1 通过typescript代码获取账户余额
	- npm init -y
    - npm install ethers @polkadot/api
	- npm install -D typescript ts-node @types/node
	- src/index.ts
        - 选择和testnet对应的rpc-url：https://testnet-passet-hub-eth-rpc.polkadot.io
            代码里测试网url 要改成和钱包一样的测试网地址
		- 修改钱包地址：注意看清楚，eth account address还是substrate account address
            substrate 和 talisman 代码需要修改, 和 metamask 不一样
	- npx ts-node src/index.ts
    ![ 4.1.checkBalance.by.typescript.png ](assets/4.1.checkBalance.by.typescript.png)


### 4.2 通过钱包工具代码获取账户余额
    - 通过metamask获取账户余额：
    ![ 3.1.metamask_wallet_got_token.png ](assets/3.1.metamask_wallet_got_token.png)
    - 通过talisman获取账户余额
    ![ 3.2.talisman_wallet_got_token.png ](assets/3.2.talisman_wallet_got_token.png)
    - 通过subwallet获取账户余额
    ![ 3.3.subwallet_wallet_got_token.png ](assets/3.3.subwallet_wallet_got_token.png)



结果截图通过PR提交到  https://github.com/papermoonio/2026-h1-building-production-grade-dApps/tree/main/homework/lesson-1


---------------------------------

