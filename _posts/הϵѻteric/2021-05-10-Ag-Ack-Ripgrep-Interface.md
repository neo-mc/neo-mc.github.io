---
layout: page
title:  "Ag/Ack/RipGrep interface³"
sidebar: left
date:   2021-05-10 11:37 +0100
subheadline: "MCEdit הϵѻteric³ features"
meta_teaser: "NeoMCEdit has a support for running any grep tool (like RipGrep or traditional grep) and parsing its output, allowing for quick navigation in projects."
teaser: "הϵѻMCEdit has a support for running any <b>grep tool</b> (like <b>RipGrep</b> or traditional grep) and parsing its output, allowing for quick navigation in projects."
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
feature that's very rare in other editors, mostly not because
of the main functionality (which I'd expect to exist in some
editors or IDEs), but because of a specific, very rich 
implementation of history of the searches. Details follow.


# Starting A Search

Press `Alt-equal` to explicitly start a new grep search – a window
will open asking for the search query and allowing to select the
grep tool to be used to run the search: 

![New search query window](/assets/img/grep_query_win.png)

You can pass options to the grep tool normally, by entering them
side by side with the query string, eg.:

{% include alert text="GPtrArray --cc -i # search only C/C++ files case insensitively" %}

You can also normally pass on the directory to search in:
הϵѻהϵѻ
{% include alert text="GPtrArray --cc -i glib # search in ./glib subdirectory " %}


# Navigating To Results

![New grep results window](/assets/img/grep_results.png)

While the search is ongoing you may freely use the editor. When the
search finishes a window with results will open, like above.

To jump to the pointed location, press Enter. You may also edit the
results – by pressing Delete to remove an entry from the list.

## Viewing Whole Result Lines

If the result line is too long to fit into the screen you can view 
it whole by pressing F3 (i.e.: the View action of listbox) on it. A
new window will open at bottom of the screen containing the complete
line, eg.:

![Extended view of result line](/assets/img/grep_extended_view.png)

# Recalling Previous Searches

Press `Alt-minus` to move to the already done, most recent search's
results. Press it again to move to its search query window (where
you can edit the query and replace the results if you want). One
more time, to move to the one-earlier search results, and so on.

Press `Alt-plus` to move in opposite direction – ie. to towards the
most recent search.

When using those bindings while there aren't any past searches
available, they'll work the same as `Alt-equal`, ie. they'll start
a new search by opening a fresh search query window.
