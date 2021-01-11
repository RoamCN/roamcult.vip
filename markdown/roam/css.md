- mono themeset
    - ```css
@import url('https://abhayprasanna.github.io/better-dark-age.css');

@import url('https://fonts.googleapis.com/css?family=Commissioner|Crimson+Text|Fira+Code|Bitter|Work+Sans');

@media (prefers-color-scheme: light) {
  :root {
    /* FONTS */
    --global-font             : 'Work Sans', sans-serif;
    --secondary-font          : 'Fira Code', monospace;
    --header-font             : 'Crimson Text', serif;
    /* WIDTH FIXES - default 568px,1032px - increase to increase WIDTH */
    --reduce-padding-right    : 3400px;
    --reduce-padding-left     : 3400px;
    /* COLORS - One light*/
    --page-links              : #2979ff;
    --attributes-color        : #986801;
    --external-links          : #50A14E;
    --links-hover             : #E4564A;
    --hashtags                : #A626A4;
    --body-text               : #292D31;
    --italics-color           : #E4564A;
    --bold-color              : #0184BC;
    --highlight-text-color    : #292D31;
    --highlighter             : #FFFF80;
    --background              : #FAFAFA;
    --sidebar-background      : #EAEAEB;
    --sidebar-text            : #292D31;
    --page-heading            : #2979ff;
    --daily-heading           : #2979ff;
    --headings                : #292D31;
    --bullets                 : #4078F2;
    --closed-bullets          : #4078F277;
    --references              : #4078F2;
    --block-reference-text    : #0184BC;
    --namespaces              : #E4564A;
    --all-pages-mentions      : #0184BC;
    --cursor                  : #292D31;
    --icons                   : #4078F2;
    --icons-hover             : #E4564A;
    --filter-icon             : #50A14E;
    /* FONT SIZES */
    --main-font-size          : 1em;
    --page-head-font-size     : 2.2em;
    --h1-font-size            : 2em;
    --h2-font-size            : 1.6em;
    --h3-font-size            : 1.2em;
    --sidebar-h1-size         : 2.2em;
    /* DROPDOWN MENU */
    --dropdown-menu-background: #EAEAEB;
    --dropdown-menu-highlight : #FAFAFA;
    --dropdown-menu-text      : #292D31;
    --dropdown-newpage        : #2979ff;
    /* SEARCH BAR */
    --search-bar-background   : #F7F8FA;
    --search-bar-text         : #292D31;
    /* KANBAN CARD COLORS */
    --kanban-main-background  : #FAFAFA;
    --kanban-column-background: #EAEAEB;
    --kanban-card-background  : #FAFAFA;
    --kanban-text-hover       : #E4564A;
  }
}
@media (prefers-color-scheme: dark) {
  :root {
    /* FONTS */
    --global-font             : 'Work Sans', sans-serif;
    --secondary-font          : 'Fira Code', monospace;
    --header-font             : 'Bitter', serif;
    /* WIDTH FIXES - default 568px,1032px - increase to increase WIDTH */
    --reduce-padding-right    : 3400px;
    --reduce-padding-left     : 3400px;
    /* COLORS (HT: Jack Laing for [[Dracula Pro]] color theme) */
    --page-links              : #9580FF;
    --attributes-color        : #FFFF80;
    --external-links          : #8AFF80;
    --links-hover             : #92FFFF;
    --hashtags                : #FE7FBF;
    --body-text               : #F2F2F2;
    --italics-color           : #92FFFF;
    --bold-color              : #FF9580;
    --highlight-text-color    : #1B1A23;
    --highlighter             : #FFFF80;
    --background              : #1B1A23;
    --sidebar-background      : #2B2640;
    --sidebar-text            : #F2F2F2;
    --page-heading            : #9580FF;
    --daily-heading           : #9580FF;
    --headings                : #F2F2F2;
    --bullets                 : #7C6EAD;
    --closed-bullets          : #313340;
    --references              : #7C6EAD;
    --block-reference-text    : #FF9580;
    --namespaces              : #92FFFF;
    --all-pages-mentions      : #FF9580;
    --cursor                  : #F2F2F2;
    --icons                   : #7C6EAD;
    --icons-hover             : #92FFFF;
    --filter-icon             : #8AFF80;
    /* FONT SIZES */
    --main-font-size          : 1em;
    --page-head-font-size     : 2.2em;
    --h1-font-size            : 2em;
    --h2-font-size            : 1.6em;
    --h3-font-size            : 1.2em;
    --sidebar-h1-size         : 2.2em;
    /* DROPDOWN MENU */
    --dropdown-menu-background: #2B2640;
    --dropdown-menu-highlight : #1B1A23;
    --dropdown-menu-text      : #F2F2F2;
    --dropdown-newpage        : #9580FF;
    /* SEARCH BAR */
    --search-bar-background   : #1B1A23;
    --search-bar-text         : #F2F2F2;
    /* KANBAN CARD COLORS */
    --kanban-main-background  : #1B1A23;
    --kanban-column-background: #2A2C37;
    --kanban-card-background  : #1B1A23;
    --kanban-text-hover       : #81FFEA;
  }
}


[data-link-title^='🍚 今天'] {
  padding: 8px;
  color: gray !important;
  background: #C6D1D7;
}

[data-link-title^='🍚 今天']:before {
  content: '🌞 '
}
[data-link-title^='🍚 今天']:after {
  content: ' 🌑'
}```
- ```javascript
[roam-table-background="visible"] {
  background-color:  #52b788 !important;
}

/* Rainbow indentation */
/* 
Feel free to adjust the colors - this one loops every
7 colors like the rainbow but you can change that to 
cycle earlier or choose more unique colors.
To add deeper indents:
1. Add { > div.flex-v-box > div } incrementally to the first line, and
2. Add {> div.flex-v-box > div:nth-child(n) } incrementally to the second line
*/
#rm-log-container > div > div > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n),
.flex-v-box > div:nth-child(n) > div.flex-v-box > div {
    border-left-color: #D0CECEAD !important;
}
#rm-log-container > div > div > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div,
.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div {
    border-left-color: #9580FFAD !important;
}
#rm-log-container > div > div > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div:nth-child(n),
.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div {
    border-left-color: #92FFFFAD !important;
}
#rm-log-container > div > div > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n),
.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div {
    border-left-color: #8AFF80AD !important;
}
#rm-log-container > div > div > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n),
.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div {
    border-left-color: #FFFF80AD !important;
}
#rm-log-container > div > div > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n),
.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div {
    border-left-color: #FF9580AD !important;
}
#rm-log-container > div > div > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n),
.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div {
    border-left-color: #FE7FBFAD !important;
}
#rm-log-container > div > div > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n),
.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div {
    border-left-color: #DA53EEAD !important;
}
#rm-log-container > div > div > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n),
.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div {
    border-left-color: #6600EDAD !important;
}
#rm-log-container > div > div > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n),
.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div {
    border-left-color: #0079FFAD !important;
}
#rm-log-container > div > div > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n),
.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div {
    border-left-color: #00F11DAD !important;
}
#rm-log-container > div > div > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n),
.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div {
    border-left-color: #FFEF00AD !important;
}
#rm-log-container > div > div > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n),
.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div {
    border-left-color: #FF7F00AD !important;
}
#rm-log-container > div > div > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n) > div.flex-v-box > div:nth-child(n),
.flex-v-box > div:nth-child(n) > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div > div.flex-v-box > div {
    border-left-color: #FF0900AD !important;
}

/* 
Optional border adjustments:
1. You can add a border-radius: 5px or more to get an interesting delineation
2. You can adjust the width of the border but make sure to adjust margin to align the border with the bullets  
*/
.block-border-left {
    border-left-width: 2px !important;
    margin-left: 5px !important;
}```
- [[SmartBlocks]] 插件样式
    - ```css
.rm-bq {
    background-color: #F5F8FA !important;
    border-left: 5px solid #2196f3 !important;
  	color: black !important;
  	border-top-right-radius: 20px;
  	border-bottom-right-radius: 20px;
}```
- #good
- 
- ```css
- 
- mermaid
    ```css
.rm-mermaid{
  background: transparent !important;
  min-width: 0px !important;
}

.rm-mermaid .node rect{
  stroke: #2A496F !important;
}

.rm-mermaid div
{
  color: #448889 !important;
  margin-right: 15px;
}

.rm-mermaid text
{
  fill: #34A5A5 !important;
  font-size: 25px !important;
}

.rm-mermaid rect{
  fill: transparent !important;
  stroke-width: 0px !important;
}

.rm-mermaid tspan{
  fill: #438BE0 !important;
  font-size: 20px !important;
}```
- /* -------------------------- */
- /*           MISC             */
- /* -------------------------- */
- /* for when filter is active on page */
- .bp3-icon-filter[style*="color"] {
    - color: rgb(var(--color-secondary)) !important;
- }
- /* better caret positioning in linked references */
- .bp3-icon-caret-down::before {
    - color: var(--bullet-color) !important;
- }
- .bp3-icon-caret-down {
    - display: inline-block !important;
    - /*margin-bottom: 8px;*/
    - /* fix positioning when rotated 90 deg */
    - /*transform-origin: 9px 13px;*/
- }
- /* */
- .roam-center > div[style*="width: 100%; height: 100%;"] {
    - width: 616px !important;
- }
- .roam-center > div[style*="width: 100%; height: 100%;"] > div {
    - position: fixed !important;
    - top: 0; left: 0;
    - width: 100vw !important;
    - height: 100vw !important;
- }
- /* GRAPH VIEW */
- /* you can't actually style the graph view because it uses canvas elements, but we *can* apply CSS filters to it to slightly change the appearance */
- canvas[data-id="layer2-node"] {
    - /*filter: invert(1) drop-shadow(0px 3px 4px rgba(0,0,0,0.1));*/
    - filter: invert(1) hue-rotate(110deg) saturate(2.5);
    - opacity: 0.3;
    - transition: opacity .2s ease-out;
- }
- [id*="cyto-wrapper"]:hover canvas[data-id="layer2-node"] {
    - opacity: 1;
- }
- /* SLIDER */
- .bp3-intent-primary {
    - background-color: rgb(var(--color-primary)) !important;
- }
- .bp3-slider-handle {
    - border-radius: 10px;
- }
- /* CHECKBOX */
- .check-container .checkmark {
    - width: 14px;
    - height: 14px;
- }
- .check-container .checkmark::after {
    - left: 4.5px;
    - top: 1px;
- }
- .check-container input[checked] + .checkmark {
    - background-color: rgb(var(--color-primary)) !important;
- }
- /*
- .roam-topbar .bp3-popover-wrapper .bp3-popover-content {
    - background-color: #FFFFFF !important;
    - color: #000000 !important;
- }
- .roam-topbar > .bp3-popover-wrapper .bp3-popover-arrow svg * {
    - fill: #FFFFFF;
- }*/
- #buffer {
    - background: transparent !important;
    - right: 7px !important;
    - bottom: 10px !important;
- }
- #buffer .bp3-popover-target >.bp3-button {
    - background: rgba(0, 0, 0, 0.1);
    - height: 30px;
    - width: 30px;
- }
- #buffer > div {
    - z-index: 99999 !important;
    - background: rgb(var(--color-secondary), 0.7) !important;
    - backdrop-filter: blur(5px);
    - border-radius: 10px;
    - padding: 2px 8px 8px 8px;
    - box-shadow: 0px 8px 14px rgba(0, 0, 0, 0.1)
- }
- #buffer > div .bp3-button::before {
    - color: #FFFFFF !important;
- }
- #buffer .help-title {
    - color: var(--color-secondary-contrast) !important;
- }
- #buffer .help-sub-title {
    - color: var(--color-secondary-contrast) !important;
    - opacity: 0.5;
- }
- #buffer span {
    - color: rgba(255, 255, 255, 0.8) !important;
- }
- #buffer a {
    - text-decoration: underline;
    - color: var(--color-secondary-contrast) !important;
- }
- #buffer a:hover {
    - opacity: 0.5;
- }
- /* ------------- Red Pomodoro ------------- */
- /* credit: https://github.com/theianjones/roam-research-themes/blob/master/pomodoros.css */
- .rm-pomodoro {
    - background: transparent !important;
    - color: #ff4747 !important;
    - padding: 4px 14px;
    - line-height: 2em;
    - font-weight: 600;
    - border-radius: 2em;
    - border: 1px solid #ff474770;
- }
- .rm-pomodoro::first-letter {
    - margin-right: 8px;
- }
- /* BUTTON */
- .block-bullet-view .bp3-button:not([class*="bp3-icon"]) {
    - background: transparent !important;
    - color: rgb(var(--color-primary)) !important;
    - padding: 4px 14px;
    - line-height: 2em;
    - font-weight: 600;
    - border-radius: 2em !important;
    - border: 1px solid rgba(var(--color-primary), 0.5) !important;
    - box-shadow: none !important;
- }
- .block-bullet-view .bp3-button:hover {
    - background: rgba(var(--color-primary), 0.2) !important;
- }
- /* KANBAN */
- .kanban-board {
    - background-color: transparent;
    - padding: 0;
    - max-width: 500px;
- }
- .kanban-title {
    - background: rgb(var(--color-primary));
    - color: var(--color-primary-contrast) !important;
    - font-weight: bold;
    - padding: 0px !important;
    - max-height: 30px;
    - border: none;
    - display: flex;
    - align-items: center;
- }
- .kanban-title > span {
    - display: block;
    - margin: auto;
- }
- .kanban-column {
    - border-radius: 10px;
    - box-shadow: 0px 8px 14px rgba(0, 0, 0, 0.05);
    - padding: 0;
    - overflow: hidden;
- }
- .kanban-card {
    - border-radius: 10px;
    - box-shadow: 0px 8px 14px rgba(0, 0, 0, 0.05);
- }
- .kanban-card {
    - background-color: var(--page-color);
    - margin: 8px;
    - box-shadow: 0px 1px 2px #9EB3C0;
    - padding: 10px;
    - border-radius: 4px;
    - line-height: 1.3em;
- }
- .kanban-column {
    - background-color: ;
    - margin: 0px 4px 0px 4px;
    - min-width: 200px;
    - border-radius: 6px;
- }
- /* ASTROLABE */
- /* Breathing Loader */
- /* https://codepen.io/Mathi_C/pen/mMWaaW */
- .loading-astrolabe {
    - height: 100px;
    - width: 100px;
    - border-radius: 200px;
    - margin: auto;
- }
- .loading-astrolabe {
    - animation-name: orb_1;
    - animation-duration: 3s;
    - animation-delay: 0s;
    - animation-iteration-count: infinite;
    - animation-timing-function: ease-in-out;
    - animation-direction: alternate;
- }
- @keyframes orb_1 {
    - from {
        - transform: scale(0.2);
        - background: rgb(var(--color-secondary));
    - }
    - to {
        - transform: scale(2);
        - background: rgb(var(--color-primary));
    - }
- }
- /* Hide original loader */
- .loading-astrolabe img {
    - display: none;
- }
- .bp3-spinner {
    - visibility: hidden;
- }
- .bp3-spinner > * {
    - visibility: visible;
- }
- .bp3-spinner-head {
    - stroke: rgb(var(--color-primary)) !important;
- }
- .roam-center > div > div > div svg {
    - background-color: var(--bg-color) !important;
- }
- /* fix specific popover sizes and positions... */
- .roam-topbar .bp3-popover-wrapper:nth-child(6) .bp3-popover,
- .roam-topbar .bp3-popover-wrapper:nth-child(7) .bp3-popover{
    - width: 600px;
    - max-width: calc(100vw - 20px);
- }
- #roam-right-sidebar-content > div .flex-h-box > .bp3-popover-wrapper .bp3-transition-container {
    - transform: translate3d(-15px, 41px, 0px) !important;
- }
- #roam-right-sidebar-content > div .flex-h-box > .bp3-popover-wrapper .bp3-transition-container .bp3-popover-arrow {
    - left: 10px !important;
- }
- /* -------------------------- */
- /*         MOBILE             */
- /* -------------------------- */
- @media only screen and (max-width: 600px) {
    - .roam-topbar {
        - margin: 0px !important;
        - padding: 10px 0px 0px 0px !important;
        - width: 100%;
        - justify-content: center;
        - position: fixed !important;
        - top: 0px;
        - left: 0px;
        - backdrop-filter: blur(5px);
    - }
    - .roam-topbar::before {
        - content: "";
        - position: absolute;
        - top: 0; left: 0;
        - width: 100%; height: 100%;
        - background-color: var(--bg-color) !important;
        - opacity: 0.7;
    - }
    - .roam-topbar > .flex-h-box {
        - flex-direction: row;
        - height: 1px !important;
        - align-items: start !important;
        - text-align: center;
        - /*position: -webkit-sticky !important;
        - position: fixed !important;
        - left: 0px;
        - top: 0;*/
        - position: relative !important;
        - width: 300px !important;
        - margin: auto;
        - justify-content: space-evenly;
    - }
    - .roam-topbar > div >.bp3-button:first-child {
        - position: static !important;
    - }
    - .roam-sidebar-container {
        - padding-right: 0;
        - width: 232px !important;
    - }
    - .roam-sidebar-container > .roam-sidebar-content::before {
        - right: 0px !important;
    - }
    - .roam-body-main {
        - padding-left: 0 !important;
    - }
    - #find-or-create-input {
        - max-width: calc(100% - 20px);
        - left: 10px !important;
    - }
    - .roam-article,
    - .rm-all-pages > .table,
    - .rm-all-pages > .table > div {
        - max-width: calc(100vw - 20px) !important;
        - min-width: calc(100vw - 20px) !important;
        - width: calc(100vw - 20px) !important;
    - }
    - .rm-all-pages > .table {
        - margin-left: 10px;
        - margin-right: 10px;
    - }
    - .roam-article {
        - margin: 50px 10px !important;
        - margin-bottom: 100px !important;
    - }
    - .roam-article > div {
        - padding: 30px 30px 30px 20px;
    - }
    - #roam-right-sidebar-content > div > *{
        - max-width: calc(100vw - 20px) !important;
    - }
    - /* position minus button */
    - #roam-right-sidebar-content > div .bp3-icon-minus, #roam-right-sidebar-content > div .bp3-icon-plus {
        - top: 60px;
    - }
    - /* position filter button */
    - #roam-right-sidebar-content > div .bp3-icon-minus ~ .bp3-popover-wrapper {
        - top: 60px;
    - }
    - /* position references button */
    - #roam-right-sidebar-content > div .bp3-icon-minus ~ button.bp3-button {
        - top: 60px;
    - }
    - /* position close button */
    - #roam-right-sidebar-content > div .bp3-icon-minus ~ .bp3-button.bp3-icon-cross {
        - top: 60px;
    - }
    - .rm-title-display, .rm-title-textarea {
        - margin-left: 0 !important;
    - }
    - #roam-right-sidebar-content > div .bp3-icon-minus + * {
        - margin: 30px 10px 5px 30px !important;
    - }
    - .roam-topbar > div > *:nth-child(2) {
        - margin-top: 0 !important;
    - }
    - #right-sidebar {
        - padding-right: 10px !important;
    - }
- }
- #mobile-capture {
    - height: 100vh !important;
    - background-color: var(--bg-color) !important;
- }
- #mobile-capture textarea, #mobile-capture input {
    - background-color: var(--page-color) !important;
- }
- #mobile-capture textarea::placeholder, #mobile-capture input::placeholder {
    - color: var(--text-color) !important;
    - opacity: 0.3
- }
- #mobile-capture textarea {
    - margin-top: 10px;
- }
- #rm-mobile-bar {
    - max-width: 100vw;
    - background-color: rgb(var(--color-secondary)) !important;
    - position: fixed !important;
    - z-index: 999999;
- }
- #rm-mobile-bar .bp3-button {
    - vertical-align: top;
    - margin: 5px 0px !important;
- }
- #rm-mobile-bar .bp3-button::before, #rm-mobile-bar .bp3-button i::before {
    - color: var(--color-secondary-contrast) !important;
