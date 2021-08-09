- [[Day log shortnames]]
    - study: Study
    - work: Work
    - life: Life
- 
- ^^操作方法^^
    1. 安装插件。创建一个`{{[[roam/js]]}}`块并在其下复制插件的代码。单击`是，我知道我在做什么`按钮。重新加载漫游。
    2. 创建一个名为`[[Day log shortnames]]`的块，它将帮助您为要跟踪的任务添加小键
        - `[[Day log shortnames]]`子级内容: `:`左边为`[[Day Log]]`子级的任务简称,右边为输入 `--ws`后的时间归集类别
    3. 现在您可以开始在`[[Day Log]]`下编写您的条目。__请确保条目嵌套在此块下。__
        - 条目的格式应为: `开始时间 - 结束时间 任务简称: 任务描述`
            - ^^注意点^^
                - 起止日期与`-`之间要空一格,不然归集不到
                - 任务简称一定要先在`[[Day log shortnames]]`子级下进行描述,不然归集不到
    4. 在一周结束时，您可以在任何地方键入`--ws`以查看您的时间摘要。
- 
- 
- 修改一周的开始为周一而非周日 `startOf("week")`改为 `startOf("isoweek")`
- 
- {{[[roam/js]]}}
    - ```javascript
function include_script(url){var script=document.createElement("script");script.src=url;script.type="text/javascript";const scripts=Array.from(document.getElementsByTagName("script"));if(scripts.filter((x)=>x.src==url).length==0)
document.getElementsByTagName("head").item(0).appendChild(script);}
include_script("https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.29.1/moment.min.js");document.addEventListener("input",function(e){if("_daylogTemplateHook"in window){setTimeout(function(){window._daylogTemplateHook(e);},0);}});window._daylogTemplateHook=async function(e){var elem=e.target;if(elem.nodeName!="TEXTAREA"||elem.value!=="--ws")return;console.log("ok",elem.value,e.data,elem);const results=await getSummary();const parentBlockId=elem.id.replace(/^.*-/,"");window.roamAlphaAPI.updateBlock({block:{string:results[0],uid:parentBlockId},});for(i=1;i<results.length;i++){window.roamAlphaAPI.createBlock({location:{"parent-uid":parentBlockId,order:0},block:{string:results[i],uid:window.roamAlphaAPI.util.generateUID(),},});}};const getSummary=async()=>{const daylogEntries=window.roamAlphaAPI.q(`[
                        :find (pull ?referencingBlock [
                      		:node/title
                      		:block/string
							:block/children
                            :block/parents
                        	{:block/children ...}
                            {:block/parents [ :node/title ]}
                      	])
                        :in $ ?pagetitle
                        :where
                            [?referencingBlock :block/refs ?referencedPage]
                            [?referencedPage :node/title ?pagetitle]
                        ]`,"Day Log");const lastWeekEntries=daylogEntries.map((arr)=>arr[0]).filter((entry)=>{const date=moment(entry.parents[0].title,"MMMM Do, YYYY");return date.isSameOrAfter(moment().startOf("isoweek"));});const timeEntries=lastWeekEntries.reduce((acc,cur)=>[...acc,...cur.children],[]).map((child)=>child.string);const titleForKeyEntries=window.roamAlphaAPI.q(`[
                        :find (pull ?referencingBlock [
                      		:node/title
                      		:block/string
							:block/children
                        	{:block/children ...}
                      	])
                        :in $ ?pagetitle
                        :where
                            [?referencingBlock :block/refs ?referencedPage]
                            [?referencedPage :node/title ?pagetitle]
                        ]`,"Day log shortnames");const titleForKey={};if(titleForKeyEntries[0][0].children){titleForKeyEntries[0][0].children.forEach(({string})=>{const matcher=string.match(/(.*?): (.*?)$/);if(matcher){titleForKey[matcher[1].trim()]=matcher[2];}});}
const results={};timeEntries.forEach((entry)=>{const logMatch=entry.match(/^(\d+:\d+) - (\d+:\d+) (.*?):/);if(logMatch){const timeDiff=moment(logMatch[2],"HH:mm").diff(moment(logMatch[1],"HH:mm"),"minutes");const key=logMatch[3].trim();const existingTime=results[titleForKey[key]||key]??0;results[titleForKey[key]||key]=existingTime+timeDiff;}});console.log(results);const toPrint=[`[[Weekly Summary]] from [[${moment().startOf("isoweek").format("MMMM Do, YYYY")}]] to [[${moment().format("MMMM Do, YYYY")}]]`,];Object.keys(results).forEach((key)=>{toPrint.push(`Spent ${moment.duration(results[key],"minutes").hours()}h ${moment.duration(results[key],"minutes").minutes()}m ${key}`);});return toPrint;};```
