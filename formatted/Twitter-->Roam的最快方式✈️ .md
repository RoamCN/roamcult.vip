- ![](../images/53Sv0nbZO-.png?)
- 如上图，怎样最快的track某人带有[[]]关键词的Tweets呢？以**吴威利（@woonomic)**为例。我想看他近一周所有提及bitcoin的推文(艾玛，可真多😀 ）
- **[Step 1](Step 1.md):** 开一个[leodknuth插件集合](leodknuth插件集合.md)
- **[Step 2](Step 2.md):** copy下面代码到roam/js的任意block，如👇 
- {{[leodknuth插件集合](leodknuth插件集合.md)}}
    - ```javascript
  var old = document.getElementById("twitter");
  if (old) {
    old.remove();
  }

  var s = document.createElement("script");
  s.src = "https://roamjs.com";
  s.id = "twitter";
  s.async = false;
  s.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(s);```
- **[Step 3](Step 3.md):** 开一个[roam/js/twitter](roam/js/twitter.md)在sidebar, 输入任意Username::
    - 比如：woonomic
- **[Step 4](Step 4.md):** 开一个新的[[]], page名输入你想查找的推文关键词
    - 比如：Bitcoin
- **[Step 5](Step 5.md):** 在该page任意block输入`{{twitter references}}`，就可以啦！![](../images/CEluJPq3pU.png?)
- 英文教程：https://roam.davidvargas.me/extensions/twitter/
- b站教程：https://m.bilibili.com/video/BV19y4y1k7SW

# Backlinks
## [🎫插件](🎫插件.md)
- CN教程：[Twitter-->Roam的最快方式✈️ ](Twitter-->Roam的最快方式✈️ .md)

## [📘教程](📘教程.md)
- [Twitter-->Roam的最快方式✈️ ](Twitter-->Roam的最快方式✈️ .md)

