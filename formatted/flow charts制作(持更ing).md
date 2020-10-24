- __The YAM Rebase Mechanism — process flow chart__
- {{mermaid:}}
    - graph TD
        - A([Start]) --> B(Get TWAP from last rebase)
        - B --> C{TWAP<0.95?}
        - C --yes--> D(Negative rebase)-->I[Calculate supply delta update scaling factor sync uniswap pools]
        - C --no--> E{0.95<TWAP<1.05?}
        - E --yes-->F(No rebase)
        - E --no--> G{TWAP>1.05?}
        - G --yes-->H(Positive rebase)-->I
        - I -->J{Was rebase positive?}
        - J --good-->K(Mint additional YAM-10% of rebase)-->L(Buy yUSD from uniswap pool-capped at max slippage)-->M(Send yUSD and any excess YAM to reserves)-->N
        - J --no-->N([done])
- 参考：[mermaid md格式教程](https://mermaid-js.github.io/mermaid/diagrams-and-syntax-and-examples/flowchart.html)
    - TD--top down
    - LR--left right

# Backlinks
## [October 1st, 2020](October 1st, 2020.md)

#@Jessie [TIL](TIL.md) #[flow charts制作(持更ing)](flow charts制作(持更ing).md)

## [September 23rd, 2020](September 23rd, 2020.md)
- [flow charts制作(持更ing)](flow charts制作(持更ing).md)之

