---
layout: post
title: "Strikeouts"
categories: [hitting, pitching]
excerpt: "Who wins this war?"
link:
share: true
---

For this post, the question I'm trying to answer a question is by request, "Have the number of strikeouts in college softball changed over time?" A strikeout can be interpreted as a display of dominance on the pitcher's part, but it could also indicate that a hitter is "free swinging" and will naturally strike out more as a result.  

I think many times with questions like these, whatever the results are, there are many things that can contribute to the change. I find it interesting to think about how the sport has changed from an anecdotal perspective as well as an objective one. Unfortunately I don't have access to the granular data to provide much of concrete answers, but perhaps one day this data will become available to everyone. Prayers up.

In addition to wondering why things happen, I think it's also important to consider what this change means in the future. How can we use this information to be more successful? If strikeouts are less likely to happen, how do we prioritize what to focus on as a hitter? As a spectator, is the sport more entertaining than it was 10 years ago? Why? But, if this information only makes you nostalgic or curmudgeon about the way things used to be, I guess that's ok too.

#### Data

This one is pretty simple, I normalize the strikeouts for each player by dividing by the total number of at bats. Since each player will have a different number of chances each season, it's important to normalize the data instead of taking absolute numbers. I also removed pitchers from the dataset, which were negligible to the overall mean. I grouped the data by year and conference.

#### Observations

The figure below shows the results for strikeouts over time. It appears that there is a downward trend for every conference. Very interesting! These results made me think about the great pitchers that have come and gone over this time period. I also thought about some major milestones that occurred. For example, when the mound moved to 43ft (college and travel ball), when softball was removed from the Olympics and the evolution of composite bats to name a few. Not to mention the evolution of recruiting and its methodology, in softball but other sports as well. Any and all of these things can contribute to this decrease in strikeouts.

![so_per_ab](../../img/so_per_ab.png)
*Average strikeouts per at bat grouped by conference and year*

Why do you think this trend exists? If players are striking out less, are they getting on base more? The figure below shows the average on base percentage over time.

![obp](../../img/onbase_by_year.png)
*On base percentage (OBP) over time*

Overall it looks to be that strikeouts are decreasing and on base percentage is increasing. So why are hitters winning this race? [A Sports Illustrated article][mlb] published last year indicates that Major League Baseball shows an opposite trend where the strikeout rate has increased every year since 2008. One thing the article notes is the increase in the number of pitchers. As a hitter, I always felt it was much easier to hit a pitcher later in the game when it was the 3rd or 4th time through the lineup. Later in the game you're more likely to have a pick, steal a sign and overall have better familiarity to have an advantage over the pitcher. And as noted in a previous post, most of the best teams have a single pitcher to carry the load for the season.

#### Conclusion

In NCAA Division 1 softball, hitters are striking out less than they were in the past. Why this is happening, we can't be too sure. I think the data can tell many different stories, and can provide talking points and food for thought about the game. Unlike on Twitter, there are no wrong answers. So please discuss and be nice!

[mlb]: https://www.si.com/mlb/2019/05/15/strikeout-record-pace-best-pitchers
