- {{[[roam/js]]}}
    - ```javascript
var CARD_MODE_VERSION = "gh-pages";
// window.URLScriptServer = `https://raw.githack.com/JimmyLv/styled-roam/${CARD_MODE_VERSION}/`;
// window.URLScriptServer = `https://cdn.jsdelivr.net/gh/JimmyLv/styled-roam@${CARD_MODE_VERSION}/`;
window.URLScriptServer = `https://styled-roam.vercel.app/`;

var existing = document.getElementById("styled-roam");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = window.URLScriptServer + "js/index.js";
  extension.id = "styled-roam";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}```
