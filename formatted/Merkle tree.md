
# Backlinks
## [Ethereum Whitepaper](<Ethereum Whitepaper.md>)
- An important scalability feature of Bitcoin is that the block is stored in a multi-level data structure. The "[hash](<hash.md>)" of a block is actually only the hash of the block header, a roughly 200-byte piece of data that contains the timestamp, nonce, previous block hash and the root hash of a data structure called the [Merkle tree](<Merkle tree.md>)

- The [Merkle tree](<Merkle tree.md>)

- The approach may seem highly inefficient at first glance, because it needs to store the entire state with each [block](<block.md>), but in reality efficiency should be comparable to that of [Bitcoin](<Bitcoin.md>). The reason is that the state is stored in the tree structure, and after every block only a small part of the tree needs to be changed. Thus, in general, between two adjacent blocks the vast majority of the tree should be the same, and therefore the data can be stored once and referenced twice using pointers (ie. hashes of subtrees). A special kind of tree known as a "[Patricia tree](<Patricia tree.md>)" is used to accomplish this, including a modification to the [Merkle tree](<Merkle tree.md>)

