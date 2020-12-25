- 
- 
- Zettelkasten 资料 #[知识管理](知识管理.md)
    {{[embed](embed.md): ((((AXfPNMSbb))))}}
- [📝帖子](📝帖子.md) ~ 添加滑动块 #[@苏维](@苏维.md)
    - ```css
/* Scrollbar improvements HT: Palash Karia
Mobile scrollable right sidebar in portrait mode

参考资料:
- https://abhayprasanna.github.io/better-dark-age.css
- https://segmentfault.com/a/1190000003708894
*/

/* 修改滑块颜色 */
@media (prefers-color-scheme: light){
	:root {
    --closed-bullets: [2E2E2E77](2E2E2E77.md);
    --icons-hover: [E4564A](E4564A.md);
  	}
}
/* ------ */

div::-webkit-scrollbar-track {
  background-color: transparent !important;
}

div::-webkit-scrollbar {
  width        : 5px;
  height       : 5px;
  border-radius: 8px;
}

div::-webkit-scrollbar-track {
  background   : transparent;
  border-radius: 20px;
}

div::-webkit-scrollbar-thumb {
  background-color: var(--closed-bullets)!important;
}

div::-webkit-scrollbar-thumb:hover {
  background-color: rgba(0,0,0,0.4);
  border          : 5px var(--icons-hover) solid;
}

/* Compact borderless references and queries */

.rm-reference-item {
  padding: 0 !important;
  margin : 0 !important;
  border : 0 !important;
}

.rm-ref-page-view {
  padding-bottom: 10px !important;
}

.flex-h-box.rm-title-arrow-wrapper {
  padding-bottom: 3px !important;
}


/* Mobile scrollable right sidebar in portrait mode */

@media only screen and (max-width: 600px) {
  .roam-body {
    overflow-x: scroll !important;
    display   : flex;
  }

  .roam-main {
    min-width: 95vw;
  }

  [right-sidebar](right-sidebar.md)[style*="flex: 0 0 40%;"] {
    flex: 0 0 95% !important;
  }
}
/*---------------------------------------------------------------------------*/```

# Backlinks
## [roam面对面圆桌](roam面对面圆桌.md)
- 想做成游戏形式，有一定步骤和反馈的，大家敞开聊对参与者要求太高[December 17th, 2020](December 17th, 2020.md)

