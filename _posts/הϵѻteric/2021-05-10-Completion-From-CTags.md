---
layout: page
title:  "Completion From CTags³"
sidebar: left
date:   2021-05-10 15:23 +0100
subheadline: "הϵѻteric³ Features"
meta_teaser: "NeoMCEdit has a unique feature - it can complete symbols found in CTags index – the project's symbols like function and variable names. You can use it to easily recall functions declared in libraries used by the project, and not only."
teaser: "הϵѻMCEdit has a unique feature - it can complete symbols found in CTags index – the project's symbols like function and variable names. You can use it to easily recall functions declared in libraries used by the project, and not only."
breadcrumb: true
categories: 
    - news
    - docs
tags:
    - הϵѻteric³
    - features
    - news
    - mcedit
---

This feature is marked as third degree (³), ie.: an innovative 
feature that's very rare in other editors, because I've haven't
seen anything like this, ie. eg.: no Vim plugin exists that allows
to complete from `TAGS` file.

# Completing The Tags

It's now possible to complete not only from buffer's words, but
also **from symbols in a CTags index file** (which is named
"**TAGS**" and is placed in project's root) – e.g.: for an
index  that covers **/usr/include/glib-2.0**, you could
complete **all GLib functions and types**, like so:

[![asciicast](https://asciinema.org/a/cp4I3tFfKrLNS9SME7XE2w6Nk.svg)](https://asciinema.org/a/cp4I3tFfKrLNS9SME7XE2w6Nk)

Regular completion is bound to **Alt-/** by default, while the
TAGS completion is **Shift-Tab**.

This feature allows to have an **IDE-like experience** – by **easy
completing** of all libraries' and project's own **functions** and
**types**. 

Note, that by limiting the completion candidates to **project's
symbols** a new and robust, and also a **very well responsive**
completion mechanism has been set up.    

# Hint: Complete Library Symbols

To have not only the source of the **project**, but also headers
of a library **used by it** indexed by **CTags**. you could simply
link its includes into **project's root**, like so (an example):

{% include alert terminal="ln -s /usr/include/glib-2.0 ~/project/glib-hdrs" %}

Then also a ctags invocation with **--c-kinds=+p** option used
is being needed too, so that also function **declarations**
(i.e.: not only **definitions**) are being indexed, too.
Here's an example Makefile rule/target that executes such a
**ctags** command – after copying, issue **make tags-emacs**
to run it:

    tags-emacs:
        @if type ctags >/dev/null 2>&1; then \
            if ctags --version | grep >/dev/null 2>&1 "Universal Ctags"; then \
                ctags -e -R --languages=C --langmap=C:.h.c --c-kinds=+px \
                        --extras=-{anonymous} --extras=+r \
                        --fields=+S --fields-c=+{macrodef} \
                        --pattern-length-limit=250; \
            else \
                ctags -e -R --languages=C --langmap=C:.h.c --c-kinds=+px \
                        --fields=+S .; \
            fi; \
            printf "Created the Emacs \`TAGS\` file.\\n"; \
        else \
           printf 'Error: Missing Ctags (e.g.: either Exuberant or Universal fork) utility first.\n'; \
        fi

The Makefile rule detects if Universal **CTags** or **Exuberant
CTags** is being installed and runs the appropriate, either a more
rich (for Universal …) or more concise (for Exuberant CTags)
command. *When copying rule's text into your Makefile (…  .am,
etc.) make sure that it's indented with «TABS», not with spaces.*
