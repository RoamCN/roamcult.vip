
#@Jessie
    
#[每天一条CN tweet](每天一条CN tweet.md)
        - Some observations from folks we engaged to use @Roamresearch: in the beginning they just treat it as a very simple"notebook" with indenting structure,they dump random ideas/notes/daily stuff in the daily note and just do very simple journaling with no need of other features. 
        - After they do the writing for some time,they start to have the 'DEMAND' to be educated. They want to know 'how i can set routine stuff as template' 'how can i quote blocks' 'maybe i can use it for project management,for CRM building,for research etc'.
        - In the collaboration scenario(RoamCN public graph) is also interesting,people see what others doing and want to keep up with the cult/geeky move. They asked 'how can i add css/js' 'wow we can find the thoughts in common (by using attr-table or query) ' etc. More surprisingly,some of them develop more geeky stuff and some try to design some 'collective experiment'. The process begins to repete itself,dope!!
        - we do collaborate note-taking for Roamstack 0915 journaling Summit
        - ![](../images/s17pfUXjTK.png?)
        - ![](../images/tlVcszh6nw.png?)
        - ![](../images/omC7iJfyhl.png?)
    - [query](query.md) 用法之
        
#[创投CRM](创投CRM.md)匹配
            - ![](../images/9EQWZK7YM8.png?)
            - ABC
                - **[身份](身份.md):** 创业者 👨🏽‍💻 
                - **[领域](领域.md):** [NLP](NLP.md) [ML](ML.md)
                - **[所在城市](所在城市.md):** BJ
                - **[在哪里相识的](在哪里相识的.md):** soho二楼星爸爸
                - **[简介](简介.md):** bulabula 
            - DE
                - **[身份](身份.md):** 投资人 🧙‍♂️ 
                - **[领域](领域.md):** 看[NLP](NLP.md) #[医疗](医疗.md)方向
                - **[所在城市](所在城市.md):** BJ
                - **[在哪里相识的](在哪里相识的.md):** 生日一起吃臭鳜鱼
                - **[简介](简介.md):** bulabulabula
            - {{[query](query.md): {and: [创投CRM](创投CRM.md) {or: [领域](领域.md) [NLP](NLP.md)}}}}
        - 筛选Todo{{[query](query.md):{and:[TODO](TODO.md){not:[query](query.md)}}}}
- [帖子](帖子.md) ~ #[@码客](@码客.md): allPage显示不全的解决方案
    /* chrome浏览器 4240.111 版本上 table出现了不同的加载方式 导致allpage长度显示不全  本修改只针对azlen样式 */
    __**css部分**__
    /* chrome浏览器 4240.111 版本上 出现了 allPage显示不全的兼容性问题 */
    [all-pages-search](all-pages-search.md) {
        - max-height: calc(100%);
        - overflow-y: auto;
        - height:100% !important;
    }
    .rm-pages-col-word-count > span:first-child, .rm-pages-col-word-count + div > span:first-child {
    display: none;
    }
