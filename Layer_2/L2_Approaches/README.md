## What actually is L2 scaling

Everyone who is mildly familiar with blockchain has heard about transaction throughput.  The typical comparison is between the bitcoin network, which can process around 6 transactions per second, and VISA's, which can handle upwards of 1700 transactions per second.

Even though you often hear this remark from anti-bitcoiners, low transaction throughput is a problem for blockchains. 
There are two ways of solving this problem. They are layer 1 scaling and layer 2 scaling.  
You can read more about layer 1 scaling in my directory on layer 1s.  Breifly though, layer-1 scaling is changing the protocol of the underlying blockchain to allow for greater transaction throughput.  

layer 2 scaling is simply changing the way that users interface with the blockchain.  
Presently, users perform all of their activity on chain.  Layer 2 changes this paradigm so that users perform most of their activity in an off-chain protocol.  
At first, this might seem like it defeats the purpose of having a a blockchain, but it actually works well. In a layer 2, there is a smart contract that lives on the main chain.  This smart contract perform two tasks. First, it processes deposits and withdrawls.  That is, it allows for funds to be moved back and forth between the main chain and the side chain.  Second, the contract verifies that the events happening off-chain are all legitimate.  You might wonder how the mainchain can verify the events happening on a sidechain if it is not tracking everything happening on that chain.  The contract is able to verify the state of the side chain through various proofs.  The way that these proofs work make up the predominate difference between different L2 approaches.  The common thread between all of these approaches is that submitting and verifying the proofs is much less costly and allows for more transactions per second than simply performing all of the transactions on chain. 

I reccomend reading about L2 approaches in the following order.

0. Side Chains (if you are not already familiar with the concept)
1. State Channels
2. Plasma
3. Rollups
4. Validium
5. Hybrid Approaches
