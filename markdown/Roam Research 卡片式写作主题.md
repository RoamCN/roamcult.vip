- Styled Roam (Research):  ✍️ Writing with your lovely cards 🧩 and beautiful theme 🎨https://github.com/JimmyLv/styled-roam
    - ![Roam Research 卡片式写作 Candy 主题](https://camo.githubusercontent.com/8d511ec4e0b18dbe30063154ba72b0c88de0c561/68747470733a2f2f63646e2e6a7364656c6976722e6e65742f67682f6a696d6d796c762f696d61676573406d61737465722f323032302f30392f526f616d253230526573656172636825323025453525384425413125453725383925383725453525424325384625453525383625393925453425424425394325323043616e64792532302545342542382542422545392541322539382e6a7067)
    - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FRoamCN%2FoBtA-zX051.png?alt=media&token=5123b195-7f6b-4c2f-98f9-16f236acc8b2)
    - ![RoamResearch卡片Flow模式](https://raw.staticdn.net/JimmyLv/images/master/2020/Roam Research 卡片 Flow 模式.gif)
    - ![RoamResearch卡片式青色主题](https://raw.staticdn.net/JimmyLv/images/master/2020/Roam Research 卡片式青色主题.jpg)
- ## Quick Start
    1. Add a [[roam/js]] tag
    2. Add a child JavaScript code block to it with this code...
        - ```javascript

const CARD_MODE_VERSION = 'master'
window.URLScriptServer = `https://cdn.jsdelivr.net/gh/JimmyLv/styled-roam@${CARD_MODE_VERSION}/`
var s = document.createElement('script')
	s.type = "text/javascript"
    s.src =  window.URLScriptServer + "js/index.js"
	s.async = true
document.getElementsByTagName('head')[0].appendChild(s)```
    3. Press the BIG RED button (also works with [roam42](https://github.com/roamhacker/roam42), so you can just put them together)
    4. Change CARD_MODE_VERSION value `master` to the latest Git commit hash whenever you're ready to upgrade
        - ![](https://raw.staticdn.net/JimmyLv/styled-roam/master/preview/git%20hash.png)
- ## Quick Review
    - Gingko 卡片式写作完整视频 Demo
        - https://twitter.com/Jimmy_JingLv/status/1305893239187103749?s=20
    - 卡片式写作模式切换演示 Demo
        - https://twitter.com/Jimmy_JingLv/status/1304451043594387456
- ## 模式切换
    - 其实加上[[roam42]]的 alt+m 快捷键，可以快速显示当前内容为Markdown格式，所以说总共4种模式：
        - 1. 卡片列表：Shift+Alt+1
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FRoamCN%2FZeWNE1A7CC.png?alt=media&token=e3c89407-d34f-430c-8ed8-c94e33fb5e04)µ
        - 2. Flow模式：Shift+Alt+2
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FRoamCN%2FqySyBrU86K.png?alt=media&token=db345b85-c0b5-4e8f-a8f4-0e49aeaa5732)
        - 3. 文档模式：Shift+Alt+3
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FRoamCN%2Fq7PDWN7W_B.png?alt=media&token=538959fc-5737-4386-95a7-a4084b2bc670)
        - 4. 文本模式：Alt+M
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FRoamCN%2FVVNUqkOHTn.png?alt=media&token=4520a47a-3bf5-40fa-96d1-aa33aec1adb9)
