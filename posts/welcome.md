---
title: Welcome
date: 2025-10-20
summary: Welcome to my blog.
---

This post will be pretty short, however here's the gist. I'll publish things I find interesting here!

This website is custom-made using **React** and **Node.js** - yes, I finally gave in (though just this once!). I wanted to play around with the technology of sorts and found it mildly interesting (obviously, otherwise we wouldn't be here right now).

### The domain name
Wow! That's pretty short hm? ``jay.fish`` - an amazing find right? I spent around 3 hours searching for a decent domain name under the premium price point of £40 or more. For example, one candidate was ``jay.zip`` which was £196/year. Bit steep for a personal website, right?

### Spotify & last.fm connection
I am using Spotify's Web API to show what I am currently playing, and then last.fm to fetch what I have previously played and how many times I have played said song.

![Music Player](https://raw.githubusercontent.com/jaysalw/jaysalw/refs/heads/main/blog-assets/2025/music-status.png)

### GitHub Activity Tracking & Stats
Since I'm petty, I added my github activity and statistics on the home page. This simply uses a GitHub fine-grained personal access token stored in an ENV with read-only flags to view my profile and view my public repos.

Cool Right?

### Does the website store anything in a database?
Nope, I was lazy - or rather wanted GitHub to foot the bill 😈 mwhahahaha!

Everything is placed within my profile repository on GitHub: https://github.com/jaysalw/jaysalw
Quite fiting right?

Everything is placed within a MarkDown file (well, each post that is), and I built my own custom renderer too! It caches the current pages for up to 2 hours, then re-renders them. This means that I do not have to store too much data actively on my server's drive and instead place it in memory - which I have more than enough of.
