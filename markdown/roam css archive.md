- 亮色 #@Jerry
    - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FRoamCN%2FhtAFHcFb7a.png?alt=media&token=550b22f9-7aa0-4594-897d-60238538a486)
    - abhay
        ```css
@import url('https://abhayprasanna.github.io/better-dark-age.css');

@import url('https://fonts.googleapis.com/css?family=Commissioner|Crimson+Text|Fira+Code|Bitter|Work+Sans');

@media (prefers-color-scheme: light) {
  :root {
    /* FONTS */
    --global-font             : 'Work Sans', '黑体';
    --secondary-font          : 'Fira Code', monospace;
    --header-font             : 'Crimson Text', '黑体';
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
    --global-font             : 'Georgia','华文楷体';
    --secondary-font          : 'Fira Code', monospace;
    --header-font             : 'Georgia','华文楷体';
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
}```
    - linked reference shadow
        - ```css
.rm-ref-page-view {
  border-radius: 4px;
  box-shadow: 0.5px 0.5px 3px 0px #4E7ADB;
  margin-right: 5px !important;
}```
    - sidebar设置
        - ```css
#roam-right-sidebar-content>.sidebar-content>div{
  background-color: #fafafa;
  border-radius: 6px;
  margin: 5px;
  margin-left: -10px;
  margin-right: 0px;
}
#roam-right-sidebar-content>.sidebar-content{
  margin-top: -8px;
  border-radius: 0px !important;
}

div[style*="border-bottom: 1px solid rgb(138, 155, 168);"]{
  border-bottom: none !important;
}

div#roam-right-sidebar-content{
  border-radius: 0px !important;
  border:0px solid #d7e0e7 !important;
}

#roam-right-sidebar-content > div > div:nth-child(n) > div{
  padding-top: 4px !important;
  padding-bottom: 4px !important;
}```
    - 背景
        - ```css
:root{
  --background-image: url("https://image-icons.oss-cn-beijing.aliyuncs.com/img/Colección de wallpapers de la app Telegram – Pinsho.com  Chat wallpape.jpg");
}
.flex-h-box>.roam-main,
.flex-h-box>.roam-main>.roam-topbar,
#right-sidebar,
#right-sidebar>#roam-right-sidebar-content,
div.sidebar-content
{
  background-image: var(--background-image) !important;
}```
    - bullet颜色
        - ```css
.simple-bullet-inner{
  background: #4078f2 !important;
}

span.simple-bullet-outer.cursor-pointer.roam-bullet-closed{
  background: none !important;
  border: 1px solid #4078f2;
}```
    - a 链接颜色 [链接](🔗)
        - ```css
a.rm-alias.rm-alias-block{
  border-bottom: 2px dotted #67C69A;
}

a.rm-alias.rm-alias-external{
  color: #03A9F4 !important;
  border-bottom: 2px dotted #9E9E9E;
}

a.rm-alias.rm-alias-external:after{
   content: '🔗';
}```
    - select {{or: 50% | 25% | 0% | 75% | 100%}} 
        ```css
div:not(.bp3-datepicker-month-select):not(.bp3-datepicker-year-select)>select {
   border: 1px solid #A2A2A2 !important ;
   border-radius: 2px;
   font-style: normal !important;
   background-color: var(--background) !important;
   padding-left:5px;
   color: #673AB7;
 }```
    - ^^高亮^^
        - ```css
.roam-highlight{
  border-radius: 3px;
  background-color: rgba(255,255,128,0.75);
}```
    - 隐藏路径中视频显示
        - ```css
.rm-zoom-item-content>.parent-path-wrapper>div>span>div{
  display: none !important;
}```
    - YouTube Play Button
        - ```css
.timestamp-control{
  background-color: rgba(108,109,36,0.1); 
  color: rgb(251,106,13);
  margin-right: 8px;
  margin-top: 3px;
  margin-bottom: 3px;
  border-radius: '50%';
  border-style: inset;  
  border-color: #FF3200;
  font-size: 0.9em;
}
.timestamp-control:hover {
  background-color: rgba(108,109,36,0.25); 
  border-style: outset;  
  color: #FFFFFF;
}```
    - #unfinished
        - ```css
span.rm-page-ref[data-tag="unfinished"] {
    background: #EFD1EF;
  	color: #101102 !important;
    padding: 2px 2px 2px 5px;
    line-height: 1em;
    font-weight: bold;
    border-radius: 3px;
    position:relative;
}
span.rm-page-ref[data-tag="unfinished"]:before{
  content: '⏳';
}```
    - query
        - ```css
.rm-query{
    box-shadow: 0px 0px 0px 0px #C4BC4B;
    border-radius:4px;
    border: 2px solid #009688;
}
.rm-query-title{
  border-radius: 0;
}```
