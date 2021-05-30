- {{[[roam/js]]}}
    - ```javascript
function addScript(src, id) {
  const old = document.getElementById(id);
  old && old.remove();
  const s = document.createElement('script');
  s.src = src;
  id && (s.id = id);
  s.async = true;
  s.type = 'text/javascript';
  document.getElementsByTagName('head')[0].appendChild(s);
}

window.roamEnhance = {
  plugins: [
//    'metadata', 
//    'template-button',
//    'change-fontsize',
    'reading-mode',
    'video',
//    'link-favicon',
    ['table-of-content', { 
      fontIcon: 'layers',
/*      isHeading: [
        /\s{2,}$/,
        /^\d+(\.|、)/,
        /^[一二三四五六七八九十]{1,}(\.|、)/,
        (block) => block.level === 1,
        a => !yoyo.utils.removeLinks(a.string)
      ] */
    }]
  ],
  dynamicMenu: [
    'Pull zhihu article',
    'Show highlight'
  ]
}

// no cache,lastest version
addScript(`https://roam-enhance.vercel.app/main.js`, 'roam-enhance')
// with cache
//addScript(`https://cdn.jsdelivr.net/gh/yoyooyooo/roam-enhance/dist/main.js`, 'roam-enhance')```
