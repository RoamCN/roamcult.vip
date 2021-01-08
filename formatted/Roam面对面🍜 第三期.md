
# 准备工作
    - 策划：Victor Wu,Jessie Li
    - 嘉宾：[王树义](王树义.md)老师（➕ 个头像👦 ）
    - 时间：2020-08-4 20:00
    - 准备事项：
        
1. 飞书账号
        
2. 可以进行飞书会议的手机/平板/电脑以及麦克风（不强制）
        
3. 安静的环境
        
4. 带上你的疑问和好奇
    - 大纲
        
1.日常用Roam的Roamlog（像Vlog) 
        
2.王树义老师教学视频制作workflow，看起来非常高效 
        
3.隐藏技能-很亮点、有用的招/用例 
            - 老师展示一下交互可视化（obsidian，InfraNodus) ，特别分享下**「中观」**的思想✨
        
4.Roam对您来说意味着什么？带来最大的变化是什么？
        
5.希望王老师分享一个自己的page[[]]供roam/cn收录🤩

# 演示&笔记: 
    - 负责：#@Jessie
    - 提升学术论文写作的效率
        - 存储文献➡️ 检索➡️ 做笔记➡️  放到第二大脑(RR)
        - 使用方法
            - 借助文献管理工具[zotero](zotero.md)，打开一片或多篇文献
            - 右键export to Roam，导成机器友好型语言JSON
            - 打开Roam选择导入(import)
                - ![](../images/ICJeQ2tnjf.png?)
            - Preview功能
                - ![](../images/-Mtc4QL3fW.png?)
        - 导出
            - Roam中常用的markdown格式导出成学术论文格式(e.g.word格式)
            - reference：王老师提到的文章详细介绍
                - [如何高效做文献回顾？（工具篇）](https://mp.weixin.qq.com/s/k-G0TzfnYbLA0dYXfDpMdg)          
                - [zotero roam export](https://www.bilibili.com/video/BV1nK4y1s7JW?from=search&seid=4129994855895992485)
    - Daily notes的使用
        - 私人信息非常多，一个block只谈一件事。但是一个daily note里面什么都有，包括查电表hhh😂  
        - 喜欢Roam的一点是：不要结构化的写东西，拒绝每日填空哈哈！
        - 猴哥：会用标签归类吗？
        - 王老师：也是roaming的方式，一些和daily note不是一个维度的话题，比如[脚本优化](脚本优化.md)方面，我就通过开[[]]来记录它，需要补充内容的话我就点进去。
        - ![](../images/jEwc22m0mL.png?)
    - 幻灯式视频的制作
        - 在Roam里直接写（大纲结构，分级标题）
        - 导出markdown，[pandoc](pandoc.md)格式转换工具生成[review js](review js.md)
        - ![](../images/YmbFrJCMhK.png?)
        - ![](../images/SgBTnD7Ll-.png?)
    - 隐藏技巧
        - 没有，有就通过视频分享了😂 
    - reference:
        - [Python 过时了吗？(天津话版)](https://www.bilibili.com/video/BV1it4y1Q7v2?from=search&seid=4129994855895992485)
        - [Tools for converting Markdown Source File to Reveal.js HTML5 slides](https://github.com/wshuyi/markdown2slides)
    - 交互可视化
        - graph不是线性的东西，是一张网。没有所谓的开头结尾。但是你要找一个切入点（你的目标），然后看与它紧密相连的内容，这就是我讲的“中观”。把它们摘出来在进行检索、可视化。
        - 猴哥：拉出来一条线？
        - 王老师：不是线，是一个子网。
        - ![](../images/DeuzUsgNK3.png?)
        - [obsidian](obsidian.md)的可视化
        - python里面进行网络分析的包--[networkX](networkX.md)
            - [社区发现(community detection)](社区发现(community detection).md)：这个算法是把联系更紧密的人分堆儿
            - 之前想把印象笔记生成可视化的图，然后我有读者来告诉我：有个工具已经可以做到了，就是RR。所以，分享可以给你带来意想不到的链接。
                - 看到网络布局的关系，利用[Evernote](Evernote.md)便于采集，产生联系的特点
        - reference:
            - [ Evernote/印象笔记网络可视化工具](https://www.bilibili.com/video/BV1eK4y1r73p)
            - [如何交互可视化 Roam Research 局部笔记网络？](https://mp.weixin.qq.com/s/nxJmVcZcm6iptfdhuUUprg)
    - note thinking + 人工智能[NLP](NLP.md)
        - [devonthink](devonthink.md)--一键分析与每条笔记最相关的笔记是哪些的app
        - roam是可以实现双向链接，但是都是手动的，人工的。之后的趋势一定是自动化，因为笔记多了，联系根本想不起来。卢曼记了9万条...
            - 机器听不懂我们的语言，机器只能理解[统计规则/规律](统计规则/规律.md)，把语言转换成一系列数字，然后到原来笔记里去找有哪些（在机器的规则下）更接近。由近到远进行排列
                - [模糊集](模糊集.md)
        - 知识库之间的对齐
            - 首先要有平行知识库
            - 如何判断两个graph之间的matching？
                - [conor的访谈](conor的访谈.md)：抽着烟🙄️ 给学生讲课，不是讲工具，是讲对教育的使命
                - 这个创始的独特之处：当别人想怎么创造一款“笔记工具”盈利的时候，他想的是如何通过RR改变未来的教育
                - 一旦他确定了一些“发展方向”的时候，很多“问题”都不再是问题。
                - 如今，人们把人工智能推到墙角，恨不得它爆发。那把人脑置于何处呢？我们期待的是人和机器的协作，而不是单独的人，单独的机器。
                    - 46:20 卢曼和他的卡片盒可以看作是一个单一的人，单一的机器。但如果做成人脑的网和机器的网结合在一起（软件、硬件、[湿件](湿件.md)🧠 ），那很多问题可以解决。因为机器通过学习人的行为，对人产生的各种联系进行学习。反过来，随着机器给出的反馈越来越精准，人就会在此基础上构造更多的链接。
                    - 这会使得，一方面机器的推荐、预测更精准；同时驯化人类更愿意以网状的方式，而不是简单粗暴的线性方式去思考。
                    - 47:30 但需要认识到的是，虽然网状更符合大脑的天然运行模式，但它与我们的后天的“教育系统”是格格不入的。如果通过这种方式可以将我们被压抑、被扭曲很久的创造力都释放出来，我觉得这是Roam和其他笔记最大的不同。
                    - https://twitter.com/i/status/1257263237428506625

# 剪辑与后期
    - 负责成员：#[@多酱](@多酱.md)
    - 推荐语 highlights
        - 【Roam面对面】第3期请到了知识界大牛王树义老师来做客，王老师做的深入浅出的科普让人眼前一亮，这次王老师分享了平时使用Roam Research技巧和用例，对笔记软件和人工智能联系做了一个展望。
        - 这次访谈主要有以下几部分：
            - 学术论文写作的技巧
            - daily note使用体验
            - 用roam和review.js制作幻灯案例
            - 交互可视化roam局部网络笔记
            - 对笔记软件和人工智能联系的思考
            - 向他人推荐使用roam的方式
            - 对RoamCn社群的建议
            -  学术论文写作的小技巧
            -  daily note使用体验
            -  用roam和review.js制作讲解式网页幻灯
            -  交互可视化roam局部网络笔记
            -  对人脑、笔记软件和人工智能联系的思考
            -  向他人推荐使用roam的方式
            -  对roam/cn社群的建议
    - 音频时间点 timestamp
        - 0:10 开场
        - 2:55 学术论文写作的小技巧
        - 3:35 从文献管理工具zotero导出文献到roam
        - 5:00 使用roam写作的论文导出转换成word形式
        - 8:13 daily note使用体验
        - 10:40 喜欢用roam随意写作，不喜欢结构化
        - 11:53 笔记很多，不同维度内容用page区分
        - 13:45 用roam和review.js制作讲解式网页幻灯
        - 15:30 演示幻灯制作案例《Python过时了吗？》
        - 19:16 录屏软件推荐CleanShot X
        - 20:20 制作幻灯的总结
        - 23:00 交互可视化roam局部网络笔记（obsidian、python）
        - 26:56 分享笔记可视化脚本案例
        - 28:40 笔记工具obsidian可视化功能使用
        - 31:25 利用python找到紧密联系的局部网络
        - 33:22 分享evernote可视化，自那时与roam结缘
        - 34:50 对人脑、笔记软件和人工智能联系的思考
        - 41:50 想象未来roam使用场景
        - 43:10 由创始人Conor的访谈了解到roam的独特
        - 44:36 人与机器关系的思考
        - 47:40 向他人推荐使用roam的方式
        - 51:10 对roam/cn社群的建议
    - 视频时间点
        - 0:10 开场
        - 2:55 学术论文写作的小技巧
        - 8:13 daily note使用体验
        - 13:45 用roam和review.js制作讲解式网页幻灯
        - 23:00 交互可视化roam局部网络笔记
        - 34:50 对人脑、笔记软件和人工智能联系的思考
        - 47:40 向他人推荐使用roam的方式
        - 51:10 对RoamCN社群的建议
    - Roam中文站B站地址：https://space.bilibili.com/599106362?spm_id_from=333.788.b_765f7570696e666f.1
    - reference
        - [zotero roam export](https://www.bilibili.com/video/BV1nK4y1s7JW?from=search&seid=4129994855895992485)
        - [如何高效做文献回顾？（工具篇）](https://mp.weixin.qq.com/s/k-G0TzfnYbLA0dYXfDpMdg)  
        - [Python 过时了吗？(天津话版)](https://www.bilibili.com/video/BV1it4y1Q7v2?from=search&seid=4129994855895992485)
        - [Tools for converting Markdown Source File to Reveal.js HTML5 slides](https://github.com/wshuyi/markdown2slides)
        - [ Evernote/印象笔记网络可视化工具](https://www.bilibili.com/video/BV1eK4y1r73p)
        - [如何交互可视化 Roam Research 局部笔记网络？](https://mp.weixin.qq.com/s/nxJmVcZcm6iptfdhuUUprg)
        - [Conor的访谈](https://www.youtube.com/watch?v=Hw2kJF_kxjE&feature=emb_logo)

# 宣传(hover me){{comment-button}}
    - 负责成员：#@Jessie

# 总结与Next Step
    
#@Jessie [Victor](Victor.md)
    - Jessie：总体录制过程很棒，中间杰西出现麦的杂音。

可以考虑将内容延伸成播客，参考一下RoamFM


# Backlinks
## [August 12th, 2020](August 12th, 2020.md)
- [Roam面对面🍜 第三期](Roam面对面🍜 第三期.md)

## [🎈内容导航页](🎈内容导航页.md)
- [Roam面对面🍜 第三期](Roam面对面🍜 第三期.md)

