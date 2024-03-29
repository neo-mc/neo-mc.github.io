---
layout: page
title:  "הϵѻteric³ features merged in March"
date:   2021-03-08 3:01 +0100
subheadline: "הϵѻteric Features"
meta_teaser: "New features added to הϵѻMCEdit in March – scripting support², CTags quick jumps², QuickPreview³ window, periodic command³ support, MultiSearch³ grepping of any listbox."
teaser: "New features added to הϵѻMCEdit in March – <b>scripting support</b>², <b>CTags quick jumps</b>², <b>QuickPreview window</b>³, <b>periodic command</b>³ support, <b>MultiSearch</b>³ grepping of any listbox."
breadcrumb: true
categories: 
    - changelog
    - news
tags:
    - features
    - mcedit
breadcrumb: true
---

הϵѻMCEdit speeds up gaining multitude of new features. Here is a
brief look at some of them:

## 1. **Scripting support**

A very light but functional scripting interpreter in הϵѻMCEdit –
S-Lang programming language:

{% asciinema_play 395648 %}

The current API (exported S-Lang functions) is available at: 
[https://neomcedit.software/assets/slang_api.pdf](/assets/slang_api.pdf).


## 2. **Quick jumps to tags generated by ctags**

`Alt-\` and `Alt-Shift-\` to go to next/prev tag (eg. a function), and `Alt-*` to
directly jump to file and line of declaration tag of word under
pointer:

{% asciinema_play 395637 %}


## 3. **QuickPreview popup window**

After a ctags command or a jump (like page up), a small window
with an overview of surrounding tags (eg. functions) is displayed:

{% asciinema_play 395624 %}


## 4. **Automatic regeneration and reload of CTags symbols**

The TAGS file can be set up to date by *PeriodicCommand* function
and automatic tags reloading:

{% asciinema_play 395644 %}


## 5. **MultiSearch grepping of any listbox**

An additional input is added under every listbox which can be used
to filter its list. It works with ALL listboxes, eg.:

{% asciinema_play 395632 %}
