<h1>Blockchain-based-File-Storage</h1>



<h2>How to run the application</h2>

1. Install required libraries using :
   `pip install -r requirements.txt`
2. Open one terminal and start server/peer:
   `python peer.py`
3. Open another terminal and start a client:
   `python run_app.py`
4. Copy the link from the client terminal and paste it in any browser.
5. To run our experiment of different Proof of Work concepts:
`python POW_Comparison.py`
<h2> Project Information </h2>
We developed a web-based application for decentralized file storing using blockchain. In this application any user can upload as many files(one at a time) as he/she likes. All other peers and the user himself can download and access those file in their system. File can be of any type and any size. Refer to project demo link to see the detailed explanation. <br />
We are using randomly generated nonce in proof of work concept to acheive the required difficulty (diff = 3). Once peer uploads the file, the file is stored in a block including username, filesize and file data. These block gets appended to the current blockchain, which makes it impossible to edit or delete the file/block.<br /> 
The reason to implement file storing using blockchain is its abilitiy to avoid any modification or deletion. No one can delete or corrupt our files that are stored.


<h2>Importance of Blockchain:</h2>

Blockchain data structure is used to store digital information securely. Blockchain is an open ledger which can be accessed by multiple parties all at once. Blockchain holds various types of digital information such as transaction information, files, messages, etc. The successful implementation of blockchain holds different types of functionalities such as consensus algorithm, mining block, validation of block etc.

As part of this project, we have implemented a blockchain containing file information, which also allows users to upload/download all types of files from publicly available website. It uses SHA256 cryptographic algorithm to ensure that the block is kept secret. As a consensus algorithm, proof of work is implemented, which requires miners to solve any cryptographic puzzle before they get to announce new block on chain. In our application, we require to find a hash value that starts with three 0's as part of a puzzle.

<h2>Proof of Work Algorithm:</h2>

Blockchain-based applications are typically peer-to-peer networks that must be as decentralized as possible. To support and enhance network decentralization, all peers in the network should be able to add new blocks to the network. Proof of work algorithms simulate the idea of each peer being able to add a new block. The goal of proof of work algorithms is to solve various cryptographic puzzles. Peers who solve these puzzles more quickly can add a new block to the blockchain.

Two different proof of work algorithms are included in our blockchain implementation. Both are attempting to solve the same cryptographic puzzle, but in different ways. According to these proof of work algorithms, whoever finds a hash value for their block that contains a certain number of leading zeros will be able to announce it to the chain. For example, our blockchain only allows miners to add a block if the hash value of their block begins with three zeros, indicating that the difficulty of the blockchain is 3. The term miner refers to peers who attempt to add blocks to the blockchain.

Based on this idea, we have implemented two algorithms. Both calculate nonce differently. One calculates nonce randomly in each iteration and another one simply increments nonce by one in each iteration. We have analyzed running time and behavior of both algorithms in the file named POW_Comparison.py. Based on the output of the file, we have concluded some results for both the methods.











<h2>Comparison for On-chain and Off-Chain Blockchain:</h2>

Blockchain applications can also be divided into two types: On-chain Blockchain & Off-chain Blockchain. On-chain Blockchain refers to storing information inside blocks and Off-chain Blockchain refers to storing actual data outside the block and only keep metadata in block. 

<h3>Advantages of On-chain blockchain: </h3>

On-chain blockchain can be more secure because information is capsulated in secure blocks.
Infomation can be recovered easily in case of break in the system.

<h3>Disadvantages of On-chain blockchain:</h3>

Runnning time of the insertion and other block-operations can be slow because it holds too much data to process.
It is expensive and requires more resources to maintain.

Here, issues with On-chain blockchain can be solved by using off-chain blockchain but On-chain blockchain is more effective where main concern is security and back-up of information. For this project, we have implemented On-chain blockchain which contains entire file data in block including file size and file name.

<h2>References:</h2>
1. https://ieeexplore.ieee.org/abstract/document/9031420                                                                                                            
2.https://ieeexplore.ieee.org/abstract/document/8915819
3.https://ieeexplore.ieee.org/abstract/document/8915819


