---
layout: project
title:  A Data State of Mind
date:   2013-11-25 00:10:20
categories: projects datapersonal
tag: datapersonal
author: Michael Mott
picture: <img src="/assets/img/post/temp.jpg" alt="NYC Weather" width="300">
---

I was working on a long-form project at Columbia's School of Journalism, when I realized: Learning how to explore data gives another tool to satisfy journalists' curiosity.

My story was about how boilers in the city were switching fuels from heavy oil to natural gas and other supposedly cleaner alternatives. My lede began with the day of conversion for one building owner.

The story attracted me because whoever you are in New York, you need heat and shelter. So I began to wonder — what temperature was it that day of conversion?

I Googled first of course. Then I found the great [wunderground.com](http://www.wunderground.com/):

![weather](/assets/img/post/weather.jpg)

Wunderground has a great open weather search, where I specified dates. They even have a nice .csv link at the bottom of the page here.

Looking at this again, I would definitely search longer for a median number — as it's more statistically accurate than an average — but I thought it came out well anyway:

<pre>
	#Daily Mean Temperatures of NYC
weather <- read.csv("~/Documents/Data/masters-temp/weather 9-23 - 1-15.csv")
#Loading in weather from wunderground.com

load(ggplot2)
#Package needed for plot

weather$EST <- as.Date(weather$EST)
#making the factor column a date column to be able to use.

#Plot to illustrate mean temps and to see (for reporting mostly) NYC's
#temperature when Laura Bruno's conversion was finished and her first
#shipment of biofuel came.

ggplot(aes(x=EST, y=Mean.TemperatureF), data=weather) + geom_point() + geom_smooth() +
  geom_vline(x=unclass(as.Date("2013-10-24")), color="red", linetype="dashed", size=1) +
  ylab("Degrees (Fahrenheit)") +
  xlab("Time") + ggtitle("Daily Mean Temperatures for NYC's 2013-14 Winter (Indicating at Laura Bruno's Conversion)")
</pre>

The code reveals:

![Temp](/assets/img/post/temp.jpg)

From this graph we can figure out weather the temperature on the day of conversion from was high or low — in this case relatively low. This day was at the start of winter, and that led to my lede:

> Winter was just beginning in New York City when Laura Bruno’s building converted its heating fuel. While the October of 2013 had been mild, temperatures were dropping fast and the 2013-14 heating season had begun.