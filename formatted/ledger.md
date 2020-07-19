
# Backlinks
## [Ethereum Whitepaper](Ethereum Whitepaper.md)
- The mechanism behind [proof of work](proof of work.md) was a breakthrough in the space because it simultaneously solved two problems. First, it provided a simple and moderately effective [consensus](consensus.md) algorithm, allowing nodes in the network to collectively agree on a set of canonical updates to the state of the [Bitcoin](Bitcoin.md) [ledger](ledger.md).

- From a technical standpoint, the [ledger](ledger.md)

- If we had access to a trustworthy [centralized](centralized.md) service, this system would be trivial to implement; it could simply be coded exactly as described, using a centralized server's hard drive to keep track of the state. However, with [Bitcoin](Bitcoin.md) we are trying to build a decentralized currency system, so we will need to combine the state transition system with a [consensus](consensus.md) system in order to ensure that everyone agrees on the order of transactions. Bitcoin's decentralized consensus process requires nodes in the network to continuously attempt to produce packages of transactions called "[blocks](blocks.md)". The network is intended to produce roughly one block every ten minutes, with each block containing a timestamp, a nonce, a reference to (ie. hash of) the previous block and a list of all of the transactions that have taken place since the previous block. Over time, this creates a persistent, ever-growing, "[blockchain](blockchain.md)" that constantly updates to represent the latest state of the [Bitcoin](Bitcoin.md) [ledger](ledger.md).

