---
layout: project
title:  A Congressional 'Drone' Search
date:   2013-11-25 00:10:20
categories: projects featured
author: Michael Mott
---

Our data class (taught by the wonderful <a href="http://www.stat.ucla.edu/~cocteau/">Mark Hansen</a>) at Columbia's School of Journalism was given an opportunity last November reporters traditionally haven't: “Find something interesting in this data.” 

Diving into the Sunlight Foundation's <a href="http://capitolwords.org/api/1/">Capitol Words API</a>, we started looking at all words spoken on the floor of the U.S. Congress since 1996. With drones trending after recent bombing in the middle east, we searched in R how often the word was said. We wondered if we could use that as a milestick for the conversation around drone warfare.

First step was to examine the data. We pulled the word drone going back to 1996 on the API:

<xmp>
   sll_cw_timeseries("drone",key="b1884b38a7e04ffeb9bdc91a0a63fe1b")
</xmp>

Then plotted it simply:

<xmp>
plot(dronets$day,dronets$count)
</xmp>

![Drone sketch]({{ base.url }}/assets/img/post/drone1.jpg/)

From this rough sketch we saw there was a major outlier: the spike on the y-axis. 

<xmp>
	# ggplot of word 'drone' over time, sorted by party.
	install.packages(ggplot2)
	library(ggplot2)
	dat_d <- sll_cw_timeseries(phrase='drones', party="D", 
														 key = "6a0998f8ba3c4a8b888ef28b20975174")
	dat_d$party <- rep("D", nrow(dat_d))
	dat_r <- sll_cw_timeseries(phrase='drones', party="R", 
														 key = "6a0998f8ba3c4a8b888ef28b20975174")
	dat_r$party <- rep("R", nrow(dat_r))
	dat_both <- rbind(dat_d, dat_r)
	ggplot(dat_both, aes(day, count, colour=party)) + geom_line() +
	theme_grey(base_size=20) + scale_colour_manual(values=c("blue","red"))
</xmp>

Breaking this down by party showed the general trend of the word's usage between parties.

![Drone finish]({{ base.url }}/assets/img/post/drone2.jpg/)

As we can see, the largest usage was Rand Paul's 235 repetitions during his filibuster in mid-March of last year.

Does this get us any closer to figuring out the formula for the national conversation? Maybe not. <a href="https://twitter.com/tjl">Tom Lee</a>, the director of Sunlight Labs, advised us to as always be careful in drawing conclusions. Correlation, not causation.

But we did find a story, and I'm sure this dataset will be useful in the future. 

See our full R file (with comments), <a href="{{ base.url }}/assets/code/FriNov22Memo.R" download="drones.R">here</a>.