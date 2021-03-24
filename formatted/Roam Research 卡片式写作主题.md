- Styled Roam (Research):  ✍️ Writing with your lovely cards 🧩 and beautiful theme 🎨https://github.com/JimmyLv/styled-roam
    - ![Roam Research 卡片式写作 Candy 主题](https://camo.githubusercontent.com/8d511ec4e0b18dbe30063154ba72b0c88de0c561/68747470733a2f2f63646e2e6a7364656c6976722e6e65742f67682f6a696d6d796c762f696d61676573406d61737465722f323032302f30392f526f616d253230526573656172636825323025453525384425413125453725383925383725453525424325384625453525383625393925453425424425394325323043616e64792532302545342542382542422545392541322539382e6a7067)
    - ![](../images/oBtA-zX051.png?)
    - ![RoamResearch卡片Flow模式](https://raw.staticdn.net/JimmyLv/images/master/2020/Roam Research 卡片 Flow 模式.gif)
    - ![RoamResearch卡片式青色主题](https://raw.staticdn.net/JimmyLv/images/master/2020/Roam Research 卡片式青色主题.jpg)

## Quick Start
    1. Add a [leodknuth插件集合](leodknuth插件集合.md) tag
    2. Add a child JavaScript code block to it with this code...
        - ```javascript
const CARD_MODE_VERSION = "gh-pages";
window.URLScriptServer = `https://raw.githack.com/JimmyLv/styled-roam/${CARD_MODE_VERSION}/`;

var existing = document.getElementById("styled-roam");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = window.URLScriptServer + "js/index.js";
  extension.id = "styled-roam";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}```
    3. Press the BIG RED button (also works with [roam42](https://github.com/roamhacker/roam42), so you can just put them together)
    4. Change CARD_MODE_VERSION value `master` to the latest Git commit hash whenever you're ready to upgrade
        - ![](https://raw.staticdn.net/JimmyLv/styled-roam/master/preview/git%20hash.png)

## Quick Review
    - Gingko 卡片式写作完整视频 Demo
        - https://twitter.com/Jimmy_JingLv/status/1305893239187103749?s=20
    - 卡片式写作模式切换演示 Demo
        - https://twitter.com/Jimmy_JingLv/status/1304451043594387456

## 模式切换
    - 其实加上[roam42](roam42.md)的 alt+m 快捷键，可以快速显示当前内容为Markdown格式，所以说总共4种模式：
        
1. 卡片列表：Shift+Alt+1
            - ![](../images/ZeWNE1A7CC.png?)µ
        
2. Flow模式：Shift+Alt+2
            - ![](../images/qySyBrU86K.png?)
        
3. 文档模式：Shift+Alt+3
            - ![](../images/q7PDWN7W_B.png?)
        
4. 文本模式：Alt+M
            - ![](../images/VVNUqkOHTn.png?)

# Backlinks
## [November 14th, 2020](November 14th, 2020.md)
- 文档地址：[Roam Research 卡片式写作主题](Roam Research 卡片式写作主题.md)

## [September 16th, 2020](September 16th, 2020.md)
- [Roam Research 卡片式写作主题](Roam Research 卡片式写作主题.md)

- **[feat](feat.md):** 将[Roam Research 卡片式写作主题](Roam Research 卡片式写作主题.md)文

## [September 21st, 2020](September 21st, 2020.md)
- **[fix](fix.md):** 修复了[Roam Research 卡片式写作主题](Roam Research 卡片式写作主题.md)对

## [📘教程](📘教程.md)
- [Roam Research 卡片式写作主题](Roam Research 卡片式写作主题.md)

