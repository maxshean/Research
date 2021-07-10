## zk-Rollups

As the name might suggest zk-Rollups involve zero knowledge proofs.  However, what actually are they? 
Well, let's start with what a Rollup actually is.  

Rollup: a bundle of transactions on a side chain that can be reported onto the mainchain.  These transactions are bundled and tracked inside of a smart contract.  
Rolling up transactions in this way reduceds fees and network traffic because it increases the network throughput capacity. 
Rollups were proposed by Vitalik as a solution to the failures of state channels and Plasma.  Specifically, state channels and Plasma allow for orders of magnitude more transactions per secord, these solutions are not compatible with smart contracts. 

Now onto zk-Rollups.

zk-Rollup: funds on a mainchain are held in a smart contract. These funds are then brought to a side chain where users can perform transactions.  The validity of the side chains is ensured by a zero-knowledge proofs.  zk-Proofs are posted to the main chain regularly.  These proofs essentially act as the bundling mechanism, as they show the validity of the bundle of transactions contained between proof posting periods. 

In a zk-Rollup solution, Merkle Trees are used to represent accounts and balances. Merkle tree roots are stored in the smart contract on ethereum.  Storing the roots in this way is simply a way of representing the state of the side-chain.  This is the only data that is stored on the main chain. 

There are two types of users involved in zk-Rollups.  

Transactions: 
These users create and broadcast transfers across the side chain.  Different protocols have different ways of optimizing this process.  

Relayers: 
Relayers collect large amounts of transactions into rollups.  They then generate a zk-SNARK which represents the state of the sidechain.  The proof essentially compares the state of the chain before the transfers to the chain after.  

zk-Rollups are designed to solve the problem of data availability in Plasma scaling solutions (see directory on plasma).  
