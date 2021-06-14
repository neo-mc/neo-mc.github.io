---
layout: page
title: "Change is good!"
meta_title: "הϵѻMCEdit Changelog"
subheadline: "הϵѻMCEdit Changelog"
teaser: "History and changelog of הϵѻMCEdit, Midnight Commander's fork"
permalink: "/changelog/"
---

2021-05-30 // Version 5.0.0
:   A new feature almost finished and mostly working – an interface
    to grep-like tools (namely Ag, Ack and RipGrep). It allows to
    query the source tree easily, fast and reliable. Try-bindings
    are `Alt-equal` and `Alt-minus`.

2021-03-16 // Version 5.0.0
:   Assign and display numerical IDs. Each buffer now has a
    constant identifier assigned. The goal is to make buffer 
    switching with `Ctrl-q NUM` more reliable. Currently, the
    header/source file pairing (clustering) seems to be a problem
    – it moves the buffers without reasigning the IDs.

2021-03-11 // Version 5.0.0
:   A new feature – a small status line window called "message
    line" has been added. It significantly unmutes the editor
    and makes it possible to communicate what's going on.
