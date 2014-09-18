---
layout: project
title:  Amazon in Europe
date:   2013-11-25 00:10:20
categories: projects seattletimes
tag: seattletimes
author: Michael Mott
picture: <img src="/assets/img/post/octo.jpg" alt="Amazon in Europe" width="300">


---

During the last half of my internship at <span style="font-style: italic;">The Seattle Times</span>, I had the opportunity to produce a graphic which would connect three business stories in a series.

Working with illustrator Susan Jouflas, I produced the following interactive, learning how to use CSS and jQuery animations and how to connect images to videos along the way. <b>Click one of the country-icons to see an animated video on how European countries are confronting Amazon.</b>

<div id="pym-amazon"></div>
<script src="/assets/code/amazon-in-europe/lib/pym.js"></script>
<script>
    var pymParent = new pym.Parent('pym-amazon', '/assets/code/amazon-in-europe/index.html', {});
</script>

<div class="span4">
  Each of these stories needed a slightly different graphic, so I also learned to use LESS and CSS child classes to make different versions for each story. For the producers, all that was needed to be changed was a # with the name of the country  appended to the URL (e.g. '#england' or '#germany', as seen here).
</div>

  ![Country-icons](/assets/img/post/england.jpg)
  ![Country-icons](/assets/img/post/germany.jpg)

<br/>
<br/>