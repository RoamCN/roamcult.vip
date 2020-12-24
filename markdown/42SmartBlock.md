- 
- {{embed: ((tBZdhZHM-))}}
- > 不要担心自己问的问题听起来很傻。99% 的情况下，其他人都有和你一样的问题，只不过羞于问出口而已。 [*](https://q24.io/api/v1/idea/link/419)
[[ 凯文·凯利（Kevin Kelly）（翻译：赵嘉敏）]]
- #42SmartBlock Due me 提醒我
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
- #42SmartBlock Random Quotes 随机语录
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
[[<%GET:author%>]]
    - 
    - 
    - 
- #42SmartBlock TickTick 滴答清单
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
- #42SmartBlock Flomo 回顾浮墨岛
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
- #42SmartBlock Useless Ideas 随机灵感
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
    - <%JAVASCRIPT: document.activeElement.value = ""; return'> ';%><%GET:quote%> [*](<%GET:url%>)
[[<%GET:author%>]]
- 
- #42SmartBlock Random Poem 随机诗词
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
[[<%GET:author%>]]
- 
- #42SmartBlock Tweet this
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
