---
title: GitHub Contribution Graph Legend
date: 2019-02-26 04:55:17
type: post
blog: true
excerpt: Ever wonder what it takes to achieve certain colors in the GitHub contribution graph? Here's a quick post on what I found.
tags:
commitLegend:
 - numberOfContributions: "0"
   color: "#ebedf0"
 - numberOfContributions: "1-6"
   color: "#c6e48b"
 - numberOfContributions: "7-13"
   color: "#7bc96f"
 - numberOfContributions: "14-19"
   color: "#239a3b"
 - numberOfContributions: "20+"
   color: "#196127"
---

On every GitHub user's profile page, there is a graph that is hard to ignore:

![My GitHub contribution graph](/images/2019/2019-02-26-contribution-graph.png)

While there is controversy whether the graph is more harmful to developers ([see discussion thread](https://twitter.com/EmmaWedekind/status/1099235211555074048)), I have always been curious the amount of commits needed to generate a certain color within the graph. And while the internet is great for finding random information like this, I was unsuccessful at finding it. 

So, thankfully my GitHub contribution graph has a fair amount of variance in the data to allow me to figure it out.

## Contribution Square Legend

::: warning
So it turns out that there may be more to the algorithm than I'm aware of, I discovered that other people's contribution graphs don't match up with mine when it comes to number of contributions and what color the square is. 🤦‍
:::

<ul style="padding-left: 0">
  <li v-for="item in this.$frontmatter.commitLegend" 
    style="padding: 5px 15px; display: flex; align-items: center; margin-left: 0">
    <div :style="`background-color: ${item.color}; width: 50px; height: 50px; margin-right: 15px`"></div>
    <p>{{ item.numberOfCommits }} contributions: <code>{{ item.color }}</code></p>
  </li>
</ul>

## Final Thoughts

If it isn't obvious, I have been embarking to try and fill all of my squares for 2019. Is this gamification ultimately negative? Only time will tell. At the very least though, it has helped me to build a habit of working on something consistently rather than in one big swoop. I'll probably need a whole post dedicated to this, but that's for another time. 

Till next time!