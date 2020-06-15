---
layout: post
title: "Run Expectancy and Me"
categories: [hitting, opinion]
excerpt: "It's never easy"
link:
share: true
---

This post is inspired by the work done by Jon Nachtigal. He has created the website [Fastpitch Analytics][fp_analytics] and has a couple articles on this topic, I encourage you to check those out. Run expectancy is just like it sounds, how many runs can I expect my team to score in any given situation. Where a situation is defined as an out-to-base-runners configuration. The figure below is an example run expectancy matrix I took from [Fan Graphs][fan_graphs]. This is a generalist matrix they calculated from 2014, but you can create these catered to different ball parks and to different teams.

![obp](../../img/run_expectancy.png)
*Run expectancy chart from Fan Graphs. The highlighted row is the run expectancy for a runner on second. With 0 outs the average number of runs scored is 1.068, 0.644 with 1 out and 0.305 with 2 outs.*

Run expectancy is a neat tool to have in your back pocket. By knowing the general numbers for your team, you can gauge your level of aggressiveness, like deciding whether to bunt or steal for example. There is also a metric called RE24 which is used to compare hitters and pitchers and is calculated with this matrix. RE24 is given by the equation below.

> RE24 = RE End State - RE Beginning State + Runs Scored

For example, if a batter comes up with a runner on first base with none out (re_start = 0.831), she hits a single and the end state is a runner on first and third (re_end = 1.798), there are no runs that scored so the result is **1.798 - 0.831 + 0 = 0.967 RE24**. This metric of RE24 is effectively a measure of "clutchness," and how much an impact a hitter has on the end result on a game. RE24 can be a good measure when trying to decide an MVP of a league, or even when you're trying to decide who would be a good pinch hitter.

#### The Problem

So this is great, we should all have a run expectancy matrix for our own teams! Unfortunately, creating them is not so easy to do ourselves. As Jon indicated in [this post][re_article], it is a "painstaking process" to create on your own. There are calculators out there that can give you an estimate, but to make the real thing it requires parsing **all the play by play data**. Take a look at this sample from the PAC12 website. This type of data is good for humans to read, but pretty awful for data analysis.

![obp](../../img/pbp_screenshot.png)
*Snippet of 2019 play by play data from the PAC12 website*

The end goal, and the format I'd find more useful to make my own run expectancy matrices would be something like this below. I filled in this data in an excel spreadsheet by hand just to show you, but over a span of an entire season this is just not something a sane person would be willing to do.

{% highlight text %}
date,inning,road_score,home_score,batting_team,batter,rob_1b,rob_2b,rob_3b,pitching_team,pitcher,play_type,runs,outs,description
6/4/19,1T,0,0,Oklahoma,"Romero, S",,,,UCLA,Garcia,double,,0,"Romero, S. doubled to right center"
6/4/19,1T,0,0,Oklahoma,"Clifton, C.",,"Romero, S",,UCLA,Garcia,strike out,,0,"Clifton, C. struck out swinging"
{% endhighlight %}

*CSV snippet of the first two plays of UCLA vs Oklahoma*

Reformatting data from one form into another is often referred to as "cleaning." As a former professional data cleaner I have a few tricks to do things like this, but it definitely involves a bit of code gymnastics. The nature of this data is very...irregular. I haven't run through all the data, but some things that could go sideways could be, typos, inconsistent names, inconsistent language when referring to play results, and substitutions that aren't captured to name a few. Basically the moral of the story is that this processing this data is far from foolproof.

Another obstacle is the lack of data availability. I think it's near close to a Christmas miracle that every single game from 2019 is available on the PAC12 website. This is most definitely not true for other years in the PAC12, not to mention the other high profile conferences for softball. In fact, as I was investigating how to scrape and parse data like this from the SEC website, all of a sudden their website decided to stop working. They no longer have individual team statistics available on their website 🤦‍♀️.

![obp](../../img/404_error.png)
*Error message when trying to access Alabama softball statistics from the [SEC website][sec_site]*

Again, this lack of data availability is very frustrating and disheartening. This form of data is not going to give anyone an advantage over anyone else, and by removing it from public view it just creates yet another barrier to those who might be, or become, interested in our sport.

#### Conclusion

In closing, I really want to make my own run expectancy matrix for softball programmatically. It is an uphill battle and I'm going to try reasonably hard to get there with the PAC12 data from 2019. I can't tell the future but I foresee this ending in two ways, I get decently close with a subset of the data and come up with a matrix that looks halfway ok, the second path is me giving up and never trying again. I'm giving it a 50/50 chance because the truth of the matter is that I don't care that much to try *too* hard to get this to work, I do have an actual job I should be doing after all. What I would really love is for there to be an "Export to CSV" button for every play by play boxscore on the internet! Who out there can make this happen? I will wait here. Until then, I will keep picking away at this and hope the PAC12 doesn't shut their website down too.


[fp_analytics]: https://fastpitchanalytics.com/
[fan_graphs]: https://library.fangraphs.com/misc/re24/
[re_article]: https://fastpitchanalytics.com/2013/05/11/run-expectancy/
[sec_site]: https://www.secsports.com/clubhouse/softball/alabama-crimson-tide
