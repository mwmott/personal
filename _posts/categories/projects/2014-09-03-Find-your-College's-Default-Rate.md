---
layout: project
title:  Find your college's default rate
date:   2013-11-25 00:10:20
categories: projects seattletimes
tag: seattletimes
author: Michael Mott
picture: <img src="/assets/img/thumbs/chart.jpg" alt="Find your college's default rate" width="300">

---

When my internship started at <em>The Seattle Times</em>, I was able to meet various reporters to see if a data-angle might be possible on any ongoing projects. It was in this way I met <a href="https://twitter.com/katherinelong">Katherine Long</a>, a fantastic higher-education reporter who was looking into the differences in financial aid between for-profit, public and private schools.

With help from <a href="http://thomaswilburn.net/">Thomas Wilburn</a>, I made this interactive chart to accompany Katherine's <a href="http://seattletimes.com/html/localnews/2023980122_careercollegesxml.html">story</a> on the subject. Using <a href="https://angularjs.org/">AngularJS</a>, it allowed readers to sort schools by institution type and other factors to see which had the breakdown on student-default rates and types of aid.

From the article - "<b>To use this chart:</b> Click on a bar to see detailed loan and grant information for each institution. You can also sort by college, city, type and default rate by clicking the column headers. You may also search or filter by college type at the top." I owe a lot to Thomas for helping me with this, my first project at <em>The Seattle Times</em>. <a href="http://seattletimes.com/html/localpages/2023892102_ceo-pay-2014.html">His</a> chart was a great reference.

<div id="pym-student-aid"></div>
<script src="/assets/code/student-aid/pym.js"></script>
<script>
    var pymParent = new pym.Parent('pym-student-aid', '/assets/code/student-aid/index.html', {});
</script>