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


Zero Knowledege Proofs:

To learn more about Zero Knowledge proofs, I suggest you read the <a href="https://en.wikipedia.org/wiki/Zero-knowledge_proof">wiki</a>.  It is fairly good.  
The whole idea of a zk-proof is that someone can prove to someone else that they know something without revealing any information other than that they know that thing. 

Here we refer to the proof of a statement that the prover has some knowledge without stating the knowledge itself.  We could dive into model theory and logic to define what a proof means, but this is unnecessary for our purposes.  Simply use your intuitive understanding of a proof. I am purposefully avoiding discourse on proof systems and probability theory.  These complicate things. 

a proof is a zk-proof iff all of the following hold:

0. the proof is complete: if the statement is true, then the proof will convince the verifier will be convinced of the truth of the statement 
1. the proof is sound: if the statement is false, then the prover will not be able to convince the verifier that it is true 
2. the proof is zero-knowledge: if the statement is true, the verifier only lears that the statement is true and nothing else. 


An example of a zero-knowledge proof is a signature on a blockchain.  Becuase of the properties of the cryptographic hash function SHA-256, when someone signs a transaction on the bitcoin blockchain
you have a proof that this person knows the secret key that corresponds to the public key doing the signing.  The world however does not learn what the individual's secret key actually is.


ZK-SNARKs: 

zk-snark stands for zero-knowledge Succinct Non-transparent Argument of Knowledge. 
A zk-snark is a type of zk-proof.  Above and beyond satisfying the above properties, a zk-snark also has the following properties

3. succinctness: the proof can be quickly verified
4. non-interactiveness: the proof consists of a single message.  Specifically, there is no back and forth or repeated protocol involved in the proof. 
5. the proof is an argument of knowledge: the prover convinces the verifer that information exists and that only they can acess that information 

Any transaction hidden behind a zk-SNARK is called a shielded transaction. Specifically, a zk-SNARK can be used to show that a transaction is valid without revealing any information about the transaction or the involved parties. 

To sum it up, zk-SNARKs are super important for privacy.  

One blockchain that makes use of zk-SNARKs is the Horizen blockchain.  The entire appeal of Horizen is that one can transact on side chains privately and zk-SNARKs are used to prove that the transactions are valid and private. 


Now that we have a basic understanding of zero-knowledge proofs and zk-SNARKS, we can dive into rollups.  

