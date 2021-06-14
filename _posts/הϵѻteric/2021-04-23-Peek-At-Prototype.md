---
layout: page
title:  "Peek At Prototype"
sidebar: left
date:   2021-05-10 13:17 +0100
subheadline: "MCEdit הϵѻteric² features"
meta_teaser: "NeoMCEdit has a support for showing the signature of a function under the pointer, in a small window appearing at bottom of display."
teaser: "הϵѻMCEdit has a support for showing the signature of a function under the pointer, in a small window appearing at bottom of display."
breadcrumb: true
categories: 
    - news
    - docs
tags:
    - הϵѻteric²
    - features
    - news
    - mcedit
---


# Using The Feature

If text pointer will be placed at a function name and `Ctrl-s`
will be pressed, then a **small window containing its signature
will pop-up** at bottom of the display. Here's an asciicast which
presents this feature: 

{% asciinema_play 420119 %}

More, if **Alt-?** will be following pressed, then a **jump to
implementation** of last requested function's prototype will be
done. 

Thus, it will be to, i.e.: in case of C language, **a .c, not a .h
file** (if possible), or similar for a given, supported language.
Remember that tags **aren't unique** and can repeat but with
different pointers – for example one to a **.c**, the other to a
**.h** file. NeoMCEdit in general prefers **C**-file unless the
jump is limited to be within the same file from the beginning.

## Accessing Libraries' Implementations

You could have utilized this by downloading **a library's source
code** into root of your project tree (**untracked**) – to have
access **not only** to its function's **prototypes** (accessible
via the symlink to the includes as outlined in  [**Completion From
CTags**][1]), but also to **implementations** (it
might be useful, for example, to occasionally be able to
**exactly** see what a library function does). 

Eg.: to index **GLib's** source you could've simply cloned it to
an untracked **subdirectory** in your project's tree (before
running the `ctags -e …` command) by: `git clone
https://gitlab.gnome.org/GNOME/glib.git ~/project/glib-src`, so
that CTags can access and index it **normally** when   processing
also the **project's own symbols**.

CTags can be run via eg.: the Makefile target as given in the
[**article on CTags completion**][1], from PeriodicCommand tool. 

The above asciicast utilizes this which is being presented by the
jump to the `g_strsplit()` implementation inside GLib sources.

 [1]: {{ site.url }}/news/docs/Completion-From-CTags/ "Level 3 הϵѻteric feature"
