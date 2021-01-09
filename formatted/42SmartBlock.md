- 
- {{embed: ((tBZdhZHM-))}}
- > 不要担心自己问的问题听起来很傻。99% 的情况下，其他人都有和你一样的问题，只不过羞于问出口而已。 [*](https://q24.io/api/v1/idea/link/419)
[ 凯文·凯利（Kevin Kelly）（翻译：赵嘉敏）]( 凯文·凯利（Kevin Kelly）（翻译：赵嘉敏）.md)
- [42SmartBlock](42SmartBlock.md) Due me 提醒我
    - <%CURRENTBLOCKREF:blockRef%>
    - <%SET:curBlock,<%RESOLVEBLOCKREF:<%GET:blockRef%>%>%><%NOBLOCKOUTPUT%>
    - <%JAVASCRIPT:
```javascript
var curBlock = roam42.smartBlocks.activeWorkflow.vars["curBlock"];
var content = curBlock.substring(0,curBlock.indexOf(';;')).trim();
var currentUrl = encodeURIComponent(window.location.href);
window.open("due://x-callback-url/add?title=" + content + "&x-success=" + currentUrl);
return '';```
%><%NOBLOCKOUTPUT%>
- [42SmartBlock](42SmartBlock.md) Random Quotes 随机语录
    - <%NOBLOCKOUTPUT%><%JAVASCRIPTASYNC: ```javascript
var settings = {
  "url": "https://api.quotable.io/random",
  "method": "GET",
  "timeout": 0,
  "async": false
};

$.ajax(settings).done(function (response) {
  console.log(response);
  var jsonQuotes = JSON.stringify(response);
  var quote = JSON.parse(jsonQuotes);
  roam42.smartBlocks.activeWorkflow.vars['author'] = quote.author;
  roam42.smartBlocks.activeWorkflow.vars['quote'] = quote.content;
});
return '';``` %>
    - <%JAVASCRIPT: document.activeElement.value = ""; return'> ';%><%GET:quote%>
[<%GET:author%>](<%GET:author%>.md)
    - 
    - 
    - 
- [42SmartBlock](42SmartBlock.md) TickTick 滴答清单
    - <%CURRENTBLOCKREF:blockRef%>
    - <%SET:curBlock,<%RESOLVEBLOCKREF:<%GET:blockRef%>%>%><%NOBLOCKOUTPUT%>
    - <%JAVASCRIPT:
```javascript
var curBlock = roam42.smartBlocks.activeWorkflow.vars["curBlock"];
var content = curBlock.substring(0,curBlock.indexOf(';;')).trim();
var currentUrl = encodeURIComponent(window.location.href);
window.open("ticktick://x-callback-url/v1/add_task?title=" + content + "&x-success=" + currentUrl);
return '';```
%><%NOBLOCKOUTPUT%>
- 
- 
- [42SmartBlock](42SmartBlock.md) Flomo 回顾浮墨岛
    - <%CURRENTBLOCKREF:blockRef%>
    - <%SET:curBlock,<%RESOLVEBLOCKREF:<%GET:blockRef%>%>%><%NOBLOCKOUTPUT%>
    - <%JAVASCRIPT:
```javascript
var curBlock = roam42.smartBlocks.activeWorkflow.vars["curBlock"];
var content = curBlock.substring(0,curBlock.indexOf(';;')).trim();
var currentUrl = window.location.href;

var settings = {
  "url": "https://flomoapp.com/iwh/NzE5/6ba1568079857c2c7de64941ab4f2caf/",
  "data": {
    "content": `${content} ${currentUrl}`
  },
  "method": "POST",
  "timeout": 0,
  "async": false
};

$.ajax(settings).done(function (response) {
  console.log(response);
});

return '';```
%><%NOBLOCKOUTPUT%>
    - 
- [42SmartBlock](42SmartBlock.md) Useless Ideas 随机灵感
    - <%NOBLOCKOUTPUT%><%JAVASCRIPTASYNC: ```javascript
var settings = {
  "url": "https://q24.io/api/v1/idea",
  "method": "GET",
  "timeout": 0,
  "async": false
};

$.ajax(settings).done(function (response) {
  console.log(response);
  var jsonQuotes = JSON.stringify(response);
  var quote = JSON.parse(jsonQuotes);
  roam42.smartBlocks.activeWorkflow.vars['author'] = quote.author;
  roam42.smartBlocks.activeWorkflow.vars['quote'] = quote.idea;
  roam42.smartBlocks.activeWorkflow.vars['url'] = quote.url;
});
return '';``` %>
    - <%JAVASCRIPT: document.activeElement.value = ""; return'> ';%><%GET:quote%> [*](%GET:url%>)
[<%GET:author%>](<%GET:author%>.md)
- 
- [42SmartBlock](42SmartBlock.md) Random Poem 随机诗词
    - <%NOBLOCKOUTPUT%><%JAVASCRIPTASYNC: ```javascript
var settings = {
  "url": "https://v1.jinrishici.com/all.json",
  "method": "GET",
  "timeout": 0,
  "async": false
};

$.ajax(settings).done(function (response) {
  console.log(response);
  var jsonQuotes = JSON.stringify(response);
  var quote = JSON.parse(jsonQuotes);
  roam42.smartBlocks.activeWorkflow.vars['author'] = quote.author;
  roam42.smartBlocks.activeWorkflow.vars['quote'] = quote.content;
  roam42.smartBlocks.activeWorkflow.vars['source'] = quote.origin;
});
return '';``` %>
    - <%JAVASCRIPT: document.activeElement.value = ""; return'> ';%><%GET:quote%> __——《<%GET:source%>》__
[<%GET:author%>](<%GET:author%>.md)
- 
- [42SmartBlock](42SmartBlock.md) Tweet this
    - <%CURRENTBLOCKREF:blockRef%>
    - <%SET:curBlock,<%RESOLVEBLOCKREF:<%GET:blockRef%>%>%><%NOBLOCKOUTPUT%>
    - <%JAVASCRIPTASYNC:```javascript
var curBlock = roam42.smartBlocks.activeWorkflow.vars["curBlock"];
var content = curBlock.substring(0,curBlock.indexOf(';;')).trim();
// Encode as URL
var tweetURLstart = "https://twitter.com/intent/tweet?text=";
var tweetURL = tweetURLstart.concat(encodeURIComponent(content));
// Open tab with Tweet in compose box!
var currentUrl = encodeURIComponent(window.location.href);
window.open(tweetURL + ' ' + currentUrl);
return '';```%>
- 
- > Hello 待开发~
- 
- 
- 
- ---
- 
- [用Smartblocks从unsplash中获取图片](用Smartblocks从unsplash中获取图片.md)
    - ![](../images/zySuNf9H2I.gif?)
    - 视频教程：https://www.loom.com/share/3115dffc8a6c47a7b178ce0068af0314
    - 代码：https://github.com/roamhacker/SmartBlocks/issues/152
- [用Smartblocks自动生成时间序列](用Smartblocks自动生成时间序列.md)
    - ![](../images/Y_1JrnWfHV.gif?)
    - 视频教程：https://www.loom.com/share/232f57b1fb4d4d6c90918bd4522bfea3?sharedAppSource=personal_library
    - Github代码：https://github.com/roamhacker/SmartBlocks/issues/154
- [用Smartblocks一键做ppt](用Smartblocks一键做ppt.md)
    - ![](../images/jiWESDOQuY.gif?)
    - 视频教程：https://www.loom.com/share/71953a50f8c446f28a82abba88d91d13?sharedAppSource=personal_library
    - 用到的插件：https://roamjs.com/docs/extensions/presentation
- [用Smartblocks收集用户信息](用Smartblocks收集用户信息.md)
    - ![](../images/_nlmmpoy2u.gif?)
    - 视频演示：https://www.loom.com/share/4492180e1ca248b0ba46a124292f4f29?sharedAppSource=personal_library
    - 用到的commend:
        - dates
        - input
- [用Smartblocks打造自己的计算器](用Smartblocks打造自己的计算器.md)
    - ![](../images/JHLDabkA3q.gif?)
    - 
- [Chris的官方教程热乎版](Chris的官方教程热乎版.md) updated 12.26
    - {{[youtube](youtube.md): https://www.youtube.com/watch?v=UzKOi0LHxQU}}

# Backlinks
## [🎫插件](🎫插件.md)
- [42SmartBlock](42SmartBlock.md)

- 更多模板请点击 [42SmartBlock](42SmartBlock.md)

## [📘教程](📘教程.md)
- [42SmartBlock](42SmartBlock.md)

