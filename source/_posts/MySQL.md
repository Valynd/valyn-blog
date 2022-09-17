---
title: MySQL回顾
date: 2022-09-10 12:51:23
tags: MySQL
categories:
- Web后端
cover: https://pic1.zhimg.com/80/v2-a4ab7117cba24c41b826271bfd78fb6c_1440w.jpg?source=1940ef5c
---

<h2>MySQL是一个关系型数据库管理系统，由瑞典MySQL AB 公司开发，属于 Oracle 旗下产品。MySQL 是最流行的关系型数据库管理系
统之一，在 WEB 应用方面，MySQL是最好的 RDBMS (Relational Database Management System，关系数据库管理系统) 应用软
件之一。</h2>


<!doctype html>
<html>
<head>
<meta charset='UTF-8'><meta name='viewport' content='width=device-width initial-scale=1'>

<link href='https://fonts.loli.net/css?family=PT+Serif:400,400italic,700,700italic&subset=latin,cyrillic-ext,cyrillic,latin-ext' rel='stylesheet' type='text/css' /><style type='text/css'>html {overflow-x: initial !important;}:root { --bg-color:#ffffff; --text-color:#333333; --select-text-bg-color:#B5D6FC; --select-text-font-color:auto; --monospace:"Lucida Console",Consolas,"Courier",monospace; --title-bar-height:20px; }
.mac-os-11 { --title-bar-height:28px; }
html { font-size: 14px; background-color: var(--bg-color); color: var(--text-color); font-family: "Helvetica Neue", Helvetica, Arial, sans-serif; -webkit-font-smoothing: antialiased; }
body { margin: 0px; padding: 0px; height: auto; inset: 0px; font-size: 1rem; line-height: 1.42857; overflow-x: hidden; background: inherit; tab-size: 4; }
iframe { margin: auto; }
a.url { word-break: break-all; }
a:active, a:hover { outline: 0px; }
.in-text-selection, ::selection { text-shadow: none; background: var(--select-text-bg-color); color: var(--select-text-font-color); }
#write { margin: 0px auto; height: auto; width: inherit; word-break: normal; overflow-wrap: break-word; position: relative; white-space: normal; overflow-x: visible; padding-top: 36px; }
#write.first-line-indent p { text-indent: 2em; }
#write.first-line-indent li p, #write.first-line-indent p * { text-indent: 0px; }
#write.first-line-indent li { margin-left: 2em; }
.for-image #write { padding-left: 8px; padding-right: 8px; }
body.typora-export { padding-left: 30px; padding-right: 30px; }
.typora-export .footnote-line, .typora-export li, .typora-export p { white-space: pre-wrap; }
.typora-export .task-list-item input { pointer-events: none; }
@media screen and (max-width: 500px) {
  body.typora-export { padding-left: 0px; padding-right: 0px; }
  #write { padding-left: 20px; padding-right: 20px; }
  .CodeMirror-sizer { margin-left: 0px !important; }
  .CodeMirror-gutters { display: none !important; }
}
#write li > figure:last-child { margin-bottom: 0.5rem; }
#write ol, #write ul { position: relative; }
img { max-width: 100%; vertical-align: middle; image-orientation: from-image; }
button, input, select, textarea { color: inherit; font: inherit; }
input[type="checkbox"], input[type="radio"] { line-height: normal; padding: 0px; }
*, ::after, ::before { box-sizing: border-box; }
#write h1, #write h2, #write h3, #write h4, #write h5, #write h6, #write p, #write pre { width: inherit; }
#write h1, #write h2, #write h3, #write h4, #write h5, #write h6, #write p { position: relative; }
p { line-height: inherit; }
h1, h2, h3, h4, h5, h6 { break-after: avoid-page; break-inside: avoid; orphans: 4; }
p { orphans: 4; }
h1 { font-size: 2rem; }
h2 { font-size: 1.8rem; }
h3 { font-size: 1.6rem; }
h4 { font-size: 1.4rem; }
h5 { font-size: 1.2rem; }
h6 { font-size: 1rem; }
.md-math-block, .md-rawblock, h1, h2, h3, h4, h5, h6, p { margin-top: 1rem; margin-bottom: 1rem; }
.hidden { display: none; }
.md-blockmeta { color: rgb(204, 204, 204); font-weight: 700; font-style: italic; }
a { cursor: pointer; }
sup.md-footnote { padding: 2px 4px; background-color: rgba(238, 238, 238, 0.7); color: rgb(85, 85, 85); border-radius: 4px; cursor: pointer; }
sup.md-footnote a, sup.md-footnote a:hover { color: inherit; text-transform: inherit; text-decoration: inherit; }
#write input[type="checkbox"] { cursor: pointer; width: inherit; height: inherit; }
figure { overflow-x: auto; margin: 1.2em 0px; max-width: calc(100% + 16px); padding: 0px; }
figure > table { margin: 0px; }
tr { break-inside: avoid; break-after: auto; }
thead { display: table-header-group; }
table { border-collapse: collapse; border-spacing: 0px; width: 100%; overflow: auto; break-inside: auto; text-align: left; }
table.md-table td { min-width: 32px; }
.CodeMirror-gutters { border-right: 0px; background-color: inherit; }
.CodeMirror-linenumber { user-select: none; }
.CodeMirror { text-align: left; }
.CodeMirror-placeholder { opacity: 0.3; }
.CodeMirror pre { padding: 0px 4px; }
.CodeMirror-lines { padding: 0px; }
div.hr:focus { cursor: none; }
#write pre { white-space: pre-wrap; }
#write.fences-no-line-wrapping pre { white-space: pre; }
#write pre.ty-contain-cm { white-space: normal; }
.CodeMirror-gutters { margin-right: 4px; }
.md-fences { font-size: 0.9rem; display: block; break-inside: avoid; text-align: left; overflow: visible; white-space: pre; background: inherit; position: relative !important; }
.md-fences-adv-panel { width: 100%; margin-top: 10px; text-align: center; padding-top: 0px; padding-bottom: 8px; overflow-x: auto; }
#write .md-fences.mock-cm { white-space: pre-wrap; }
.md-fences.md-fences-with-lineno { padding-left: 0px; }
#write.fences-no-line-wrapping .md-fences.mock-cm { white-space: pre; overflow-x: auto; }
.md-fences.mock-cm.md-fences-with-lineno { padding-left: 8px; }
.CodeMirror-line, twitterwidget { break-inside: avoid; }
.footnotes { opacity: 0.8; font-size: 0.9rem; margin-top: 1em; margin-bottom: 1em; }
.footnotes + .footnotes { margin-top: 0px; }
.md-reset { margin: 0px; padding: 0px; border: 0px; outline: 0px; vertical-align: top; background: 0px 0px; text-decoration: none; text-shadow: none; float: none; position: static; width: auto; height: auto; white-space: nowrap; cursor: inherit; -webkit-tap-highlight-color: transparent; line-height: normal; font-weight: 400; text-align: left; box-sizing: content-box; direction: ltr; }
li div { padding-top: 0px; }
blockquote { margin: 1rem 0px; }
li .mathjax-block, li p { margin: 0.5rem 0px; }
li blockquote { margin: 1rem 0px; }
li { margin: 0px; position: relative; }
blockquote > :last-child { margin-bottom: 0px; }
blockquote > :first-child, li > :first-child { margin-top: 0px; }
.footnotes-area { color: rgb(136, 136, 136); margin-top: 0.714rem; padding-bottom: 0.143rem; white-space: normal; }
#write .footnote-line { white-space: pre-wrap; }
@media print {
  body, html { border: 1px solid transparent; height: 99%; break-after: avoid; break-before: avoid; font-variant-ligatures: no-common-ligatures; }
  #write { margin-top: 0px; padding-top: 0px; border-color: transparent !important; }
  .typora-export * { -webkit-print-color-adjust: exact; }
  .typora-export #write { break-after: avoid; }
  .typora-export #write::after { height: 0px; }
  .is-mac table { break-inside: avoid; }
  .typora-export-show-outline .typora-export-sidebar { display: none; }
}
.footnote-line { margin-top: 0.714em; font-size: 0.7em; }
a img, img a { cursor: pointer; }
pre.md-meta-block { font-size: 0.8rem; min-height: 0.8rem; white-space: pre-wrap; background: rgb(204, 204, 204); display: block; overflow-x: hidden; }
p > .md-image:only-child:not(.md-img-error) img, p > img:only-child { display: block; margin: auto; }
#write.first-line-indent p > .md-image:only-child:not(.md-img-error) img { left: -2em; position: relative; }
p > .md-image:only-child { display: inline-block; width: 100%; }
#write .MathJax_Display { margin: 0.8em 0px 0px; }
.md-math-block { width: 100%; }
.md-math-block:not(:empty)::after { display: none; }
.MathJax_ref { fill: currentcolor; }
[contenteditable="true"]:active, [contenteditable="true"]:focus, [contenteditable="false"]:active, [contenteditable="false"]:focus { outline: 0px; box-shadow: none; }
.md-task-list-item { position: relative; list-style-type: none; }
.task-list-item.md-task-list-item { padding-left: 0px; }
.md-task-list-item > input { position: absolute; top: 0px; left: 0px; margin-left: -1.2em; margin-top: calc(1em - 10px); border: none; }
.math { font-size: 1rem; }
.md-toc { min-height: 3.58rem; position: relative; font-size: 0.9rem; border-radius: 10px; }
.md-toc-content { position: relative; margin-left: 0px; }
.md-toc-content::after, .md-toc::after { display: none; }
.md-toc-item { display: block; color: rgb(65, 131, 196); }
.md-toc-item a { text-decoration: none; }
.md-toc-inner:hover { text-decoration: underline; }
.md-toc-inner { display: inline-block; cursor: pointer; }
.md-toc-h1 .md-toc-inner { margin-left: 0px; font-weight: 700; }
.md-toc-h2 .md-toc-inner { margin-left: 2em; }
.md-toc-h3 .md-toc-inner { margin-left: 4em; }
.md-toc-h4 .md-toc-inner { margin-left: 6em; }
.md-toc-h5 .md-toc-inner { margin-left: 8em; }
.md-toc-h6 .md-toc-inner { margin-left: 10em; }
@media screen and (max-width: 48em) {
  .md-toc-h3 .md-toc-inner { margin-left: 3.5em; }
  .md-toc-h4 .md-toc-inner { margin-left: 5em; }
  .md-toc-h5 .md-toc-inner { margin-left: 6.5em; }
  .md-toc-h6 .md-toc-inner { margin-left: 8em; }
}
a.md-toc-inner { font-size: inherit; font-style: inherit; font-weight: inherit; line-height: inherit; }
.footnote-line a:not(.reversefootnote) { color: inherit; }
.md-attr { display: none; }
.md-fn-count::after { content: "."; }
code, pre, samp, tt { font-family: var(--monospace); }
kbd { margin: 0px 0.1em; padding: 0.1em 0.6em; font-size: 0.8em; color: rgb(36, 39, 41); background: rgb(255, 255, 255); border: 1px solid rgb(173, 179, 185); border-radius: 3px; box-shadow: rgba(12, 13, 14, 0.2) 0px 1px 0px, rgb(255, 255, 255) 0px 0px 0px 2px inset; white-space: nowrap; vertical-align: middle; }
.md-comment { color: rgb(162, 127, 3); opacity: 0.6; font-family: var(--monospace); }
code { text-align: left; vertical-align: initial; }
a.md-print-anchor { white-space: pre !important; border-width: initial !important; border-style: none !important; border-color: initial !important; display: inline-block !important; position: absolute !important; width: 1px !important; right: 0px !important; outline: 0px !important; background: 0px 0px !important; text-decoration: initial !important; text-shadow: initial !important; }
.os-windows.monocolor-emoji .md-emoji { font-family: "Segoe UI Symbol", sans-serif; }
.md-diagram-panel > svg { max-width: 100%; }
[lang="flow"] svg, [lang="mermaid"] svg { max-width: 100%; height: auto; }
[lang="mermaid"] .node text { font-size: 1rem; }
table tr th { border-bottom: 0px; }
video { max-width: 100%; display: block; margin: 0px auto; }
iframe { max-width: 100%; width: 100%; border: none; }
.highlight td, .highlight tr { border: 0px; }
mark { background: rgb(255, 255, 0); color: rgb(0, 0, 0); }
.md-html-inline .md-plain, .md-html-inline strong, mark .md-inline-math, mark strong { color: inherit; }
.md-expand mark .md-meta { opacity: 0.3 !important; }
mark .md-meta { color: rgb(0, 0, 0); }
@media print {
  .typora-export h1, .typora-export h2, .typora-export h3, .typora-export h4, .typora-export h5, .typora-export h6 { break-inside: avoid; }
}
.md-diagram-panel .messageText { stroke: none !important; }
.md-diagram-panel .start-state { fill: var(--node-fill); }
.md-diagram-panel .edgeLabel rect { opacity: 1 !important; }
.md-fences.md-fences-math { font-size: 1em; }
.md-fences-advanced:not(.md-focus) { padding: 0px; white-space: nowrap; border: 0px; }
.md-fences-advanced:not(.md-focus) { background: inherit; }
.typora-export-show-outline .typora-export-content { max-width: 1440px; margin: auto; display: flex; flex-direction: row; }
.typora-export-sidebar { width: 300px; font-size: 0.8rem; margin-top: 80px; margin-right: 18px; }
.typora-export-show-outline #write { --webkit-flex:2; flex: 2 1 0%; }
.typora-export-sidebar .outline-content { position: fixed; top: 0px; max-height: 100%; overflow: hidden auto; padding-bottom: 30px; padding-top: 60px; width: 300px; }
@media screen and (max-width: 1024px) {
  .typora-export-sidebar, .typora-export-sidebar .outline-content { width: 240px; }
}
@media screen and (max-width: 800px) {
  .typora-export-sidebar { display: none; }
}
.outline-content li, .outline-content ul { margin-left: 0px; margin-right: 0px; padding-left: 0px; padding-right: 0px; list-style: none; }
.outline-content ul { margin-top: 0px; margin-bottom: 0px; }
.outline-content strong { font-weight: 400; }
.outline-expander { width: 1rem; height: 1.42857rem; position: relative; display: table-cell; vertical-align: middle; cursor: pointer; padding-left: 4px; }
.outline-expander::before { content: ""; position: relative; font-family: Ionicons; display: inline-block; font-size: 8px; vertical-align: middle; }
.outline-item { padding-top: 3px; padding-bottom: 3px; cursor: pointer; }
.outline-expander:hover::before { content: ""; }
.outline-h1 > .outline-item { padding-left: 0px; }
.outline-h2 > .outline-item { padding-left: 1em; }
.outline-h3 > .outline-item { padding-left: 2em; }
.outline-h4 > .outline-item { padding-left: 3em; }
.outline-h5 > .outline-item { padding-left: 4em; }
.outline-h6 > .outline-item { padding-left: 5em; }
.outline-label { cursor: pointer; display: table-cell; vertical-align: middle; text-decoration: none; color: inherit; }
.outline-label:hover { text-decoration: underline; }
.outline-item:hover { border-color: rgb(245, 245, 245); background-color: var(--item-hover-bg-color); }
.outline-item:hover { margin-left: -28px; margin-right: -28px; border-left: 28px solid transparent; border-right: 28px solid transparent; }
.outline-item-single .outline-expander::before, .outline-item-single .outline-expander:hover::before { display: none; }
.outline-item-open > .outline-item > .outline-expander::before { content: ""; }
.outline-children { display: none; }
.info-panel-tab-wrapper { display: none; }
.outline-item-open > .outline-children { display: block; }
.typora-export .outline-item { padding-top: 1px; padding-bottom: 1px; }
.typora-export .outline-item:hover { margin-right: -8px; border-right: 8px solid transparent; }
.typora-export .outline-expander::before { content: "+"; font-family: inherit; top: -1px; }
.typora-export .outline-expander:hover::before, .typora-export .outline-item-open > .outline-item > .outline-expander::before { content: "−"; }
.typora-export-collapse-outline .outline-children { display: none; }
.typora-export-collapse-outline .outline-item-open > .outline-children, .typora-export-no-collapse-outline .outline-children { display: block; }
.typora-export-no-collapse-outline .outline-expander::before { content: "" !important; }
.typora-export-show-outline .outline-item-active > .outline-item .outline-label { font-weight: 700; }
.md-inline-math-container mjx-container { zoom: 0.95; }


.CodeMirror { height: auto; }
.CodeMirror.cm-s-inner { background: inherit; }
.CodeMirror-scroll { overflow: auto hidden; z-index: 3; }
.CodeMirror-gutter-filler, .CodeMirror-scrollbar-filler { background-color: rgb(255, 255, 255); }
.CodeMirror-gutters { border-right: 1px solid rgb(221, 221, 221); background: inherit; white-space: nowrap; }
.CodeMirror-linenumber { padding: 0px 3px 0px 5px; text-align: right; color: rgb(153, 153, 153); }
.cm-s-inner .cm-keyword { color: rgb(119, 0, 136); }
.cm-s-inner .cm-atom, .cm-s-inner.cm-atom { color: rgb(34, 17, 153); }
.cm-s-inner .cm-number { color: rgb(17, 102, 68); }
.cm-s-inner .cm-def { color: rgb(0, 0, 255); }
.cm-s-inner .cm-variable { color: rgb(0, 0, 0); }
.cm-s-inner .cm-variable-2 { color: rgb(0, 85, 170); }
.cm-s-inner .cm-variable-3 { color: rgb(0, 136, 85); }
.cm-s-inner .cm-string { color: rgb(170, 17, 17); }
.cm-s-inner .cm-property { color: rgb(0, 0, 0); }
.cm-s-inner .cm-operator { color: rgb(152, 26, 26); }
.cm-s-inner .cm-comment, .cm-s-inner.cm-comment { color: rgb(170, 85, 0); }
.cm-s-inner .cm-string-2 { color: rgb(255, 85, 0); }
.cm-s-inner .cm-meta { color: rgb(85, 85, 85); }
.cm-s-inner .cm-qualifier { color: rgb(85, 85, 85); }
.cm-s-inner .cm-builtin { color: rgb(51, 0, 170); }
.cm-s-inner .cm-bracket { color: rgb(153, 153, 119); }
.cm-s-inner .cm-tag { color: rgb(17, 119, 0); }
.cm-s-inner .cm-attribute { color: rgb(0, 0, 204); }
.cm-s-inner .cm-header, .cm-s-inner.cm-header { color: rgb(0, 0, 255); }
.cm-s-inner .cm-quote, .cm-s-inner.cm-quote { color: rgb(0, 153, 0); }
.cm-s-inner .cm-hr, .cm-s-inner.cm-hr { color: rgb(153, 153, 153); }
.cm-s-inner .cm-link, .cm-s-inner.cm-link { color: rgb(0, 0, 204); }
.cm-negative { color: rgb(221, 68, 68); }
.cm-positive { color: rgb(34, 153, 34); }
.cm-header, .cm-strong { font-weight: 700; }
.cm-del { text-decoration: line-through; }
.cm-em { font-style: italic; }
.cm-link { text-decoration: underline; }
.cm-error { color: red; }
.cm-invalidchar { color: red; }
.cm-constant { color: rgb(38, 139, 210); }
.cm-defined { color: rgb(181, 137, 0); }
div.CodeMirror span.CodeMirror-matchingbracket { color: rgb(0, 255, 0); }
div.CodeMirror span.CodeMirror-nonmatchingbracket { color: rgb(255, 34, 34); }
.cm-s-inner .CodeMirror-activeline-background { background: inherit; }
.CodeMirror { position: relative; overflow: hidden; }
.CodeMirror-scroll { height: 100%; outline: 0px; position: relative; box-sizing: content-box; background: inherit; }
.CodeMirror-sizer { position: relative; }
.CodeMirror-gutter-filler, .CodeMirror-hscrollbar, .CodeMirror-scrollbar-filler, .CodeMirror-vscrollbar { position: absolute; z-index: 6; display: none; outline: 0px; }
.CodeMirror-vscrollbar { right: 0px; top: 0px; overflow: hidden; }
.CodeMirror-hscrollbar { bottom: 0px; left: 0px; overflow: auto hidden; }
.CodeMirror-scrollbar-filler { right: 0px; bottom: 0px; }
.CodeMirror-gutter-filler { left: 0px; bottom: 0px; }
.CodeMirror-gutters { position: absolute; left: 0px; top: 0px; padding-bottom: 10px; z-index: 3; overflow-y: hidden; }
.CodeMirror-gutter { white-space: normal; height: 100%; box-sizing: content-box; padding-bottom: 30px; margin-bottom: -32px; display: inline-block; }
.CodeMirror-gutter-wrapper { position: absolute; z-index: 4; background: 0px 0px !important; border: none !important; }
.CodeMirror-gutter-background { position: absolute; top: 0px; bottom: 0px; z-index: 4; }
.CodeMirror-gutter-elt { position: absolute; cursor: default; z-index: 4; }
.CodeMirror-lines { cursor: text; }
.CodeMirror pre { border-radius: 0px; border-width: 0px; background: 0px 0px; font-family: inherit; font-size: inherit; margin: 0px; white-space: pre; overflow-wrap: normal; color: inherit; z-index: 2; position: relative; overflow: visible; }
.CodeMirror-wrap pre { overflow-wrap: break-word; white-space: pre-wrap; word-break: normal; }
.CodeMirror-code pre { border-right: 30px solid transparent; width: fit-content; }
.CodeMirror-wrap .CodeMirror-code pre { border-right: none; width: auto; }
.CodeMirror-linebackground { position: absolute; inset: 0px; z-index: 0; }
.CodeMirror-linewidget { position: relative; z-index: 2; overflow: auto; }
.CodeMirror-wrap .CodeMirror-scroll { overflow-x: hidden; }
.CodeMirror-measure { position: absolute; width: 100%; height: 0px; overflow: hidden; visibility: hidden; }
.CodeMirror-measure pre { position: static; }
.CodeMirror div.CodeMirror-cursor { position: absolute; visibility: hidden; border-right: none; width: 0px; }
.CodeMirror div.CodeMirror-cursor { visibility: hidden; }
.CodeMirror-focused div.CodeMirror-cursor { visibility: inherit; }
.cm-searching { background: rgba(255, 255, 0, 0.4); }
span.cm-underlined { text-decoration: underline; }
span.cm-strikethrough { text-decoration: line-through; }
.cm-tw-syntaxerror { color: rgb(255, 255, 255); background-color: rgb(153, 0, 0); }
.cm-tw-deleted { text-decoration: line-through; }
.cm-tw-header5 { font-weight: 700; }
.cm-tw-listitem:first-child { padding-left: 10px; }
.cm-tw-box { border-style: solid; border-right-width: 1px; border-bottom-width: 1px; border-left-width: 1px; border-color: inherit; border-top-width: 0px !important; }
.cm-tw-underline { text-decoration: underline; }
@media print {
.CodeMirror div.CodeMirror-cursor { visibility: hidden; }
}


/* meyer reset -- http://meyerweb.com/eric/tools/css/reset/ , v2.0 | 20110126 | License: none (public domain) */

@include-when-export url(https://fonts.loli.net/css?family=PT+Serif:400,400italic,700,700italic&subset=latin,cyrillic-ext,cyrillic,latin-ext);

/* =========== */

/* pt-serif-regular - latin */
/* pt-serif-italic - latin */
/* pt-serif-700 - latin */
/* pt-serif-700italic - latin */
:root {
--active-file-bg-color: #dadada;
--active-file-bg-color: rgba(32, 43, 51, 0.63);
--active-file-text-color: white;
--bg-color: #f3f2ee;
--text-color: #1f0909;
--control-text-color: #444;
--rawblock-edit-panel-bd: #e5e5e5;

	--select-text-bg-color: rgba(32, 43, 51, 0.63);
--select-text-font-color: white;
}

pre {
--select-text-bg-color: #36284e;
--select-text-font-color: #fff;
}

html {
font-size: 16px;
-webkit-font-smoothing: antialiased;
}

html, body {
background-color: #f3f2ee;
font-family: "PT Serif", 'Times New Roman', Times, serif;
color: #1f0909;
line-height: 1.5em;
}

/*#write {
overflow-x: auto;
max-width: initial;
padding-left: calc(50% - 17em);
padding-right: calc(50% - 17em);
}

@media (max-width: 36em) {
#write {
padding-left: 1em;
padding-right: 1em;
}
}*/

#write {
max-width: 40em;
}

@media only screen and (min-width: 1400px) {
#write {
max-width: 914px;
}
}

ol li {
list-style-type: decimal;
list-style-position: outside;
}
ul li {
list-style-type: disc;
list-style-position: outside;
}

ol,
ul {
list-style: none;
}

blockquote,
q {
quotes: none;
}
blockquote:before,
blockquote:after,
q:before,
q:after {
content: '';
content: none;
}
table {
border-collapse: collapse;
border-spacing: 0;
}
/* styles */

/* ====== */

/* headings */

h1,
h2,
h3,
h4,
h5,
h6 {
font-weight: bold;
}
h1 {
font-size: 1.875em;
/*30 / 16*/
line-height: 1.6em;
/* 48 / 30*/
margin-top: 2em;
}
h2,
h3 {
font-size: 1.3125em;
/*21 / 16*/
line-height: 1.15;
/*24 / 21*/
margin-top: 2.285714em;
/*48 / 21*/
margin-bottom: 1.15em;
/*24 / 21*/
}
h3 {
font-weight: normal;
}
h4 {
font-size: 1.125em;
/*18 / 16*/
margin-top: 2.67em;
/*48 / 18*/
}
h5,
h6 {
font-size: 1em;
/*16*/
}
h1 {
border-bottom: 1px solid;
margin-bottom: 1.875em;
padding-bottom: 0.8125em;
}
/* links */

a {
text-decoration: none;
color: #065588;
}
a:hover,
a:active {
text-decoration: underline;
}
/* block spacing */

p,
blockquote,
.md-fences {
margin-bottom: 1.5em;
}
h1,
h2,
h3,
h4,
h5,
h6 {
margin-bottom: 1.5em;
}
/* blockquote */

blockquote {
font-style: italic;
border-left: 5px solid;
margin-left: 2em;
padding-left: 1em;
}
/* lists */

ul,
ol {
margin: 0 0 1.5em 1.5em;
}
/* tables */
.md-meta,.md-before, .md-after {
color:#999;
}

table {
margin-bottom: 1.5em;
/*24 / 16*/
font-size: 1em;
/* width: 100%; */
}
thead th,
tfoot th {
padding: .25em .25em .25em .4em;
text-transform: uppercase;
}
th {
text-align: left;
}
td {
vertical-align: top;
padding: .25em .25em .25em .4em;
}

code,
.md-fences {
background-color: #dadada;
}

code {
padding-left: 2px;
padding-right: 2px;
}

.md-fences {
margin-left: 2em;
margin-bottom: 3em;
padding-left: 1ch;
padding-right: 1ch;
}

pre,
code,
tt {
font-size: .875em;
line-height: 1.714285em;
}
/* some fixes */

h1 {
line-height: 1.3em;
font-weight: normal;
margin-bottom: 0.5em;
}

p + ul,
p + ol{
margin-top: .5em;
}

h3 + ul,
h4 + ul,
h5 + ul,
h6 + ul,
h3 + ol,
h4 + ol,
h5 + ol,
h6 + ol {
margin-top: .5em;
}

li > ul,
li > ol {
margin-top: inherit;
margin-bottom: 0;
}

li ol>li {
list-style-type: lower-alpha;
}

li li ol>li{
list-style-type: lower-roman;
}

h2,
h3 {
margin-bottom: .75em;
}
hr {
border-top: none;
border-right: none;
border-bottom: 1px solid;
border-left: none;
}
h1 {
border-color: #c5c5c5;
}
blockquote {
border-color: #bababa;
color: #656565;
}

blockquote ul,
blockquote ol {
margin-left:0;
}

.ty-table-edit {
background-color: transparent;
}
thead {
background-color: #dadada;
}
tr:nth-child(even) {
background: #e8e7e7;
}
hr {
border-color: #c5c5c5;
}
.task-list{
padding-left: 1rem;
}

.md-task-list-item {
padding-left: 1.5rem;
list-style-type: none;
}

.md-task-list-item > input:before {
content: '\221A';
display: inline-block;
width: 1.25rem;
height: 1.6rem;
vertical-align: middle;
text-align: center;
color: #ddd;
background-color: #F3F2EE;
}

.md-task-list-item > input:checked:before,
.md-task-list-item > input[checked]:before{
color: inherit;
}

#write pre.md-meta-block {
min-height: 1.875rem;
color: #555;
border: 0px;
background: transparent;
margin-top: -4px;
margin-left: 1em;
margin-top: 1em;
}

.md-image>.md-meta {
color: #9B5146;
}

.md-image>.md-meta{
font-family: Menlo, 'Ubuntu Mono', Consolas, 'Courier New', 'Microsoft Yahei', 'Hiragino Sans GB', 'WenQuanYi Micro Hei', serif;
}


#write>h3.md-focus:before{
left: -1.5rem;
color:#999;
border-color:#999;
}
#write>h4.md-focus:before{
left: -1.5rem;
top: .25rem;
color:#999;
border-color:#999;
}
#write>h5.md-focus:before{
left: -1.5rem;
top: .0.3125rem;
color:#999;
border-color:#999;
}
#write>h6.md-focus:before{
left: -1.5rem;
top: 0.3125rem;
color:#999;
border-color:#999;
}

.md-toc:focus .md-toc-content{
margin-top: 19px;
}

.md-toc-content:empty:before{
color: #065588;
}
.md-toc-item {
color: #065588;
}
#write div.md-toc-tooltip {
background-color: #f3f2ee;
}

#typora-sidebar {
background-color: #f3f2ee;
-webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.375);
box-shadow: 0 6px 12px rgba(0, 0, 0, 0.375);
}

.pin-outline #typora-sidebar {
background: inherit;
box-shadow: none;
border-right: 1px dashed;
}

.pin-outline #typora-sidebar:hover .outline-title-wrapper {
border-left:1px dashed;
}

.outline-item:hover {
background-color: #dadada;
border-left: 28px solid #dadada;
border-right: 18px solid #dadada;
}

.typora-node .outline-item:hover {
border-right: 28px solid #dadada;
}

.outline-expander:before {
content: "\f0da";
font-family: FontAwesome;
font-size:14px;
top: 1px;
}

.outline-expander:hover:before,
.outline-item-open>.outline-item>.outline-expander:before {
content: "\f0d7";
}

.modal-content {
background-color: #f3f2ee;
}

.auto-suggest-container ul li {
list-style-type: none;
}

/** UI for electron */

.megamenu-menu,
#top-titlebar, #top-titlebar *,
.megamenu-content {
background: #f3f2ee;
color: #1f0909;
}

.megamenu-menu-header {
border-bottom: 1px dashed #202B33;
}

.megamenu-menu {
box-shadow: none;
border-right: 1px dashed;
}

header, .context-menu, .megamenu-content, footer {
font-family: "PT Serif", 'Times New Roman', Times, serif;
color: #1f0909;
}

#megamenu-back-btn {
color: #1f0909;
border-color: #1f0909;
}

.megamenu-menu-header #megamenu-menu-header-title:before {
color: #1f0909;
}

.megamenu-menu-list li a:hover, .megamenu-menu-list li a.active {
color: inherit;
background-color: #e8e7df;
}

.long-btn:hover {
background-color: #e8e7df;
}

#recent-file-panel tbody tr:nth-child(2n-1) {
background-color: transparent !important;
}

.megamenu-menu-panel tbody tr:hover td:nth-child(2) {
color: inherit;
}

.megamenu-menu-panel .btn {
background-color: #D2D1D1;
}

.btn-default {
background-color: transparent;
}

.typora-sourceview-on #toggle-sourceview-btn,
.ty-show-word-count #footer-word-count {
background: #c7c5c5;
}

#typora-quick-open {
background-color: inherit;
}

.md-diagram-panel {
margin-top: 8px;
}

.file-list-item-file-name {
font-weight: initial;
}

.file-list-item-summary {
opacity: 1;
}

.file-list-item {
color: #777;
}

.file-list-item.active {
background-color: inherit;
color: black;
}

.ty-side-sort-btn.active {
background-color: inherit;
}

.file-list-item.active .file-list-item-file-name  {
font-weight: bold;
}

.file-list-item{
opacity:1 !important;
}

.file-library-node.active>.file-node-background{
background-color: rgba(32, 43, 51, 0.63);
background-color: var(--active-file-bg-color);
}

.file-tree-node.active>.file-node-content{
color: white;
color: var(--active-file-text-color);
}

.md-task-list-item>input {
margin-left: -1.7em;
margin-top: calc(1rem - 12px);
-webkit-appearance: button;
}

input {
border: 1px solid #aaa;
}

.megamenu-menu-header #megamenu-menu-header-title,
.megamenu-menu-header:hover,
.megamenu-menu-header:focus {
color: inherit;
}

.dropdown-menu .divider {
border-color: #e5e5e5;
opacity: 1;
}

/* https://github.com/typora/typora-issues/issues/2046 */
.os-windows-7 strong,
.os-windows-7 strong  {
font-weight: 760;
}

.ty-preferences .btn-default {
background: transparent;
}

.ty-preferences .window-header {
border-bottom: 1px dashed #202B33;
box-shadow: none;
}

#sidebar-loading-template, #sidebar-loading-template.file-list-item {
color: #777;
}

.searchpanel-search-option-btn.active {
background: #777;
color: white;
}

.export-detail, .light .export-detail,
.light .export-item.active,
.light .export-items-list-control {
background: #e0e0e0;
border-radius: 2px;
font-weight: 700;
color: inherit
}


</style><title>MySQL基础回顾</title>
</head>
<body class='typora-export os-windows'><div class='typora-export-content'>
<div id='write'  class=''><h3 id='mysql基础回顾'><span>MySQL基础回顾</span></h3><h3 id='数据库概述'><span>数据库概述</span></h3><ol start='' ><li><p><span>数据库</span></p><ul><li><span>数据储存的仓库</span></li></ul></li><li><p><span>数据库管理系统</span></p><ul><li><span>操作和管理数据库的软件</span></li></ul></li><li><p><span>SQL</span></p><ul><li><span>操作关系型数据库的编程语言（一套标准）</span></li></ul></li></ol><h3 id='mysql数据库'><span>MySQL数据库</span></h3><ol start='' ><li><p><span>MySQL介绍</span></p><ul><li><span>关系型的数据库</span></li><li><span>由多张二维表组成的数据库</span></li></ul></li><li><p><span>SQL分类</span></p><figure><table><thead><tr><th style='text-align:center;' ><span>分类</span></th><th style='text-align:center;' ><span>全称</span></th><th style='text-align:center;' ><span>说明</span></th></tr></thead><tbody><tr><td style='text-align:center;' ><span>DDL</span></td><td style='text-align:center;' ><span>Data Definition Language</span></td><td style='text-align:center;' ><span>数据定义语言，用来定义数据库对象(数据库，表，字段)</span></td></tr><tr><td style='text-align:center;' ><span>DML</span></td><td style='text-align:center;' ><span>Data Manipulation Language</span></td><td style='text-align:center;' ><span>数据操作语言，用来对数据库表中的数据进行增删改</span></td></tr><tr><td style='text-align:center;' ><span>DQL</span></td><td style='text-align:center;' ><span>Data Query Language</span></td><td style='text-align:center;' ><span>数据查询语言，用来查询数据库中表的记录</span></td></tr><tr><td style='text-align:center;' ><span>DCL</span></td><td style='text-align:center;' ><span>Data Control Language</span></td><td style='text-align:center;' ><span>数据控制语言，用来创建数据库用户、控制数据库的访问权限</span></td></tr></tbody></table></figure></li></ol><h4 id='ddl数据库操作）'><span>DDL（数据库操作）</span></h4><ol start='' ><li><p><span>查询</span></p><ul><li><p><span>查询所有数据库</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">SHOW</span> <span class="cm-keyword">DATABASES</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 25px;"></div><div class="CodeMirror-gutters" style="display: none; height: 25px;"></div></div></div></pre></li><li><p><span>查询当前数据库</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">SELECT</span> <span class="cm-keyword">DATABASE</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 25px;"></div><div class="CodeMirror-gutters" style="display: none; height: 25px;"></div></div></div></pre></li></ul></li><li><p><span>创建</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.1689px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">CREATE</span> <span class="cm-keyword">DATABASE</span> <span class="cm-bracket">[</span><span class="cm-keyword">IF</span> <span class="cm-keyword">NOT</span> <span class="cm-keyword">EXISTS</span><span class="cm-bracket">]</span> 数据库名<span class="cm-bracket">[</span><span class="cm-keyword">DEFAULT</span> <span class="cm-builtin">CHARSET</span> 字符集<span class="cm-bracket">][</span><span class="cm-keyword">COLLATE</span> 排序规则<span class="cm-bracket">]</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 49px;"></div><div class="CodeMirror-gutters" style="display: none; height: 49px;"></div></div></div></pre></li><li><p><span>删除</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">DROP</span> <span class="cm-keyword">DATABASE</span> <span class="cm-bracket">[</span><span class="cm-keyword">IF</span> <span class="cm-keyword">EXISTS</span><span class="cm-bracket">]</span> 数据库名<span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 25px;"></div><div class="CodeMirror-gutters" style="display: none; height: 25px;"></div></div></div></pre></li><li><p><span>使用</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">USE</span> 数据库名<span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 25px;"></div><div class="CodeMirror-gutters" style="display: none; height: 25px;"></div></div></div></pre></li></ol><h4 id='dml操作数据）'><span>DML（操作数据）</span></h4><h5 id='1添加'><span>1.添加</span></h5><ol start='' ><li><p><span>给指定字段添加数据</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.1694px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">INSERT</span> <span class="cm-keyword">INTO</span> 表名<span class="cm-bracket">(</span>字段名1<span class="cm-punctuation">,</span>字段名2<span class="cm-punctuation">,...</span><span class="cm-bracket">)</span><span class="cm-keyword">VALUES</span><span class="cm-bracket">(</span>值1<span class="cm-punctuation">,</span>值2<span class="cm-punctuation">,...</span><span class="cm-bracket">)</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 49px;"></div><div class="CodeMirror-gutters" style="display: none; height: 49px;"></div></div></div></pre></li><li><p><span>给全部字段添加数据</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">INSERT</span> <span class="cm-keyword">INTO</span> 表名 <span class="cm-keyword">VALUES</span><span class="cm-bracket">(</span>值1<span class="cm-punctuation">,</span>值2<span class="cm-punctuation">,...</span><span class="cm-bracket">)</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 25px;"></div><div class="CodeMirror-gutters" style="display: none; height: 25px;"></div></div></div></pre></li><li><p><span>批量添加数据</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.1689px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">INSERT</span> <span class="cm-keyword">INTO</span> 表名<span class="cm-bracket">(</span>字段名1<span class="cm-punctuation">,</span>字段名2<span class="cm-punctuation">,...</span><span class="cm-bracket">)</span><span class="cm-keyword">VALUES</span><span class="cm-bracket">(</span>值1<span class="cm-punctuation">,</span>值2<span class="cm-punctuation">,...</span><span class="cm-bracket">)</span><span class="cm-punctuation">,</span><span class="cm-bracket">(</span>值1<span class="cm-punctuation">,</span>值2<span class="cm-punctuation">,...</span><span class="cm-bracket">)</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 49px;"></div><div class="CodeMirror-gutters" style="display: none; height: 49px;"></div></div></div></pre><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">INSERT</span> <span class="cm-keyword">INTO</span> 表名 <span class="cm-keyword">VALUES</span><span class="cm-bracket">(</span>值1<span class="cm-punctuation">,</span>值2<span class="cm-punctuation">,...</span><span class="cm-bracket">)</span><span class="cm-punctuation">,</span><span class="cm-bracket">(</span>值1<span class="cm-punctuation">,</span>值2<span class="cm-punctuation">,...</span><span class="cm-bracket">)</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 25px;"></div><div class="CodeMirror-gutters" style="display: none; height: 25px;"></div></div></div></pre><p><span>注意：</span></p><ul><li><span>插入数据时，指定的字段顺序需要与值的顺序是一一对应的。</span></li><li><span>字符串和日期型数据应该包含在引号中。</span></li><li><span>插入的数据大小，应该在字段的规定范围内。</span></li></ul></li></ol><h5 id='2修改'><span>2.修改</span></h5><ol start='' ><li><p><span>修改数据</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">UPDATE</span> 表名 <span class="cm-keyword">SET</span> 字段名1<span class="cm-operator">=</span>值1<span class="cm-punctuation">,</span>字段名1<span class="cm-operator">=</span>值1<span class="cm-punctuation">,...</span><span class="cm-bracket">[</span><span class="cm-keyword">WHERE</span>条件<span class="cm-bracket">]</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 25px;"></div><div class="CodeMirror-gutters" style="display: none; height: 25px;"></div></div></div></pre><p><span>注意：修改语句的条件可以有，也可以没有，如果没有条件，则会修改整张表的所有数据。</span></p></li></ol><h5 id='3删除'><span>3.删除</span></h5><ol start='' ><li><p><span>删除数据</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">DELETE</span> <span class="cm-keyword">FROM</span> 表名 <span class="cm-bracket">[</span><span class="cm-keyword">WHERE</span>条件<span class="cm-bracket">]</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 25px;"></div><div class="CodeMirror-gutters" style="display: none; height: 25px;"></div></div></div></pre><p><span>注意：</span></p><ul><li><span>DELETE 语句的条件可以有，也可以没有，如果没有条件，则会删除整张表的所有数据。</span></li><li><span>DELETE 语句不能删除某一个字段的值（可以使用UPDATE)。</span></li></ul></li></ol><h4 id='dql'><span>DQL</span></h4><h5 id='语法'><span>语法</span></h5><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312030284.png" referrerpolicy="no-referrer" alt="image-20220708174538729"></p><h5 id='基本查询'><span>基本查询</span></h5><ol start='' ><li><p><span>查询多个字段</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">SELECT</span> 字段1<span class="cm-punctuation">,</span>字段2<span class="cm-punctuation">,</span>字段3<span class="cm-punctuation">,...</span><span class="cm-keyword">FROM</span> 表名<span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 25px;"></div><div class="CodeMirror-gutters" style="display: none; height: 25px;"></div></div></div></pre><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">SELECT</span> <span class="cm-operator">*</span> <span class="cm-keyword">FROM</span> 表名<span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 25px;"></div><div class="CodeMirror-gutters" style="display: none; height: 25px;"></div></div></div></pre></li><li><p><span>设置别名</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">SELECT</span> 字段1<span class="cm-bracket">[</span><span class="cm-keyword">AS</span>别名1<span class="cm-bracket">]</span>，字段2<span class="cm-bracket">[</span><span class="cm-keyword">AS</span>别名2<span class="cm-bracket">]</span>，...<span class="cm-keyword">FROM</span> 表名<span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 25px;"></div><div class="CodeMirror-gutters" style="display: none; height: 25px;"></div></div></div></pre></li><li><p><span>去除重复记录</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">SELECT</span> <span class="cm-keyword">DISTINCT</span> 字段列表 <span class="cm-keyword">FROM</span> 表名<span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 25px;"></div><div class="CodeMirror-gutters" style="display: none; height: 25px;"></div></div></div></pre></li></ol><h5 id='条件查询'><span>条件查询</span></h5><ol start='' ><li><p><span>语法</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">SELECT</span> 字段列表 <span class="cm-keyword">FROM</span> 表名 <span class="cm-keyword">WHERE</span> 条件列表<span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 25px;"></div><div class="CodeMirror-gutters" style="display: none; height: 25px;"></div></div></div></pre></li><li><p><span>条件</span></p><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312030285.png" referrerpolicy="no-referrer" alt="image-20220708175224244"></p></li></ol><h5 id='分页查询'><span>分页查询</span></h5><ol start='' ><li><p><span>语法</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">SELECT</span> 字段列表 <span class="cm-keyword">FROM</span> 表名 <span class="cm-keyword">LIMIT</span> 起始索引<span class="cm-punctuation">,</span>查询记录数<span class="cm-punctuation">;</span></span></pre></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">SELECT</span> <span class="cm-operator">*</span> <span class="cm-keyword">FROM</span> tb_user <span class="cm-keyword">LIMIT</span> <span class="cm-number">0</span> <span class="cm-punctuation">,</span> <span class="cm-number">2</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 49px;"></div><div class="CodeMirror-gutters" style="display: none; height: 49px;"></div></div></div></pre><p><span>注意：</span></p><ul><li><span>起始索引从0开始，起始索引=（查询页码-1）* 每页显示记录数。</span></li><li><span>分页查询是数据库的方言，不同的数据库有不同的实现，MySQL中是LIMIT。</span></li><li><span>如果查询的是第一页数据，起始索引可以省略，直接简写为 limit 10。</span></li></ul></li></ol><h5 id='连接查询'><span>连接查询</span></h5><ol start='' ><li><p><span>内连接</span></p><ul><li><p><span>隐式内连接</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">SELECT</span> 字段列表 <span class="cm-keyword">FROM</span> 表名1<span class="cm-punctuation">,</span>表名2 <span class="cm-keyword">WHERE</span> 条件...<span class="cm-punctuation">;</span> </span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 25px;"></div><div class="CodeMirror-gutters" style="display: none; height: 25px;"></div></div></div></pre></li><li><p><span>显示内连接</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.1694px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">SELECT</span> 字段列表 <span class="cm-keyword">FROM</span> 表名1 <span class="cm-bracket">[</span><span class="cm-keyword">INNER</span><span class="cm-bracket">]</span><span class="cm-keyword">JOIN</span> 表名2 <span class="cm-keyword">ON</span> 条件...<span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 49px;"></div><div class="CodeMirror-gutters" style="display: none; height: 49px;"></div></div></div></pre></li><li><p><span>内连接查询的是两张表的交集部分。</span></p></li></ul></li><li><p><span>外连接查询</span></p><ul><li><p><span>左外连接</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.1692px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">SELECT</span> 字段列表 <span class="cm-keyword">FROM</span> 表名1 <span class="cm-keyword">LEFT</span><span class="cm-bracket">[</span><span class="cm-keyword">OUTER</span><span class="cm-bracket">]</span><span class="cm-keyword">JOIN</span> 表名2 <span class="cm-keyword">ON</span> 条件...<span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 49px;"></div><div class="CodeMirror-gutters" style="display: none; height: 49px;"></div></div></div></pre><p><span>相当于查询左表所有数据+左表和右表的交集部分。</span></p></li><li><p><span>右外连接</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.1692px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">SELECT</span> 字段列表 <span class="cm-keyword">FROM</span> 表名1 <span class="cm-keyword">RIGHT</span><span class="cm-bracket">[</span><span class="cm-keyword">OUTER</span><span class="cm-bracket">]</span><span class="cm-keyword">JOIN</span> 表名2 <span class="cm-keyword">ON</span> 条件...<span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 49px;"></div><div class="CodeMirror-gutters" style="display: none; height: 49px;"></div></div></div></pre><p><span>相当于查询右表所有数据+左表和右表的交集部分。</span></p></li></ul></li><li><p><span>自连接</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.1694px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">SELECT</span> 字段列表 <span class="cm-keyword">FROM</span> 表名1 别名1 <span class="cm-keyword">JOIN</span> 表名2 别名2 <span class="cm-keyword">ON</span> 条件...<span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 49px;"></div><div class="CodeMirror-gutters" style="display: none; height: 49px;"></div></div></div></pre><p><span>自连接查询，可以是内连接查询也可以是外连接查询。</span></p></li></ol><h5 id='子查询'><span>子查询</span></h5><ol start='' ><li><p><span>概念：SQL语句中嵌套SELECT语句，称为嵌套查询，又称子查询</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.1692px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">SELECT</span> <span class="cm-operator">*</span> <span class="cm-keyword">FROM</span> t1 <span class="cm-keyword">WHERE</span> column1 <span class="cm-operator">=</span> <span class="cm-bracket">(</span> <span class="cm-keyword">SELECT</span> column1 <span class="cm-keyword">FROM</span> t2<span class="cm-bracket">)</span><span class="cm-punctuation">:</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 49px;"></div><div class="CodeMirror-gutters" style="display: none; height: 49px;"></div></div></div></pre><p><span>子查询外部的语句可以是INSERT / UPDATE / DELETE / SELECT 的任何一个。</span></p></li><li><p><span>根据子查询结果不同，分为：</span></p><ul><li><span>标量子查询（子查询结果为单个值)</span></li><li><span>列子查询(子查询结果为一列)</span></li><li><span>行子查询(子查询结果为一行)</span></li><li><span>表子查询(子查询结果为多行多列)</span></li></ul></li><li><p><span>根据子查询位置，分为：WHERE之后、FROM之后、SELECT 之后。</span></p></li></ol><h3 id='事务'><span>事务</span></h3><h4 id='简介'><span>简介</span></h4><ul><li><em><strong><span>事务是一组操作的集合</span></strong></em><span>，它是一个不可分割的工作单位，事务会把所有的操作作为一个整体一起向系统提交或撤销操作请求，即这些操作</span><em><strong><span>要么同时成功，要么同时失败</span></strong></em><span>。</span></li><li><em><strong><span>默认MySQL的事务是自动提交</span></strong></em><span>的，也就是说，当执行一条DML语句，MySQL会立即隐式的提交事务。</span></li></ul><h4 id='事务操作'><span>事务操作</span></h4><ol start='' ><li><p><span>查看/设置事务的提交发送</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">SELECT</span> <span class="cm-variable-2">@@autocommit</span><span class="cm-punctuation">;</span></span></pre></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">SET</span> <span class="cm-variable-2">@@autocommit</span> <span class="cm-operator">=</span><span class="cm-number">0</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 49px;"></div><div class="CodeMirror-gutters" style="display: none; height: 49px;"></div></div></div></pre></li><li><p><span>提交事务</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">COMMIT</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 25px;"></div><div class="CodeMirror-gutters" style="display: none; height: 25px;"></div></div></div></pre></li><li><p><span>回滚事务</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">ROLLBACK</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 25px;"></div><div class="CodeMirror-gutters" style="display: none; height: 25px;"></div></div></div></pre></li><li><p><span>开启事务</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">START</span> <span class="cm-keyword">TRANSACTION</span><span class="cm-punctuation">;</span> 或 <span class="cm-keyword">BEGIN</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 25px;"></div><div class="CodeMirror-gutters" style="display: none; height: 25px;"></div></div></div></pre></li></ol><h4 id='并发事务问题'><span>并发事务问题</span></h4><figure><table><thead><tr><th style='text-align:center;' ><span>问题</span></th><th style='text-align:center;' ><span>描述</span></th></tr></thead><tbody><tr><td style='text-align:center;' ><span>脏读</span></td><td style='text-align:center;' ><span>一个事务读到另外一个事务还没有提交的数据</span></td></tr><tr><td style='text-align:center;' ><span>不可重复读</span></td><td style='text-align:center;' ><span>一个事务先后读取同一条记录，但两次读取的数据不同，称之为不可重复读。</span></td></tr><tr><td style='text-align:center;' ><span>幻读</span></td><td style='text-align:center;' ><span>一个事务按照条件查询数据时，没有对应的数据行，但是在插入数据时，又发现这行数据已经存在，好像出现了幻影</span></td></tr></tbody></table></figure><h4 id='事务隔离级别'><span>事务隔离级别</span></h4><figure><table><thead><tr><th style='text-align:center;' ><span>隔离级别</span></th><th style='text-align:center;' ><span>脏读</span></th><th style='text-align:center;' ><span>不可重复读</span></th><th style='text-align:center;' ><span>幻读</span></th></tr></thead><tbody><tr><td style='text-align:center;' ><span>Read uncommitted</span></td><td style='text-align:center;' ><span>T</span></td><td style='text-align:center;' ><span>T</span></td><td style='text-align:center;' ><span>T</span></td></tr><tr><td style='text-align:center;' ><span>Read committed</span></td><td style='text-align:center;' ><span>F</span></td><td style='text-align:center;' ><span>T</span></td><td style='text-align:center;' ><span>T</span></td></tr><tr><td style='text-align:center;' ><span>Repeatable Read(默认)</span></td><td style='text-align:center;' ><span>F</span></td><td style='text-align:center;' ><span>F</span></td><td style='text-align:center;' ><span>T</span></td></tr><tr><td style='text-align:center;' ><span>Serializable</span></td><td style='text-align:center;' ><span>F</span></td><td style='text-align:center;' ><span>F</span></td><td style='text-align:center;' ><span>F</span></td></tr></tbody></table></figure><h3 id='mysql体系结构'><span>MySQL体系结构</span></h3><h4 id='体系'><span>体系</span></h4><ul><li><p><span>连接层</span></p><p><span>最上层是一些客户端和链接服务，主要完成一些类似于连接处理、授权认证、及相关的安全方案。服务器也会为安全接入的每个客户端验证它所具有的操作权限。</span></p></li><li><p><span>服务层</span></p><p><span>第二层架构主要完成大多数的核心服务功能，如SQL接口，并完成缓存的查询，SQL的分析和优化，部分内置函数的执行。所有跨存储引擎的功能也在这一层实现，如过程、函数等。</span></p></li><li><p><span>引擎层</span></p><p><span>存储引擎真正的负责了MySQL中数据的存储和提取，服务器通过API和存储引擎进行通信。不同的存储引擎具有不同的功能，这样我们可以根据自己的需要，来选取合适的存储引擎。</span></p></li><li><p><span>储存层</span></p><p><span>主要是将数据存储在文件系统之上，并完成与存储引擎的交互。</span></p></li></ul><h4 id='储存引擎'><span>储存引擎</span></h4><ol start='' ><li><p><span>简介</span></p><p><span>存储引擎就是存储数据、建立索引、更新/查询数据等技术的实现方式。</span><em><strong><span>存储引擎是基于表</span></strong></em><span>的，而不是基于库的，所以存储引擎也可被称为表类型。</span></p></li></ol><h5 id='innodb'><span>InnoDB</span></h5><ol start='' ><li><p><span>介绍</span></p><p><span>InnoDB是一种兼顾高可靠性和高性能的通用存储引擎，在MySQL5.5 之后，InnoDB是默认的 MySQL 存储引擎。</span></p></li><li><p><span>特点</span></p><ul><li><span>DML操作遵循ACID模型，支持事务;</span></li><li><span>行级锁，提高并发访问性能;</span></li><li><span>支持外键 FOREIGN KEY约束;</span></li><li><span>保证数据的完整性和正确性；</span></li></ul><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312030286.png" referrerpolicy="no-referrer" alt="image-20220709002917176"></p></li></ol><h5 id='myisam'><span>MyISAM</span></h5><ol start='' ><li><p><span>介绍</span></p><p><span>MyISAM是MySQL早期的默认存储引擎。</span></p></li><li><p><span>特点</span></p><ul><li><em><strong><span>不支持事务，不支持外键</span></strong></em></li><li><em><strong><span>支持表锁，不支持行锁</span></strong></em></li><li><span>访问速度快</span></li></ul></li></ol><h4 id='储存引擎特点'><span>储存引擎特点</span></h4><figure><table><thead><tr><th style='text-align:center;' ><span>特点</span></th><th style='text-align:center;' ><span>Innodb</span></th><th style='text-align:center;' ><span>MyISAM</span></th><th style='text-align:center;' ><span>memory</span></th></tr></thead><tbody><tr><td style='text-align:center;' ><span>存储限制</span></td><td style='text-align:center;' ><span>64TB</span></td><td style='text-align:center;' ><span>有</span></td><td style='text-align:center;' ><span>有</span></td></tr><tr><td style='text-align:center;' ><span>事务安全</span></td><td style='text-align:center;' ><span>支持</span></td><td style='text-align:center;' ><span>-</span></td><td style='text-align:center;' ><span>-</span></td></tr><tr><td style='text-align:center;' ><span>锁机制</span></td><td style='text-align:center;' ><span>行锁</span></td><td style='text-align:center;' ><span>表锁</span></td><td style='text-align:center;' ><span>表锁</span></td></tr><tr><td style='text-align:center;' ><span>B+tree索引</span></td><td style='text-align:center;' ><span>支持</span></td><td style='text-align:center;' ><span>支持</span></td><td style='text-align:center;' ><span>支持</span></td></tr><tr><td style='text-align:center;' ><span>Hash索引</span></td><td style='text-align:center;' ><span>-</span></td><td style='text-align:center;' ><span>-</span></td><td style='text-align:center;' ><span>支持</span></td></tr><tr><td style='text-align:center;' ><span>全文索引</span></td><td style='text-align:center;' ><span>支持(5.6版本之后)</span></td><td style='text-align:center;' ><span>支持</span></td><td style='text-align:center;' ><span>-</span></td></tr><tr><td style='text-align:center;' ><span>空间使用</span></td><td style='text-align:center;' ><span>高</span></td><td style='text-align:center;' ><span>低</span></td><td style='text-align:center;' ><span>N/A</span></td></tr><tr><td style='text-align:center;' ><span>内存使用</span></td><td style='text-align:center;' ><span>高</span></td><td style='text-align:center;' ><span>低</span></td><td style='text-align:center;' ><span>中等</span></td></tr><tr><td style='text-align:center;' ><span>批量插入速度</span></td><td style='text-align:center;' ><span>低</span></td><td style='text-align:center;' ><span>高</span></td><td style='text-align:center;' ><span>高</span></td></tr><tr><td style='text-align:center;' ><span>支持外键</span></td><td style='text-align:center;' ><span>支持</span></td><td style='text-align:center;' ><span>-</span></td><td style='text-align:center;' ><span>-</span></td></tr></tbody></table></figure><ul><li><p><span>储存引擎选择</span></p><ol start='' ><li><span>InnoDB：是MySQL的默认存储引擎，支持事务、外键。如果应用对事务的完整性有比较高的要求，在并发条件下要求数据的一致性，数据操作除了插入和查询之外，还包含很多的更新、删除操作，那么InnoDB存储引擎是比较合适的选择。</span></li><li><span>MyISAM ：如果应用是以读操作和插入操作为主，只有很少的更新和删除操作，并且对事务的完整性、并发性要求不是很高，那</span>
<span>么选择这个存储引擎是非常合适的。</span></li><li><span>MEMORY：将所有数据保存在内存中，访问速度快，通常用于临时表及缓存。MEMORY的缺陷就是对表的大小有限制，太大的表无法缓存在内存中，而且无法保障数据的安全性。</span></li></ol></li></ul><h3 id='索引'><span>索引</span></h3><h4 id='介绍'><span>介绍</span></h4><p><span>索引(index）是</span><em><strong><span>帮助MySQL高效获取数据的数据结构(有序)</span></strong></em><span>。在数据之外，数据库系统还维护着满足特定查找算法的数据结构，这些数据结构以某种方式引用（指向）数据，这样就可以在这些数据结构上实现高级查找算法，这种数据结构就是索引。</span></p><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312030287.png" referrerpolicy="no-referrer" alt="image-20220709221131424"></p><ol start='' ><li><p><span>优缺点</span></p><ol start='' ><li><p><span>优点</span></p><ul><li><em><strong><span>提高数据检索的效率</span></strong></em><span>，降低数据库的IO成本。</span></li><li><span>通过索引列对数据进行排序，降低数据排序的成本，降低CPU的消耗。</span></li></ul></li><li><p><span>缺点</span></p><ul><li><em><strong><span>索引列也是要占用空间</span></strong></em><span>的。</span></li><li><em><strong><span>索引大大提高了查询效率，同时却也降低更新表的速度</span></strong></em><span>，如对表进行INSERT ，UPDATE，DELETE时，效率降低。（</span><em><strong><span>增删改更新表索引要重新排序</span></strong></em><span>）</span></li></ul></li></ol></li></ol><h4 id='索引结构'><span>索引结构</span></h4><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312030288.png" referrerpolicy="no-referrer" alt="image-20220709221923660"></p><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312030289.png" referrerpolicy="no-referrer" alt="image-20220709222149100"></p><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312030290.png" referrerpolicy="no-referrer" alt="image-20220709222213798"></p><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312030291.png" referrerpolicy="no-referrer" alt="image-20220709222221774"></p><ul><li><p><span>Hash</span></p><ol start='' ><li><span>Hash索引1只能用于对等比较(=，in)，不支持范围查询(between,&gt;,&lt;)。</span></li><li><span>无法利用索引完成排序操作</span></li><li><span>查询效率高，通常只需要一次检索就可以了，效率通常要高于B+tree索引。</span></li></ol></li></ul><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312030292.png" referrerpolicy="no-referrer" alt="image-20220709223616190"></p><ul><li><p><span>为什么InnoDB存储引擎选择使用B+tree索引结构？</span></p><ol start='' ><li><em><strong><span>相对于二叉树，层级更少，搜索效率高</span></strong></em><span>；</span></li><li><em><strong><span>对于B-tree，无论是叶子节点还是非叶子节点，都会保存数据，这样导致一页中存储的键值减少</span></strong></em><span>，指针跟着减少，</span><em><strong><span>要同样保存大量数据，只能增加树的高度</span></strong></em><span>，导致性能降低；</span></li><li><em><strong><span>相对Hash索引，B+tree支持范围匹配及排序操作</span></strong></em><span>；</span></li></ol></li></ul><h4 id='索引分类'><span>索引分类</span></h4><figure><table><thead><tr><th style='text-align:center;' ><span>分类</span></th><th style='text-align:center;' ><span>含义</span></th><th style='text-align:center;' ><span>特点</span></th><th style='text-align:center;' ><span>关键字</span></th></tr></thead><tbody><tr><td style='text-align:center;' ><span>主键索引</span></td><td style='text-align:center;' ><span>针对于表中主键创建的索引</span></td><td style='text-align:center;' ><span>默认自动创建，只能有一个</span></td><td style='text-align:center;' ><span>PRIMARY</span></td></tr><tr><td style='text-align:center;' ><span>唯一索引</span></td><td style='text-align:center;' ><span>避免同一个表中某数据列中的值重复</span></td><td style='text-align:center;' ><span>可以有多个</span></td><td style='text-align:center;' ><span>UNIQUE</span></td></tr><tr><td style='text-align:center;' ><span>常规索引</span></td><td style='text-align:center;' ><span>快速定位特定数据</span></td><td style='text-align:center;' ><span>可以有多个</span></td><td style='text-align:center;' >&nbsp;</td></tr><tr><td style='text-align:center;' ><span>全文索引</span></td><td style='text-align:center;' ><span>全文索引查找的是文本中的关键词，而不是比较索引中的值</span></td><td style='text-align:center;' ><span>可以有多个</span></td><td style='text-align:center;' ><span>FULLTEXT</span></td></tr></tbody></table></figure><p><span>   在InnoDB存储引擎中，根据</span><em><strong><span>索引的存储形式</span></strong></em><span>，又可以分为以下两种：</span></p><figure><table><thead><tr><th style='text-align:center;' ><span>分类</span></th><th style='text-align:center;' ><span>含义</span></th><th style='text-align:center;' ><span>特点</span></th></tr></thead><tbody><tr><td style='text-align:center;' ><span>聚集索引</span></td><td style='text-align:center;' ><span>将</span><em><strong><span>数据存储与索引放到了一块</span></strong></em><span>，索引结构的</span><em><strong><span>叶子节点保存了行数据</span></strong></em></td><td style='text-align:center;' ><span>必须要，且只有一个</span></td></tr><tr><td style='text-align:center;' ><span>二级索引</span></td><td style='text-align:center;' ><span>将</span><em><strong><span>数据与索引分开存储</span></strong></em><span>，索引结构的</span><em><strong><span>叶子节点关联的是对应的主键</span></strong></em></td><td style='text-align:center;' ><span>可以存在多个</span></td></tr></tbody></table></figure><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312030293.png" referrerpolicy="no-referrer" alt="image-20220709225118725"></p><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312030294.png" referrerpolicy="no-referrer" alt="image-20220709225127530"></p><p><em><strong><span>尽量减少回表查询</span></strong></em></p><h4 id='索引语法'><strong><span>索引语法</span></strong></h4><ul><li><p><span>创建索引</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.1693px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">CREATE</span> <span class="cm-bracket">[</span><span class="cm-keyword">UNIQUE</span><span class="cm-bracket">]</span> <span class="cm-bracket">[</span><span class="cm-keyword">FULLTEXT</span><span class="cm-bracket">]</span> <span class="cm-keyword">INDEX</span> inde_name <span class="cm-keyword">ON</span> <span class="cm-keyword">table_name</span> <span class="cm-bracket">(</span>index_col_name<span class="cm-punctuation">,...</span><span class="cm-bracket">)</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 49px;"></div><div class="CodeMirror-gutters" style="display: none; height: 49px;"></div></div></div></pre></li><li><p><span>查看索引</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">SHOW</span> <span class="cm-keyword">INDEX</span> <span class="cm-keyword">FROM</span> <span class="cm-keyword">table_name</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 25px;"></div><div class="CodeMirror-gutters" style="display: none; height: 25px;"></div></div></div></pre></li><li><p><span>删除索引</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">DROP</span> <span class="cm-keyword">INDEX</span> index_name <span class="cm-keyword">ON</span> <span class="cm-keyword">table_name</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 25px;"></div><div class="CodeMirror-gutters" style="display: none; height: 25px;"></div></div></div></pre></li></ul><h4 id='sql性能分析'><span>SQL性能分析</span></h4><ul><li><p><span>SQL执行频率</span></p><p><span>MySQL客户端连接成功后，通过 show [session|global] status 命令可以提供服务器状态信息。通过如下指令，可以查看当前数据库的INSERT、 UPDATE、 DELETE、SELECT的访问频次：</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">SHOW</span> <span class="cm-keyword">GLOBAL</span> <span class="cm-keyword">STATUS</span> <span class="cm-keyword">LIKE</span> <span class="cm-string">'COM____'</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 25px;"></div><div class="CodeMirror-gutters" style="display: none; height: 25px;"></div></div></div></pre><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312030295.png" referrerpolicy="no-referrer" alt="image-20220709230246104"></p></li><li><p><span>慢查询日志</span></p><p><span>慢查询日志记录了所有执行时间超过指定参数(long_query_time， 单位：秒，默认10秒）的所有SQL语句的日志。MySQL的慢查询日志默认没有开启，需要在MySQL的配置文件 （/etc/my.cnf） 中配置如下信息：</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;">＃开启MySOL慢日志查询开关</span></pre></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;">slow_query _ log<span class="cm-operator">=</span><span class="cm-number">1</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;">＃设置慢日志的时间为2秒，SQL语句执行时间超过2秒，就会视为慢查询，记录慢查询日志</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;">long_query <span class="cm-type">time</span><span class="cm-operator">=</span><span class="cm-number">2</span></span></pre></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 123px;"></div><div class="CodeMirror-gutters" style="display: none; height: 123px;"></div></div></div></pre><ul><li><span>配置完毕之后，通过以下指令重新启动MySQL服务器进行测试，查看慢日志文件中记录的信息 /var/lib /mysql/locathost-slow.log。</span></li></ul></li><li><p><span>profile详情</span></p><p><span>执行一系列的业务SQL的操作，然后通过如下指令查看指令的执行耗时：</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation" style=""><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-comment">#查看每一条SQL的耗时基本情况</span></span></pre></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">show</span> <span class="cm-keyword">profiles</span><span class="cm-punctuation">;</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-comment">#查看指定query_ id的SQL语句各个阶段的耗时情况</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">show</span> <span class="cm-keyword">profile</span> <span class="cm-keyword">for</span> <span class="cm-keyword">query</span> query_id<span class="cm-punctuation">;</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;">＃查看指定query id的SOL语句CPU的使用情况</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">show</span> <span class="cm-keyword">profile</span> cpu <span class="cm-keyword">for</span> <span class="cm-keyword">query</span> query_id<span class="cm-punctuation">;</span></span></pre></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 148px;"></div><div class="CodeMirror-gutters" style="display: none; height: 148px;"></div></div></div></pre></li></ul><h4 id='索引使用'><strong><span>索引使用</span></strong></h4><ul><li><p><span>最左前缀法则</span></p><p><span>如果索引了多列（联合索引） ，要遵守最左前缀法则。最左前缀法则指的是</span><em><strong><span>查询从索引的最左列开始，并且不跳过索引中的列</span></strong></em><span>。如果</span><em><strong><span>跳跃某一列，索引将部分失效(后面的字段索引失效）</span></strong></em><span>。</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.1693px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">explain</span> <span class="cm-keyword">select</span> <span class="cm-operator">*</span> <span class="cm-keyword">from</span> tb <span class="cm-keyword">user</span> <span class="cm-keyword">where</span> profession <span class="cm-operator">=</span> <span class="cm-string">'软件工程'</span><span class="cm-keyword">and</span> age <span class="cm-operator">=</span> <span class="cm-number">31</span> <span class="cm-keyword">and</span> <span class="cm-keyword">status</span> <span class="cm-operator">=</span> <span class="cm-string">'o'</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 49px;"></div><div class="CodeMirror-gutters" style="display: none; height: 49px;"></div></div></div></pre><p>&nbsp;</p></li><li><p><span>范围查询</span></p><p><span>联合索引中，</span><em><strong><span>出现范围查询(&gt;,&lt;)，范围查询右侧的列索引失效</span></strong></em><span>。</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">explain</span> <span class="cm-keyword">select</span> <span class="cm-operator">*</span> <span class="cm-keyword">from</span> tb <span class="cm-keyword">user</span> <span class="cm-keyword">where</span></span></pre></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;">profession <span class="cm-operator">=</span><span class="cm-string">'软件工程'</span><span class="cm-keyword">and</span> age <span class="cm-operator">&gt;</span><span class="cm-number">30</span> <span class="cm-keyword">and</span> <span class="cm-keyword">status</span> <span class="cm-operator">=</span><span class="cm-string">'0'</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 49px;"></div><div class="CodeMirror-gutters" style="display: none; height: 49px;"></div></div></div></pre></li><li><p><span>索引列运算</span></p><p><em><strong><span>不要在索引列上进行运算操作，索引将失效。</span></strong></em></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.1693px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">explain</span> <span class="cm-keyword">select</span> <span class="cm-operator">*</span> <span class="cm-keyword">from</span> tb <span class="cm-keyword">user</span> <span class="cm-keyword">where</span> substring<span class="cm-bracket">(</span>phone<span class="cm-punctuation">,</span> <span class="cm-number">10</span><span class="cm-punctuation">,</span><span class="cm-number">2</span><span class="cm-bracket">)</span> <span class="cm-operator">=</span> <span class="cm-string">'15'</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 49px;"></div><div class="CodeMirror-gutters" style="display: none; height: 49px;"></div></div></div></pre></li><li><p><span>字符串不加引号</span></p><p><strong><span>字符串类型字段使用时，不加引号，索引将失效。</span></strong></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.1693px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><span><span>​</span>x</span></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">explain</span> <span class="cm-keyword">select</span> <span class="cm-operator">*</span> <span class="cm-keyword">from</span> tb <span class="cm-keyword">user</span> <span class="cm-keyword">where</span> profession <span class="cm-operator">=</span> <span class="cm-string">'软件工程'</span> <span class="cm-keyword">and</span> age <span class="cm-operator">=</span> <span class="cm-number">31</span> <span class="cm-keyword">and</span> <span class="cm-keyword">status</span> <span class="cm-operator">=</span><span class="cm-number">0</span><span class="cm-punctuation">;</span></span></pre></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span cm-text="" cm-zwsp="">
</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">explain</span> <span class="cm-keyword">select</span> <span class="cm-operator">*</span> <span class="cm-keyword">from</span> tb <span class="cm-keyword">user</span> <span class="cm-keyword">where</span> phone <span class="cm-operator">=</span> <span class="cm-number">17799990015</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 123px;"></div><div class="CodeMirror-gutters" style="display: none; height: 123px;"></div></div></div></pre></li><li><p><span>模糊查询</span></p><p><span>如果仅仅是</span><em><strong><span>尾部模糊匹配，索引不会失效</span></strong></em><span>。如果是</span><em><strong><span>头部模糊匹配，索引失效</span></strong></em><span>。</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.1693px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">explain</span> <span class="cm-keyword">select</span> <span class="cm-operator">*</span> <span class="cm-keyword">from</span> tb <span class="cm-keyword">user</span> <span class="cm-keyword">where</span> profession <span class="cm-keyword">like</span> <span class="cm-string">'软件%'</span>； <span class="cm-comment">#生效</span></span></pre></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">explain</span> <span class="cm-keyword">select</span> <span class="cm-operator">*</span> <span class="cm-keyword">from</span> tb <span class="cm-keyword">user</span> <span class="cm-keyword">where</span> profession <span class="cm-keyword">like</span> <span class="cm-string">'%工程'</span><span class="cm-punctuation">;</span> <span class="cm-comment">#失效</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">explain</span> <span class="cm-keyword">select</span> <span class="cm-operator">*</span> <span class="cm-keyword">from</span> tb <span class="cm-keyword">user</span> <span class="cm-keyword">where</span> profession <span class="cm-keyword">like</span> <span class="cm-string">'%I%'</span><span class="cm-punctuation">;</span> <span class="cm-comment">#失效</span></span></pre></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 148px;"></div><div class="CodeMirror-gutters" style="display: none; height: 148px;"></div></div></div></pre></li><li><p><span>or连接的条件</span></p><p><span>用or分割开的条件，如果or前的条件中的列有索引，而后面的列中没有索引，那么涉及的索引都不会被用到。</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.1693px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">explain</span> <span class="cm-keyword">select</span> <span class="cm-operator">*</span> <span class="cm-keyword">from</span> tb <span class="cm-keyword">user</span> <span class="cm-keyword">where</span> id <span class="cm-operator">=</span> <span class="cm-number">10</span> <span class="cm-keyword">or</span> age <span class="cm-operator">=</span> <span class="cm-number">23</span><span class="cm-punctuation">;</span></span></pre></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">explain</span> <span class="cm-keyword">select</span> <span class="cm-operator">*</span> <span class="cm-keyword">from</span> tb <span class="cm-keyword">user</span> <span class="cm-keyword">where</span> phone <span class="cm-operator">=</span> <span class="cm-string">'17799990017'</span> <span class="cm-keyword">or</span> age <span class="cm-operator">=</span> <span class="cm-number">23</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 99px;"></div><div class="CodeMirror-gutters" style="display: none; height: 99px;"></div></div></div></pre><p><span>注：由于age没有索引，所以即使id、phone有索引，索引也会失效。所以需要针对于age也要建立索引。</span></p></li><li><p><span>数据分布影响</span></p><p><span>如果MySQL评估使用索引比全表更慢，则不使用索引。</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">select</span> <span class="cm-operator">*</span> <span class="cm-keyword">from</span> tb <span class="cm-keyword">user</span> <span class="cm-keyword">where</span> phone <span class="cm-operator">&gt;=</span><span class="cm-string">'17799990005'</span><span class="cm-punctuation">;</span></span></pre></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">select</span> <span class="cm-operator">*</span> <span class="cm-keyword">from</span> b_user <span class="cm-keyword">where</span> phone <span class="cm-operator">&gt;=</span> <span class="cm-string">'17799990015'</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 49px;"></div><div class="CodeMirror-gutters" style="display: none; height: 49px;"></div></div></div></pre></li><li><p><span>SQL提示</span></p><p><span>SQL提示，是优化数据库的一个重要手段，简单来说，就是在SQL语句中加入一些人为的提示来达到优化操作的目的。</span></p><p><span>use index:     #推荐使用</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.1694px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">explain</span> <span class="cm-keyword">select</span> <span class="cm-operator">*</span> <span class="cm-keyword">from</span> tb <span class="cm-keyword">user</span> <span class="cm-keyword">use</span> <span class="cm-keyword">index</span><span class="cm-bracket">(</span>idx <span class="cm-keyword">user</span> pro<span class="cm-bracket">)</span> <span class="cm-keyword">where</span> profession <span class="cm-operator">=</span> <span class="cm-string">'软件工程'</span>； </span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 49px;"></div><div class="CodeMirror-gutters" style="display: none; height: 49px;"></div></div></div></pre><p><span>ignore index:</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.1692px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">explain</span> <span class="cm-keyword">select</span> <span class="cm-operator">*</span> <span class="cm-keyword">from</span> tb <span class="cm-keyword">user</span> <span class="cm-keyword">ignore</span> <span class="cm-keyword">index</span><span class="cm-bracket">(</span>idx <span class="cm-keyword">user</span> pro<span class="cm-bracket">)</span> <span class="cm-keyword">where</span> profession <span class="cm-operator">=</span> <span class="cm-string">'软件工程'</span>；</span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 49px;"></div><div class="CodeMirror-gutters" style="display: none; height: 49px;"></div></div></div></pre><p><span>force index:</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.1692px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">explain</span> <span class="cm-keyword">select</span> <span class="cm-operator">*</span> <span class="cm-keyword">from</span> tb <span class="cm-keyword">user</span> <span class="cm-keyword">force</span> <span class="cm-keyword">index</span><span class="cm-bracket">(</span>idx <span class="cm-keyword">user</span> pro<span class="cm-bracket">)</span> <span class="cm-keyword">where</span> profession <span class="cm-operator">=</span> <span class="cm-string">'软件工程'</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 49px;"></div><div class="CodeMirror-gutters" style="display: none; height: 49px;"></div></div></div></pre></li><li><p><span>覆盖索引</span></p><p><em><strong><span>尽量使用覆盖索引</span></strong></em><span>（查询使用了索引，并且</span><em><strong><span>需要返回的列，在该索引中已经全部能够找到</span></strong></em><span>），减少select *。</span></p><ul><li><p><span>知识小贴士：</span></p><p><span>using index condition ：查找使用了索引，但是需要回表查询数据 。</span></p><p><span>using where; using index ：查找使用了索引，但是需要的数据都在索引列中能找到，所以不需要回表查询数据 。</span></p></li></ul><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312030296.png" referrerpolicy="no-referrer" alt="image-20220709233131469"></p></li><li><p><span>前缀索引</span></p><p><span>当字段类型为字符串(varchar， text等） 时，有时候需要索引很长的字符串，这会让索引变得很大，查询时，浪费大量的磁盘IO，影响查询效率。此时可以只将字符串的一部分前缀，建立索引，这样可以大大节约索引空间，从而提高索引效率。</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">create</span> <span class="cm-keyword">index</span> id_xxxx <span class="cm-keyword">on</span> <span class="cm-keyword">table_name</span><span class="cm-bracket">(</span><span class="cm-keyword">column</span><span class="cm-bracket">(</span>n<span class="cm-bracket">))</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 25px;"></div><div class="CodeMirror-gutters" style="display: none; height: 25px;"></div></div></div></pre><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312030298.png" referrerpolicy="no-referrer" alt="image-20220709233637441"></p></li><li><p><span>单列索引与联合索引</span></p><ol start='' ><li><span>单列索引：即一个索引只包含单个列。</span></li><li><span>联合索引：即一个索引包含了多个列。</span></li></ol><ul><li><p><span>在业务场景中，如果存在多个查询条件，考虑针对于查询字段建立索引时，建议建立联合索引，而非单列索引。</span></p><p><span>多条件联合查询时，MySQL优化器会评估哪个字段的索引效率更高，会选择该索引完成本次查询。</span></p></li></ul><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312030299.png" referrerpolicy="no-referrer" alt="image-20220711135016340"></p></li></ul><h4 id='索引设计原则'><span>索引设计原则</span></h4><ol start='' ><li><span>针对于数据量较大，且查询比较频繁的表建立索引。</span></li><li><span>针对于常作为查询条件(where）、排序 (order by）、分组（group by）操作的字段建立索引。</span></li><li><span>尽量选择区分度高的列作为索引，尽量建立唯一索引，区分度越高，使用索引的效率越高。</span></li><li><span>如果是字符串类型的字段，字段的长度较长，可以针对于字段的特点，建立前缀索引。</span></li><li><span>尽量使用联合索引，减少单列索引，查询时，联合索引很多时候可以覆盖索引，节省存储空间，避免回表，提高查询效率。</span></li><li><span>要控制索引的数量，索引并不是多多益善，索引越多，维护索引结构的代价也就越大，会影响增删改的效率。</span></li><li><span>如果索引列不能存储NULL值，请在创建表时使用NOT NULL约束它。当优化器知道每列是否包含NULL值时，它可以更好地确定哪个索引最有效地用于查询。</span></li></ol><h4 id='索引优化'><span>索引优化</span></h4><p><span>insert优化</span></p><ol start='' ><li><p><span>批量插入</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.1693px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">INSERT</span> <span class="cm-keyword">INTO</span> tb_test <span class="cm-keyword">VALUES</span><span class="cm-bracket">(</span><span class="cm-number">1</span><span class="cm-punctuation">,</span><span class="cm-string">'Tom'</span><span class="cm-bracket">)</span><span class="cm-punctuation">,</span><span class="cm-bracket">(</span><span class="cm-number">2</span><span class="cm-punctuation">,</span><span class="cm-string">'Cat'</span><span class="cm-bracket">)</span><span class="cm-punctuation">,</span><span class="cm-bracket">(</span><span class="cm-number">3</span><span class="cm-punctuation">,</span><span class="cm-string">'Jerry'</span><span class="cm-bracket">)</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 49px;"></div><div class="CodeMirror-gutters" style="display: none; height: 49px;"></div></div></div></pre></li><li><p><span>手动提交事务</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">START</span> <span class="cm-keyword">TRANSACTION</span><span class="cm-punctuation">;</span></span></pre></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">INSERT</span> <span class="cm-keyword">INTO</span> tb_test <span class="cm-keyword">VALUES</span><span class="cm-bracket">(</span><span class="cm-number">1</span><span class="cm-punctuation">,</span><span class="cm-string">'Tom'</span><span class="cm-bracket">)</span><span class="cm-punctuation">,</span> <span class="cm-bracket">(</span><span class="cm-number">2</span><span class="cm-punctuation">,</span><span class="cm-string">'Cat'</span><span class="cm-bracket">)</span><span class="cm-punctuation">,</span><span class="cm-bracket">(</span><span class="cm-number">3</span><span class="cm-punctuation">,</span><span class="cm-string">'Jerry'</span><span class="cm-bracket">)</span><span class="cm-punctuation">;</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">COMMIT</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 99px;"></div><div class="CodeMirror-gutters" style="display: none; height: 99px;"></div></div></div></pre></li><li><p><span>主键顺序插入</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;">主键乱序插入<span class="cm-punctuation">:</span> <span class="cm-number">8</span> <span class="cm-number">1</span> <span class="cm-number">9</span> <span class="cm-number">21</span> <span class="cm-number">88</span> <span class="cm-number">2</span> <span class="cm-number">4</span> <span class="cm-number">15</span> <span class="cm-number">89</span> <span class="cm-number">5</span> <span class="cm-number">7</span> <span class="cm-number">3</span></span></pre></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;">主键顺序插入<span class="cm-punctuation">:</span><span class="cm-number">1</span> <span class="cm-number">2</span> <span class="cm-number">3</span> <span class="cm-number">4</span> <span class="cm-number">5</span> <span class="cm-number">7</span> <span class="cm-number">8</span> <span class="cm-number">9</span> <span class="cm-number">15</span> <span class="cm-number">21</span> <span class="cm-number">88</span> <span class="cm-number">89</span></span></pre></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 49px;"></div><div class="CodeMirror-gutters" style="display: none; height: 49px;"></div></div></div></pre></li></ol><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312030300.png" referrerpolicy="no-referrer" alt="image-20220711140103101"></p><p><span>主键优化</span></p><ol start='' ><li><p><span>页分裂</span></p><p><span>页可以为空，也可以填充一半，也可以填充100%。每个页包含了2-N行数据(如果一行数据多大，会行溢出)，根据主键排列。</span></p><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312030301.png" referrerpolicy="no-referrer" alt="image-20220711140312372"></p></li><li><p><span>页合并</span></p><p><span>当删除一行记录时，实际上记录并没有被物理删除，只是记录被标记(flaged）为删除并且它的空间变得允许被其他记录声明使用。当页中删除的记录达到 MERGE_ THRESHOLD（默认为页的50%），InnoDB会开始寻找最靠近的页（前或后）看看是否可以将两个页合并以优化空间使用。</span></p><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312030302.png" referrerpolicy="no-referrer" alt="image-20220711140424130"></p></li></ol><p><span>主键设计原则</span></p><ol start='' ><li><span>满足业务需求的情况下，尽量降低主键的长度。</span></li><li><span>插入数据时，尽量选择顺序插入，选择使用AUTO_INCREMENT自增主键。</span></li><li><span>尽量不要使用UUID做主键或者是其他自然主键，如身份证号。</span></li><li><span>业务操作时，避免对主键的修改。</span></li></ol><p><span>order by优化</span></p><ol start='' ><li><span>Using filesort ：通过表的索引或全表扫描，读取满足条件的数据行，然后在排序缓冲区sort buffer中完成排序操作，所有不是通过索引直接返回排序结果的排序都叫 FileSort 排序。</span></li><li><span>Using index：通过有序索引顺序扫描直接返回有序数据，这种情况即为 using index， 不需要额外排序，操作效率高。</span></li></ol><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312030303.png" referrerpolicy="no-referrer" alt="image-20220711141131673"></p><ul><li><p><span>order by优化</span></p><ol start='' ><li><span>根据排序字段建立合适的索引，多字段排序时，也遵循最左前缀法则。</span></li><li><span>尽量使用覆盖索引。</span></li><li><span>多字段排序，一个升序一个降序，此时需要注意联合索引在创建时的规则 (ASC/DESC)。</span></li><li><span>如果不可避免的出现filesort， 大数据量排序时，可以适当增大排序缓冲区大小 sort_buffer_size（默认 256k)。</span></li></ol></li><li><p><span>group by优化</span></p><ol start='' ><li><span>在分组操作时，可以通过索引来提高效率。</span></li><li><span>分组操作时，索引的使用也是满足最左前缀法则的。</span></li></ol></li><li><p><span>limit优化</span></p><ul><li><p><span>一个常见又非常头疼的问题就是 limit 2000000,10，此时需要MySQL排序前2000010记录，仅仅返回2000000-2000010的记录，其他记录丢弃，查询排序的代价非常大。（</span><em><strong><span>偏移量大</span></strong></em><span>）</span></p></li><li><p><span>优化思路：一般分页查询时，通过创建覆盖索引能够比较好地提高性能，可以</span><em><strong><span>通过覆盖索引加子查询形式进行优化</span></strong></em><span>。</span></p><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="sql"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="sql"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.1693px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><pre><span>xxxxxxxxxx</span></pre></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">explain</span> <span class="cm-keyword">select</span> <span class="cm-operator">*</span> <span class="cm-keyword">from</span> tb skut <span class="cm-punctuation">,</span> <span class="cm-bracket">(</span><span class="cm-keyword">select</span> id <span class="cm-keyword">from</span> tb sku <span class="cm-keyword">order</span> <span class="cm-keyword">by</span> id <span class="cm-keyword">limit</span> <span class="cm-number">2000000</span><span class="cm-punctuation">,</span><span class="cm-number">10</span><span class="cm-bracket">)</span> a <span class="cm-keyword">where</span> t<span class="cm-variable-2">.id</span> <span class="cm-operator">=</span> a<span class="cm-variable-2">.id</span><span class="cm-punctuation">;</span></span></pre></div></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 74px;"></div><div class="CodeMirror-gutters" style="display: none; height: 74px;"></div></div></div></pre></li></ul></li><li><p><span>count优化</span></p><ul><li><p><span>count的几种用法</span></p><ol start='' ><li><p><span>count （主键）</span></p><p><span>InnoDB 引擎会遍历整张表，把每一行的主键id 值都取出来，返回给服务层。服务层拿到主键后，直接按行进行累加(主键不可能为null)。</span></p></li><li><p><span>count（字段）</span></p><p><span>没有not null 约束：InnoDB 引擎会遍历整张表把每一行的字段值都取出来，返回给服务层，服务层判断是否为null，不为null，计数累加。</span></p><p><span>有not null 约束：InnoDB 引擎会遍历整张表把每一行的字段值都取出来，返回给服务层，直接按行进行累加。</span></p></li><li><p><span>count (1)</span></p><p><span>InnoDB 引擎遍历整张表，但不取值。服务层对于返回的每一行，放一个数字“1〞进去，直接按行进行累加。</span></p></li><li><p><span>count （*）</span></p><p><span>InnoDB引擎并不会把全部字段取出来，而是专门做了优化，不取值，服务层直接按行进行累加。</span></p></li></ol></li><li><p><span>按照效率排序的话，count(字段定count(主键 id)&lt;count(1)约等count(星</span><em><span>)，所以尽量使用count(星</span></em><span>)。</span></p></li></ul></li><li><p><span>update优化</span></p><ul><li><span>InnoDB的行锁是针对索引加的锁，不是针对记录加的锁，并且该索引不能失效，否则会从行锁升级为表锁。</span></li></ul></li></ul><p>&nbsp;</p><p>&nbsp;</p></div></div>
</body>
</html>