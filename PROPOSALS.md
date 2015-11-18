# Paper proposals

## 1) distributed e-cash wallet with instant transactions supporting multiple different bitcoin-esque currencies  

-> Kademlia DHT for storage  
-> Clients find DHT & other clients via DNS similar to bitcoins client discovery  
-> Client generates related wallets by downloading and hooking into the wallet software for respective wallets  
-> client creates tokens for each currency in wallet  
-> Clients store objects in DHT of form  
	{  
		Wallet Id          : string (wallet id = hash(username, password);)  
		bitcoin wallet id  : string  
		litecoin wallet id : string  
		btc tokens         : integer  
		litecoin tokens    : integer  
	}  
-> On tx wallet id is sent to both recieving wallet and a distributed lock service (similar to chubby/zookeper/darkcoins masternodes)  
-> lock service locks wallets   
-> on reciept from recieving wallet, the lock service unlocks wallet  
-> if a reciept never arrives the wallets btc output is locked indefinitely  

## 2) Distributed platform  
-> Use speed, storage and computational capacities as benchmarks  
-> proof of stake -> 3 tokens, respectively speed, storage and comp, can be measured via PCA, PoR and PoW respectively  
-> With sufficient number of tokens node becomes privileged node  
-> Paxos rings  
-> Paxos ring of speed stake holders above  

Ring of high speed nodes  
|        |       |  
rings of high storage & high comp nodes led by high speed paxos leader  
|   |    |   |   |  
All other nodes  

-> Use RT-SADS to schedule tasks  
-> Use graph partioning to store data in a distributed manner  
-> High speed nodes act as coordinators between rings and heirarchically  
-> Allow applications to be verified manually(test suites) similar to android/apple app store  
-> Uploaded onto platform  
-> Simple API via dependency injection into app  
-> app now has access to a decentralized data store and compute network, will exist as long as people want it.   

