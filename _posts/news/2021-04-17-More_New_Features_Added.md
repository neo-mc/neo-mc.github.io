---
layout: page
title:  "April's הϵѻteric³ features"
date:   2021-04-03 9:43 +0100
subheadline: "MCEdit הϵѻteric features"
meta_teaser: "New features added to הϵѻMCEdit in April – CTags completion³, peek at prototype² and status message line."
teaser: "New features added to הϵѻMCEdit in April – <b>CTags completion</b>³, <b>peek at prototype</b>² and <b>status message line</b>."
breadcrumb: true
categories: 
    - changelog
    - news
tags:
    - features
    - news
    - mcedit
---

A set of new features have been recently merged to הϵѻMCEdit. Here's a
incomplete list of them:

## 1. **Completion from Ctags**

It's possible to complete not from entered words, but from Ctags
file – e.g.: for a project that covers `/usr/include/glib`, you
could complete all GLib functions and types, like so:

[![asciicast](https://asciinema.org/a/cp4I3tFfKrLNS9SME7XE2w6Nk.svg)](https://asciinema.org/a/cp4I3tFfKrLNS9SME7XE2w6Nk)

Regular completion is bound to Alt-/ by default, while the TAGS
completion is Shift-Tab.

<br/>

## 2. **Peek at prototype**

If pointer will be placed at a function name and `Ctrl-Alt-p` will be pressed, then
a small window will pop-up with its signature:

[![asciicast](https://asciinema.org/a/IoguysLw2wO8BUzddWRW9k7lG.svg)](https://asciinema.org/a/IoguysLw2wO8BUzddWRW9k7lG)

More, if `Alt-?` will be pressed, then a jump to last shown function's implementation
will be done.


## 3. **Status message**

A feature that has been missing in MCEdit (and MC filemanager) – a status message:

[![asciicast](https://asciinema.org/a/SMFkQjO3ju3nObNmcvefhPWvy.svg)](https://asciinema.org/a/SMFkQjO3ju3nObNmcvefhPWvy)

<br/>
