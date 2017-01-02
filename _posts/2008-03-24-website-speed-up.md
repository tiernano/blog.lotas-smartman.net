---
title: website speed up
author: admin
layout: post
permalink: /website-speed-up/
categories:
  - Uncategorized
---
One of the things i had on my site was a view counter for wordpress that told users how many times a post had been viewed. although it was handy, i realized that it made a load of connections to the database and slowed page loading times down. so, i removed this feature and page load times are down from around 6 seconds to 2 seconds. not bad for removing a single line of code&#8230; going to work on a MySQL cluster now, so that if the workstation gets overloaded, one of the other machines will take over, or if the workstation goes down for a minuite or 2, the others will take over, etc. more on that later.