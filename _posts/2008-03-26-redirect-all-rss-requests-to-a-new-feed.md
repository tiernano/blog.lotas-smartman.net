---
title: Redirect all RSS requests to a new Feed
author: admin
layout: post
permalink: /redirect-all-rss-requests-to-a-new-feed/
dsq_thread_id:
  - 26016508
categories:
  - Uncategorized
---
When i moved from Community Server to Graffiti, my RSS Feed end point, by default, moved from /rss.aspx to /feed. Since the rss.aspx request was being handled by Community Server and automatically 301ed the user to FeedBurner, most Feed readers had that as their endpoint. the problem is that there is no rss.aspx with Graffiti, and over the last 9 hours or so, i have recieved 520 requests to the old address, all returning an error message. The solution follows the break.

&nbsp;