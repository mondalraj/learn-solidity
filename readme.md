# Blockchain Development Notes

## What is Blockchain Technology?
Blockchain is a distributed (every system has copy of the block stored) immutable (cannot be changed) ledger (record book) which is completely transparent.  
This is decentralized system.

### Applications of Blockchain
- Product Tracking
- Smart Contracts
- Healthcare System
- International Wire Transfer
- and there are tons as well..

### Blockchain hashing Algorithm
Hash code is generated using **SHA 256 Algorithm**
A Block consists of following attributes -> block no, data, previous hash, hash, etc..
First Block of the blockchain is called **Genesis Block**
A new block hash is generated using data in contains and previous hash.

Docs, Audio, Video etc.. -> SHA 256 Algo -> Hashed Code (It has 64 hexadecimal characters, each character is of 4 bits, Total it has 256 bits.)

> 5 Requirements of Hash Algorithm
- One way (Data cannot is regain from encrypted data)
- Deterministic (Same output should be generated for the same input, output should not change)
- Fast Computation (Algo should be fast)
- Withstand Collision (Cannot be hacked easily by Hackers)
- Avalanche Effect (Output should change completely if data is manipulated)

### Blockchain Immutable Ledger
If any block is tampered by hacker on a system,
then all the data/hash code of the next blocks will be changed automatically because it is connected to previous block hash.
And a block is copied on every system which uses blockchain.
So, even if it changed all systems will notify that something wrong happened.
It this way it is impossible to manipulate data by hackers.

### What is a P2P Network?
Centralized Network -> Data is stored in single server, and server sends data as a response to client. I.E. easily hackable

In Distributed P2P network there is no centralized server. Data is stored in every peer server, so an individual can take data from any on the peers, so if by chance a data is hacked from an individual, others will have the actual data which cannot be manipulated.

If a block is added in single's blockchain then the miners/peers associated with that peer also adds the block in their blockchain after verification and it goes on like this till last peer.

We can recover the corrupt data from different peers using P2P network if the data by chance gets manipulated by the hacker.
Blocks which are in majority will dominate.

### Blockchain Mining
If a cryptocurrency transaction take place, then that transaction is stored in mempool.
Miners pick the transation from the mempool and start solving the mathematical problem which is given to them.
All the miners have to solve a mathematical problem, and the miner who solved the problem is verified by other miners and if it is correct then block is added to blockchain and that miner is rewarded.

Blockchain mining is necessary because there is no central authority, so it generates validation and trust.

### Byzantine Generals Problem
What the majority will say, that will happen no matter what.
We will listen to 2/3rd of population.

### Consensus Protocol
Types ->
- Proof Of Work
- Proof Of Stake
- Others

It is used to prevent attacks on blockchain maily while adding malicious blocks.
When a node is added all the miners have to verify the authenticity of the block by running an algorithm.
Solving a mathematical problem for miners, is time, effort and money taking process so if they add malicious blocks they are not rewarded and it have a loss on the hacker.

## What is Ethereum?
Ethereum is an open-source blockchain-based platform.
Ethereum currency -> Ether
An decrentralized application which allows you to run a program on blockchain.

### Nodes in Ethereum
> Types of Nodes
- Full Node (Locally stores a copy of the entire blockchain)
- Light Node (Stores only the block header, Depends on full node. For low capacity devices which cannot afford to store the gb's of data)
- Archive Node (Stores everything kept in full node and built an archive of historical data. Requires tetabytes of diskspace)

### Ethereum Accounts
An entity with an ether (ETH) balance that can send or receive transactions on Ethereum.

> Types of Ethereum Accounts
- Externally Owned Account (EOA)  
Whenever a wallet is created EOA is created which can be accessed by Private key.
EOA is used to send/receive transaction and to interact with Smart Contracts.  
- Contract Account (CA)  
Controlled by contract code.
When a smart contract is deployed on ethereum blockchain then contract account is created.

### Smart Contract
A program that run on Ethereum blockchain.  
Mainly (if-else) contition program.  
> Each node has the following :-
- Current state of all smart contracts.
- History of both transaction and smart contract.

### Decentralized Apps (Dapps)
Dapps -> Smart Contract (Backend) + Frontend  
> Diff b/w Centralized and decentralized apps
Centralized Apps : Not trustworthy, censorship, you pay, go down.
Dapps : Trusthworthy, no censorship, they pay, can never go down.

### Ethereum Virtual Machine (EVM)
It is used to protect the attack of viruses and hackers in our system.
Every program on ethereum runs on EVM not directly on system so that if any hacker adds a new block on virus on the blockchain so it cannot harm our system.

### Ethereum Gas
It is a fees which is used to run a program on ethereum blockchain.
More the number of operations, more the gas is required.
Eg. 
10 * 3 - 6 = ?
Multiplication - 5gas, Subtraction - 3gas, equal to - 3 gas.
Total gas = 5 + 3 + 3 = 11 gas unit
[Ethereum Gas Costs](https://github.com/djrtwo/evm-opcode-gas-costs/blob/master/opcode-gas-costs_EIP-150_revision-1e18248_2017-04-12.csv)

- Any transaction that modifies the blockchain costs gas.
- The user that generated the transaction pays for the gas.

### Ethereum Gas Price
It is the amount the sender wants to pay per unit of gas to get the transaction mined, gasPrice is set by the sender.  
Gas Price are denoted in gwei. ( 1gwei = 10^-9 ETH )

Eg. 1 gas price = 10 gwei

The higher the gas price the faster the transaction will be mined.

### Ethereum Gas limit
It is the maximum gas the transaction can consume.
Set by the sender.

Example - 
Let say A wants to send B 2 ETH. So what will be the total fees A that has to pay?
- A set the gas price per unit = 100 gwei
Transaction gas limit = 21,000 units
> Total fee will be: Gas units(limit) * Gas price per unit

Total fee will be : 21,000 * 100 = 210,000 gwei or 0.0021ETH

### Ethereum Block