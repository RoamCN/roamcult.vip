- cc x
- 
- [42SmartBlock](42SmartBlock.md) 测试
    - articles:
        - **[source](source.md):**
        - **[link](link.md):**
        - **[topics](topics.md):**
        - **[I am reading this to](I am reading this to.md):**
    - book:
        - **[author](author.md):**
        - **[category](category.md):**
        - **[highlight](highlight.md):**
        - **[reading status](reading status.md):** {{or:to read | reading | read}}
        - **[published year](published year.md):**
    - 专栏
        - **[author](author.md):**
        - **[source](source.md):**
        - **[topics](topics.md):**
    - video
        - **[source](source.md):**
        - **[topic](topic.md):**
        - **[author](author.md):**
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
