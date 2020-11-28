- {{[roam/js](../roam/js.md)}}
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
    s.src =  "https://roam42.glitch.me/main.js"
  	s.async = true
document.getElementsByTagName('head')[0].appendChild(s)

const CARD_MODE_VERSION = 'ef847c84'
window.URLScriptServer = `https://cdn.jsdelivr.net/gh/JimmyLv/styled-roam@${CARD_MODE_VERSION}/`
var s = document.createElement('script')
	s.type = "text/javascript"
    s.src =  window.URLScriptServer + "js/index.js"
	s.async = true
document.getElementsByTagName('head')[0].appendChild(s)```
- <script src="https://kit.fontawesome.com/8c717ed232.js" crossorigin="anonymous"></script>

# Backlinks
## [Roam Research 卡片式写作主题](Roam Research 卡片式写作主题.md)
1. Add a [roam/js](../roam/js.md)

## [Twitter-->Roam的最快方式✈️ ](Twitter-->Roam的最快方式✈️ .md)
- **[Step 1](../Step 1.md):** 开一个[roam/js](../roam/js.md)

- {{[roam/js](../roam/js.md)}

## [roam/js](roam/js.md)
- {{[roam/js](../roam/js.md)}

## [roam/js/Roam42](roam/js/Roam42.md)
- {{[roam/js](../roam/js.md)}

## [roam/js/image-tagging](roam/js/image-tagging.md)
- {{[roam/js](../roam/js.md)}

## [用roam/js创建和使用模版](用roam/js创建和使用模版.md)
- From any page in Roam, create a page titled roam/js by typing [roam/js](../roam/js.md).

- Click the link so you’re on the roam/js page. There, enable JavaScript by typing {{[roam/js](../roam/js.md)}

