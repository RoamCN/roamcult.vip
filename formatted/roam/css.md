- mono themeset
    - ```css
@import url('https://abhayprasanna.github.io/better-dark-age.css');
a
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
    --page-links              : [2979ff](../2979ff.md);
    --attributes-color        : [986801](../986801.md);
    --external-links          : [50A14E](../50A14E.md);
    --links-hover             : [E4564A](../E4564A.md);
    --hashtags                : [A626A4](../A626A4.md);
    --body-text               : [292D31](../292D31.md);
    --italics-color           : [E4564A](../E4564A.md);
    --bold-color              : [0184BC](../0184BC.md);
    --highlight-text-color    : [292D31](../292D31.md);
    --highlighter             : [FFFF80](../FFFF80.md);
    --background              : [FAFAFA](../FAFAFA.md);
    --sidebar-background      : [EAEAEB](../EAEAEB.md);
    --sidebar-text            : [292D31](../292D31.md);
    --page-heading            : [2979ff](../2979ff.md);
    --daily-heading           : [2979ff](../2979ff.md);
    --headings                : [292D31](../292D31.md);
    --bullets                 : [4078F2](../4078F2.md);
    --closed-bullets          : [4078F277](../4078F277.md);
    --references              : [4078F2](../4078F2.md);
    --block-reference-text    : [0184BC](../0184BC.md);
    --namespaces              : [E4564A](../E4564A.md);
    --all-pages-mentions      : [0184BC](../0184BC.md);
    --cursor                  : [292D31](../292D31.md);
    --icons                   : [4078F2](../4078F2.md);
    --icons-hover             : [E4564A](../E4564A.md);
    --filter-icon             : [50A14E](../50A14E.md);
    /* FONT SIZES */
    --main-font-size          : 1em;
    --page-head-font-size     : 2.2em;
    --h1-font-size            : 2em;
    --h2-font-size            : 1.6em;
    --h3-font-size            : 1.2em;
    --sidebar-h1-size         : 2.2em;
    /* DROPDOWN MENU */
    --dropdown-menu-background: [EAEAEB](../EAEAEB.md);
    --dropdown-menu-highlight : [FAFAFA](../FAFAFA.md);
    --dropdown-menu-text      : [292D31](../292D31.md);
    --dropdown-newpage        : [2979ff](../2979ff.md);
    /* SEARCH BAR */
    --search-bar-background   : [F7F8FA](../F7F8FA.md);
    --search-bar-text         : [292D31](../292D31.md);
    /* KANBAN CARD COLORS */
    --kanban-main-background  : [FAFAFA](../FAFAFA.md);
    --kanban-column-background: [EAEAEB](../EAEAEB.md);
    --kanban-card-background  : [FAFAFA](../FAFAFA.md);
    --kanban-text-hover       : [E4564A](../E4564A.md);
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
    /* COLORS (HT: Jack Laing for [Dracula Pro](../Dracula Pro.md) color theme) */
    --page-links              : [9580FF](../9580FF.md);
    --attributes-color        : [FFFF80](../FFFF80.md);
    --external-links          : [8AFF80](../8AFF80.md);
    --links-hover             : [92FFFF](../92FFFF.md);
    --hashtags                : [FE7FBF](../FE7FBF.md);
    --body-text               : [F2F2F2](../F2F2F2.md);
    --italics-color           : [92FFFF](../92FFFF.md);
    --bold-color              : [FF9580](../FF9580.md);
    --highlight-text-color    : [1B1A23](../1B1A23.md);
    --highlighter             : [FFFF80](../FFFF80.md);
    --background              : [1B1A23](../1B1A23.md);
    --sidebar-background      : [2B2640](../2B2640.md);
    --sidebar-text            : [F2F2F2](../F2F2F2.md);
    --page-heading            : [9580FF](../9580FF.md);
    --daily-heading           : [9580FF](../9580FF.md);
    --headings                : [F2F2F2](../F2F2F2.md);
    --bullets                 : [7C6EAD](../7C6EAD.md);
    --closed-bullets          : [313340](../313340.md);
    --references              : [7C6EAD](../7C6EAD.md);
    --block-reference-text    : [FF9580](../FF9580.md);
    --namespaces              : [92FFFF](../92FFFF.md);
    --all-pages-mentions      : [FF9580](../FF9580.md);
    --cursor                  : [F2F2F2](../F2F2F2.md);
    --icons                   : [7C6EAD](../7C6EAD.md);
    --icons-hover             : [92FFFF](../92FFFF.md);
    --filter-icon             : [8AFF80](../8AFF80.md);
    /* FONT SIZES */
    --main-font-size          : 1em;
    --page-head-font-size     : 2.2em;
    --h1-font-size            : 2em;
    --h2-font-size            : 1.6em;
    --h3-font-size            : 1.2em;
    --sidebar-h1-size         : 2.2em;
    /* DROPDOWN MENU */
    --dropdown-menu-background: [2B2640](../2B2640.md);
    --dropdown-menu-highlight : [1B1A23](../1B1A23.md);
    --dropdown-menu-text      : [F2F2F2](../F2F2F2.md);
    --dropdown-newpage        : [9580FF](../9580FF.md);
    /* SEARCH BAR */
    --search-bar-background   : [1B1A23](../1B1A23.md);
    --search-bar-text         : [F2F2F2](../F2F2F2.md);
    /* KANBAN CARD COLORS */
    --kanban-main-background  : [1B1A23](../1B1A23.md);
    --kanban-column-background: [2A2C37](../2A2C37.md);
    --kanban-card-background  : [1B1A23](../1B1A23.md);
    --kanban-text-hover       : [81FFEA](../81FFEA.md);
  }
}


[data-link-title^='🍚 今天'] {
  padding: 8px;
  color: gray !important;
  background: [C6D1D7](../C6D1D7.md);
}

[data-link-title^='🍚 今天']:before {
  content: '🌞 '
}
[data-link-title^='🍚 今天']:after {
  content: ' 🌑'
}```
- [SmartBlocks](../SmartBlocks.md) 插件样式
    - ```css
.rm-bq {
    background-color: [F5F8FA](../F5F8FA.md) !important;
    border-left: 5px solid [2196f3](../2196f3.md) !important;
  	color: black !important;
  	border-top-right-radius: 20px;
  	border-bottom-right-radius: 20px;
}```
- [good](../good.md)
- 
- 
- mermaid
    ```css
.rm-mermaid{
  background: transparent !important;
  min-width: 0px !important;
}

.rm-mermaid .node rect{
  stroke: [2A496F](../2A496F.md) !important;
}

.rm-mermaid div
{
  color: [448889](../448889.md) !important;
  margin-right: 15px;
}

.rm-mermaid text
{
  fill: [34A5A5](../34A5A5.md) !important;
  font-size: 25px !important;
}

.rm-mermaid rect{
  fill: transparent !important;
  stroke-width: 0px !important;
}

.rm-mermaid tspan{
  fill: [438BE0](../438BE0.md) !important;
  font-size: 20px !important;
}```

# Backlinks
## [August 12th, 2020](August 12th, 2020.md)
- [roam/css](../roam/css.md)

## [December 23rd, 2020](December 23rd, 2020.md)
- -> 大纲圆点颜色 #[roam/css](../roam/css.md)

- css 菜鸟指南 #[roam/css](../roam/css.md)

## [roam 用例](roam 用例.md)
- [Digital Garden](../Digital Garden.md)[roam/css](../roam/css.md)

## [🎫插件](🎫插件.md)
- [roam/css](../roam/css.md)

