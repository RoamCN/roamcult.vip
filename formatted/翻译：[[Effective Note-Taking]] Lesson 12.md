- **[Metadata](Metadata.md):**
    - **[Tags](Tags.md):** #[翻译](翻译.md) #[未发布](未发布.md)
    - **[Source](Source.md):** #[Andy Henson Series](Andy Henson Series.md)
    - 初翻: #[品痞](品痞.md) [wangxh1000](wangxh1000.md)
    - 校对:
- 原文：[[[Effective Note-Taking]([[Effective Note-Taking.md) Lesson 12]]
- 
- 嗨，
- 多人协作是 Roam 的一个挺显著的优势。正如我在第一课中提到的，Roam 不仅仅是个笔记应用。对以一种更具协作的方式进行研究和知识管理，Roam 团队有着更宏伟的[愿景](https://roamresearch.com/?ck_subscriber_id=909315694#/app/help/page/pLXWFvNB3)。如果你有兴趣了解更多，强烈推荐阅读帮助数据库中的[白皮书](https://roamresearch.com/?ck_subscriber_id=909315694#/app/help/page/Vu1MmjinS)内容。
- Roam 离它更广大的目标还有距离，但可供尝试的雏形都已经在了。目前，这些功能许多仍处于试验阶段，后期还会调整变化，另外，确保安全是必须的。如果你对公开笔记给外部访问有任何疑虑，就请保持在 Private 或 Local 数据库，这能确保笔记不会失控泄露。
- 我还想重申第八课中的观点，即除非事先加密，否则不要把任何高度敏感或秘密的内容放进 Roam。

### Public 和 Private 数据库
- 当你成为一名 Roam 的付费用户，你最多可以创建三个 graph (数据库)。它们可以是 Public 或 Private 的。Private 数据库意味着除你以外没人能访问。反之，Public 数据库则代表任何人只要持有链接就能进行只读访问。你也可以把数据库改为 Public 可编辑。

### 授权访问 Private 数据库
- 也许，你决定与他人分享笔记。有几种不同的做法。首先，是设置只读或编辑选项。
- 在 ... 菜单中选择 Share 菜单项
    - ![](../images/Z5HR8B6UXV.png?)
    - 你能看到我的数据库设置为 Private，并且我被授予了只读权限。
    - ![](../images/wI65cE4Qiv.png?)
    - 只需在文本框中输入电子邮件地址并且回车就能授予用户对应的权限(Readers文本框是只读权限，Editors文本框是编辑权限)。
- 把数据库的 URL 发给用户，登录 Roam 后，他们就能像你一样访问数据库。
    - 注意，Roam 数据库的合作者无需支付任何费用。他们可以免费查看或编辑数据库。但除非处于试用或付费状态，否则他们将不能创建任何数据库。一旦共享数据库，你就能在 Account Settings 页看到更多有关协作的详细信息。
- ![](../images/pYmK2UlnO8.png?)
- 你可以点击当前数据库的名字，然后点击 Account Settings and All Graphs 进入该页面。
- ![](../images/CjzHmaGFEx.png?)

### 分享单个页面
- 如果你想分享单个页面，首先到 Share 菜单项中启用页面级别的权限控制。
    - ![](../images/UBxBX-Ri-x.png?)
    - 现在，如果再次访问 ... 菜单，就会看到一个新的 Share Page 菜单项。
    - ![](../images/C12jURwuqa.png?)
- 在该菜单项里，你能在三种模式之间进行切换：Private 模式、默认的 Public Readonly 模式，和 Public Editable 模式。
    - ![](../images/FgOtbKE1pR.png?)
    - 如果人们以 Public Readonly 的方式查看页面，他们会看到包括链接在内的任何内容，但他们无法查看链接页面的内容，除非它们也被公开。页面包含的任何内容，比如 queries 都会被显示出来，所以你确实需要考虑这种动态数据的情况。如果你公开分享了一个从 private 数据库中拉取内容的页面，你可能会意外暴露一些不想暴露的信息。
- 如果你对外共享了数据库或页面，并进而授予他人编辑权限，他们就能像你一样对笔记进行改动，添加页面和 block。Roam 会在编辑过的 block 旁显示一个小的用户头像，用于帮助大家辨别哪里有过改动。根据使用情况的不同，如果你想保留笔记的修改历史，你可能要和其他协作者就 block 内容的版本管理达成一些约定。

## 备份
- 这把我们很好地带入关于数据导出和定期备份重要性的简短讨论。我坚定地认为备份再多也不嫌多。二等于一，而一等于无，这句话可能来自军事领域，但绝对适用于备份。不久前，就有不少关于用户丢失数据的报道，安全总比遗憾好。如果你花了好几个小时写下笔记，完全不想承受丢失数据的风险，那就做一下备份。

### 导出
- Roam 提供了几种导出数据的方法。可以导出单个页面或者整个数据库。这两个选项都在 ... 菜单中。无论你选了哪一个，都能指定导出 markdown(纯文本) 还是 JSON 格式。如果需要再次导入和全面重建数据库，你就要选择 JSON 格式，因为它比 markdown 格式包含更多关于每个页面和 block 的元数据。
- 就我个人而言，我至少会在每周自我回顾的时候做次完整的数据导出。我会同时导出 markdown 和 JSON 格式的数据，并将其保存在以日期命名的文件夹中。值得注意的是，你上传 Roam 的任何文件都不会包含在导出结果中。它们在 markdown 和 JSON 文件中都是以 URL 方式被引用的，所以如果你想下载之前添加到 Roam 中的每张图片或文件的副本，需要另外费些功夫。

### Roam Public
- 来自精彩的 [RoamBrain](https://el2.convertkit-mail2.com/c/68u5q5qvvpuoul2d36to/g3hnhwuz4m42z0/aHR0cHM6Ly93d3cucm9hbWJyYWluLmNvbQ==) 网站的 Francis Miller 还创建了一个内容正在稳步增长的 public Roam 数据库目录。[RoamPublic](https://el2.convertkit-mail2.com/c/68u5q5qvvpuoul2d36to/9qhzhdu2odo828/aHR0cHM6Ly93d3cucm9hbXB1YmxpYy5jb20=) 包含了从圣经到伟大的演讲和讲座，再到像 Marcus Aurelius 的 Meditations 作品这样的公开文本。
- 你可能会想导入其中的一些到自己的数据库中。因为这些都是由其他 Roam 用户创建的 Public 数据库，里面可能会有些没任何意义的每日笔记或页面，所以你不会想导入全部内容。

### 选择性导出
- 这种情况下，更好的做法就是在 All Pages 页面进行选择性导出。点击左侧复选框选择你想导出的页面。为减少干扰，可以点击右侧的日历图标隐藏每日笔记页面。此外，你还能对栏目进行排序，这样不仅可以从连接数或标记页面，还可以通过字数排序更方便地识别包含内容的页面。
- ![](../images/jzXymLqTPL.png?)
- 选完以后，点击向上的箭头图标就能导出格式为 JSON 或 markdown 的数据。我建议导出导入 Roam 数据库时使用 JSON 格式。

### 导入
- 把数据导入 Roam 的过程差不多是相反的。从数据库的 ... 菜单中选择 Import Files。你一次最多能导入 10 个 markdown 文件。Roam 会对它们进行处理，并把结果呈现在列表中，你能继续确认是否导入，或更改页面标题。
- ![](../images/jwqvXRMjqP.png?)
- 对导入其他 Roam 数据库的 JSON 数据，你只要选择 JSON 文件即可。
- 
- 如果你有任何反馈或者迫切想得到回答的问题，欢迎回复这封邮件。我会尽最大努力回复，并将其纳入修订版和今后的课程中。
- 明天是我们的倒数第二课，明天见
- Andy
