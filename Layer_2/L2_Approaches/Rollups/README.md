## All about rollups

Rollups are an approach to L2s which can provide privacy and relieve L1 of computation burden. Rollups bundle up sidechain transactions into a single transaction and generate a cryptographic proof, known as a Succinct Non-transparent Argument of Knowledge, this proof is then submitted to the main-chain.  This alleviates burden because not every transaction is recorded on the blockchain. 

In a rollup solution  contract exection, signature verification, state checks, etc. are all handled on the side chain. The main chain is only responsible for storing transaction data and proofs posted by the side chains. 

The purpose of a rollup solution is to use reduce fees for users and to increase transaction throughput. 

There are two main types of rollups. 

0. ZKRollups: Computations are completed off of the main chain and a validity proof is submitted to the mainchain.
1. Optimistic Rollups: transactions are bundled, submitted to the chain, and assumed to be valid.  Challenges can be issued if fraud is suspected.  A fraud proof checks the transactions to see if fraud occured. 

I have a dedicated directory to each.  In these directories I will explain how each type of rollup works, and investigate some of the projects that implement the rollup solutions. 

As this applies generally to both types of rollups, I will include this note here. 
Rollups use relayers who stake a bond in the rollup contract.  Relayers send information back and forth between the mainchain and the sidechain. Each protocol rewards relayers differently for their work. 
