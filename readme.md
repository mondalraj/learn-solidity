# Blockchain Development Notes

### What is Blockchain Technology?
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