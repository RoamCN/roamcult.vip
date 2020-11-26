
# Backlinks
## [Ethereum Whitepaper](<Ethereum Whitepaper.md>)
- Once step (1) has taken place, after a few minutes some miner will include the transaction in a block, say block number 270. After about one hour, five more blocks will have been added to the chain after that block, with each of those blocks indirectly pointing to the transaction and thus "confirming" it. At this point, the merchant will accept the payment as finalized and deliver the product; since we are assuming this is a digital good, delivery is instant. Now, the attacker creates another transaction sending the 100 BTC to himself. If the attacker simply releases it into the wild, the transaction will not be processed; miners will attempt to run `APPLY(S,TX)` and notice that `TX` consumes a UTXO which is no longer in the state. So instead, the attacker creates a "[fork](<fork.md>)"

