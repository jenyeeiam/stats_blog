---
layout: post
title: "Sophomore Slump Busters"
categories: [hitting]
excerpt: "This pain 😭"
link:
share: true
---

Urban Dictionary defines the [sophomore slump][ud_site] as a disappointing follow up to a successful first recorded album. We've all been there, that feeling of inadequacy, not feeling like you're living to your fullest potential. Our perception of ourselves is the worst! No matter what, we just can't help comparing our success or failures to our previous selves. I'd like to find out whether the sophomore slump is an actual thing in college softball.

#### Data

I will be focusing on hitting for this project. I filtered the dataset to only include players in the `So.` and `Fr.` class. I created two dataframes, one for sophomores and one for freshman, then I did an inner join on the `Name` and `School` to eliminate entries that were not shared by both dataframes. Sometimes players play their freshman and sophomore seasons at different schools, so I will not be counting those cases. And lastly, I subtracted the freshman stats from the sophomore stats. This was the first time I learned how to merge dataframes like an sql join so I thought I'd share that snippet.

{% highlight python %}
so_ops = df[(df['Class'] == 'So.') & (df['OPS'].notna())][['Name', 'School', 'OPS']]
fr_ops = df[(df['Class'] == 'Fr.') & (df['OPS'].notna())][['Name', 'School', 'OPS']]
merged = fr_ops.merge(so_ops, on=['Name', 'School'], suffixes=('_fr', '_so'))
merged['delta'] = merged['OPS_so'] - merged['OPS_fr']
{% endhighlight %}

#### Equations

I used OPS as the metric to compare players. OPS is on base percentage plus slugging.

> OPS = On Base Percentage (OBP) + Slugging Percentage (Slg %)

#### Observations

The distribution of the change (Δ) in OPS from freshman to sophomore seasons is shown in the figure below. Personally I think these color-coded bars are not only helpful, but beautiful as well. Also, check out that normal distribution!

![ops1](../../img/ops_hist.png)
*Change in OPS from freshman to sophomore year across all NCAA D1 athletes*

|Number of Players|Mean|St. Deviation
|:-------:|:-------:|:-------:|
|12623|0.037|0.318

The biggest takeaway I get from this is that the delta/change is pretty centered around zero. In other words, not much happened between freshman and sophomore year! We should all stop being so hard on ourselves.

I was a bit disappointed in this non result. So instead of packing it in, I went and compared the senior and freshman seasons as well.

![ops2](../../img/ops_hist_sr_to_fr.png)

|Number of Players|Mean|St. Deviation
|:-------:|:-------:|:-------:|
|7931|0.086|0.299

Again, not a data scientist, but that yellow chunk looks bigger and more leaning right! And indeed our mean shifted a whopping 0.05 points to the right. Is this significant? I think that's up to you.

#### Conclusion

Humans are naturally negatively biased. It's an evolution thing so it's not our fault. As the saying goes, "Life has to win every day. Death only has to win once." In other words, in a pool of a lot of good things, we're still going to focus on the one or two bad things because it's the one poison mushroom you come across that could be the end. As hitters, we see our freshman year as our first point of reference to ourselves as college athletes. As we navigate through our sophomore year we might focus on our performance and compare it to our freshman season negatively. I'm here to say this behavior is unwarranted! Across thousands of players, the data shows that you're more likely to be performing just as you were this whole time, maybe slightly better.

<!--more-->
[ud_site]: https://www.urbandictionary.com/define.php?term=sophomore%20slump
