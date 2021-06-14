---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth: header_unsplash_12.jpg
widget1:
  title: "Ag/Ack/RipGrep integration
  ;"
  url: '/news/docs/Ag-Ack-Ripgrep-Interface/'
  image: widget-1.png
  text: 'Ever used `:grep` in Vim? הϵѻMCEdit has similar, decent support for it, with history that remembers all your previous searches with results, and ability to edit them, ie. to remove single matches. You can grep all sources multiple times, jump to the results and browse all your past searches.'
widget2:
  title: "QuickOverview 3rd degree feature"
  url: '/unwritten_planned/'
  text: "הϵѻMCEdit has many advanced features, called הϵѻteric³ ones. One of them is QuickOverview – a small window displayed after any jump in the buffer. It holds names of surrounding functions. No other editor has this feature, hence it's labeled as 3rd degree."
  image: widget-2.png
widget3:
  title: "הϵѻteric features of 1st, 2nd and 3rd degree.,"
  url: '/unwritten_planned/'
  image: widget-3.png
  text: 'New features are of 3 degrees - the greater, the more advanced one is. Examples of 3rd degree features are: completing symbols from CTags index, periodic background command, selection history; 2nd degree are i.a.: scripting engine, terminal window and more.'
#
# Use the call for action to show a button on the frontpage
#
# To make internal links, just use a permalink like this
# url: /getting-started/
#
# To style the button in different colors, use no value
# to use the main color or success, alert or secondary.
# To change colors see sass/_01_settings_colors.scss
#
callforaction:
  url: https://tinyletter.com/neomcedit
  text: Inform me about new updates and הϵѻteric² and ³ features ›
  style: alert
permalink: /index.html
#
# This is a nasty hack to make the navigation highlight
# this page as active in the topbar navigation
#
homepage: true
---

<div id="videoModal" class="reveal-modal large" data-reveal="">
  <div class="flex-video widescreen vimeo" style="display: block;">
    <iframe width="1280" height="720" src="https://www.youtube.com/embed/3b5zCFSmVvU" frameborder="0" allowfullscreen></iframe>
  </div>
  <a class="close-reveal-modal">&#215;</a>
</div>
