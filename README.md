
# Cyptocurrency-Blockchain

<h3>Cryptography Team Project</h3>
Implemented a basic version of Cryptocurrency (<b>Litcoin</b>) from scratch. The project implements the prime ideas of blockchain technology, namely:
1) Distributed P2P network
2) Mining of Block using a valid Proof of Work
3) Creating new users 
4) View User
5) Consensus Protocol
6) Verify Transaction 
7) Validate Chain
<h3>Structure of Source Code</h3>
• The code is divided into 2 subfolders named "blockchain" and "blockchain_client".
<br>
• The folder "blockchain" consists of scripts from the server side (nodes). It is further divided into 3 sub directories. File named "blockchain.py" consists of the python script used to implement various functionalities like <b>create block, verify transaction, Proof of Work, </b>etc. Directory "templates" has the HTML and Javascript (templates) which have been used for the UI. The "static" folder contains the custom CSS and bootstrap frameworks. 
<br>
• The  folder blockchain_client consists of the scripts from the user's side. It is further divided into 3 parts. One which has the HTML and Javascript(templates) which is used for UI for the user. The static folder contains the custom CSS part and bootstrap frameworks. blockchain_client.py consists of the python script used to implement various functionalities like <b>signing the transaction, generating transaction, view user</b> etc.<br>

<h3>Dependencies</h3>
<p>For running our project following dependencies would be required:
<br>
1) Python compiler (preferably 3.7.x)<br>
2) Python libraries such as Flask, Crypto, cors, requests.hashlib, urllib, json, & other UI libraries<br>
3) An IDE supporting Python (e.g. IntelliJ or Pycharm)
</p>
<h3>Running The Project</h3>
In the IDE, <br>
1) Configure different nodes according to their requirements. If we are creating a peer node, we have to configure it on blockchain.py and assign 5000 port series to it. <br>
2) For creating a user client, we need to configure it on blockchain_client.py and assign 8000 series port to it.<br>
3) Finally run all these configurations to get a running project.<br>
4) We have essentially simulated a network with <b>3 peer nodes and 2 user clients</b>.
<br>
<h3>Key Functionalities</h3>
<h4>Creating New Wallet</h4>
• Creates a new wallet for any client. The wallet contains the public and private key for the client. These keys are generated using the RSA algorithm. <br>
<h4>Generating Transaction</h4>
• Generates the transaction by accumulating all details like sender's public and private key, recipient's public key and the amount of cryptocurrency to be transferred. All these values are requested from the form using Java Script modules. <br>
<h4>Signing the Transaction</h4>
• Generates the digital signature for the transaction using the sender’s private key using the <b>SHA256 algorithm</b>.
<h4>Mining the Block/Proof of Work</h4>
• The process of mining the block. Using brute force, we try to get the required nonce and in turn the Hash value which satisfies the difficulty specified. The proof of work computes the computational complexity/work it took to reach the correct Hash.
<h4>Verify Transaction</h4>
• Verifies the signature generated during the transaction by using the <i>verifier</i> method in the Json library. It uses the sender's public key along with the transaction list to verify the signature. 
<h4>Consensus Protocol</h4>
• Checks the longest valid chain and replaces all smaller sub-chains present on other nodes by the longest chain in case of clashes.
<h4>Validate Chain</h4>
• Checks the validity of the chain by cross-checking the previous_hash stored in current_block, and actual hash of previous block. It also changes the index of the current_block according to the validity.
<h4>Reward</h4>
• A reward of 1 Litcoin is given to the node which mines the block.
