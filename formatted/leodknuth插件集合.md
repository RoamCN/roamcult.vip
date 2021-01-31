- >说明：
1. 不要在本页点击“Yes, I know what I'm doing.”按钮，这会让我们RoamCN的js插件生效，可能会造成js插件之间的冲突
2.建议选择合适的插件，将javascript代码拷贝粘贴到自己roam/js运营
3.以下排版是以一个功能js插件前用一个\{roam/js\}打头的方式，目的是修改某个js功能模块时，不影响其他js功能模块的运行
- 第一个js模块：roam42启用模块
    - > 启用roam42，很多js代码会基于roam42基础运行（特别是42smartblock）。代码如下：
- {{roam/js}}
    - ```javascript
// DISABLE FEATURES
// Remove two forward slashes from in front of name 
// of feature to DISABLE it
// Everything is enabled by default
window.disabledFeatures = [
  // 'quickReference',
  // 'turnDown',
  // 'dateProcessing',
  // 'lookupUI',
  // 'livePreview',
  // 'dailyNote',
  // 'jumpToDate',
  // 'jumpNav',
];

// Live Preview - to change the defaults 
// 1) remove // in front of parameter to ACTIVATE the change
// 2) modify the value to change it's behavior
// width  = width of preview window
// height = height of preview window
// delay  = milliseconds of delay for preview to 
// 			fire (defaults to 200) can be set to 0
window.roam42LivePreview = {
  //width:	'400px',
  //height: '600px',
  //delay: 500,
}

// Change the Deep navigation options
// activate-on-no-focus - activate navigation mode when body is focused (default: false)
// REMOVE // in front of setting to change it from default setting
window.roamNavigatorSettings = {
 //  'activate-on-no-focus': true, 
}

var s = document.createElement('script')
	s.type = "text/javascript"
    s.src =  "https://cdn.jsdelivr.net/gh/roamhacker/roam42/main.js"
  	s.async = true
document.getElementsByTagName('head')[0].appendChild(s)

const CARD_MODE_VERSION = 'dev'
window.URLScriptServer = `https://cdn.jsdelivr.net/gh/JimmyLv/styled-roam@${CARD_MODE_VERSION}/`
var s = document.createElement('script')
	s.type = "text/javascript"
    s.src =  window.URLScriptServer + "js/index.js"
	s.async = true
document.getElementsByTagName('head')[0].appendChild(s)```
- <script src="https://kit.fontawesome.com/8c717ed232.js" crossorigin="anonymous"></script>
- 第二个js模块：卡片写作模块
    - > 该模块由 @JimmyLv 提供，模拟卡片写作的环境。代码如下：
- {{roam/js}}
    - 
    - ```javascript

// DISABLE FEATURES
// Remove two forward slashes from in front of name 
// of feature to DISABLE it
// Everything is enabled by default
window.disabledFeatures = [
  // 'quickReference',
  // 'turnDown',
  // 'dateProcessing',
  // 'lookupUI',
  // 'livePreview',
  // 'dailyNote',
  // 'jumpToDate',
  // 'jumpNav',
];

// Live Preview - to change the defaults 
// 1) remove // in front of parameter to ACTIVATE the change
// 2) modify the value to change it's behavior
// width  = width of preview window
// height = height of preview window
// delay  = milliseconds of delay for preview to 
// 			fire (defaults to 200) can be set to 0
window.roam42LivePreview = {
  //width:	'400px',
  //height: '600px',
  //delay: 500,
};

// Change the Deep navigation options
// activate-on-no-focus - activate navigation mode when body is focused (default: false)
// REMOVE // in front of setting to change it from default setting
window.roamNavigatorSettings = {
 //  'activate-on-no-focus': true, 
};

var s = document.createElement('script');
	s.type = "text/javascript";
    // s.src =  "https://roam42.glitch.me/main.js";
	s.src =  "https://cdn.jsdelivr.net/gh/roamhacker/roam42/main.js";
  	s.async = true;
document.getElementsByTagName('head')[0].appendChild(s);```
- {{roam/js}}
    - ```javascript
const CARD_MODE_VERSION = 'master'
window.URLScriptServer = `https://cdn.jsdelivr.net/gh/JimmyLv/styled-roam@${CARD_MODE_VERSION}/`
var s = document.createElement('script')
	s.type = "text/javascript"
    s.src =  window.URLScriptServer + "js/index.js"
	s.async = true
document.getElementsByTagName('head')[0].appendChild(s)```
- 第三个js模块：获取tweet
    - > 当你拷贝某条tweet的链接，粘贴到roam，自动将链接的推文获取到粘贴位置。代码如下：
- {{roam/js}}
    - ```javascript
var old = document.getElementById("twitter");
if (old) {
  old.remove();
}

var s = document.createElement("script");
s.src = "https://roamjs.com/master/twitter.js";
s.id = "twitter";
s.async = false;
s.type = "text/javascript";
document.getElementsByTagName("head")[0].appendChild(s);```
- 第四个js模块：拉取所在页面的references到本页
    - > 激活语法为 {{pull references}}**（不要试图按本页的pull references按钮）**
- {{roam/js}}
    - ```javascript
var old = document.getElementById("pull-references");
if (old) {
  old.remove();
}

var s = document.createElement("script");
s.src = "https://roamjs.com/pull-references.js";
s.id = "pull-references";
s.async = false;
s.type = "text/javascript";
document.getElementsByTagName("head")[0].appendChild(s);```
- 第五个js模块：TO-DO Trigger
    - >当todo被标记完成时，可以自动添加标签、自定义尾缀，同时将此条todo画上删除线。代码如下：
- {{roam/js}}
    - Filter attribute tables
    - ```javascript
//v0.3
//Github Gist: https://gist.github.com/GitMurf/aece9f105628640cb79925d1310449ec
//DEMO on how to use: https://user-images.githubusercontent.com/64155612/95652671-9f198c80-0aa7-11eb-8f8e-bc08fe81b985.gif
    //Click the '---' in header row of attribute table (1st column)
    //Click a filter icon and start typing filter in input box above the table
    //CONDITIONS and "BLANK" cells
        //Add {not} before any search term to exclude the term e.g., {not}invoice
        //Add {and} to require multiple e.g., invoice {and} payment {and} {not} september
            //Notice on the last example i combined {and} with the {not} clause for the third term
        //Add {or} to find "either" criteria e.g., invoice {or} payment {or} purchase
            //NOTE: You CANNOT combine {and} with {or} conditions
        //TIP: For large attr-tables it may be a bit laggy since it updates filter with every keystroke.
            //To speed it up, you can also enclose a search term in {search term} and it won't apply filter until the closing "}" is pressed
//MUST have David's Sorting Attribute Tables script installed
//Details on David Vargas' Sorting Attribute Tables script:
  //Website: https://roam.davidvargas.me/extensions/attr-tables/
  //Tweet: https://twitter.com/dvargas92495/status/1313897302201958401?s=20

function filterAttr(evt){
    //Get the sort button clicked by user to activate the filter
    var clickedElem = evt.target
    var clickedElemTag = clickedElem.tagName
    if(clickedElemTag !== 'TH'){return}
    if(clickedElem.cellIndex !== 0){return}
    //if(clickedElem.innerText !== '---'){return}

    //Get table header element
    var tableHeaderRow = clickedElem.parentElement
    //check if filter already created
    var filtersCreated = tableHeaderRow.querySelectorAll('[data-filter-index]')[0]
    if(filtersCreated !== null && filtersCreated !== 'undefined' && typeof filtersCreated !== 'undefined')
    {
        //Found a filter already so exit function
        //console.log("found filter")
        return
    }

    //Get the roam-table parent element
    var roamTableElem = clickedElem.parentElement.parentElement.parentElement.parentElement

    //Create the parent DIV for the filter input box
    var newDiv = document.createElement('div')
    newDiv.id = 'filterBox'
    newDiv.style.cssText = 'display:flex;margin-bottom:5px'
    roamTableElem.insertBefore(newDiv, roamTableElem.lastElementChild)

    //Create the input box that user enters filter criteria
    var newInput = document.createElement('input')
    newInput.value = ''
    newInput.id = 'fbFilterInput'
    newInput.name = 'fbFilterInput'
    newInput.style.cssText = 'width:150px;display:flex;color:black;caret-color:black'
    newDiv.appendChild(newInput)

    //Create span that shows row count
    var filterRowCt = document.createElement("span")
    filterRowCt.id = 'filterRowCt'
    filterRowCt.style.cssText = 'display:flex;color:yellow;'
    filterRowCt.textContent = ''
    newInput.parentNode.insertBefore(filterRowCt, newInput.nextSibling)

    //Add filter buttons next to each sort button
    for(var col = 0; col < tableHeaderRow.cells.length; col++)
    {
        var curHeader = tableHeaderRow.cells[col]
        //Find sort icon span
        var curSortIcon = curHeader.getElementsByClassName("bp3-icon")[0]
        //Find parent span of icon
        var sortParSpan = curSortIcon.parentElement

        //Create new parent span for filter icon next to the parent of sort icon
            //add BEFORE sort so its "attr-table-priority-label" still goes on end and stays next to it
        var filterIconParent = document.createElement("span")
        filterIconParent.className = 'bp3-button bp3-minimal bp3-small'
        //Add the new parent span for the filter icon being created below
        sortParSpan.parentNode.insertBefore(filterIconParent, sortParSpan);
        //Create the filter icon
        var filterIcon = document.createElement("span")

        //Had to remove bp3-icon from front of class because David sort extension looks for first bp3-icon (it was 'bp3-icon bp3-icon-filter')
            //Will fix when integrate with David's code
        filterIcon.className = 'bp3-icon-filter' //Choose icons (add after bp3-icon-NAMEofICON) from https://blueprintjs.com/docs/[icons](icons.md)

        //Because of issue above with conflict with David's script, need to add these css formats to make up for know bp3-icon class
        filterIcon.style.cssText = 'margin:0 -7px;font-family:Icons20;font-weight:400'
        filterIcon.id = 'filter' + col
        filterIcon.setAttribute('data-filter-index', col)
        filterIcon.setAttribute('data-filter-value', '')

        //Add onclick function to each filter icon
        filterIcon.onclick = function () {
            var clickedElem = this
            //Get current InputBox element for filtering
            var newInput = document.getElementById("fbFilterInput")
            //console.log('clicked filter button')
            //Check what column index/number it is that was clicked to know which column to filter
            var colIndexClicked = clickedElem.getAttribute('data-filter-index')
            //Set the attribute to the input box
            newInput.setAttribute('data-filter-index', colIndexClicked)

            //Get the current last filter for that column
            var curFilterVal = clickedElem.getAttribute('data-filter-value')
            //Populate the input box with that previous filter
            newInput.value = curFilterVal
            newInput.focus()
            newInput.select()
        }

        filterIconParent.appendChild(filterIcon)
    }

    //Add oninput function to the input box where user types their filter
    newInput.oninput = function () {
        var curFilterInput = this
        //Check what column index/number it is that was clicked to know which column to filter
        var colIndexClicked = curFilterInput.getAttribute('data-filter-index')
        //Get the current value from the filter box
        var inputTxtVal = curFilterInput.value.toString()

        //if opened up an operator like {not} {or} {and} {blank}, do not run all the code below until you close it with } to speed up filtering
        if((inputTxtVal.split("{").length - 1) > (inputTxtVal.split("}").length - 1)){return}

        //Set the corresponding filter span data attribute to the value the user just typed in input box
        var curFilterIcon = document.getElementById("filter" + colIndexClicked)
        curFilterIcon.setAttribute('data-filter-value', inputTxtVal)

        //Get the table element
        var roamTableElem = curFilterInput.parentElement.parentElement

        //Get the rows of attribute table
        var tableRows = roamTableElem.getElementsByTagName("table")[0].rows
        //Get the column count of the attribute table
        var tableCols = tableRows[0].cells.length

        //Set color of filter/sort button if a filter is present
        if(inputTxtVal == '')
        {
            curFilterIcon.style.borderWidth = 'unset'
            curFilterIcon.style.borderStyle = 'unset'
        }
        else
        {
            curFilterIcon.style.borderWidth = '2px'
            curFilterIcon.style.borderStyle = 'dotted'
            curFilterIcon.style.borderColor = 'springgreen'
            curFilterIcon.style.marginLeft = '5px'
        }

        //Looping through each column
        const filterArr = [];

        for(var j = 0; j < tableCols; j++)
        {
            //Check if filter value present from column filters
            var eachFilterElem = document.getElementById("filter" + j)
            if(eachFilterElem !== null && eachFilterElem !== 'undefined' && typeof eachFilterElem !== 'undefined')
            {
                //Col filter value
                var eachFilterVal = eachFilterElem.getAttribute('data-filter-value')
                filterArr.push(eachFilterVal.toString());
            }
        }

        var rowCtr = 0
        for(var i = 1; i < tableRows.length; i++) //Skip header row starting with 1 instead of 0
        {
            //Loop through each row
            var curRow = tableRows[i]

            //Start by showing each row and then filter with each column below
            curRow.style.display = "table-row"
            var hideRow = 0
            for (itm = 0; itm < filterArr.length; itm++)
            {
                var eachFilterElem = filterArr[itm]
                if(eachFilterElem !== '')
                {
                    //Col filter value
                    var eachFilterTextOrig = eachFilterElem.toString()
                    var eachFilterText = eachFilterTextOrig.toLowerCase()

                    //Replace the operators to put into query syntax form for the loop below
                    var querySyntax = eachFilterText.split("{blank}").join("{||}{blank}{||}").split("{not}").join("{||}{not}{||}").split("{and}").join("{||}{and}{||}").split("{or}").join("{||}{or}{||}")

                    //Current row / col value in table to check against filter
                    var curCell = curRow.cells[itm]
                    var curValue = curCell.innerText
                    var curElemText = curValue.toString().toLowerCase()
                    var queryArray = querySyntax.split('{||}')
                    var lastOperator = ''
                    var isNot = 0

                    //Loop through each criteria to see if row qualifies
                    for(var ctr = 0; ctr < queryArray.length; ctr++)
                    {
                        var eachArrVal = queryArray[ctr].trim()
                        if(eachArrVal != '')
                        {
                            if(eachArrVal == '{not}'){isNot = 1}
                            if(eachArrVal == '{and}'){lastOperator = 'and'}
                            if(eachArrVal == '{or}'){lastOperator = 'or'}

                            if(eachArrVal != '{not}' && eachArrVal != '{and}' && eachArrVal != '{or}' && eachArrVal != '{blank}')
                            {
                                //Clean out / remove the leading and trailing {SEARCH TERM} around a search
                                eachArrVal = eachArrVal.split("{").join("").split("}").join("")
                            }

                            if(eachArrVal != '{not}' && eachArrVal != '{and}' && eachArrVal != '{or}')
                            {
                                if(lastOperator == '' && isNot == 0)
                                {
                                    //No operators so just simply filter for this value
                                    switch(eachArrVal)
                                    {
                                        case '{blank}':
                                            if(curElemText != '')
                                            {
                                                hideRow = 1
                                            }else{hideRow = -1}
                                            break;
                                        default:
                                            if(curElemText.indexOf(eachArrVal) == -1)
                                            {
                                                hideRow = 1
                                            }else{hideRow = -1}
                                    }
                                }
                                else
                                {
                                    if(isNot == 1)
                                    {
                                        //NOT clause is activated so look for inverse of search term
                                        isNot = 0
                                        if(lastOperator != 'or')
                                        {
                                            //Looking to exclude/hide row if matches this value
                                            if((curElemText.indexOf(eachArrVal) > -1 && eachArrVal != '{blank}') || (eachArrVal == '{blank}' && curElemText == ''))
                                            {
                                                hideRow = 1
                                            }
                                        }
                                        else
                                        {
                                            //OR clause means show the row if found this time because may have been hidden from the first or clause
                                            if((curElemText.indexOf(eachArrVal) == -1 && eachArrVal != '{blank}') || (eachArrVal == '{blank}' && curElemText != ''))
                                            {
                                                //Using -1 to account for situation where any can be satisfied with OR
                                                hideRow = -1
                                            }
                                            else
                                            {
                                                if(hideRow == 0){hideRow = 1}
                                            }
                                        }
                                    }
                                    else
                                    {
                                        //NOT clause is not activated
                                        if(lastOperator != 'or')
                                        {
                                            //Looking to exclude/hide row if does not match this
                                            if(curElemText.indexOf(eachArrVal) == -1 || (eachArrVal == '{blank}' && curElemText != ''))
                                            {
                                                hideRow = 1
                                            }
                                        }
                                        else
                                        {
                                            //OR clause means show the row if found this time because may have been hidden from the first or clause
                                            if((curElemText.indexOf(eachArrVal) > -1 && eachArrVal != '{blank}') || (eachArrVal == '{blank}' && curElemText == ''))
                                            {
                                                //Using -1 to account for situation where any can be satisfied with OR
                                                hideRow = -1
                                            }
                                            else
                                            {
                                                if(hideRow == 0){hideRow = 1}
                                            }
                                        }
                                    }
                                }
                            }
                        }
                    }
                }
                else
                {
                    //No filter entered for this column
                }
                if(hideRow == 1)
                {
                    curRow.style.display = "none"
                    break
                }
            }
            if(hideRow != 1){rowCtr = rowCtr + 1}
        }
        var filterRowCt = document.getElementById("filterRowCt")
        filterRowCt.textContent = 'Results: ' + rowCtr
    };
}

document.addEventListener('click', filterAttr)```
- {{roam/js}}
    - ```javascript
var old = document.getElementById("todo-trigger");
if (old) {
  old.remove();
}

var s = document.createElement("script");
s.src = "https://roamjs.com/todo-trigger.js";
s.id = "todo-trigger";
s.async = false;
s.type = "text/javascript";
document.getElementsByTagName("head")[0].appendChild(s);```
        - 完成以上代码复制后，仍需在你的roam里创建一个名为"roam/js/todo-trigger"的页面，并将以下三行内容粘贴进入:
            - **[Append Text](Append Text.md):** /Today  /Current Time
            - **[Replace Tags](Replace Tags.md):**
            - **[Strikethrough](Strikethrough.md):**{{True}}
- {{roam/js}}
    - Wikipedia Search and Insert
    - ```javascript
var old = document.getElementById("wiki-data");
if (old) {
  old.remove();
}

var s = document.createElement("script");
s.src = "https://roamjs.com/wiki-data.js";
s.id = "wiki-data";
s.async = false;
s.type = "text/javascript";
document.getElementsByTagName("head")[0].appendChild(s);```
- {{roam/js}}
    - Youtube Player Time Stamp
    - ```javascript
// ==UserScript==
// @name         Responsive YouTube with Timestamp Control for Roamresearch
// @author       Connected Cognition Crumbs <c3founder@gmail.com>
// @version      0.2
// @description  Add timestamp controls to YouTube videos embedded in Roam and makes the player responsive. 
// @match        https://*.roamresearch.com

(function() {
    let ytApiReady = false;
    const players = new Map();  	
    const activateYtVideos = () => {	
        if (!ytApiReady) {
            if (window.YT !== undefined) loadYtApi(); // wait until Roam loads its YT, then insert script on top
            return null;
        }
        Array.from(document.getElementsByTagName('IFRAME'))
            .filter(iframe => iframe.src.includes('youtube.com'))            
            .forEach(ytEl => {          		
          		const block = ytEl.closest('.roam-block-container');          		
          		if(ytEl.src.indexOf("enablejsapi") === -1){
                  var ytId = extractVideoID(ytEl.src); 
                  var frameId = genUniquePlayerId(ytEl,ytId);			
                  ytEl.parentElement.id = frameId; 
                  ytEl.remove();
                  players[frameId] = new window.YT.Player(frameId, {
                    height: '300',
                    width: '450', 
                    videoId: ytId
                  });                        
                  wrapIframe(frameId);
                } else {				                                      
                  var frameId = ytEl.id				  
                }         
          		addTimestampControls(block, players[frameId]);   
          		var sideBarOpen = document.getElementById("right-sidebar").childElementCount - 1;
          		//Make iframes flexible
          		adjustIframe(frameId, sideBarOpen);  
        	});
    };

	const genUniquePlayerId = (ytEl, ytId) => {
      var d = new Date();
      var n = d.getTime();
      const rsideBar = ytEl.closest('[right-sidebar](right-sidebar.md)');
      return (rsideBar ? (ytId + '-rSide') : ytId) + n;
    };  	
  
    const addTimestampControls = (block, player) => {
      if (block.children.length < 2) return null;
      const childBlocks = Array.from(block.children[1].querySelectorAll('.roam-block-container'));
      childBlocks.forEach(child => {
        const timestamp = getTimestamp(child);
        const buttonIfPresent = child.querySelectorAll('.timestamp-control')[0]
        if (buttonIfPresent) {
          	buttonIfPresent.remove();
        }
        if (timestamp) { 
          addControlButton(child, () => player.seekTo(timestamp, true));
        }
      });
	};
  
	const adjustIframe = (frameId, sideBarOpen) => {
      var child = document.getElementById(frameId); //Iframe
      var par = child.parentElement;
      if(sideBarOpen){
        child.style.position = 'absolute';
        child.style.margin = '0px';
        child.style.border = '0px';
        child.style.width = '100%';
        child.style.height = '100%';
        child.style.borderStyle = 'inset';
        child.style.borderRadius = '25px';
        par.style.position = 'relative';
        par.style.paddingBottom = '56.25%';     
        par.style.height = '0px';
      } else {
      	child.style.position = null;
        child.style.margin = '0px';
        child.style.border = '0px';        
        child.style.width = '600px';
        child.style.height = '400px';
        child.style.borderStyle = 'inset';
        child.style.borderRadius = '25px';
        par.style.position = null;
        par.style.paddingBottom = '0px';   
		par.style.height = '420px';
      }
    }
    
    //const wrapIframe = (frameId, divId) => {
    const wrapIframe = (frameId) => {
      var child = document.getElementById(frameId); //Iframe
      var par = document.createElement('div');
      child.parentNode.insertBefore(par, child);
      par.appendChild(child);
      child.style.position = 'absolute';
      child.style.margin = '0px';
      child.style.border = '0px';
      child.style.width = '100%';
      child.style.height = '100%';
      par.style.position = 'relative';
      par.style.paddingBottom = '56.25%';     
      par.style.height = '0px';
      //par.id = divId;
    };
    const getControlButton = (block) => block.querySelectorAll('.timestamp-control')[0];

    const addControlButton = (block, fn) => {
        const button = document.createElement('button');
        button.innerText = '►';
        button.classList.add('timestamp-control');
      	button.style.borderRadius = '50%';
        button.addEventListener('click', fn);
        const parentEl = block.children[0].children[0];
        parentEl.insertBefore(button, parentEl.querySelectorAll('.roam-block')[0]);
    };

    const getTimestamp = (block) => {
        const innerBlockSelector = block.querySelectorAll('.roam-block');
        const blockText = innerBlockSelector.length ? innerBlockSelector[0].textContent : '';
        const matches = blockText.match(/^((?:\d+:)?\d+:\d\d)\D/); // start w/ m:ss or h:mm:ss
      	//console.log(matches)
        if (!matches || matches.length < 2) return null;
        const timeParts = matches[1].split(':').map(part => parseInt(part));
        if (timeParts.length == 3) return timeParts[0]*3600 + timeParts[1]*60 + timeParts[2];
        else if (timeParts.length == 2) return timeParts[0]*60 + timeParts[1];
        else return null;
    };
  
    const loadYtApi = () => {
        const tag = document.createElement('script');
        tag.src = 'https://www.youtube.com/iframe_api';
        const firstScriptTag = document.getElementsByTagName('script')[0];
        firstScriptTag.parentNode.insertBefore(tag, firstScriptTag); 
        window.onYouTubeIframeAPIReady = () => { ytApiReady = true; };
    };
  
  	const extractVideoID = (url) => {
      var regExp = /^(https?:\/\/)?((www\.)?(youtube(-nocookie)?|youtube.googleapis)\.com.*(v\/|v=|vi=|vi\/|e\/|embed\/\/?|user\/.*\/u\/\d+\/)|youtu\.be\/)([_0-9a-z-]+)/i;
      var match = url.match(regExp);
      if ( match && match[7].length == 11 ){
          return match[7];
      }else{
          return null; 
      }
    };
  
    setInterval(activateYtVideos, 1000);
})();```
- {{roam/js}}
    - Add day of the week to Daily Notes title
    - ```javascript
// Roam42 is a prerequisite for this code, as it uses Roam42 libraries
// Install & Config:
//   Add the code from this gist to a roam/js block in your roam graph and enable it
//   If you prefer foreign day names, modify the english in the Javascript below
//   CSS can be customized using [roam-title-day-banner](roam-title-day-banner.md) CSS selector. Example:
//   [roam-title-day-banner](roam-title-day-banner.md) {
//      color:silver;
//   }
//  to exclude sidebars, change 'var includeSidebars = true;' in the code o 
//  var includeSidebars = false;

;(()=>{
  
  if( typeof window.roamhacker_daytitle != 'undefined') return;

  window.roamhacker_daytitle = ()=> {
    var includeSidebars = true;
    var querystring =  includeSidebars ? '.rm-title-display, .sidebar-content .level2 a' : '.rm-title-display';
    const addDateToRoamTitleBanners = ()=> {
      setTimeout(()=>{
        document.querySelectorAll(querystring).forEach(title=>{
        try {
          if(title.nextElementSibling.classList.contains('roam-title-day-banner')) { 
            return;            
          }
        } catch(e) {}
        let pageDate = chrono.parseDate( title.innerText );
        if(	pageDate!=null ) {            
	      var weekdays = new Array( "Sunday: Plan your agenda for next week.", "Monday: Life is beautiful, fight for your dream & family.", "Tuesday", "Wednesday", 
                                   	"Thursday", "Friday", "Saturday: Enjoy your family time and your interesting thing." );
          var day = pageDate.getDay();
          var div = document.createElement('DIV');
              div.className = 'roam-title-day-banner';
              div.innerText = weekdays[day];
              div.style.fontSize="13pt";
          	  div.style.top = -(Number(getComputedStyle(title).marginBottom.replace('px','')) + 6) + 'px';
              div.style.position="relative";
              div.style.fontStyle="oblique";
          title.insertAdjacentElement('afterend', div);
         }
        });
      },300)
    };

    setTimeout(()=>{
      addDateToRoamTitleBanners();
      const observerHeadings = new MutationObserver(addDateToRoamTitleBanners);
      observerHeadings.observe(document.querySelector('.roam-body'), {
        childList: true,
        subtree: true
      });
    },10000);
  }
  
  window.roamhacker_daytitle();
})();```
- {{roam/js}}
    - Cato's Block Colors
    - ```javascript


;(()=>{
  
  if( typeof window.catominor_tags != 'undefined') return;

  window.catominor_tags = {};

  const scanTags = () => {
    document.querySelectorAll('[data-tag]').forEach( (element)=>{
      console.log("start");
      let divBlockTagAttributeArray;
      let divBlock = element.parentElement.parentElement;
      const tagAttribute = " " + element.getAttribute('data-tag') + " ";
      
      
      

      
      let divBlockTagAttribute = divBlock.getAttribute("data-tags");
      
      if (divBlockTagAttribute ==  null){
        divBlockTagAttributeArray = [];
      } else {
        
        divBlockTagAttributeArray = divBlockTagAttribute.split(","); 
      }
    
      let index;
	 
      if(element) {
        console.log(tagAttribute);
        let index = divBlockTagAttributeArray.indexOf(tagAttribute);
        if (index == -1) {
       			divBlockTagAttributeArray.push(tagAttribute);
   		 }
     
      } else {
         let index = divBlockTagAttributeArray.indexOf(tagAttribute);
		 if (index > -1) {
       			divBlockTagAttributeArray.splice(index, 1);
   		 }
         
        
        
      }
      console.log(divBlockTagAttributeArray);
      divBlock.dataset.tags = divBlockTagAttributeArray.join();
      divBlock.parentNode.parentNode.parentNode.dataset.tagsUp = " " + divBlockTagAttributeArray.join() + " ";
     // divBlock.parentNode.parentNode.parentNode.childNodes[0].dataset.tagsDown = divBlockTagAttributeArray.join();


      console.log(divBlock.dataset.tags);
  
    })
  }

  scanTags()
  var observerTags = new MutationObserver(scanTags);
  observerTags.observe(document.querySelector('[app](app.md)'), {
    childList: true,
    subtree: true
  })

})();```
- {{roam/js}}
    - Articles clipping
    - ```javascript
var installScript = name => {var existing = document.getElementById(name);
                             if (existing) {return;}
                             var extension = document.createElement("script");
                             extension.type = "text/javascript";
                             extension.src = `https://roamjs.com/${name}.js`;
                             extension.async = true;extension.id = name;
                             document.getElementsByTagName("head")[0].appendChild(extension);};
installScript("article");

```
- {{roam/js}}
    - Dragons
    - ```javascript
// ==UserScript==
// @name         Here be Dragons!
// @version      0.1
// @include      https://roamresearch.com/*
// @author       Azlen
// @grant        none
// ==/UserScript==

/*
 * arrive.js
 * v2.4.1
 * https://github.com/uzairfarooq/arrive
 * MIT licensed
 *
 * Copyright (c) 2014-2017 Uzair Farooq
 */

var Arrive=function(e,t,n){"use strict";function r(e,t,n){l.addMethod(t,n,e.unbindEvent),l.addMethod(t,n,e.unbindEventWithSelectorOrCallback),l.addMethod(t,n,e.unbindEventWithSelectorAndCallback)}function i(e){e.arrive=f.bindEvent,r(f,e,"unbindArrive"),e.leave=d.bindEvent,r(d,e,"unbindLeave")}if(e.MutationObserver&&"undefined"!=typeof HTMLElement){var o=0,l=function(){var t=HTMLElement.prototype.matches||HTMLElement.prototype.webkitMatchesSelector||HTMLElement.prototype.mozMatchesSelector||HTMLElement.prototype.msMatchesSelector;return{matchesSelector:function(e,n){return e instanceof HTMLElement&&t.call(e,n)},addMethod:function(e,t,r){var i=e[t];e[t]=function(){return r.length==arguments.length?r.apply(this,arguments):"function"==typeof i?i.apply(this,arguments):n}},callCallbacks:function(e,t){t&&t.options.onceOnly&&1==t.firedElems.length&&(e=[e[0]]);for(var n,r=0;n=e[r];r++)n&&n.callback&&n.callback.call(n.elem,n.elem);t&&t.options.onceOnly&&1==t.firedElems.length&&t.me.unbindEventWithSelectorAndCallback.call(t.target,t.selector,t.callback)},checkChildNodesRecursively:function(e,t,n,r){for(var i,o=0;i=e[o];o++)n(i,t,r)&&r.push({callback:t.callback,elem:i}),i.childNodes.length>0&&l.checkChildNodesRecursively(i.childNodes,t,n,r)},mergeArrays:function(e,t){var n,r={};for(n in e)e.hasOwnProperty(n)&&(r[n]=e[n]);for(n in t)t.hasOwnProperty(n)&&(r[n]=t[n]);return r},toElementsArray:function(t){return n===t||"number"==typeof t.length&&t!==e||(t=[t]),t}}}(),c=function(){var e=function(){this._eventsBucket=[],this._beforeAdding=null,this._beforeRemoving=null};return e.prototype.addEvent=function(e,t,n,r){var i={target:e,selector:t,options:n,callback:r,firedElems:[]};return this._beforeAdding&&this._beforeAdding(i),this._eventsBucket.push(i),i},e.prototype.removeEvent=function(e){for(var t,n=this._eventsBucket.length-1;t=this._eventsBucket[n];n--)if(e(t)){this._beforeRemoving&&this._beforeRemoving(t);var r=this._eventsBucket.splice(n,1);r&&r.length&&(r[0].callback=null)}},e.prototype.beforeAdding=function(e){this._beforeAdding=e},e.prototype.beforeRemoving=function(e){this._beforeRemoving=e},e}(),a=function(t,r){var i=new c,o=this,a={fireOnAttributesModification:!1};return i.beforeAdding(function(n){var i,l=n.target;(l===e.document||l===e)&&(l=document.getElementsByTagName("html")[0]),i=new MutationObserver(function(e){r.call(this,e,n)});var c=t(n.options);i.observe(l,c),n.observer=i,n.me=o}),i.beforeRemoving(function(e){e.observer.disconnect()}),this.bindEvent=function(e,t,n){t=l.mergeArrays(a,t);for(var r=l.toElementsArray(this),o=0;o<r.length;o++)i.addEvent(r[o],e,t,n)},this.unbindEvent=function(){var e=l.toElementsArray(this);i.removeEvent(function(t){for(var r=0;r<e.length;r++)if(this===n||t.target===e[r])return!0;return!1})},this.unbindEventWithSelectorOrCallback=function(e){var t,r=l.toElementsArray(this),o=e;t="function"==typeof e?function(e){for(var t=0;t<r.length;t++)if((this===n||e.target===r[t])&&e.callback===o)return!0;return!1}:function(t){for(var i=0;i<r.length;i++)if((this===n||t.target===r[i])&&t.selector===e)return!0;return!1},i.removeEvent(t)},this.unbindEventWithSelectorAndCallback=function(e,t){var r=l.toElementsArray(this);i.removeEvent(function(i){for(var o=0;o<r.length;o++)if((this===n||i.target===r[o])&&i.selector===e&&i.callback===t)return!0;return!1})},this},s=function(){function e(e){var t={attributes:!1,childList:!0,subtree:!0};return e.fireOnAttributesModification&&(t.attributes=!0),t}function t(e,t){e.forEach(function(e){var n=e.addedNodes,i=e.target,o=[];null!==n&&n.length>0?l.checkChildNodesRecursively(n,t,r,o):"attributes"===e.type&&r(i,t,o)&&o.push({callback:t.callback,elem:i}),l.callCallbacks(o,t)})}function r(e,t){return l.matchesSelector(e,t.selector)&&(e._id===n&&(e._id=o++),-1==t.firedElems.indexOf(e._id))?(t.firedElems.push(e._id),!0):!1}var i={fireOnAttributesModification:!1,onceOnly:!1,existing:!1};f=new a(e,t);var c=f.bindEvent;return f.bindEvent=function(e,t,r){n===r?(r=t,t=i):t=l.mergeArrays(i,t);var o=l.toElementsArray(this);if(t.existing){for(var a=[],s=0;s<o.length;s++)for(var u=o[s].querySelectorAll(e),f=0;f<u.length;f++)a.push({callback:r,elem:u[f]});if(t.onceOnly&&a.length)return r.call(a[0].elem,a[0].elem);setTimeout(l.callCallbacks,1,a)}c.call(this,e,t,r)},f},u=function(){function e(){var e={childList:!0,subtree:!0};return e}function t(e,t){e.forEach(function(e){var n=e.removedNodes,i=[];null!==n&&n.length>0&&l.checkChildNodesRecursively(n,t,r,i),l.callCallbacks(i,t)})}function r(e,t){return l.matchesSelector(e,t.selector)}var i={};d=new a(e,t);var o=d.bindEvent;return d.bindEvent=function(e,t,r){n===r?(r=t,t=i):t=l.mergeArrays(i,t),o.call(this,e,t,r)},d},f=new s,d=new u;t&&i(t.fn),i(HTMLElement.prototype),i(NodeList.prototype),i(HTMLCollection.prototype),i(HTMLDocument.prototype),i(Window.prototype);var h={};return r(f,h,"unbindAllArrive"),r(d,h,"unbindAllLeave"),h}}(window,"undefined"==typeof jQuery?null:jQuery,void 0);

let pages = [];

let dragging;
let startBBox;
let startMouse;
let startTransform;

function getMousePos(e) {
    return {
        x: e.pageX - document.querySelector('.roam-main').scrollLeft,
        y: e.pageY
    }
}

let style = document.createElement('style');
style.textContent = `
body > svg {
    position: absolute;
    top: 0; left: 0; width: 100vw; height: 100vh;
    pointer-events: none;
}
body > svg rect , body > svg path{
    fill: rgba(0,255,125,0.31);
}
rect.offscreen, path.offscreen {
    opacity: 0.2;
}
body > svg path:hover {
    fill: rgba(0,200,125,0.5);
}
svg.xanadu *.bl_link {
    fill: rgba(0,255,125,0.31);
}
svg.xanadu *.bl_ref {
    fill: rgba(255,0,125,0.31);
}
.pg_link {
    background-color: rgba(0,125,255,0.41);
    fill: rgba(0,125,255,0.41);
}
`
document.body.appendChild(style);

let svg = document.createElementNS('http://www.w3.org/2000/svg', 'svg');
svg.classList.add('xanadu');
document.body.appendChild(svg);

function findMatchingBlocks(text) {
    text = text.replace(/(__|\*\*)/g, '');
    var matchIterator = document.evaluate(`//div[contains(@class, "rm-block-text") and contains(span, "${ text }")]`, document, null, XPathResult.UNORDERED_NODE_ITERATOR_TYPE, null);
    var matchingElements = [];

    var nextElement;
    while((nextElement = matchIterator.iterateNext()) != null) {
        matchingElements.push(nextElement);
    }

    return matchingElements;
}

function findPages(title) {
    //title = title.replace(/(__|\*\*)/g, '');
    var matchIterator = document.evaluate(`//h1[contains(@class, "level2") and contains(a, "${ title }")]/parent::div`, document, null, XPathResult.UNORDERED_NODE_ITERATOR_TYPE, null);
    var matchingElements = [];

    var nextElement;
    while((nextElement = matchIterator.iterateNext()) != null) {
        matchingElements.push(nextElement);
    }

    return matchingElements;
}

function isOffscreen(rect) {
    if(rect.x + rect.width < 0 || rect.y + rect.height < 0 || rect.x > window.innerWidth || rect.y > window.innerHeight) {
        return true;
    } else {
        return false;
    }
}

function createRectangle(boundingRect, type) {
    let rect = document.createElementNS('http://www.w3.org/2000/svg', 'rect');

    rect.setAttribute('x', boundingRect.x);
    rect.setAttribute('y', boundingRect.y);
    rect.setAttribute('width', boundingRect.width);
    rect.setAttribute('height', boundingRect.height);
    rect.classList.add(type);

    if(isOffscreen(boundingRect)) {
       rect.classList.add('offscreen');
    }

    svg.appendChild(rect);
}

function createConnection(rectA, rectB, type) {
    let A, B;

    if (rectA.x+rectA.width < rectB.x) {
        A = rectA; B = rectB;
    } else if (rectB.x+rectB.width < rectA.x) {
        B = rectA; A = rectB;
    }

    if (A != undefined) {
        let path = document.createElementNS('http://www.w3.org/2000/svg', 'path');

        //path.setAttribute('d', `M ${A.x + A.width} ${A.y} L ${B.x} ${B.y} L ${B.x} ${B.y + B.height} L ${A.x + A.width} ${A.y + A.height} Z`);

        let pathB = `L ${B.x + B.width} ${B.y} L ${B.x + B.width} ${B.y + B.height}`;

        path.setAttribute('d', `M ${A.x} ${A.y} L ${A.x + A.width} ${A.y} L ${B.x} ${B.y} ${ pathB } L ${B.x} ${B.y + B.height} L ${A.x + A.width} ${A.y + A.height} L ${A.x} ${A.y + A.height} Z`);
        path.classList.add(type);

        if(isOffscreen(A)) {
            path.classList.add('offscreen');
        }

        svg.appendChild(path);

        return true;
    }
}

function searchAndConnect(elementA, searchText, type) {
    let blocks;
    if(type !== 'pg_link') {
        blocks = findMatchingBlocks(searchText);
    } else {
        blocks = findPages(searchText);
    }
    if(blocks.indexOf(elementA) != -1) {
        blocks = blocks.splice(blocks.indexOf(elementA), 1);
    }

    if(blocks.length > 0) {
        var rectA = elementA.getBoundingClientRect();

        blocks.forEach(function(elementB) {
            var rectB = elementB.getBoundingClientRect();

            createConnection(rectA, rectB, type);
        })
    }
}

function renderConnections() {
    svg.innerHTML = '';

    // [text](((block id)))

    let bl_links = [].slice.call(document.querySelectorAll('a[title^="block:"]'));

    bl_links.forEach(el => searchAndConnect(el, el.getAttribute('title').slice(7), 'bl_link') );

    // ((block id))

    let bl_refs = [].slice.call(document.querySelectorAll('.rm-block-ref'));

    bl_refs.forEach(el => searchAndConnect(el, el.textContent, 'bl_ref') );

    // [page name](page name.md)

    let pg_links = [].slice.call(document.querySelectorAll('span[data-link-title]'));

    pg_links.forEach(el => {
        //searchAndConnect(el, el.dataset.linkTitle, 'pg_link')
        if(findPages(el.dataset.linkTitle).length > 0) {
            //createRectangle(el.getBoundingClientRect(), 'pg_link');
            el.classList.add('pg_link');
        } else {
            el.classList.remove('pg_link');
        }
    });
}


document.arrive("[roam-right-sidebar-content](roam-right-sidebar-content.md)", function() {
    let selector = 'div[style*="margin-left: 16px; margin-right: 16px;"]';

    this.arrive(selector, {existing: true}, function() {
        let page = this;
        let header = this.querySelector('div.flex-h-box');

        header.addEventListener('mousedown', function(e) {
            dragging = page;
            let mpos = getMousePos(e);
            let rect = page.getBoundingClientRect();

            /*startOffset = {
                x: rect.x - mpos.x,
                y: rect.y - mpos.y
            };*/

            let match = dragging.style.getPropertyValue('transform').match(/([-0-9\.]+)px, ([-0-9]+)px/);
            if(match != null) {
                let [tx, ty] = match.slice(1).map(Number);
                startTransform = { x: tx, y: ty };
            } else {
                startTransform = { x: 0, y: 0 };
            }


            startBBox = {x: rect.x - document.querySelector('.roam-body-main').getBoundingClientRect().left, y: rect.y};
            startMouse = {x: mpos.x, y: mpos.y};

        });

        renderConnections();
    })

    this.leave(selector, function() {
        pages = pages.splice(pages.indexOf(this), 1);
    })
});

window.addEventListener('mousemove', function(e) {
    if(dragging != null) {
        let currentMouse = getMousePos(e);
        //mpos.x += startOffset.x;
        //mpos.y += startOffset.y;

        let dx = currentMouse.x - startMouse.x;
        let dy = currentMouse.y - startMouse.y;

        let x = startBBox.x + currentMouse.x - startMouse.x;
        let y = startBBox.y + currentMouse.y - startMouse.y;

        dragging.style.setProperty('position', 'absolute', 'important');
        /*dragging.style.setProperty('left', startBBox.x + 'px');
        dragging.style.setProperty('top', startBBox.y + 'px');*/
        dragging.style.setProperty('transform', `translate3d(${ startTransform.x + dx }px, ${ startTransform.y + dy }px, 0px)`);

        renderConnections();

        // prevent text selection
        e.preventDefault();
    }
})

window.addEventListener('scroll', function(e) {
    renderConnections();
}, true)

window.addEventListener('mouseup', function() {
    dragging = null;
})```
- {{roam/js}}
    - Roam Template
    - ```javascript
/*
 * Roam template PoC by @ViktorTabori
 * 0.1alpha
 *
 * How to install it:
 *  - go to `roam/js` page`
 *  - make a new node: {{[roam/js](roam/js.md)}}

	// resolve templates
	var tab = 0;
	var text = elem.value;
	elem.value.replace(/:([^:]+):/g, async function(_, v, position){
		// lookup template
		var tmp = getTemplate(v);

		// if no result
		if (!tmp) {
			return _;
		}

		console.log('template:',v,tmp);

		// remove first 
		tmp = tmp.replace(/^\s*- /,'').split("\n");

		// process first line
		var line = tmp.shift();
		text = text.replace(_, line);

		// handle heading
		heading = (line.match(/^(#*) ?/)||['',''])[1].length;
		if (heading > 0) {
			console.log('heading:', heading, line.match(/^(#*) ?/));
			KeyboardLib.changeHeading(heading);
		}
		line = line.replace(/^#* ?/, '');
		if (line == '') line = ' ';

		// set value
		nativeSetter.call(e.target, line);
		e.target.selectionStart = position;
		e.target.selectionEnd = position;
		e.target.dispatchEvent(new Event('input', {bubbles: true, cancelable: true }));

		// process lines
		while (tmp.length) {
			// get new line
			elem.focus();
			elem.selectionStart = elem.value.length;
			elem.selectionEnd = elem.value.length;

			// get new line and row
			await KeyboardLib.pressEnter();
			elem = KeyboardLib.getActiveEditElement();
			line = tmp.shift();

			// handle tabs
			console.log('line:', line)
			tab = line.match(/^\s*/)[0].length/2-tab; // tab difference
			console.log('tab:',tab);
			if (tab > 0) {
				for (var i=0; i<tab; i++) {
					await KeyboardLib.pressTab()
				}
			} else if (tab < 0) {
				for (var i=0; i<-tab; i++) {
					await KeyboardLib.pressShiftTab();
				}
			}
			tab = line.match(/^\s*/)[0].length/2; // save current tab length

			// handle heading
			heading = (line.match(/^\s*- (#*) ?/)||['',''])[1].length;
			if (heading > 0) {
				console.log('heading:', heading, line.match(/^\s*- (#*) ?/));
				KeyboardLib.changeHeading(heading);
			}

			// set element value
			elem = KeyboardLib.getActiveEditElement();
			line = line.replace(/^\s*
#* ?/,'');
			if (line == '') line = ' ';
			nativeSetter.call(elem, line);
			elem.selectionStart = elem.value.length;
			elem.selectionEnd = elem.value.length;
			console.log('dispatch event');
			elem.dispatchEvent(new Event('input', {bubbles: true, cancelable: true }));

			await KeyboardLib.delay(150);
		}
	});
}

window.getTemplate = function(name) {
	/* resolve node function by @ViktorTabori
	 * id: node id
	 * level: depth needed for indention
	 * trail: list of ids to avoid loops
	 * resolve: resolve block references and embeds starting with an exclamation mark: !{{embed:((blockid))}} and !((blockid))
	 * skipFirstPrefix: no prefix, needed for block embeds and references
	 * stop: doesn't resolve children, needed for block reference resolution
	 */
	function resolveNode(id, level, trail, resolve, skipFirstPrefix, stop){
		var level = level || 0; // for indentation
		var trail = Object.assign({}, trail); // to avoid loops
		var prefix = skipFirstPrefix ? '' : ' '.repeat(2*Math.max(level-1,0)) + '- '; // indention starting from level 2
		var newLine = skipFirstPrefix && stop ? '' : "\n"; // no new line when we resolve simple block references
		var ret = '';

		// avoid loops: skip if trail already contains id
		if (trail[id]) return;
		trail[id] = true;

		// get node info
		var node = window.roamAlphaAPI.pull("[*]",id);

		// node order
		var order = node[':block/order'] || 0;

		// add heading to prefix
		if (node[':block/heading'] && node[':block/heading'] > 0) {
			prefix += '#'.repeat(node[':block/heading'])+' ';
		}

		// current node string
		if (typeof node[':block/string'] != 'undefined') {
			// resolve block EMBEDs
			var regexEmbed = resolve ? /!?{{\[*embed\]*\s*:\s*\(\(([^\)]*)\)\)\s*}}/ig : /!{{\[*embed\]*\s*:\s*\(\(([^\)]*)\)\)\s*}}/ig;
			node[':block/string'] = node[':block/string'].replace(regexEmbed, function(_, v){ 
				var uid = v.trim();
				var id = window.roamAlphaAPI.q("[:find ?e :in $ ?a :where [?e :block/uid ?a]]", uid);
				if (id.length == 0) {
					return _;
				}
				var block = resolveNode(id[0][0], level, trail, true, true); // resolve node, no prefix
				if (typeof block != 'undefined') { // for loops we got back undefined
					return block;
				} else {
					return 'LOOP:'+_;
				}
			});

			// resolve block REFERENCEs
			var regexReference = resolve ? /!?\(\(([^\)]*)\)\)/ig : /!\(\(([^\)]*)\)\)/ig;
			node[':block/string'] = node[':block/string'].replace(regexReference, function(_, v){ 
				var uid = v.trim();
				var id = window.roamAlphaAPI.q("[:find ?e :in $ ?a :where [?e :block/uid ?a]]", uid);
				if (id.length == 0) {
					return _;
				}
				var block = resolveNode(id[0][0], level, trail, true, true, true); // resolve node, no prefix, don't resolve children
				if (typeof block != 'undefined') { // for loops we got back undefined
					return block;
				} else {
					return 'LOOP:'+_;
				}
			});


			// add block text to return
			ret += prefix + node[':block/string'] + newLine;
		}

		// handle children
		if (node[':block/children'] && !stop) {
			var children = [];
			var tmp;

			// get children data
			for (var i in node[':block/children']) {
				tmp = resolveNode(node[':block/children'][i][':db/id'], level+1, trail);
				if (typeof tmp != 'undefined') {
					children.push(tmp);
				}
			}

			// sort children in order
			children.sort(function(a,b){return a.order-b.order})

			// concat children text
			ret += children.map(function(i){return i.txt}).join('');
		}

		// return based on how deep we are in the graph
		if (level == 0 || skipFirstPrefix) {
			return ret;
		} else {
			return {txt: ret, order: order};
		}
	}

	// check API endpoint
	if (!window.roamAlphaAPI || !window.roamAlphaAPI.q || !window.roamAlphaAPI.pull) return; // no api endpoint

	// search node ID
	var nodeId; // page we look for
	var search = ['template','[template](template.md)']; // search for template in template/name, [template](template.md)/name, ...
	for (var i in search) {
		nodeId = window.roamAlphaAPI.q("[:find ?e :in $ ?a :where [?e :node/title ?a]]", search[i]+'/'+name);
		if (nodeId.length) {
			nodeId = nodeId[0][0];
			break;
		}
	}

	if (!nodeId || nodeId.length == 0) return; // no such template

	return resolveNode(nodeId);
}

window.KeyboardLib = {
	// thank you @VladyslavSitalo for the awesome Roam Toolkit, and the basis for this code
    LEFT_ARROW: 37,
    UP_ARROW: 38,
    RIGHT_ARROW: 39,
    DOWN_ARROW: 40,
    BASE_DELAY: 20,

    delay(millis) {
    	return new Promise(resolve => setTimeout(resolve, millis))
	},
	getKeyboardEvent: function(type, code, opts) {
	    return new KeyboardEvent(type, {
	        bubbles: true,
	        cancelable: true,
	        keyCode: code,
	        ...opts,
	    })
	},
	getActiveEditElement: function() {
	    // stolen from Surfingkeys. Needs work.
	    var element = document.activeElement
	    // on some pages like chrome://history/, input is in shadowRoot of several other recursive shadowRoots.
	    while (element.shadowRoot) {
	        if (element.shadowRoot.activeElement) {
	            element = element.shadowRoot.activeElement
	        } else {
	            var subElement = element.shadowRoot.querySelector('input, textarea, select')
	            if (subElement) {
	                element = subElement
	            }
	            break
	        }
	    }
	    return element
	},
	async simulateSequence(events, delayOverride) {
    	;events.forEach(function(e){
			return KeyboardLib.getActiveEditElement().dispatchEvent(KeyboardLib.getKeyboardEvent(e.name, e.code, e.opt));
		});
        return this.delay(delayOverride || this.BASE_DELAY);
    },
    async simulateKey(code, delayOverride, opts) {
        return this.simulateSequence([{name:'keydown', code:code, opt:opts}, {name:'keyup', code:code, opt:opts}], delayOverride);
    },
    async changeHeading(heading, delayOverride) {
        return this.simulateSequence(
        	[
        		{name:'keydown', code:18, opt:{altKey:true}},
				{name:'keydown', code:91, opt:{metaKey:true}},
				{name:'keydown', code:48+heading, opt:{altKey:true, metaKey:true}},
				{name:'keyup', code:91, opt:{altKey:true}},
				{name:'keyup', code:18, opt:{}}
			],
        	delayOverride);
    },
    async pressEnter(delayOverride) {
        return this.simulateKey(13, delayOverride)
    },
    async pressEsc(delayOverride) {
        return this.simulateKey(27, delayOverride)
    },
    async pressBackspace(delayOverride) {
        return this.simulateKey(8, delayOverride)
    },
    async pressTab(delayOverride) {
        return this.simulateKey(9, delayOverride)
    },
    async pressShiftTab(delayOverride) {
        return this.simulateKey(9, delayOverride, {shiftKey: true})
    },
    async pressCtrlV(delayOverride) {
        return this.simulateKey(118, delayOverride, {metaKey: true})
    },
	getInputEvent() {
	    return new Event('input', {
	        bubbles: true,
	        cancelable: true,
	    })
	},
}```
- 
- 
- 
- 
- 
- 
- 

#@Jessie 以下plug-in 来自[推特总结](https://twitter.com/wirtzdan/status/1334976252684476417)
- 第六个js模块：显示外部链接来源的icon
    - 源文件：[Add favicons](https://gist.github.com/ottsch/51a3640910a82d36fcd1fc70ad4b109b)
    - > 在插入的外部链接前面添加一个图标，显示来源。![图像](https://pbs.twimg.com/media/EobJyxNXUAk1evj?format=jpg&name=small)
        - ```javascript
new MutationObserver(() => {
  let filtered = Array.prototype.filter.call(
    document.querySelectorAll(".roam-body a"),
    (a) => {
      return a.hostname && !a.hostname.includes("roamresearch.com");
    }
  );
  Array.prototype.forEach.call(filtered, (a) => {
    if (a.text == "*") {
      a.style.background = `url(https://www.google.com/s2/favicons?sz=16&domain=${a.hostname}) right center no-repeat`;
      a.style.paddingRight = "18px";
    } else {
      a.style.background = `url(https://www.google.com/s2/favicons?sz=16&domain=${a.hostname}) left center no-repeat`;
      a.style.paddingLeft = "20px";
    }
  });
}).observe(document.body, {
  attributes: true,
  childList: true,
  subtree: true,
});```
- 第七个js模块：在所有每日笔记页面的顶部显示带有**加密货币价格**的表格
    - ![图像](https://pbs.twimg.com/media/EobJzEbXUAIBgfg?format=jpg&name=small)
        - ```javascript
window.roamFinance = {}
window.roamFinance.crypto = {
  tickers: [
    'BTC', 
    'ETH', 
    'LTC',
    'BAT',
    'CEL',
    'NEO',
  ],
  currency: 'eur'
}

const addFinanceScript = (name) => {
  var old = document.getElementById("roam-fin-" + name);
  if (old) {
    old.remove();
  }

  var s = document.createElement("script");
  s.src = `https://roamjs-finance.andreynocap.com/${name}.js`;
  s.id = name;
  s.async = true;
  s.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(s);
};
addFinanceScript("crypto-price-table");```
- 第八个js模块：随机页面跳转
    - ![图像](https://pbs.twimg.com/media/EobJzXrW8AAHnvV?format=jpg&name=small)
        - ```javascript
function randomPagePlugin() {
  function isMac() {
    return window.navigator.platform.startsWith('Mac');
  }
  
  // settings
  const title = 'Go to random page';
  const icon = 'bp3-button bp3-minimal bp3-icon-random pointer bp3-small';
  const shortcut = isMac() ? {ctrlKey: true, key: "r"} : {altKey: true, key: "r"};

  function addButton() {
    // cleanup old versions of the button
    var randomButton = document.querySelector('[random-button](random-button.md)');
    if (randomButton != null) {
      randomButton.parentNode.removeChild(randomButton);
    }
    // create button
    var template = document.createElement('template');
    template.innerHTML = '<span id="random-button" title="' + title + '" class="' + icon + '"></span>';
    template.content.firstChild.onclick = goToRandomPage;
    randomButton = template.content.firstChild;

    // insert button into topbar
    const topbar = document.querySelector('.roam-topbar .flex-h-box');
    const dots = document.querySelector('.roam-topbar div[style="margin-left: 4px;"]');
    topbar.insertBefore(randomButton, dots);
  }

  function addKeyboardShortcut() {
    document.onkeyup = function(e) {
      if (shortcut.ctrlKey && !e.ctrlKey) return;
      if (shortcut.shiftKey && !e.shiftKey) return;
      if (shortcut.altKey && !e.altKey) return;
      if (shortcut.key === e.key) goToRandomPage(e);
    }
  }

  function goToRandomPage(e) {
    if (isAllPages()) {
      clickRandomPageLink(e.shiftKey);
    } else if (e.shiftKey) {
      goToAllPagesThen(function() {
        clickRandomPageLink(e.shiftKey);
        history.back();
      });
    } else {
      const allPages = roamAlphaAPI.q('[ :find (pull ?e [:block/uid]) :where [?e :node/title]]');
      const page = getRandomElement(allPages);
      const uid = page[0].uid;
      const db = location.hash.split('/')[2];
      location.assign('/#/app/' + db + '/page/' + uid);
    }
  }

  function isAllPages() {
    return location.hash.endsWith('/search');
  }

  function goToAllPagesThen(f) {
    document.querySelector('.bp3-icon-list').parentNode.parentNode.click();
    setTimeout(f, 0);
  }

  function clickRandomPageLink(shift) {
    // https://forum.roamresearch.com/t/what-would-be-your-top-3-tips-for-beginners/255/9
    var allPages = document.querySelectorAll('div.rm-pages-title-col a');
    var pageLink = getRandomElement(allPages);
    getEventHandlers(pageLink).onClick({ shiftKey: shift });
  }

  function getRandomElement(array) {
    return array[Math.floor(Math.random() * array.length)];
  }

  function getEventHandlers(element) {
    for (var prop in element) {
      if (prop.includes('reactEventHandlers')) {
        return element[prop];
      }
    }
  }

  addButton();
  addKeyboardShortcut();
}
randomPagePlugin();```
- 第九个js模块：前进和后退导航箭头
    - ![图像](https://pbs.twimg.com/media/EobJzqWXMAItefD?format=jpg&name=small)
        - ```javascript
Don't show navigation controls on mobile
    if(/Android|iPhone/i.test(navigator.userAgent)){
      return;
    }
  
    // Only show navigation controls when using Roam in app mode
    if ((window.navigator.standalone == true) || (window.matchMedia('(display-mode: standalone)').matches)) {
      const navigation_controls = document.createElement("div");    
      navigation_controls.id = 'roam-navigation-controls';     
      navigation_controls.style.display = 'block';
      navigation_controls.setAttribute("style", "display: block; left: 2px; width: 35px; max-width: 35px!important; top: 40px; position: relative; z-index: 100000;");

      const navigation_controls_back = document.createElement("i");    
      navigation_controls_back.id = 'roam-navigation-controls_back';     
      navigation_controls_back.style.display = 'block'; 
      navigation_controls_back.setAttribute('style', "margin-bottom:2px;border: solid black;border-width: 0 3px 3px 0;display: inline-block;position: relative;padding: 5px;transform: rotate(135deg);-webkit-transform: rotate(135deg);cursor: pointer;")
      navigation_controls_back.onclick = () => {
        window.history.back();
      }
      navigation_controls_back.title = 'Go back';

      const navigation_controls_forward = document.createElement("i");    
      navigation_controls_forward.id = 'roam-navigation-controls_forward';     
      navigation_controls_forward.style.display = 'block'; 
      navigation_controls_forward.setAttribute('style', "margin-bottom:2px;border: solid black;border-width: 0 3px 3px 0;display: inline-block;position: relative;padding: 5px;transform: rotate(-45deg);-webkit-transform: rotate(-45deg);cursor: pointer;")
      navigation_controls_forward.onclick = () => {
        window.history.forward();
      }

      navigation_controls_forward.title = 'Go forward';

      const toolbar_container = document.querySelector('.roam-topbar');
      const toolbar_container_flex_box = toolbar_container.querySelector('.flex-h-box');

      toolbar_container_flex_box.prepend(navigation_controls);

      document.getElementById("roam-navigation-controls").appendChild(navigation_controls_back);
      document.getElementById("roam-navigation-controls").appendChild(navigation_controls_forward);
    }
})();```
- 第十个js模块：查看最近访问
    - ![图像](https://pbs.twimg.com/media/EobJ0AeXUAcxXJT?format=jpg&name=small)
        - ```javascript
initiliaze();

function initiliaze() { /*removes any residual instances of breadcrumb feature*/
    window.removeEventListener("hashchange", timedFunction);
    document.removeEventListener("keydown", hotKeyEvent);
    var elem = document.querySelector('[recentLinks](recentLinks.md)');
    var btn = document.querySelector('[closeCrumbs](closeCrumbs.md)');
  	if(elem != null) { elem.parentNode.removeChild(elem); }
    if(btn != null) { btn.parentNode.removeChild(btn); }
}

//[recentLinks](recentLinks.md) div to hold breadcrumbs
var breadCrumbDiv = document.createElement('div'); // [recentLinks](recentLinks.md) div to hold breadcrumbs
breadCrumbDiv.id = 'recentLinks';
breadCrumbDiv.style.position = 'absolute';
breadCrumbDiv.style.left = '228px';
breadCrumbDiv.style.height = '45px';
breadCrumbDiv.style.padding = '10px';
var topBarDiv = document.getElementsByClassName("roam-topbar")[0];
topBarDiv.appendChild(breadCrumbDiv); //put it in the topbar div for z-index purposes
window.addEventListener("hashchange", timedFunction);

//div + button to stop/start listener, & show/hide breadcrumbs
var toggleDiv = document.createElement('div');
toggleDiv.id = 'closeCrumbs';
toggleDiv.style.position = 'absolute';
toggleDiv.style.left = '212px';
toggleDiv.style.height = '45px';
toggleDiv.style.padding = '10px';
topBarDiv.appendChild(toggleDiv);

var toggleButton = document.createElement("button");
toggleButton.id = 'buttonLayer';
toggleButton.style.border = '0';
toggleButton.style.color = 'green';
toggleButton.style.fontSize = '24px';
toggleButton.innerHTML = "‣";
toggleDiv.appendChild(toggleButton);
toggleButton.onclick = turnOnOff;

var urlArray = [];
var linksArray = [];
var onOff = true;
var n = 0;
//this function flips the toggle switch, then shows/hides the breadcrumbs and adds/removes listener
function turnOnOff() {
    onOff = !onOff;
    if (!onOff) {
        breadCrumbDiv.style.display = 'none';
        toggleButton.style.color = 'grey';
      	window.removeEventListener("hashchange", timedFunction);
    } else {
        breadCrumbDiv.style.display = 'block';
        toggleButton.style.color = 'green';
      	window.addEventListener("hashchange", timedFunction);
    }
}

//had to delay function for adding breadcrumbs to give page time to load
function timedFunction() {
    setTimeout(addPageToRecent, 150)
}

function addPageToRecent() {
    var pageUrl = window.location.href; //snags the url for said page
    if (urlArray.slice(0, 8).includes(pageUrl) == false) { //checks if the link already exists in the last 5 links
        addLinkElement(pageUrl);
    }
    else {
        var index = urlArray.indexOf(pageUrl);
        urlArray.splice(index, 1);
        linksArray.splice(index, 1);
        addLinkElement(pageUrl);
    }
}

function  addLinkElement(pageUrl) {
    var parent = document.getElementsByClassName("rm-title-display")[0]; //snags the page title
    if(pageUrl == 'https://roamresearch.com/#/app/shodty') { //checks if they are on daily notes page
        createLinkElement(parent, pageUrl, 0);
    }
    if(parent != null) {  // gets page name if not on daily pages
        var children = parent.children[0];
        createLinkElement(children, pageUrl, 1);
    }
    else { // checks if the user is zoomed into a bullet
        var parent = document.getElementsByClassName("zoom-path-view")[0];
        var children = parent.children[0].children[0].children[0];
        createLinkElement(children, pageUrl, 2);
    }
}

function createLinkElement(children, pageUrl, urlCase) {
    var lastNine = pageUrl.substr(pageUrl.length - 9);
    if(urlCase == 0) {var innerChild = "<span style='color: [FF5E00](FF5E00.md);'>✹</span> Daily Notes" }
    else if(urlCase == 1) { var innerChild = children.innerHTML.substring(0, 25) }
    else if(urlCase == 2) { var innerChild =  "<span style='color: [0D9BDB](0D9BDB.md);'>🞇</span> " + children.innerHTML.substring(0, 20) }
    var linkElement = "<a id='" + lastNine + "' href='" + pageUrl + "' class='recentLink' style='padding: 0 10px;'>" + innerChild + "</a>"; //adds <a> element to array, maximum 25 chars, increase substring size if you wish
    urlArray.unshift(pageUrl);
    linksArray.unshift(linkElement);
    linksArray = linksArray.slice(0, 8); //reduces the array to to 5 link max, in crease if you wish
    breadCrumbDiv.innerHTML = linksArray.slice(1, 8).join("‣"); //puts the <a> array into the breadCrumbDiv
    var linkElements = document.getElementsByClassName("recentLink");
    for(i=0; i<linkElements.length; i++){
        var linkNumber = "<span style='color: [0087FF](0087FF.md); padding-right: 3px;' class='linkNumber'>" + (i+1).toString() + "</span>";
    linkElements[i].innerHTML = linkNumber + linkElements[i].innerHTML;
    }
}

window.addEventListener ("keyup", hotKeyEvent);

function hotKeyEvent(zEvent) {
    if (zEvent.altKey || zEvent.ctrlKey  &&  zEvent.key === "1") { clickLink(1); }
    if (zEvent.altKey || zEvent.ctrlKey  &&  zEvent.key === "2") { clickLink(2); }
    if (zEvent.altKey || zEvent.ctrlKey  &&  zEvent.key === "3") { clickLink(3); }
    if (zEvent.altKey || zEvent.ctrlKey  &&  zEvent.key === "4") { clickLink(4); }
    if (zEvent.altKey || zEvent.ctrlKey  &&  zEvent.key === "5") { clickLink(5); }
    if (zEvent.altKey || zEvent.ctrlKey  &&  zEvent.key === "6") { clickLink(6); }
    if (zEvent.altKey || zEvent.ctrlKey  &&  zEvent.key === "7") { clickLink(7); }
}

function clickLink(n) {
    var linkToClick = linksArray[n];
    if(linkToClick != null) {
        var linkId = linkToClick.substring(7, 16)
        var someLink = document.getElementById(linkId);
        simulateClick(someLink);
    }
}

var simulateClick = function (elem) {
	// Create our event (with options)
	var evt = new MouseEvent('click', {
		bubbles: true,
		cancelable: true,
		view: window
	});
	// If cancelled, don't dispatch our event
	var canceled = !elem.dispatchEvent(evt);
};```
- 第十一个js模块：attr-table属性筛选
    - ![How to Use](https://user-images.githubusercontent.com/64155612/96104315-8cc79600-0e8d-11eb-9c68-bf930d041054.gif)
    - ![Default Filters](https://user-images.githubusercontent.com/64155612/96158005-e056d580-0ec7-11eb-8510-3b363ba6c605.gif)
    - 资源：https://github.com/GitMurf/roam-javascript[smart-linking](smart-linking.md)
- 第十二个js模块：[ViktoRoam](https://github.com/thesved/ViktoRoam)
    - 功能
        - gallery: zoom in on images 
        - longtap: long tap for right clicking on touch devices
        - dateformatter:  display dates differently than `January 1st, 2021` format to `2021.01.01 Friday`
        - relativelinks: have relative links, like [next block](block:next)
        - export: `ctrl + S` for quickly exporting the whole database
        - blockcss: create css for blocks with tags, eg [block](block.md):hide
        - autoenclose: automatically enclose " and ' characters
        - fuckitline: use [fuckitline](fuckitline.md) on a block and it highlights the first 3 children
    - {{roam/js}}
        - ```javascript
/*
 * Viktor's Roam Plugin Loader
 * version: 0.1
 * author: @ViktorTabori
 *
 * How to install it:
 *  - go to page [roam/js](roam/js.md)
 *  - create a node with: {{[roam/js](roam/js.md)}}
 *  - create a clode block under it
 *  - allow the running of the javascript on the {{[roam/js](roam/js.md)}} node
 * 
 * DISABLE a script: 
 *  1) change `true` to `false` in the load variable
 *     eg. 'gallery': false
 *  2) reload Roam 
 *      OR disable and enable the {{[roam/js](roam/js.md)}} block
 */

// settings
window.ViktorOpts = {
	dateformat: 'YYYY.MM.DD EEE',	// see for details: https://github.com/thesved/ViktoRoam/blob/master/js/dateformat.js
	nameMonths: ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'],
	nameMonthsShort: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
	nameDays: ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday'],
	nameDaysShort: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun'],
	exportFormat: 'JSON',		// EDN | JSON | Markdown
	fuckitlineTag: 'fuckitline',	// tag a block with this, eg [fuckitline](fuckitline.md)
	fuckitlineName: 'fuck it line'	// name above the fuckitline
};

// plugins handling
(()=>{
	var load = {
		'gallery': true,	// zoom in on images 
		'longtap': true,	// long tap for right clicking on touch devices
		'dateformatter': true,	// display dates differently than `January 1st, 2020` format
		'relativelinks': true,	// have relative links, like [next block](block:next)
		'export': true,		// `ctrl + S` for quickly exporting the whole database
		'blockcss': true,	// create css for blocks with tags, eg [block](block.md):hide
		'autoenclose': true,	// automatically enclose " and ' characters
		'fuckitline': true,	// use [fuckitline](fuckitline.md) on a block and it highlights the first 3 children
	};

	var defaultrepo = 'https://js.limitlessroam.com/js/';

	// add alpha channel
	if (typeof alphaChannel == 'object') Object.keys(alphaChannel).forEach(a=>{ load[a]=true });

	// handling script loading and stopping
	Object.keys(load).forEach(k=>{
		var moduleName = 'Viktor'+k.replace(/^\w/, c => c.toUpperCase()); // eg. ViktorGallery

		// remove script if exists
		var script = document.getElementById(moduleName);
		if (script) 
			script.remove();

		// if script is set to false
		if (!load[k]) {
			// stop from running
			try {
				if (window[moduleName] && typeof window[moduleName].stop === 'function') window[moduleName].stop();
			} catch(_) {}

			return;
		}

		// add it
		var extension = document.createElement("script");
		extension.src = typeof alphaChannel == 'object' && typeof alphaChannel[k] != 'undefined' ? alphaChannel[k] : defaultrepo+k+'.js';	// add url
		extension.src = extension.src + (extension.src.indexOf('?') > -1 ? '&' : '?') + 'cb='+Date.now();	// add cache buster
		extension.id = moduleName;
		extension.async = false;
		extension.type = "text/javascript";
		document.head.appendChild(extension);
	});
	
})();```

# Backlinks
## [December 8th, 2020](December 8th, 2020.md)
- [leodknuth插件集合](leodknuth插件集合.md)

## [Roam Research 卡片式写作主题](Roam Research 卡片式写作主题.md)
1. Add a [leodknuth插件集合](leodknuth插件集合.md)

## [Twitter-->Roam的最快方式✈️ ](Twitter-->Roam的最快方式✈️ .md)
- **[Step 1](Step 1.md):** 开一个[leodknuth插件集合](leodknuth插件集合.md)

- {{[leodknuth插件集合](leodknuth插件集合.md)}

## [roam/js](roam/js.md)
- [leodknuth插件集合](leodknuth插件集合.md)

## [roam/js/image-tagging](roam/js/image-tagging.md)
- {{[leodknuth插件集合](leodknuth插件集合.md)}

## [用roam/js创建和使用模版](用roam/js创建和使用模版.md)
- From any page in Roam, create a page titled roam/js by typing [leodknuth插件集合](leodknuth插件集合.md).

- Click the link so you’re on the roam/js page. There, enable JavaScript by typing {{[leodknuth插件集合](leodknuth插件集合.md)}

