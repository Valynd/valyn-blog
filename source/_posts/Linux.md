---
title: Linux基础命令
date: 2022-09-02 19:04:39
tags: Linux
categories:
- Web后端
cover: https://pic.mac89.com/pic/202008/25102612_20a4134b01.jpeg
---

<h3>Linux，全称GNU/Linux，是一种免费使用和自由传播的类UNIX操作系统，其内核由林纳斯·本纳第克特·托瓦兹于1991年10月5日首次
发布，它主要受到Minix和Unix思想的启发，是一个基于POSIX的多用户、多任务、支持多线程和多CPU的操作系统。</h3>



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


</style><title></title>
</head>
<body class='typora-export os-windows'><div class='typora-export-content'>
<div id='write'  class=''><h3 id='linux基础及命令'><span>Linux基础及命令</span></h3><h3 id='基础知识简述'><span>基础知识简述</span></h3><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312029131.png" referrerpolicy="no-referrer" alt="image-20220711142702022"></p><p><span>操作系统</span></p><ul><li><span>主要作用是管理好硬件设备，并为用户和应用程序提供一个简单的接口，以便于使用，作为中间人，连接软件和硬件</span></li></ul><p><span>Linux发现历程</span></p><ul><li><span>Unix-&gt;Minix-&gt;Linux</span></li></ul><p><span>命令行程序</span></p><ul><li><span>终端 terminal</span></li></ul><h3 id='基础命令使用'><span>基础命令使用</span></h3><h4 id='cd-切换文件夹'><span>cd 切换文件夹</span></h4><ol><li><span>cd /home    绝对路径 以根目录开头</span></li><li><span>cd admin    相等路径 不以根目录开头</span></li><li><span>cd ..   返回上级目录</span></li><li><span>cd ~   到自己的家目录 /home/admin</span></li><li><span>cd -   电视回看功能</span></li></ol><h4 id='pwd-查看当前目录'><span>pwd 查看当前目录</span></h4><h4 id='ls-查看目录的内容'><span>ls 查看目录的内容</span></h4><ol><li><span>ls -l   显示列表详情</span></li><li><span>ls -lh   把文件的大小以人性化的方式显示</span></li><li><span>ls -a   显示所有文件，包括隐藏文件，隐藏文件以.开头</span></li><li><span>ll   等价于ls -l</span></li></ol><h4 id='mkdir-创建文件夹'><span>mkdir 创建文件夹</span></h4><ol><li><p><span>mkdir tupian   在当前目录创建文件夹</span></p></li><li><p><span>mkdir /home/valyn/tupian   以绝对路径创建文件夹</span></p></li><li><p><span>mkdir /home/admin/a/tupian -p   如果上级目录不存在，加上-p自动创建父目录</span></p></li><li><p><span>mkdir a b   在当前目录创建多个文件夹</span></p></li><li><p><span>mkdir a/{c,d}    在指定目录下创建多个文件夹</span></p></li><li><p><span>mkdir .abc   以.开头 是创建隐藏文件夹</span></p><ul><li><span>任何目录下都有至少两个目录 .和..</span></li><li><span>.代表当前目录</span></li><li><span>..代表上级目录</span></li></ul></li></ol><h4 id='touch-创建空文件夹'><span>touch 创建空文件夹</span></h4><ol><li><span>touch abc.txt   在当前目录下创建 如果指定了目录，必须保证上级目录存在</span></li><li><span>touch .abc   创建隐藏文件</span></li><li><span>gedit abc.txt   使用笔记本打开文件</span></li></ol><h4 id='rm-删除文件'><span>rm 删除文件</span></h4><ol><li><p><span>rm a.txt   删除文件</span></p></li><li><p><span>rm -r abc   删除文件夹</span></p></li><li><p><span>rm -r *   不能删除隐藏文件 .和..删除不掉</span></p></li><li><p><span>drwxrwxr-x       d 代表文件夹 - 代表文件</span></p><p><span>rwx rwx r-x       r可读 w可写 x可执行</span></p><p><span>第一组指文件的拥有者的权限，第二组代表文件拥有的组的权限，第三组代表其他用户的权限</span></p><p><span>ls   查看其他目录的内容</span></p><p><span>ls *txt   查看当前目录下的所有以txt结尾的文件</span></p></li></ol><h4 id='cp-拷贝文件'><span>cp 拷贝文件</span></h4><ol><li><span>cp 1.txt 2.txt</span></li><li><span>cp -n abc abc_bak   拷贝文件夹</span></li></ol><h4 id='mv-移动-重命名'><span>mv 移动 重命名</span></h4><ol><li><span>mv 1.txt 2.txt   重命名</span></li><li><span>mv 1.txt ~   移动到指定目录</span></li></ol><h4 id='-重定向'><span>&gt; 重定向</span></h4><ol><li><span>ls &gt; 1.txt   把命令返回的结果输出到文件中，会覆盖之前的数据，默认情况命令返回的结果是显示在屏幕中</span></li><li><span>ls &gt;&gt;1.txt   把命令返回的结果输出到文件中，追加的方式</span></li></ol><h4 id='cat-查看文件内容'><span>cat 查看文件内容</span></h4><ol><li><span>cat 1.txt   把文件的内容全部显示到屏幕中</span></li><li><span>cat 1.txt 2.txt</span></li><li><span>cat 1.txt 2.txt &gt; 3.txt   把多个文件的内容合井到新的文件中</span></li></ol><h4 id='more-查看文件的内容可以分页显示'><span>more 查看文件的内容，可以分页显示</span></h4><ol><li><span>more 1.txt   查看内容多的文件，按空格键往下翻页，按b按键往回翻页，按q键退出</span></li></ol><h4 id='-管道'><span>| 管道</span></h4><ol><li><span>ls -l / | more   把左边的命令返回的结果交给右边命令进行处理</span></li></ol><h4 id='查看历史命令'><span>查看历史命令</span></h4><h4 id='ln-链接'><span>ln 链接</span></h4><ul><li><p><span>软链接 软连接本身不存储内容，只记录源文件的名称</span></p><ol><li><span>ln -s 1.txt 1_link 给1.txt   创建一个软链接，相当于windows中的快捷方式</span></li><li><span>ln -s 1.txt ~/1_link   给其他目录创建一个软链接，如果源文件不写绝对路径，软链接指向的文件是不存在的</span></li><li><span>ln -s aba abc_link 给目录创建软链接</span></li></ol></li><li><p><span>硬链接本身占空间，相当于把源文件复制一份，与源文件同步变化，删除硬链接文件不影响源文件，不能给目录创建硬链接</span></p><ul><li><span>使用ll查看时，有一个数宇，代表有几个文件能同步发生变化</span>
<span>ln 1.txt 1_hard_link</span></li></ul></li></ul><h4 id='grep-查找文件内容'><span>grep 查找文件内容</span></h4><ol><li><span>grep hello test. txt   在某个文件中查找包含hello的内容，只要一行中有he11o会把整行显示</span></li><li><span>grep -niv hello test.txt   n显示查找到的内容的行号，i查找时不区分大小号，v反向查找，查找不包含hel1o的行</span></li><li><span>grep -n hello /home/admin   查找整个目录中的所有文件，包含hello的内容</span></li></ol><h4 id='find-查找文件'><span>find 查找文件</span></h4><ol><li><span>find /home -name 1.txt   在/home 目录下查找文件名为1.txt 的文件</span></li><li><span>find /home -name &#39;*txt&#39;   在/home 目录下查找以txt结尾的文件</span></li></ol><h4 id='tar-归档-打包'><span>tar 归档 打包</span></h4><ol><li><p><span>打包</span></p><p><span>tar cvf a.tar 1.txt 2.txt    f必须放在最后，f后面的第一个参数代表要生成的文件名，后面所有的參数是要打包的文件</span></p></li><li><p><span>列出包里面的文件</span></p><p><span>tar tf a.tar</span></p></li><li><p><span>解包</span></p><p><span>tar xvf a.tar   如果没写目录，把包里面的文件解开放到当前目录</span></p><p><span>tar xvf a.tar -C tar 解包到指定的文件夹，文件夹需要提前创建好</span></p></li><li><p><span>压缩</span></p><ol><li><p><span>打包</span></p><p><span>tar cf a.tar *   生产a.tar文件</span></p></li><li><p><span>压缩</span></p><p><span>gzip -r a.tar   生成a.tar.gz文件</span></p></li></ol></li><li><p><span>解压</span></p><ul><li><p><span>解压</span></p><p><span>gzip -d a.tar.gz   生成a.tar文件</span></p></li><li><p><span>解包</span></p><p><span>tar xf a.tar -C ~/atar   解包到指定的文件夹</span></p></li></ul></li><li><p><span>一步到位</span></p><ol><li><p><span>打包并且压缩</span></p><p><span>tar czf b.tar.gz *txt   以gzip的方式打包且压缩</span></p></li><li><p><span>解压且解包</span></p><p><span>tar zxf b.tar.gz -C btar   以gzip的方式解压且解包</span></p></li></ol></li></ol><h4 id='bzip2'><span>bzip2</span></h4><ol><li><span>tar jcf j.tar .bz2 *txt</span></li><li><span>tar xjf j.tar.bz2 -C jtar</span></li></ol><h4 id='zip'><span>zip</span></h4><ol><li><span>zip -r xx *txt   zz代表要生成的压缩文件，不需要写扩展名，会自动生成zip扩展名</span></li><li><span>unzip -d zz zz.zip   解压时会自动创建目录</span></li></ol><p><span>压缩率 zip&lt;gzip&lt;bzip2</span>
<span>通用率 zip&gt;gzip&gt;bzip2</span></p><h4 id='who-查看当前登录的用户'><span>who 查看当前登录的用户</span></h4><ol><li><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="linux"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="linux"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation"><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;">admin pts/0</span></pre></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;">admin tty1</span></pre></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 49px;"></div><div class="CodeMirror-gutters" style="display: none; height: 49px;"></div></div></div></pre><p><span>pts代表一个终端 tty代表用户登录了操作系统</span></p><p><span>pkill -kill -t tty1</span></p></li><li><p><span>reboot   不需要权限</span></p></li><li><p><span>shutdown 需要root权限</span></p></li></ol><h4 id='chmod-设置权限'><span>chmod 设置权限</span></h4><ol><li><p><span>u 文件的拥有者</span></p></li><li><p><span>g 文件的拥有的组</span></p></li><li><p><span>o 其他用户</span></p></li><li><p><span>a 所有用户</span></p></li><li><p><span>+添加权限</span></p></li><li><p><span>-删除权限</span></p></li><li><p><span>=设置权限（把之前的权限换成新的权限）</span></p></li><li><p><span>chmod u+r test.txt   给文件的拥有者添加r（读）权限</span></p><ul><li><span>r（可读）</span></li><li><span>w（可写）</span></li><li><span>x（可执行）</span></li><li><span>-（无权限）</span></li></ul><p><span>chmod u=r,g+w,o-r test.txt   给自己设限读权限，所属组添加写权限，其他人删除读权限</span></p><ul><li><span>r 4</span></li><li><span>w 2</span></li><li><span>x 1</span></li><li><span>-0</span></li></ul><p><span>chmod 123 test.txt   第一位数字代表自己的权限，第二代表自己组的权限，第三位代表其他人的权限</span></p><p><span>3=1+2 代表wx权限</span></p></li></ol><h4 id='vim'><span>vim</span></h4><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312029132.png" referrerpolicy="no-referrer" alt="image-20220711155327653"></p></div></div>
</body>
</html>