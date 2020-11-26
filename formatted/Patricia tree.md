
# Backlinks
## [Ethereum Whitepaper](<Ethereum Whitepaper.md>)
- The approach may seem highly inefficient at first glance, because it needs to store the entire state with each [block](<block.md>), but in reality efficiency should be comparable to that of [Bitcoin](<Bitcoin.md>). The reason is that the state is stored in the tree structure, and after every block only a small part of the tree needs to be changed. Thus, in general, between two adjacent blocks the vast majority of the tree should be the same, and therefore the data can be stored once and referenced twice using pointers (ie. hashes of subtrees). A special kind of tree known as a "[Patricia tree](<Patricia tree.md>)"

