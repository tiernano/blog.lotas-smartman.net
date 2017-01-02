---
title: the reason i should upgrade to MySQL 4.0
author: admin
layout: post
permalink: /the-reason-i-should-upgrade-to-mysql-40/
dsq_thread_id:
  - 26008225
categories:
  - Uncategorized
---
I just found the best reason for testing MySQL 4.0: <a href=\"http://www.mysql.com/doc/en/Query_Cache.html\">Query Cache</a>. when you visit this page, the server runs a query selecting all the latest posts. when the next user arrives, the server does exactly the same. this continues till i post a new post, and then the query is the same, but the results are different. query cache enables the server to know when the same query has been run, and then uses the same results. so when 20 visitors arrive at the site and i havent posted anything new since the first user visits, the load time should go down (see the bottom of the page for load time in seconds) and the load on the server should go down too. Now to figure out how to install MySQL 4.0 on my server&#8230;