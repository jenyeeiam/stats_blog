---
layout: post
title: "Sophomore Slump Busters"
categories: [hitting]
excerpt: "I felt this pain 😭. But, softball players are crazy, so I must have been crazy."
link:
share: true
---

Urban Dictionary defines a [sophomore slump][ud_site] as a disappointing follow up to a successful first recorded album. We've all been there, that feeling of inadequacy, not feeling like you're living to your fullest potential. Our perception of ourselves is the worst! No matter what, we just can't help comparing our success or failures to our previous selves.

I'd like to find out whether this sophomore slump thing is all in our heads.

#### Data

I will be focusing on hitting for this project. I filtered the dataset to only include players with the classes of `So.` and `Fr.`. I created two dataframes, one for sophomores and one for freshman, then I did an inner join on the `Name` and `School` to eliminate entries that were not included in both dataframes. Then, I merged the dataframes back together subtracted the freshman stats from the sophomore stats.

I will be observing this data by a histogram. I want to see what the distribution of this change (Δ) in OPS and wOBA across Division I schools.

#### Equations

I used OPS as the metric to compare players. OPS is on base percentage plus slugging.

> OPS = On Base Percentage (OBP) + Slugging Percentage (Slg %)

#### Observations

The figure below shows the distribution of the change in ops from freshman to sophomore year. Personally I think these color-coded bars are not only helpful, but beautiful as well. 

![ops1](../../img/ops_hist.png)
*Change in OPS from freshman to sophomore year across all NCAA D1 athletes*

#### Conclusion

<!--more-->
[ud_site]: https://www.urbandictionary.com/define.php?term=sophomore%20slump
