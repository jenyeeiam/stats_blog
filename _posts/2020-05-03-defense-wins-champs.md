---
layout: post
title: "Does Defense Win Championships?"
categories: [pitching, hitting]
excerpt: "I am biased. Hitting is the best. I'm afraid this might be true."
link:
share: true
---

This is one of those iconic sports clichés. While I do love a good colloquial saying, I'm interested in knowing whether this saying actually holds any water. Disclaimer #1, I don't have defensive stats! All I have to work with is pitching, so that will have to do for now. However, my hypothesis is that pitching stats should be sufficient to draw some conclusions overall. Pitchers are the most important defender, they touch the ball on every single play for half the game and play a major influence in the outcome of the game.

I'd like to answer the following questions, do the best teams that come out of the WCWS have better pitching than all the other teams? What's the most important metric? Have we been saying "Defense wins championships" for nothing this whole time?

#### Data

For this project, I pared the data down to only include Power Five teams (SEC, PAC12, ACC, BIG12, BIG10). Since softball has been a Division 1 sport, only Cal State Fullerton has won the WCWS in 1986 as a team outside of the Power Five as we know it today. So with the intention of leveling the playing field and smoothing out variance, I'm first assuming that these teams have a similar strength of schedule and play a similar number of games. My second assumption is that these teams are similar in strength overall. This second assumption is a bit of a stretch, and a better way to do it would be to take the top 50 teams as ranked by the NFCA. But unfortunately this data does not exist for past years that I know of. I also realize the Power Five have gone through many realignments throughout the years and I am observing the conferences as they are today. Still, with these assumptions I am hoping this makes the analysis as much apples to apples as possible given the circumstances and data available.

#### Equations

I went with some pretty simple equations to compare pitching statistics. The first is WHIP, a measure of a pitcher's effectiveness for preventing batters from reaching base. To calculate WHIP, it is the walks plus hits divided by the number of innings pitched.

> WHIP = Hits (H) + Walks (BB) / Innings Pitched (IP)

The second stat I used is runs allowed per inning. I decided to go with runs overall instead of earned runs because I hoped to capture errors committed by the defense.

> runs_allowed_per_inning = Runs (R) / Innings Pitched (IP)

For completeness, I also looked at hitting. And although I didn't see anything groundbreaking with any of the stats I tried, I will show some results for OPS, or on-base plus slugging.

> On Base Percentage (OBP) + Slugging Percentage (Slg %)

#### Observations

The figure below shows the distribution of WHIP from 2002 to 2018. This is a boxplot, if this is foreign to you there's a good explanation of how to read them on this [site][box_plot]. The red dots plotted are the WCWS **winners** WHIP averaged for the year. The blue dots represent the WCWS **runner up** WHIP averaged for the year.

<i class="fa fa-circle" style="color: rgb(235, 174, 170)"></i> Winner
<i class="fa fa-circle" style="color: rgb(149, 181, 208)"></i> Runner Up

![whip_graph_1](../../img/whip1.png)
*WHIP over time. Comparing the WCWS winners (red) with the WCWS runner up (blue)*

What I notice with this figure is that for **every** year from 2002-2018, one or both of the best teams in the WCWS has a pitching staff with a WHIP within the 25th percentile (in the Power Five). This seems to show a pretty strong relationship between success and pitching! Some other observations can include, the distribution of WHIP seems to be getting wider as time goes on and the average WHIP increases until 2015 before showing a decline from 2016-2018. What are some things that can be attributed to these trends?

After staring at this graph for a while, I started to wonder, were these teams great because they had a great *staff* of pitchers, or was it that they had *one* very good pitcher who was the workhorse and pitched the bulk of the innings?

Here is the answer. For the WCWS winner and runner up, the table lists the number of innings thrown for the first and second string pitchers.

||  | 2002 | 2003 | 2004 | 2005 | 2006 | 2007 | 2008 | 2009 | 2010 | 2011 | 2012 | 2013 | 2014 | 2015 | 2016 | 2017 | 2018  
||:--------|:-------:|--------:|--------:|--------:|--------:|--------:|--------:|--------:|
|WCWS Winner| Most Innings  | 283 | 310 | 267 | 288 | 252 | 370 | 315 | 352 | 150 | 255 | 288 | 238 | 223 | 222 | 252 | 210 | 204 |
|| Second Most Innings   | 97 | 93 | 115 | 140 | 163 | 70 | 131 | 51 | 114 | 97 | 79 | 136 | 107 | 136 | 82 | 146 | 198 |
||=====
|WCWS Runner Up| Most Innings  | 273 | 247 | 210 | 325 | 262 | 385 | 303 | 285 | 284 | 265 | 292 | 200 | 219 | 211 | 130 | 193 | 188 |
|| Second Most Innings   | 163 | 141 | 226 | 78 | 185 | 111 | 110 | 158 | 116 | 153 | 107 | 150 | 129 | 172 | 116 | 176 | 166 |

It seems like the workhorse model is what prevails most of the time when it comes to elite teams. Could this be due to scarcity? Or, that the best pitchers do not want to be on the same team as another elite pitcher? Whatever the reason, in some years it is quite impressive the workload some of these pitchers have undertaken over a given season, not to mention their whole career.

Because I could, I overlayed the individual pitchers' WHIP from the WCWS winner and runner up and scaled the point size to the number of innings pitched. Although busy, to me this representation is even more impressive that these pitchers were able to sustain upwards of 300 innings while maintaining such effectiveness on the mound.   

<i class="fa fa-circle" style="color: rgb(235, 174, 170)"></i> Winner
<i class="fa fa-circle" style="color: rgb(149, 181, 208)"></i> Runner Up
![whip_graph_2](../../img/whip2.png)
*WHIP over time with overlayed scatter plot. The size of the points represent the number of innings pitched by that pitcher.*

To cross-check I've included a similar plot to show runs allowed per inning. Not surprisingly, this one shows similar trends to WHIP.

<i class="fa fa-circle" style="color: rgb(235, 174, 170)"></i> Winner
<i class="fa fa-circle" style="color: rgb(149, 181, 208)"></i> Runner Up
![ip_graph_1](../../img/runs_per_ip.png)
*Runs per inning over time with overlayed scatter plot. The size of the points represent the number of innings pitched by that pitcher.*

So what about hitting? Is there more to the story? The figure below shows OPS over time and compares the best two teams.

<i class="fa fa-circle" style="color: rgb(235, 174, 170)"></i> Winner
<i class="fa fa-circle" style="color: rgb(149, 181, 208)"></i> Runner Up
![ip_graph_1](../../img/ops1.png)
*OPS over time. Comparing the WCWS winners (red) with the WCWS runner up (blue)*

Looking at this graph it appears the best teams generally have middle of the road to above average hitting. It might be helpful to distinguish between regular season and post season hitting. Perhaps the best teams got hot once the post season started? But as far as I know the NCAA does not make this distinction in its record keeping, so we are left to speculate on this one.

#### Conclusion

Using some preliminary statistics to compare pitchers, it appears the old adage "Defense wins championships" holds fairly true. The pitcher is the most important player and defender on the field. She is the one that controls the game and keeps the other team from scoring, and in NCAA Division 1 softball it seems that a team really only needs 1 to do the job. In WHIP and runs allowed per inning, the best teams had a primary pitcher within the 25th percentile in the statistical category and many times a secondary pitcher in that percentile as well.
<!--more-->

[box_plot]: https://towardsdatascience.com/understanding-boxplots-5e2df7bcbd51
