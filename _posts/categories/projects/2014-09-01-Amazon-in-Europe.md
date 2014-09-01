---
layout: project
title:  Amazon in Europe
date:   2013-11-25 00:10:20
categories: projects seattletimes
tag: seattletimes
author: Michael Mott
picture: <img src="/assets/img/post/octo.jpg" alt="Amazon in Europe" width="300">


---

During the last half of my internship at <span style="font-style: italic;">The Seattle Times</span>, I had the great opportunity to produce a graphic which would connect three business stories in a series.

Working with illustrator Susan Jouflas, I produced the following interactive, learning how to use CSS and jQuery animations and connect images to videos. Click on one of the country-icons to see an animated video on how European countries are confronting Amazon.

<div id="pym-amazon"></div>
<script src="/assets/code/amazon-in-europe/lib/pym.js"></script>
<script>
    var pymParent = new pym.Parent('pym-amazon', '/assets/code/amazon-in-europe/index.html', {});
</script>

<div class="span4">
  Each of these stories had to have a slightly different graphic, so I learned how to use LESS and CSS child classes to create a different version for each story. All that was required to change was a # with the name of the country for each story appended to the end of the URL (i.e. '#england' or '#germany', as shown).
</div>

  ![Country-icons](/assets/img/post/england.jpg)
  ![Country-icons](/assets/img/post/germany.jpg)

<br/>
<br/>