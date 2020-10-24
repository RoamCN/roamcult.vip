# roam-cn.github.io Roam Research 中文社区

> 由于 GitBook 的账号限制，已 fork 至 [https://github.com/JimmyLv/roam-cn.github.io](https://github.com/JimmyLv/roam-cn.github.io)

## Styled Roam (Research)

Roam Research ✍️ Writing with your lovely cards 🧩 and beautiful theme 🎨

> My custom CSS and JavaScript extension for [Roam Research](https://roamresearch.com)

### Quick Start

1. Add a `{{[[roam/js]]}}` tag
2. Add a child JavaScript code block to it with this code...

```js
const CARD_MODE_VERSION = "cb1ded25";
window.URLScriptServer = `https://cdn.jsdelivr.net/gh/JimmyLv/styled-roam@${CARD_MODE_VERSION}/`;

var s = document.createElement("script");
s.type = "text/javascript";
s.src = window.URLScriptServer + "js/index.js";
s.async = true;
document.getElementsByTagName("head")[0].appendChild(s);
```

3. Press the BIG RED button (also works with [roam42](https://github.com/roamhacker/roam42), so you can just put them together)
4. Change CARD_MODE_VERSION value `cb1ded25` to the latest Git commit hash whenever you're ready to upgrade

![Roam Research 卡片式写作 Candy 主题](https://cdn.jsdelivr.net/gh/jimmylv/images@master/2020/09/Roam%20Research%20%E5%8D%A1%E7%89%87%E5%BC%8F%E5%86%99%E4%BD%9C%20Candy%20%E4%B8%BB%E9%A2%98.jpg)

## RoamCN Community

Hi #RoamCN 伙伴们！Roam中文社区的小伙伴目前已经组织了B站、微信圈子、公共图谱和新的Discord平台，致力于更好建设RoamCN中文生态，和大家一起探索 @RoamResearch 的可能性火箭 

- 🐦 Twitter 地址：https://twitter.com/cn_roam
- 🎬 B 站地址：https://space.bilibili.com/599106362
- 🕸Roam 中文站公共图谱（Public Graph)：https://roamresearch.com/#/app/RoamCN/page/3TbMTyHMJ
- 🤗 Discord 永久地址：[https://discord.gg/stMehBs](https://t.co/Pes3bGfqEi?amp=1 "https://discord.gg/stMehBs")
- ⭕️ 微信圈子：直接微信「搜一搜」里面搜「Roam中文社区」
- 🎧 喜马拉雅：[http://xima.tv/7hMJvm?_sonic=0](https://t.co/RnJVvHHV2C?amp=1 "http://xima.tv/7hMJvm?_sonic=0")

![](https://pbs.twimg.com/media/Ek6C1fpXYAEMpfB?format=jpg)

![](https://pbs.twimg.com/media/Ek6C1fuX0AAI7Wm?format=jpg)

![](https://pbs.twimg.com/media/Ek6C1neXYAEN6ph?format=jpg)

![](https://pbs.twimg.com/media/Ek6C1naXUAEqyJe?format=jpg)
