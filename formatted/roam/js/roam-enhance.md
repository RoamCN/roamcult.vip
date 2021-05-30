- {{[roam/js](<../../roam/js.md>)}}
    - ```javascript
window.roamEnhance = {
  plugins: [
//    'metadata', 
//    'template-button',
//    'change-fontsize',
    'reading-mode',
    'video',
//    'link-favicon',
    'table-of-content'
  ]
}

var existing = document.getElementById("roam-enhance");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roam-enhance.vercel.app/main.js";
  // extension.src = "https://cdn.jsdelivr.net/gh/yoyooyooo/roam-enhance/dist/main.js";
  extension.id = "roam-enhance";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}```

# Backlinks
## [roam/js](<roam/js.md>)
- [roam/js/roam-enhance](<../../roam/js/roam-enhance.md>)

