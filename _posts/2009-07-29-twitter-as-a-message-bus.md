---
title: Twitter as a message bus
author: admin
layout: post
permalink: /twitter-as-a-message-bus/
dsq_thread_id:
  - 27474546
  - 27474546
categories:
  - Uncategorized
tags:
  - AgTweet
  - SMS
  - Tweet Sandwich
  - 'Tweet#'
  - Twitter
---
a couple of days ago, i was browsing [Programmable Web][1] under their [SMS keyword][2], and was thinking about how interesting it would be to get an app (web app or service) to listen to SMS messages and maybe even reply. and then it came to me: [why SMS? Why not Twitter?][3]

Twitter has a [nice API][4] which you can use to get messages (be they direct or public) and also allows you send them back. And if you are in certain countries, you can send and receive SMS messages to and from Twitter also. (Ireland cant receive them at the moment, but thanks to [Agtweet][5] you can send them using either a Vodafone or Meteor mobile number which might be free depending on your package).

So, then the question gets asked: Why would you want to use SMS only? any time i have gone looking for SMS –> PC stuff (as a service) they charge quite a lot of money and are limited to certain countries… with Twitter, anyone with a twitter account, which is free, can send and receive messages from your service. There are already a few services that support this (i wont go into them now… too lazy). 

So, how do you do it in C#? there are (as of writing) [4 C# libraries listed on the Twitter Libraries page][6]. these usually include docs and code samples (Tweet# for example have [OAuth Examples for both Web and Desktop Apps][7]). There is even a library for [SQL Server T-SQL][8]! so, as a trigger on a table, you could send out a tweet when something gets inserted! 

To Give an idea of how “Twitter as a message bus

 [1]: http://www.programmableweb.com/
 [2]: http://www.programmableweb.com/apitag/sms
 [3]: http://twitter.com/tiernano/status/2873506351
 [4]: http://apiwiki.twitter.com/
 [5]: http://agtweet.com/
 [6]: http://apiwiki.twitter.com/Libraries#C/NET
 [7]: http://tweetsharp.com/?page_id=5
 [8]: http://www.sqlsharp.com/