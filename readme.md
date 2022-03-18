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