- mappletons.css [roam-research-themes/mappletons.css at master · theianjones/roam-research-themes](https://github.com/theianjones/roam-research-themes/blob/master/mappletons.css)
    - ```css
/*  Make sure you have the fonts Lato and Open Sans installed locally on your machine.
They're free to download from Google:
https://fonts.google.com/specimen/Lato
https://fonts.google.com/specimen/Open+Sans  */

h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: 'Lato';
}

div,
textarea {
  font-family: 'Open Sans';
}

.roam-block-container {
    max-width: 1000px;
}

.rm-query {
    border: 0.5px solid [e4e9ec](e4e9ec.md);
    border-radius: 5px;
    
}

.rm-query .rm-query-title {
    background-color: [f7f8f8](f7f8f8.md);
    padding: 0.8em;
    color: [d1dbe2](d1dbe2.md);
    font-size: 80%;
}

.rm-reference-main.rm-query-content {
    padding: 0.8em;
}

.rm-reference-main .rm-reference-item .rm-block-text {
    font-size: 90%;
}

.rm-ref-page-view-title span {
    
}

.rm-reference-main .rm-reference-item .controls {
    margin-left: -1em;
}

.rm-ref-page-view {
    padding: 0.4em 0.2em;
}


.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .starred-pages-wrapper .starred-pages .page {
    padding: 6px;
}

div.flex-v-box.starred-pages-wrapper > div.flex-h-box > span {
    font-size: 14px;
    opacity: 80%;
    letter-spacing: 0.04em;
}

div.roam-sidebar-container.noselect > div > div {
    font-size: 14px;
    letter-spacing: 0.03em;
    
}

[block-input](block-input.md) {
    background: black;
}

.roam-body [block-input](block-input.md) > span > div {
    padding: 6px 24px;
    background: black;
}

span.bp3-icon-small.bp3-icon-star {
    display: none;
    visibility: visible;
}

.roam-block {
    max-width: 850px;
}

[right-sidebar](right-sidebar.md) > div {
    background-color: [f7f8fa](f7f8fa.md);
    border-left: 1px solid [e9ebef](e9ebef.md);
}
.rm-page-ref-brackets {
    display: none;
}
.controls .simple-bullet-outer .simple-bullet-inner {
    background-color: [e5e9f2](e5e9f2.md);
}


/* 大纲辅助线 */
.block-border-left {
    margin-left: 5px!important;
    border-radius: 0;
    padding: 0 !important;
    border-color: [C7CEDB](C7CEDB.md) !important;
}
div.roam-block-container:hover > div:nth-child(2) > .roam-block-container{
    border-left-style:solid;
    border-left-color:[105EB391](105EB391.md)!important;
    transition:border-left-color 0.5s ease-in-out;
    box-shadow:0px 0px 0px 0px rgb(224,215,215);
    transition:box-shadow 0.5s;
}

.kanban-board {
    background-color: [fff](fff.md);
}
.kanban-card {
    background-color: white;
    margin: 8px;
    box-shadow: 0px 1px 2px [9EB3C0](9EB3C0.md);
    padding: 10px;
    border-radius: 2px;
    line-height: 1.3em;
}
.kanban-title {
    text-align: center;
    font-weight: bold;
    padding-top: 6px;
}
.kanban-column {
    background-color: [E4EDF2](E4EDF2.md);
    margin: 0px 4px 0px 4px;
    padding: 4px;
    min-width: 200px;
    border-radius: 3px;
}

/* 块引用 */
.rm-block-ref {
    padding: 1px 2px;
    margin: -4px 2px;
    font-size: 14px;
    display: inline;
    border-bottom: 1px solid [0d6da5](0d6da5.md);
    cursor: alias;
    padding-left: 0px;
    /* RTB add: align to left */
}
.rm-block-ref:hover {
    background-color: [b3d7ff](b3d7ff.md);
    border-radius: 8px;
}




.checkmark {
    background: [fff](fff.md);
}
.check-container input:checked ~ .checkmark {
    background: [33bdea](33bdea.md);
}
.check-container input:checked ~ .checkmark:after {
    border-color: [fff](fff.md);
}
.rm-reference-item {
    margin-top: 8px;
    border-radius: 6px;
    border: 1px solid [e4e9ee](e4e9ee.md);
    margin-right: 8px;
    flex: 1 1 100%;
    word-break: break-word;
    background-color: [f7f9fb](f7f9fb.md);
    padding: 8px;
}

.rm-level2 {
    font-size: 1.5em;
}
.rm-level3 {
    color: [939aae](939aae.md);
    font-weight: 400;
    font-size: 1.3em;
}
.rm-page-ref {
    color: [AF601A](AF601A.md);
}
.rm-page-ref-link-color {
    color: [FF9800](FF9800.md);
    font-weight: 600;
}
a {
    color: [673AB7](673AB7.md);
}
.intercom-app,
.intercom-launcher-frame,
[intercom-container](intercom-container.md) {
    display: none;
}
.roam-body .roam-app .roam-sidebar-container {
    background-color: white;
    border-right: 1px [eee](eee.md) solid;
}
.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .starred-pages-wrapper .starred-pages .page,
.roam-body .roam-app .roam-sidebar-container > * {
    opacity: 80%;
    box-shadow: none;
}
.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .starred-pages-wrapper .starred-pages .page:hover,
.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .log-button:hover {
    background: white;
    color: black;
    opacity: 100%;
}
[buffer](buffer.md).tall {
    height: calc(100vh - 50px);
}
.check-container {
    padding-right: 4px;
}
span.rm-page-ref {
    border-radius: 2px;
    padding-left: 1px;
    padding-right: 1px;
}
.content span.rm-page-ref {
    padding: 4px 1px 1px;
    /* required for fixing azo */
}
.center-proj {
    text-align: center;
}


/* Custom data tags */
span.rm-page-ref[data-tag="Inbox"] {
    background: [81D5ED](81D5ED.md);
    color: white;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Literature Notes"] {
    background: [E67E22](E67E22.md);
    color: white;
    padding: 3px 7px;
    font-weight: 500;
    line-height: 2em;
}

span.rm-page-ref[data-tag="Literature Notes"]:before {
    content: '📚 '
}

span.rm-page-ref[data-tag="Evergreens Notes"] {
    background: [25883d](25883d.md);
    color: white;
    padding: 3px 7px;
    font-weight: 500;
    line-height: 2em;
}

span.rm-page-ref[data-tag="Evergreens Notes"]:before {
    content: '🌲 '
}

span.rm-page-ref[data-tag="Permanent Notes"] {
    background: [9769FF](9769FF.md);
    color: [fff](fff.md);
    padding: 3px 8px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Permanent Notes"]:before {
    content: '♾️ '
}

span.rm-page-ref[data-tag="App"] {
    background: [099877](099877.md);
    color: [fff](fff.md);
    padding: 3px 3px;
    font-weight: 600;
    line-height: 1.4em;
}

span.rm-page-ref[data-tag="App"]:before {
    content: '🔨 '
}

span.rm-page-ref[data-tag="Idea"] {
    background: [E5E7E9](E5E7E9.md);
    color: [000](000.md);
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Idea"]:before {
    content: '💡 '
}

span.rm-page-ref[data-tag="Seedling Notes"] {
    background: [E5E7E9](E5E7E9.md);
    color: [000](000.md);
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Seedling Notes"]:before {
    content: '🌱 '
}

span.rm-page-ref[data-tag="Article"] {
    color: [ff913c](ff913c.md);
    padding: 3px 4px;
    font-weight: 700;
    line-height: 1.4em;
}

span.rm-page-ref[data-tag="Article"]:before {
    content: '📄 '
}

span.rm-page-ref[data-tag="python"] {
    color: [336686](336686.md);
    padding: 3px 4px;
    font-weight: 700;
    line-height: 1.4em;
}

span.rm-page-ref[data-tag="python"]:before {
    content: '🎭 '
}

span.rm-page-ref[data-tag="Reference Notes"] {
    background: [E5E7E9](E5E7E9.md);
    color: [000](000.md);
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Reference Notes"]:before {
    content: '🔗 '
}

span.rm-page-ref[data-tag="Budding Notes"] {
    background: [ADCB2A](ADCB2A.md);
    color: [fff](fff.md);
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Budding Notes"]:before {
    content: '🍏 '
}

span.rm-page-ref[data-tag="Fleeting Notes"] {
    background: [E5E7E9](E5E7E9.md);
    color: [000](000.md);
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Fleeting Notes"]:before {
    content: '💭 '
}

span.rm-page-ref[data-tag="Book"] {
    background: [E5E7E9](E5E7E9.md);
    color: [fff](fff.md);
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Book"]:before {
    content: '📖 '
}

span.rm-page-ref[data-tag="Card"] {
    background: [4CAF50](4CAF50.md);
    color: [fff](fff.md);
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Card"]:before {
    content: '🧩 '
}
```

# Backlinks
## [阅读书单接龙🐲](阅读书单接龙🐲.md)
- [@nightcat](@nightcat.md)

