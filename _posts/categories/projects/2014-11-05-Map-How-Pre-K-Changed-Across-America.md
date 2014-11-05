---
layout: project
title:  How State Pre-K Changed Across the U.S.
date:   2014-02-02 00:10:20
categories: projects seattletimes
tag: seattletimes
author: Michael Mott
picture: <img src="/assets/img/post/prek.jpg" alt="Pre-K Map" width="300">

---

At the close of my internship at <em>The Seattle Times</em>, I made <a href="http://seattletimes.com/html/localpages/2024591614_preschool-enrollment-changes.html">this</a> interactive map to complement an <a href="http://blogs.seattletimes.com/educationlab/">Education Lab</a> series on state-funded pre-k education. 

It shows how state-funded pre-kindergarten funding has changed over the last ten years. This project taught me a lot about jQuery and Javascript, along with learning how to create a CSV that the slider can "read". Many thanks to Thomas Wilburn, a fellow news nerd, for his help on this project.

<b>To use this map:</b> Hover for state-level data and move the slider to see changes through the years. 

<div id="pym-pre-k"></div>
<script src="/assets/code/pre-k-map/lib/pym.js"></script>
<script>
    var pymParent = new pym.Parent('pym-pre-k', '/assets/code/pre-k-map/index.html', {});
</script>

<h2>Source:</h2>
The shapefiles and structure come in part from ProPublica's <a href="http://www.propublica.org/nerds/item/introducing-landline-and-stateline-two-tools-for-quick-vector-maps-in-your-">Landline/Stateline</a>, which were launched together in April, 2014. The data is from a series of PDF files from <a href="http://nieer.org/publications/annual-state-pre-k-reports-state-preschool-yearbooks">NIEER</a> (The National Institute for Early Education Research, from their "State of Preschool" reports). The PDFs were scraped with <a href="https://scraperwiki.com/">scraperwiki</a>. 