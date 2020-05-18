---
layout: post
title: "Beginner's Web Scraping Tutorial"
categories: [tech]
excerpt: "First ever Vlog 🤯🤯🤯"
link:
share: true
---

This post deviates a little from the normal softball fare, but I think it's cool nonetheless. And my blog my rules amiright? Web scraping is how I extracted all the stats from the NCAA website. But what is web scraping? Why does it have a disgusting name? Why should I care about this? I'll try to answer some of these questions, and demonstrate writing a simple script in about 15min and less than 50 lines of code. And maybe after that this topic will become more interesting and inspire some web scraping of your own.

Aside from pulling stats from the NCAA, some other use cases for web scraping could include, pulling stock prices, airfare prices or product data from Amazon or eBay for competitor analysis. For use cases like these, you might set up an automated task to run every day at 9am for example. The script might go to flightnetwork.com, search for London England, get the best price at 9am that day and store it in a spreadsheet that you look at every so often. Maybe you have the task run **every hour** for a month, and when you check your spreadsheet at the end of the month you notice that prices to London drop every Tuesday at 5am. Vacation time! Computers are great at doing dumb boring things over and over again. Kindof like dogs, they want to do this work for us. We just have to teach them how.

So up until this point, I've been able to scrape the NCAA stats from 2002 to 2018. From 1982 to 2002, all the stats are in pdf format. So if I want to extract these numbers, first I have to download all the pdfs for each team, then I have to convert them all to a tabular format like xlsx. This tutorial is about the first step. The [code is here][pdf_gist] if you want to check it out or tinker with it. If you give it a go, or use it for something else please share so we can all learn!

I tried to make this video as simple as possible, but there are cases where knowing some HTML would be helpful. And of course this isn't a live coding session, so I am referring to a file I've already written. But I hope it can be helpful nonetheless.

[![tutorial_video](http://img.youtube.com/vi/x11-T0bSWcM/0.jpg)](http://www.youtube.com/watch?v=x11-T0bSWcM "Web Scraping Tutorial")


[pdf_gist]: https://gist.github.com/jenyeeiam/034c492fee97aec768f59f67a0144640
