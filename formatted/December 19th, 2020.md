- cc x
- 
- 

#@Jerry mermaid 去除背景
    - mermaid css
        ```css
.rm-mermaid{
  background: transparent !important;
  min-width: 0px !important;
}

.rm-mermaid .node rect{
  stroke: [2A496F](2A496F.md) !important;
}

.rm-mermaid div{
  color: [448889](448889.md) !important;
  margin-right: 15px;
}

.rm-mermaid text{
  fill: [34A5A5](34A5A5.md) !important;
  font-size: 25px !important;
}

.rm-mermaid rect{
  fill: transparent !important;
  stroke-width: 0px !important;
}

.rm-mermaid tspan{
  fill: [438BE0](438BE0.md) !important;
  font-size: 20px !important;
}```
    - 之前
        - ![](../images/HbH5PQatsx.png?)
    - 之后
        - {{mermaid}}
            - graph TD;
                - A-->D;
                - A-->B
                - B-->D;
                - A-->C;
                - C-->D
