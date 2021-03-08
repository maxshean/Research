## All about State Channels

State channels are a L2 scaling solution.  The goal of state channels is to increase transaction throughput by eliminating the need for many transactions to be processed on chain. State channels have some properties that make them more desireable than rollups.  

How they work: 

1. Users lock up a portion of the state by sending money to a multisignature contract that has the ability to accept ether and payout all parties who have sent it ether. 
2. Users sign transactions and send them to one another, each one making a copy of the signature for later reference.
3. Each transaction contains a nonce so the smart contract can know the chronological order of transactions
4. Once both parties are done, they close the state by submitting a transaction to the ethereum blockchain
5. after the state is updated and unlocked the smart contract sends each paryty their remaining ether balance.

A state channel is a channel ovwer which users can transact with one another 'off-chain'.  In fact, state-channels allow for any type of state altering transaction, whereas as payment channels are a type of state channel that only allow for payments. 
Importantly, State Channels do not rely on an intermediary.  
