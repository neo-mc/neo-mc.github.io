---
layout: page
title:  "Slang Scripting Engine²"
date:   2021-05-11 7:39 +0100
subheadline: "MCEdit הϵѻteric² features"
meta_teaser: "MCEdit now supports scripting in S-Lang language. It is a very light solution, yet very functional."
teaser: "MCEdit now supports scripting in <b>S-Lang</b> language. It is a very light solution, yet very functional."
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

Scripting language support is pretty essential in a vibrant, novel 
editor. Like Vim and Emacs, הϵѻMCEdit has too support for such 
feature. 

The language chosen for NeoMCEdit is S-Lang. It is a very light,
yet powerful language, with very straightforward integration
with the hosting application (meaning that it's easy to develop).


# API Functions Documentation

Below is a list of functions exported to the S-Lang interpreter. The
“cure_” prefix stands for “current editor”. All functions are in the
**mc** namespace, i.e.: `mc->func()`.

1. Movement – #1 function.
   - cure_cursor_move (offset)
:    Moves the cursor offset bytes right or left (when offset is
     smaller than 0).
2. Getting offsets – #3 functions.
   - cure_cursor_offset (void)
:    Returns an integer that is the cursor position in the buffer.
   - cure_get_bol (void)
:    Gets an integer that is the offset of the
beginning of current line. 
   - cure_get_eol (void)
:    Gets an integer that
is the offset of the end of current line.
4. Getting data from buffer – #2 functions. 
   - cure_get_left_whole_word (skip_space)
:    Returns a string that is the word on left of cursor. If
     skip_space is true, then it jumps over a single block of 
     white space if necessary.
   - cure_get_byte (byte_index)
:    Returns the byte at given byte offset.
5. Editing functions – #3 functions. 
   - cure_delete (void)
:    Deletes the char under the cursor. 
   - cure_backspace (void)
:    Deletes the char left of cursor. 
   - cure_insert_ahead (char)
:    Inserts the given char right of cursor.
6. Dialog functions – #4 functions. 
   - listbox (h, w, title, items)
:    Displays the list with given size, title and
items.
   - listbox_with_data (h, w, title, items, data)
:    Displays the list
with given size, title, items and the associated data elements.
   - listbox_auto (title, items)
:    Auto sized listbox. 
   - message (title,body)
:  A press-any-key message dialog with given title and body text.
7. Action hooks – #2 functions. 
   - set_action_hook (action_name, func_name, user_data)
:  Hooks up the given function to the given action.

# Standard Plugins Shipped With הϵѻMCEdit.

There are 4 plugins that are written in S-Lang language and shipped
with הϵѻMCEdit:

1. `grow_shrink_integer.plg.sl` – implements the well known Vim 
   feature – increasing and decreasing the number under cursor.
   Binds to `ctrl-alt-a` for increase and `ctrl-alt-x` for decrease
   by default. The bindings can be overidden by setting the 
   following actions in `~/.config/mc/mc.keymap` to a custom
   key combination (example):
   > [editor]<br/>…<br/>GrowInteger = alt-a<br/>ShrinkInteger = alt-x"

2. `capitalize.plg.sl` - implements following actions:
   - `Capitalize` - upcases the first letter of word under the 
     pointer; bound to `alt-shift-c` by default,
   - `ToUpper` – upcases the current word (ie. "aBc" becomes "ABC");
     bound to `ctrl-alt-u` by default,
   - `ToLower` – lowercases the current word; bound to `alt-shift-l`.

3. `commentify.plg.sl` – implements commenting and uncommenting
   current line with `/* … */`. It currently supports only such
   C comments. Bound to `alt-i` by default. The name of the 
   action is `Commentify`, so you can alter this binding by
   including the following in `~/.config/mc/mc.keymap` to bind
   it to `alt-c` if you want (example):

   > [editor]<br/>…<br/>Commentify = alt-c

4. `better_marks.plg.sl` – a plugin which resolves a considered 
   issue with with `MarkUp` and `MarkDown` actions – it changes
   their behavior from:
   ```
   Starting selection at current position and moving vertically 
   up/down." 
   ```

   to:
   ```
   Selecting the whole line above or below and moving
   to that line."
   ```

   Unlike other plugins `better_marks` doesn't define a new action.
   It only hooks up to the two mentioned actions and alters their
   behavior.

## «plugin» Directory In «~/.config/mc»

To use the plugins, copy them from `misc/` subdirectory of the
source tree to a new directory: `~/.config/mc/plugin`. All files
with the `*.sl` extension in this dir will be read by הϵѻMCEdit at
startup, setting up the plugins. 

In case of any problems you may want set the `mc_loglevel` 
variable to 2 or more in `~/.config/mc/init.sl` file to see 
messages confirming loading of each of plugins.






