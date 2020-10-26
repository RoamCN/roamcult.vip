- #@Jessie
    - #[[每天一条CN tweet]]
        - Some observations from folks we engaged to use @Roamresearch: in the beginning they just treat it as a very simple"notebook" with indenting structure,they dump random ideas/notes/daily stuff in the daily note and just do very simple journaling with no need of other features. 
        - After they do the writing for some time,they start to have the 'DEMAND' to be educated. They want to know 'how i can set routine stuff as template' 'how can i quote blocks' 'maybe i can use it for project management,for CRM building,for research etc'.
        - In the collaboration scenario(RoamCN public graph) is also interesting,people see what others doing and want to keep up with the cult/geeky move. They asked 'how can i add css/js' 'wow we can find the thoughts in common (by using attr-table or query) ' etc. More surprisingly,some of them develop more geeky stuff and some try to design some 'collective experiment'. The process begins to repete itself,dope!!
        - we do collaborate note-taking for Roamstack 0915 journaling Summit
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FRoamCN%2Fs17pfUXjTK.png?alt=media&token=9b432558-7080-4847-bb6b-fc6d71bcb307)
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FRoamCN%2FtlVcszh6nw.png?alt=media&token=e69f386c-8538-4913-b7d2-b8944088314a)
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FRoamCN%2FomC7iJfyhl.png?alt=media&token=4c9f7a72-bd7c-44d2-a3e3-34772a57eb0b)
    - #query 用法之
        - #[[创投CRM]]匹配
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FRoamCN%2F9EQWZK7YM8.png?alt=media&token=ff87c936-3754-4f30-a904-2c25a40b2e94)![](https://uploader.shimo.im/f/TgtzXTrzZD56NPxJ.png!thumbnail)
            - ABC
                - 身份:: 创业者 👨🏽‍💻 
                - 领域:: #NLP #ML
                - 所在城市:: BJ
                - 在哪里相识的:: soho二楼星爸爸
                - 简介:: bulabula 
            - DE
                - 身份:: 投资人 🧙‍♂️ 
                - 领域:: 看#NLP #[[医疗]]方向
                - 所在城市:: BJ
                - 在哪里相识的:: 生日一起吃臭鳜鱼
                - 简介:: bulabulabula
            - {{[[query]]: {and: [[创投CRM]] {or: [[领域]] [[NLP]]}}}}
        - 筛选Todo{{[[query]]:{and:[[TODO]]{not:[[query]]}}}}
- [[帖子]] ~ #[[@码客]]: allPage显示不全的解决方案
    /* chrome浏览器 4240.111 版本上 table出现了不同的加载方式 导致allpage长度显示不全  本修改只针对azlen样式 */
    __**css部分**__
    /* chrome浏览器 4240.111 版本上 出现了 allPage显示不全的兼容性问题 */
    #all-pages-search {
        - max-height: calc(100%);
        - overflow-y: auto;
        - height:100% !important;
    }
    .rm-pages-col-word-count > span:first-child, .rm-pages-col-word-count + div > span:first-child {
    display: none;
    }
