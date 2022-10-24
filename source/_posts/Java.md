---
title: Java回顾
date: 2022-09-02 17:20:31
tags: Java
categories:
- Web后端
cover: https://pic1.zhimg.com/v2-077a594b1a64d55e95de392755a8aa76_r.jpg?source=172ae18b
---

<h3>Java 是由Sun Microsystems公司于1995年5月推出的Java面向对象程序设计语言和 Java平台的总称。由James Gosling和同
事们共同研发，并在1995年正式推出。后来Sun公司被Oracle（甲骨文）公司收购，Java也随之成为 Oracle公司的产品。</h3>




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


</style><title>Java基础回顾</title>
</head>
<body class='typora-export os-windows'><div class='typora-export-content'>
<div id='write'  class=''><h3 id='java基础回顾'><span>Java基础回顾</span></h3><h4 id='基础'><span>基础</span></h4><ol start='' ><li><p><span>两个整数相除，结果必为整数。（如：8/3，因为最高类型为整数）</span></p></li><li><p><span>&amp;&amp;（一个为false，结果为false），||（一个为true，结果为false），^异或（相同为true，不同为false）。</span></p></li><li><p><span>switch case（适合做值匹配），if（适合做区间匹配）</span></p></li><li><p><span>while循环（不知道循环次数时使用），for循环（明确循环次数时用），do {循环体} while循环（循环体一定执行一次）。</span></p></li><li><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="java"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="java"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation" style=""><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">public</span> <span class="cm-keyword">class</span> <span class="cm-def">ArrayDemo1</span> {</span></pre></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp;<span class="cm-keyword">public</span> <span class="cm-keyword">static</span> <span class="cm-variable-3">void</span> <span class="cm-variable">main</span>(<span class="cm-variable-3">String</span>[] <span class="cm-variable">args</span>) {</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp;<span class="cm-comment">// 格式一(动态初始化)</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp;<span class="cm-variable-3">int</span>[] <span class="cm-variable">arr1</span> <span class="cm-operator">=</span> <span class="cm-keyword">new</span> <span class="cm-variable-3">int</span>[<span class="cm-number">3</span>]; <span class="cm-comment">// 数组的长度(这里为3)必须指定</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp;</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp;<span class="cm-comment">// 格式二(静态初始化)</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp;<span class="cm-variable-3">int</span>[] <span class="cm-variable">arr2</span> <span class="cm-operator">=</span> <span class="cm-keyword">new</span> <span class="cm-variable-3">int</span>[]{<span class="cm-number">1</span>, <span class="cm-number">2</span>, <span class="cm-number">3</span>}; <span class="cm-comment">// 这里数组长度不能指定，花括号里面的元素个数就是数组长度</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp;<span class="cm-comment">// 或者按照下面的简写形式</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp;<span class="cm-variable-3">int</span>[] <span class="cm-variable">arr3</span> <span class="cm-operator">=</span> {<span class="cm-number">1</span>, <span class="cm-number">2</span>, <span class="cm-number">3</span>}; <span class="cm-comment">// 格式二的简写形式</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp;  }</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;">}</span></pre></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 321px;"></div><div class="CodeMirror-gutters" style="display: none; height: 321px;"></div></div></div></pre></li><li><p><span>Java参数的传递本质上都是</span><em><strong><span>值传递</span></strong></em><span>，基本数据类型传递的是数据值，引用类型传递的是在堆里面的内存地址。</span></p></li><li><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312025857.png" referrerpolicy="no-referrer" alt="image-20220708115249661"></p></li><li><p><span>成员变量的分类和访问分别是什么样的？</span></p><ul><li><p><span>静态成员变量（类变量，由static修饰，只加载一次，可以被共享） 通过 </span><em><strong><span>类名.静态成员变量访问</span></strong></em></p></li><li><p><span>实例成员变量（无static，属于对象）</span></p><p><span>通过 </span><em><strong><span>对象.实例成员变量访问</span></strong></em></p></li></ul><p><span>两种变量在什么情况下定义？</span></p><ul><li><span>静态成员变量：</span><em><strong><span>表示在线人数等需要被共享的信息</span></strong></em></li><li><span>实例成员变量：对象需要的信息不同的时候</span></li></ul><p><span>静态方法：</span><em><strong><span>以执行通用功能为目的或者需要方便访问</span></strong></em></p><p><span>实例方法：</span><em><strong><span>表示对象自己的行为</span></strong></em></p></li><li><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312025462.png" referrerpolicy="no-referrer" alt="image-20220708121618997"></p></li><li><p><span>String变量是</span><em><strong><span>不可变字符串类型</span></strong></em><span>，一但创建就不可变。</span><em><strong><span>变的是经过运算后指向了新的地址，原数据在字符串常量池中不变。</span></strong></em></p></li><li><p><span>Sting以&quot;&quot;创建的数据储存在字符串常量池中，new创建的储存在堆中。通过两种结合的创建方式，常量池和堆都有。</span></p></li><li><p><span>数组和集合的存储个数问题？</span></p><ul><li><span>数字定义后类型确定，长度固定</span></li><li><span>集合类型可以不固定，长度可以扩展</span></li></ul><p><span> 数组和集合的应用场景？</span></p><ul><li><span>数字适用于长度固定，数据类型确定的场景</span></li><li><em><strong><span>集合适用于长度不固定，且需要增删改的场景</span></strong></em></li></ul></li><li><p><em><strong><span>集合中存储的是每个对象的内存地址。</span></strong></em></p></li><li><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312025056.png" referrerpolicy="no-referrer" alt="image-20220708122153137"></p></li><li><p><span>子类初始化之前，一定要</span><strong><em><span>调用父类构造器先完成父类数据空间的初始</span></em><span>化</span></strong><span>。（即先调用父类的构造器，再调用子类自己的构造器）</span></p></li><li><p><span>注意：</span><em><strong><span>this(…）super(…）都只能放在构造器的第一行</span></strong></em><span>，所以二者不能共存在同一个构造器中。</span></p></li><li><p><span>final修饰符</span></p><ul><li><p><span>类：不可被继承</span></p></li><li><p><span>方法：不可被重写</span></p></li><li><p><span>变量：值不能再变</span></p><ol start='' ><li><span>基础数据类型：数据值不能再变化</span></li><li><span>引用数据类型：</span><em><strong><span>储存的内存地址值不能再变化，但是地址指向的对象内容是可以改变的</span></strong></em><span>。（通过反射再用setter设置值，因为实例对象一旦初始化分配的内存地址是固定的）</span></li></ol></li></ul></li><li><p><span>抽象类</span></p><ul><li><span>类有的成员</span><em><strong><span>（成员变量、方法、构造器）抽象类都具备</span></strong></em><span>。</span></li><li><span>抽象类中不一定有抽象方法，有抽象方法的类一定是抽象类。</span></li><li><em><strong><span>一个类继承了抽象类必须重写完抽象类的全部抽象方法，否则这个类也必须定义成抽象类。</span></strong></em></li><li><em><strong><span>不能用abstract修饰变量、代码块、构造器。</span></strong></em></li></ul></li><li><p><span>抽象类和接口</span></p><ul><li><span>抽象类表示它是什么，接口表示它能做什么。</span></li><li><span>当</span><em><strong><span>需要为一些类提供公共的实现代码时，应优先考虑抽象类。</span></strong></em><span>因为抽象类中的非抽象方法可以被子类继承下来，使实现功能的代码更简单。</span></li><li><span>当</span><em><strong><span>注重代码的扩展性跟可维护性时，应当优先采用接口</span></strong></em><span>。①接口与实现它的类之间可以不存在任何层次关系，</span><em><strong><span>接口可以实现毫不相关类的相同行为</span></strong></em><span>，比抽象类的使用更加方便灵活；②接口只关心对象之间的交互的方法，而不关心对象所对应的具体类。</span><em><strong><span>接口是程序之间的一个协议</span></strong></em><span>，比抽象类的使用更安全、清晰。一般使用接口的情况更多。</span></li></ul></li><li><p><em><span>多态：</span><strong><span>同类型的对象，执行同一行为，表现出不同的行为特征。</span></strong></em></p></li></ol><h4 id='集合'><span>集合</span></h4><ol start='' ><li><p><span>数组和集合的元素存储的个数问题。</span></p><ul><li><span>数组定义后类型确定，长度固定。</span></li><li><span>集合类型可以不固定，大小是可变的。</span></li></ul><p><span>数组和集合存储元素的类型问题。</span></p><ul><li><em><strong><span>数组可以存储基本类型和引用类型的数据。</span></strong></em></li><li><em><strong><span>集合只能存储引用数据类型的数据。</span></strong></em></li></ul><p><span>数组和集合适合的场景</span></p><ul><li><span>数组适合做数据个数和类型确定的场景。</span></li><li><span>集合适合做数据个数不确定，且要做增删元素的场景。</span></li></ul></li><li><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312025596.png" referrerpolicy="no-referrer" alt="image-20220708125942065"></p></li><li><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312025796.png" referrerpolicy="no-referrer" alt="image-20220708130017882"></p></li><li><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312025568.png" referrerpolicy="no-referrer" alt="image-20220708130855573"></p></li><li><p><em><strong><span>集合储存的是对象的内存地址</span></strong></em></p></li><li><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312025814.png" alt="image-20220708131251767"  /></p></li><li><p><span>ArrayList（</span><em><strong><span>有序，可重复</span></strong></em><span>）</span></p><ul><li><em><strong><span>底层基于数组</span></strong></em><span>，根据索引定位元素，增删需要做元素移位操作。</span><em><strong><span>（查询效率高，增删效率低）</span></strong></em></li><li><span>第一次创建集合并添加第一个元素的时候，</span><em><strong><span>创建一个默认长度为10的数组</span></strong></em><span>。</span></li><li><em><strong><span>每次扩容为之前的1.5倍</span></strong></em></li></ul></li><li><p><em><strong><span>Set集合无索引，所以不能通过普通for循环进行遍历，也不能通过索引获取元素</span></strong></em></p></li><li><p><span>为什么要重写hashCode和equals方法？</span></p><ul><li><span>重写equals方法后相等的两个对象，hashCode一定相等，不相等的两个对象，hashCode可能相等。（哈希冲撞）</span></li><li><span>不重写hashCode方法是根据内存地址结合hash算法进行运算，所以hashCode几乎不会存在相同的可能，这违放了jdk文档的规定。</span></li></ul></li><li><p><span>HashSet（</span><em><strong><span>无序，不重复</span></strong></em><span>）</span></p><ul><li><span>底层为哈希表（</span><em><strong><span>数组+链表+（红黑树 jdk1.8版本后）</span></strong></em><span>链表长度大于8，且集合长度大于64）</span></li><li><em><strong><span>创建一个默认长度为16的数组</span></strong></em></li><li><span>根据元素的哈希值跟数组的长度求余计算出应存入的位置（哈希算法）</span></li><li><span>判断当前位置是否为null， 如果是null直接存入。</span></li><li><span>如果位置不为null，表示有元素，则调用equals方法比较，如果一样，则不存，如果不一样，则存入数组。</span></li><li><span>扩容因子为0.75（16*0.75=12），扩容为之前的两倍。</span></li></ul></li><li><p><span>LinkHashSet（有序，不重复）</span></p><ul><li><em><strong><span>底层依然是哈希表，只不过增加了双向链表。</span></strong></em></li></ul></li><li><p><span>TreeSet（</span><em><strong><span>排序，不重复</span></strong></em><span>）</span></p><ul><li><em><strong><span>底层基于红黑树实现排序</span></strong></em></li><li><span>默认按照升序排序</span></li></ul></li><li><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312025906.png" referrerpolicy="no-referrer" alt="image-20220708134123406"></p></li><li><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312026538.png" referrerpolicy="no-referrer" alt="image-20220708134443818"></p></li></ol><h4 id='异常'><span>异常</span></h4><ol start='' ><li><p><span>异常分为</span><em><strong><span>编译时异常</span></strong></em><span>（必须处理才能通过编译）和</span><em><strong><span>运行时异常</span></strong></em></p></li><li><p><span>异常处理的方式</span></p><ol start='' ><li><p><span>throws：用在方法上，可以将方法内部出现的异常抛出去给本方法的调用者处理。</span></p><ul><li><span>这种方式并不好，发生异常的方法自己不处理异常，如果异常最终抛出去给虚拟机将引起程序死亡。</span></li></ul></li><li><p><span>try…catch：监视捕获异常，用在方法内部，可以将方法内部出现的异常直接捕获处理。</span></p><ul><li><span>这种方式还可以，发生异常的方法自己独立完成异常的处理，程序可以继续往下执行。</span></li></ul></li><li><p><span>前两者结合</span></p><ul><li><pre class="md-fences md-end-block ty-contain-cm modeLoaded" spellcheck="false" lang="java"><div class="CodeMirror cm-s-inner cm-s-null-scroll CodeMirror-wrap" lang="java"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 10.3385px; left: 4px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" tabindex="0" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;"></textarea></div><div class="CodeMirror-scrollbar-filler" cm-not-content="true"></div><div class="CodeMirror-gutter-filler" cm-not-content="true"></div><div class="CodeMirror-scroll" tabindex="-1"><div class="CodeMirror-sizer" style="margin-left: 0px; margin-bottom: 0px; border-right-width: 0px; padding-right: 0px; padding-bottom: 0px;"><div style="position: relative; top: 0px;"><div class="CodeMirror-lines" role="presentation"><div role="presentation" style="position: relative; outline: none;"><div class="CodeMirror-measure"><span><span>​</span>x</span></div><div class="CodeMirror-measure"></div><div style="position: relative; z-index: 1;"></div><div class="CodeMirror-code" role="presentation" style=""><div class="CodeMirror-activeline" style="position: relative;"><div class="CodeMirror-activeline-background CodeMirror-linebackground"></div><div class="CodeMirror-gutter-background CodeMirror-activeline-gutter" style="left: 0px; width: 0px;"></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">try</span>{</span></pre></div><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; <span class="cm-variable-3">String</span> <span class="cm-variable">str</span> <span class="cm-operator">=</span> <span class="cm-atom">null</span>;</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; <span class="cm-variable">System</span>.<span class="cm-variable">out</span>.<span class="cm-variable">println</span>(<span class="cm-variable">str</span>.<span class="cm-variable">equals</span>(<span class="cm-string">""</span>));</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; <span class="cm-variable">System</span>.<span class="cm-variable">out</span>.<span class="cm-variable">println</span>(<span class="cm-string">"try即将结束"</span>);</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; }<span class="cm-keyword">catch</span> (<span class="cm-variable">NullPointerException</span> <span class="cm-variable">e</span>){</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; <span class="cm-comment">//抛出异常对象</span></span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;<span class="cm-keyword">throw</span> <span class="cm-keyword">new</span> <span class="cm-variable">MyException</span>(<span class="cm-string">"Demo04 第13行的 str 可能出现 null "</span>);</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; }</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; &nbsp; &nbsp; <span class="cm-variable">System</span>.<span class="cm-variable">out</span>.<span class="cm-variable">println</span>(<span class="cm-string">"程序即将结束"</span>);</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"> &nbsp; }</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;">}</span></pre><pre class=" CodeMirror-line " role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span cm-text="" cm-zwsp="">
</span></span></pre></div></div></div></div></div><div style="position: absolute; height: 0px; width: 1px; border-bottom: 0px solid transparent; top: 444px;"></div><div class="CodeMirror-gutters" style="display: none; height: 444px;"></div></div></div></pre></li></ul></li></ol></li></ol><h4 id='io'><span>IO</span></h4><ol start='' ><li><p><span>字符串常见的字符底层组成是什么样的？</span></p><ul><li><em><strong><span>英文和数字</span></strong></em><span>等在任何国家的字符集中都</span><em><strong><span>占1个字节</span></strong></em></li><li><em><strong><span>GBK字符</span></strong></em><span>中一个中文字符</span><em><strong><span>占2个字节</span></strong></em></li><li><em><strong><span>UTF-8编码</span></strong></em><span>中一个中文1般</span><em><strong><span>占3个字节</span></strong></em></li></ul></li><li><p><span>编码前的字符集和编码好的字符集有什么要求？</span></p><ul><li><span>必须一致，否则会出现中文字符乱码</span></li><li><span>英文和数字在任何国家的编码中都不会乱码</span></li></ul></li><li><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312026641.png" referrerpolicy="no-referrer" alt="image-20220708135848582"></p></li><li><p><span>缓冲流自带缓冲区(8k)、可以提高原始字节流、宇符流读写数据的性能</span></p></li><li><p><span>字符输入转换流InputstreamReader作用：</span></p><ul><li><span>可以解决字符流读取不同编码乱码的问题</span></li><li><span>public InputStreamReader(InputStream is, String charset):可以指定编码把原始字节流转换成字符流，如此字符流中的字符不乱码。</span></li></ul></li><li><p><span>对象序列化将内存中的数据储存到文件中，称为对象的序列化。</span></p></li><li><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312026804.png" referrerpolicy="no-referrer" alt="image-20220708141039990"></p></li></ol><h4 id='多线程'><span>多线程</span></h4><ol start='' ><li><p><span>多线程的实现方案：</span></p><ul><li><p><span>继承Thread类</span></p><ol start='' ><li><span>定义一个子类继承Thread类，重写run方法</span></li><li><span>调用start方法启动线程</span></li></ol></li><li><p><span>实现Runnable接口</span></p><ol start='' ><li><span>定义一个Runnable类实现Runnable接口，重写run方法</span></li><li><span>创建Runnable任务对象，交给Thread类</span></li><li><span>调用start方法启动线程</span></li></ol></li><li><p><span>实现Callable，FutureTask接口</span></p><ol start='' ><li><p><span>得到任务对象</span></p><ul><li><span>定义类实现Callable接口，重写call方法</span></li><li><span>用FutureTask把Callable对象封装成线程任务对象</span></li></ul></li><li><p><span>把线程任务对象交给Thread处理</span></p></li><li><p><span>调用start方法启动线程</span></p></li><li><p><span>可通过FutureTask的get方法获取callable返回的结果</span></p></li></ol></li></ul></li><li><figure><table><thead><tr><th style='text-align:center;' ><span>方式</span></th><th style='text-align:center;' ><span>优点</span></th><th style='text-align:center;' ><span>缺点</span></th></tr></thead><tbody><tr><td style='text-align:center;' ><span>继承Thread类</span></td><td style='text-align:center;' ><span>编程简单</span></td><td style='text-align:center;' ><span>扩展差，无法得到返回结果</span></td></tr><tr><td style='text-align:center;' ><span>实现Runnable接口</span></td><td style='text-align:center;' ><span>扩展强</span></td><td style='text-align:center;' ><span>编程相对复制，无返回结果</span></td></tr><tr><td style='text-align:center;' ><span>实现Callable接口</span></td><td style='text-align:center;' ><span>扩展强，有返回结果</span></td><td style='text-align:center;' ><span>编程复杂</span></td></tr></tbody></table></figure></li><li><p><span>锁对象的规范要求</span></p><ul><li><span>规范上：建议使用共享资源作为锁对象。</span></li><li><span>对于实例方法建议使用</span><em><strong><span>this作为锁对象</span></strong></em><span>。</span></li><li><span>对于静态方法建议使用</span><em><strong><span>字节码（类名.class）对象作为锁对象</span></strong></em><span>。</span></li></ul></li><li><p><span>同步方法是如何保证线程安全的？</span></p><ul><li><span>对出现问题的核心方法使用synchronized修饰（增删改）</span></li><li><span>每次只能一个线程占锁进入访问</span></li></ul></li><li><p><span>临时线程什么时候创建啊？ </span><strong><span>**</span></strong><span>**</span></p><ul><li><span>新任务提交时发现</span><em><strong><span>核心线程都在忙，任务队列也满了</span></strong></em><span>，并且</span><em><strong><span>还可以创建临时线程</span></strong></em><span>，此时才会创建临时线程。</span></li></ul><p><span>什么时候会开始拒绝任务？ </span><strong><span>**</span></strong><span>**</span></p><ul><li><em><strong><span>核心线程和临时线程都在忙，任务队列也满了</span></strong></em><span>，新的任务过来的时候才会开始任务拒绝。</span></li></ul></li></ol><h4 id='反射'><span>反射</span></h4><ol start='' ><li><p><span>反射的第一步是什么？</span></p><ul><li><span>获取Class类对象，如此才可以解析类的全部成分</span></li></ul><p><span>获取Class类的对象的三种方式</span></p><ol start='' ><li><span>Class c7 =Class.forName( “全类名〞）；</span></li><li><span>Class c2=类名.class</span></li><li><span>Class C3=对象•getclass();</span></li></ol></li><li><p><span>利用反射技术获取构造器对象的方式</span></p><ul><li><span>getDeclaredConstructors()</span></li><li><span>getDeclaredConstructor (Class&lt;?&gt;... parameterTypes)</span></li></ul><p><span>反射得到的构造器可以做什么？</span></p><ol start='' ><li><p><span>依然是创建对象的</span></p><ul><li><span>public newlnstance(Object... initargs)</span></li></ul></li><li><p><span>如果是非public的构造器，需要打开权限（暴力反射），然后再创建对象</span></p><ul><li><span>setAccessible(boolean)</span></li><li><span>反射可以破坏封装性，私有的也可以执行了。</span></li></ul></li></ol></li><li><p><span>利用反射技术获取成员变量的方式</span></p><ul><li><p><span>获取类中成员变量对象的方法</span></p><ol start='' ><li><span>getDeclaredFields()</span></li><li><span>getDeclaredField (String name)</span></li></ol></li></ul><p><span>反射得到成员变量可以做什么？</span></p><ul><li><p><span>依然是在某个对象中取值和赋值。</span></p><ol start='' ><li><span>void set (Object obj, Object value)</span></li><li><span>Object get (Object obj)</span></li></ol></li><li><p><span>如果某成员变量是非public的，需要打开权限（暴力反射），然后再取值、赋值</span></p><ul><li><span>setAccessible(boolean)</span></li></ul></li></ul></li><li><p><span>利用反射技术获取成员方法对象的方式</span></p><ul><li><p><span>获取类中成员方法对象</span></p><ol start='' ><li><span>getDeclaredMethods()</span></li><li><span>getDeclaredMethod (String name, Class&lt;?›... parameterTypes)</span></li></ol></li></ul><p><span> 反射得到成员方法可以做什么？</span></p><ul><li><p><span>依然是在某个对象中触发该方法执行。</span></p><ul><li><span>Object invoke(Object obj, Object... args)</span></li></ul></li></ul></li><li><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312026610.png" referrerpolicy="no-referrer" alt="image-20220708150107724"></p></li><li><p><span>反射的作用-绕过编译阶段为集合添加数据</span></p><ul><li><span>反射是作用在运行时的技术，此时集合的泛型將不能产生约束了，此时是可以为集合存入其他任意类型的元素的。</span></li></ul></li><li><p><span>泛型只是在编译阶段可以约束集合只能操作某种数据类型，在编译成Class文件进入运行阶段的时候，其真实类型都是ArrayList了，</span><em><strong><span>泛型相当于被擦除</span></strong></em><span>了。</span></p></li><li><p><span>反射的作用？</span></p><ul><li><span>可以在运行时得到一个类的全部成分然后操作。</span></li><li><span>可以破坏封装性。（很突出）</span></li><li><span>也可以破坏泛型的约束性。（很突出）</span></li><li><span>更重要的用途是适合：做Java高级框架</span></li></ul></li><li><p><span>动态代理</span><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312026214.png" referrerpolicy="no-referrer" alt="image-20220708145702385"></p></li></ol><h4 id='网络编程'><span>网络编程</span></h4><ol start='' ><li><p><span>实现网络编程关键的三要素</span></p><ul><li><span>IP地址：设备在网络中的地址，是唯一的标识。</span></li><li><span>端口：应用程序在设备中唯一的标识。</span></li><li><span>协议：数据在网络中传输的规则，常见的协议有UDP协议和TCP协议。</span></li></ul><p><span>IP</span></p><ul><li><p><span>公网地址、和私有地址（局域网使用）。</span></p></li><li><p><span>192.168. 开头的就是常见的局域网地址，范围即为192.168.0.0--192.168.255.255，专门为组织机构内部使用。</span></p></li><li><p><span>IP常用命令：</span></p><ol start='' ><li><span>ipconfig：查看本机IP地址</span></li><li><span>ping IP地址：检查网络是否连通</span></li><li><span>特殊IP地址：本机IP：127.0.0.1或者locathost：称为回送地址也可称本地回环地址，只会寻找当前所在本机。</span></li></ol></li></ul><p><span>端口</span></p><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312026939.jpg" referrerpolicy="no-referrer" alt="95bad85d623d00fb1c8785e88db4d3f"></p><p><span>协议</span></p><p><img src="https://raw.githubusercontent.com/Valynd/picture/main/202208312026157.jpg" referrerpolicy="no-referrer" alt="8d3490b5a56fa25412ca38edaadf592"></p></li><li><p><span>TCP</span></p><ul><li><p><span>三次握手</span></p><ol start='' ><li><span>客户端向服务器端发送SYN连接请求报文</span></li><li><span>服务器端接收到SYN报文后，为这次连接分配资源，并向客户端发送SYN—ACK报文</span></li><li><span>客户端接收到 ACK 报文后也向服务器端发生 ACK 报文，并分配资源，这样 TCP 连接就建立了。</span></li></ol><p><span>三次握手的关键是为了确保双方收发都没有问题</span></p><p><span>如果只有两次握手，这时候客户端无响应，会浪费服务器端的资源</span></p></li><li><p><span>四次挥手</span></p><ol start='' ><li><span>客户端向服务器发送FIN报文，用来关闭客户端到服务器端的数据传送，客户端进入FIN_WAIT_1状态。</span></li><li><span>服务器接收到FIN报文后，向客户端发送ACK，服务器端进入CLOSE_WAIT状态。</span></li><li><span>向客户端发送FIN报文，用来关闭服务器端到客户端的数据传送，客户端进入LAST_ACK状态。</span></li><li><span>客户端收到FIN报文后，客户端进入TIME_WAIT状态，发送ACK给服务器端，服务器端进入CLOSED状态，完成四次握手。</span></li></ol></li></ul><p>&nbsp;</p><p>&nbsp;</p><p>&nbsp;</p></li></ol><p>&nbsp;</p></div></div>
</body>
</html>