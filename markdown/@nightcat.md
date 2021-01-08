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
    border: 0.5px solid #e4e9ec;
    border-radius: 5px;
    
}

.rm-query .rm-query-title {
    background-color: #f7f8f8;
    padding: 0.8em;
    color: #d1dbe2;
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

#block-input {
    background: black;
}

.roam-body #block-input > span > div {
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

#right-sidebar > div {
    background-color: #f7f8fa;
    border-left: 1px solid #e9ebef;
}
.rm-page-ref-brackets {
    display: none;
}
.controls .simple-bullet-outer .simple-bullet-inner {
    background-color: #e5e9f2;
}


/* 大纲辅助线 */
.block-border-left {
    margin-left: 5px!important;
    border-radius: 0;
    padding: 0 !important;
    border-color: #C7CEDB !important;
}
div.roam-block-container:hover > div:nth-child(2) > .roam-block-container{
    border-left-style:solid;
    border-left-color:#105EB391!important;
    transition:border-left-color 0.5s ease-in-out;
    box-shadow:0px 0px 0px 0px rgb(224,215,215);
    transition:box-shadow 0.5s;
}

.kanban-board {
    background-color: #fff;
}
.kanban-card {
    background-color: white;
    margin: 8px;
    box-shadow: 0px 1px 2px #9EB3C0;
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
    background-color: #E4EDF2;
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
    border-bottom: 1px solid #0d6da5;
    cursor: alias;
    padding-left: 0px;
    /* RTB add: align to left */
}
.rm-block-ref:hover {
    background-color: #b3d7ff;
    border-radius: 8px;
}




.checkmark {
    background: #fff;
}
.check-container input:checked ~ .checkmark {
    background: #33bdea;
}
.check-container input:checked ~ .checkmark:after {
    border-color: #fff;
}
.rm-reference-item {
    margin-top: 8px;
    border-radius: 6px;
    border: 1px solid #e4e9ee;
    margin-right: 8px;
    flex: 1 1 100%;
    word-break: break-word;
    background-color: #f7f9fb;
    padding: 8px;
}

.rm-level2 {
    font-size: 1.5em;
}
.rm-level3 {
    color: #939aae;
    font-weight: 400;
    font-size: 1.3em;
}
.rm-page-ref {
    color: #AF601A;
}
.rm-page-ref-link-color {
    color: #FF9800;
    font-weight: 600;
}
a {
    color: #673AB7;
}
.intercom-app,
.intercom-launcher-frame,
#intercom-container {
    display: none;
}
.roam-body .roam-app .roam-sidebar-container {
    background-color: white;
    border-right: 1px #eee solid;
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
#buffer.tall {
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
    background: #81D5ED;
    color: white;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Literature Notes"] {
    background: #E67E22;
    color: white;
    padding: 3px 7px;
    font-weight: 500;
    line-height: 2em;
}

span.rm-page-ref[data-tag="Literature Notes"]:before {
    content: '📚 '
}

span.rm-page-ref[data-tag="Evergreens Notes"] {
    background: #25883d;
    color: white;
    padding: 3px 7px;
    font-weight: 500;
    line-height: 2em;
}

span.rm-page-ref[data-tag="Evergreens Notes"]:before {
    content: '🌲 '
}

span.rm-page-ref[data-tag="Permanent Notes"] {
    background: #9769FF;
    color: #fff;
    padding: 3px 8px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Permanent Notes"]:before {
    content: '♾️ '
}

span.rm-page-ref[data-tag="App"] {
    background: #099877;
    color: #fff;
    padding: 3px 3px;
    font-weight: 600;
    line-height: 1.4em;
}

span.rm-page-ref[data-tag="App"]:before {
    content: '🔨 '
}

span.rm-page-ref[data-tag="Idea"] {
    background: #E5E7E9;
    color: #000;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Idea"]:before {
    content: '💡 '
}

span.rm-page-ref[data-tag="Seedling Notes"] {
    background: #E5E7E9;
    color: #000;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Seedling Notes"]:before {
    content: '🌱 '
}

span.rm-page-ref[data-tag="Article"] {
    color: #ff913c;
    padding: 3px 4px;
    font-weight: 700;
    line-height: 1.4em;
}

span.rm-page-ref[data-tag="Article"]:before {
    content: '📄 '
}

span.rm-page-ref[data-tag="python"] {
    color: #336686;
    padding: 3px 4px;
    font-weight: 700;
    line-height: 1.4em;
}

span.rm-page-ref[data-tag="python"]:before {
    content: '🎭 '
}

span.rm-page-ref[data-tag="Reference Notes"] {
    background: #E5E7E9;
    color: #000;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Reference Notes"]:before {
    content: '🔗 '
}

span.rm-page-ref[data-tag="Budding Notes"] {
    background: #ADCB2A;
    color: #fff;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Budding Notes"]:before {
    content: '🍏 '
}

span.rm-page-ref[data-tag="Fleeting Notes"] {
    background: #E5E7E9;
    color: #000;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Fleeting Notes"]:before {
    content: '💭 '
}

span.rm-page-ref[data-tag="Book"] {
    background: #E5E7E9;
    color: #fff;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Book"]:before {
    content: '📖 '
}

span.rm-page-ref[data-tag="Card"] {
    background: #4CAF50;
    color: #fff;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Card"]:before {
    content: '🧩 '
}
```
