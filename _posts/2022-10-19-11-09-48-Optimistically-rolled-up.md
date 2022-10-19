---
layout: post
title: 'Optimistically rolled-up'
image: optimistic-rollups.png
---

![optimistic-rollups]({{site.url}}/assets/img/optimistic-rollups.png)
Optimistic rollups are a type of second-layer scaling solution for blockchain networks that allow for increased transactional throughput /without/ sacrificing “security” or decentralization. Optimistic rollups work by batching transactions off-chain into a so-called “optimistic” data structure. This data structure is then “rolled up” onto the main chain, where it is anchored with a cryptographic proof. This proof ensures that the data in the optimistic rollup is valid, even though it was generated off-chain. 

### Advantages
The main advantage of optimistic rollups is that they allow for much higher transactional throughput than traditional on-chain solutions. (Like lots) This is because the data structure can be updated off-chain, without having to wait for each individual transaction to be included in a block. 

Another advantage of optimistic rollups is that they are much more flexible than traditional on-chain solutions. This flexibility allows for a wide variety of applications to be built on top of them, including smart contracts, decentralized exchanges, and more. 

### Concerns
But it’s not all roses, the main downside of optimistic rollups is that they are not yet as secure as traditional on-chain solutions. This is because the data structure is not anchored to the main chain until it is “rolled up”. This means that if an attacker were to modify the data in the optimistic rollup, they could do so without being detected. Overall, optimistic rollups are a promising scaling solution for blockchain networks. They offer a significant increase in transactional throughput, without sacrificing security or decentralization.

### Thoughts
I know you’re probably thinking, Ok, but how does this compare to the ZKPs we were discussing yesterday? I’m glad you asked. Optimistic rollups are a type of zero knowledge proof that allows for efficient verification of computation on large data sets. In a rollup, data is arranged into a Merkle tree, with each leaf node containing a piece of data and each non-leaf node containing a hash of the data in its child nodes. To verify a computation, one only needs to provide the root hash of the tree and a proof that the computation was performed correctly. The proof can be verified quickly and efficiently, without needing to download the entire data set.

_Uhoh, I said Merkle tree…did I lose anyone? Don’t worry that’s it. That’s the thought, now you’ve heard a bit about ZKStarks and Optimistic Rollups. Next thought let’s compare and contrast. Is one better? Are they the same thing?_