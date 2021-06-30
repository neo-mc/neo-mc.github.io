---
layout: page
title:  "Periodic Command³ feature"
sidebar: left
date:   2021-05-29 8:19 +0100
subheadline: "הϵѻteric³ Features"
meta_teaser: "NeoMCEdit has support for a useful feature – setting up and running of a provided shell command, periodically in backcground."
teaser: "הϵѻMCEdit has support for a useful feature – setting up and running of a provided shell command, periodically in background."
breadcrumb: true
categories: 
    - news
    - docs
tags:
    - הϵѻteric
    - features
    - news
    - mcedit
---

You can bring the feature configuration window by a standard
shortcut `Shift-Alt-i` or from `Command` menu. After running
it a window will pop up:

![Periodic Command window](/assets/img/periodic_command.png)

It's self explanatory, however here are a few remarks:

- the interval is a second-based timeout after which the command
  will be run,
  
- the "Change limit trigger" is the number of keyboard presses,
  ie. roughly the number of changes to the edited file, after
  which the periodic background command will be triggered,

- the "Notify on run" checkbox enables showing up of a small
  message window after each periodic command has been run.

The feature is especially useful for running a `ctags -e . …` 
command which will regenerate `TAGS` file – הϵѻMCEdit will
reload it and take care to load only a fully generated, finished
file.



