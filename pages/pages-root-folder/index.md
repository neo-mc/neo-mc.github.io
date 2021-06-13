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
  image: widget-1-302x182.jpg
  text: 'Ever used `:grep` in Vim? הϵѻMCEdit has similar, decent support for it, with history that remembers all your previous searches with results, and ability to edit them, ie. to remove entries. You can grep all sources multiple times, jump to the results and browse all your past searches.'
widget2:
  title: "QuickOverview 3rd degree feature"
  url: 'http://phlow.github.io/feeling-responsive/info/'
  text: "הϵѻMCEdit has many advanced features, called הϵѻteric³ ones. One of them is QuickOverview – a small window displayed after any jump in the buffer. It holds names of surrounding functions. No other editor has this feature, hence it's labeled as 3rd degree."
  image: widget-3.png
widget3:
  title: "הϵѻteric features of 1st, 2nd and 3rd degree.,"
  url: 'https://github.com/Phlow/feeling-responsive'
  image: widget-github-303x182.jpg
  text: '<em>Feeling Responsive</em> is free and licensed under a MIT License. Make it your own and start building. Grab the <a href="https://github.com/Phlow/feeling-responsive/tree/bare-bones-version">Bare-Bones-Version</a> for a fresh start or learn how to use it with the <a href="https://github.com/Phlow/feeling-responsive/tree/gh-pages">education-version</a> with sample posts and images. Then tell me via Twitter <a href="http://twitter.com/phlow">@phlow</a>.'
widget4:
  title: "הϵѻteric features of 1st, 2nd and 3rd degree.,"
  url: 'https://github.com/Phlow/feeling-responsive'
  image: widget-github-303x182.jpg
  text: '<em>Feeling Responsive</em> is free and licensed under a MIT License. Make it your own and start building. Grab the <a href="https://github.com/Phlow/feeling-responsive/tree/bare-bones-version">Bare-Bones-Version</a> for a fresh start or learn how to use it with the <a href="https://github.com/Phlow/feeling-responsive/tree/gh-pages">education-version</a> with sample posts and images. Then tell me via Twitter <a href="http://twitter.com/phlow">@phlow</a>.'
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
  url: https://tinyletter.com/feeling-responsive
  text: Inform me about new updates and features ›
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
