- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FRoamCN%2F53Sv0nbZO-.png?alt=media&token=5917d532-2325-4d7b-b97b-d7288b4d1bd5)
- 如上图，怎样最快的track某人带有[[]]关键词的Tweets呢？以**吴威利（@woonomic)**为例。我想看他近一周所有提及bitcoin的推文(艾玛，可真多😀 ）
- Step 1:: 开一个[[leodknuth插件集合]]
- Step 2:: copy下面代码到roam/js的任意block，如👇 
- {{[[leodknuth插件集合]]}}
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
- Step 3:: 开一个[[roam/js/twitter]]在sidebar, 输入任意Username::
    - 比如：woonomic
- Step 4:: 开一个新的[[]], page名输入你想查找的推文关键词
    - 比如：Bitcoin
- Step 5:: 在该page任意block输入`{{twitter references}}`，就可以啦！![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FRoamCN%2FCEluJPq3pU.png?alt=media&token=5b55dc9f-b500-4edf-bcaa-02605ba2bb40)
- 英文教程：https://roam.davidvargas.me/extensions/twitter/
- b站教程：https://m.bilibili.com/video/BV19y4y1k7SW
