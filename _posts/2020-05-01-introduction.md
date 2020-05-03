---
layout: post
title:  "Introduction"
date:   2020-05-01 15:07:19
categories: [about]
comments: true
---
How often do you have a question, and you go to the Google to answer it? If you're like me, very often, and multiple times a day. Very recently I was thinking about softball, thinking about how it has changed over time and maybe reminiscing about the good old days. One doesn't have to spend much time on the internet to realize there are many opinions about softball, but not many ways to measure and compare players, teams, or anything really. Whereas baseball sabermetrics exist because of the mass expanse of metrics one can access with little to no effort.

My goal is not to analyze softball with sabermetrics. That stuff is for nerds. But, I am perturbed by the inaccessibility of softball statistics as a whole. So, what does one do it times like these? You send a few emails, find the website where the stats live and you write a script to scrape them all from the internet. That's ~300k points over 16 years baby! There are actually more, but the stats that predate 2002 are in pdf form and I haven't hired a virtual assistant to convert them yet. If you are willing to work for little to no money, please call me.

Here is a snapshot of what comes from the [NCAA][ncaa_stats_site] for 2003.
{% highlight text %}
School,Name,Class,Year,Pos,G,AB,R,H,Avg,2B,3B,HR,TB,Slug Pct.,RBI,SB,SBA,BB,SO,HBP,App,GS,CG,W,L,SV,ShO,IP,H,R,ER,BB,SO,ERA
A&M-Corpus Christi,"Amos, Kelly",Sr.,2002-03,Shortstop,55,178,24,50,0.281,5,2,1,62,0.348,16,1,4,14,24,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0
A&M-Corpus Christi,"Burton, Amanda",Sr.,2002-03,Starting Pitcher,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,1,0,0,0,0,0,0,3.2,8,7,5,2,0,9.46
A&M-Corpus Christi,"Cortez, Christy",So.,2002-03,Outfield,53,157,18,27,0.172,6,1,1,38,0.242,9,3,8,4,31,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0
A&M-Corpus Christi,"Damel, Dani",Jr.,2002-03,Starting Pitcher,23,53,6,6,0.113,0,0,1,9,0.170,3,0,0,4,18,0,21,19,5,8,8,0,1,103.0,101,51,37,28,82,2.51
A&M-Corpus Christi,"Evans, Katie",Jr.,2002-03,Third Base,55,165,17,59,0.358,13,0,3,81,0.491,26,2,3,13,24,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0
{% endhighlight %}

As you can tell, these stats are not the best, but I don't think they're the worst either. With these, one could reverse engineer the single season or career records that the NCAA does have accessible to the general public. In addition, I am not a data scientist, nor do I care to be one. But, I think I'm capable of asking some reasonable questions. Such as, "Does defense really win championships? Does the Sophomore Slump really exist? Does the President of the United States really matter?" So I'm going to do my best and to take this opportunity to learn some things about softball, and learn how to use [Pandas][pandas] at the same time. I'll try to post code snippets when possible and let's learn together! Because, "If not us, then who? If not now, then when?"

Unlike the NCAA, I will be willing to share this data dump with anyone who would like it. I'm sure there are many more people than myself who can make way better visualizations and draw better conclusions than me.

<!--more-->

[pandas]: https://pandas.pydata.org/pandas-docs/stable/index.html
[ncaa_stats_site]: https://web1.ncaa.org/stats/StatsSrv/careersearch
