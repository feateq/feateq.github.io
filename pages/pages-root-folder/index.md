---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth: front_cover.jpg
widget1:
  title: "Mechanics"
  url: 'https://www.feateq.com/mechanics'
  image: widget1.jpg
  text: 'Mechanical Design blog posts covering structural mechanics, basic equations, and core engineering concepts.'
widget2:
  title: "Analysis"
  url: 'https://www.feateq.com/analysis'
  text: 'Finite Element Analysis blog posts covering various analysis types with in-depth tutorials of real-world engineering applications.'
  image: widget2.jpg
widget3:
  title: "Fatigue"
  url: 'https://www.feateq.com/fatigue'
  image: widget3.jpg
  text: 'Fatigue and Life Analysis blog posts covering various life methodologies, experimental procedures, and plasticity.'
widget4:
  title: "Vibration"
  url: 'https://www.feateq.com/vibration'
  image: widget4.jpg
  text: 'Mechanical Vibrations blog posts covering analytical and experimental vibration methods from foundational principles to industry standards.'
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
