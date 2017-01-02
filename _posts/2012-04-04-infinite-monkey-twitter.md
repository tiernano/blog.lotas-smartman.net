---
title: Infinite Monkey Twitter
author: admin
layout: post
permalink: /infinite-monkey-twitter/
dsq_thread_id:
  - 636419078
dsq_needs_sync:
  - 1
categories:
  - Code
tags:
  - Code
  - monkey
  - Twitter
---
The [Infinite Monkey Theorem][1] states: 

> a monkey hitting keys at random on a typewriter keyboard for an infinite amount of time will almost surely type a given text, such as the complete works of William Shakespeare.

This made me think&#8230; and more importantly, think about Twitter&#8230; I am thinking about my Final Year college project, and have been playing with the Twitter Streams API for the last few days. So far, i have about 650k of tweets to play with, but it made me think about using &#8220;fake&#8221; data for tweets&#8230; take the following as an example:

  * monkey tosses coin to say if its a response or a new tweet. if its a response, a new coin is used to figure if he responds to some he follows or someone he does not follow&#8230; if he does not follow, finally tosses a third time to figure if he wants to respond to a &#8220;famous&#8221; (more than 10000 followers) or not other monkey&#8230;
  * if response, find a tweet to respond to
  * monkey randomly takes a number from 1 to (140 &#8211; 1 (@) + twitter user name + 1 (space)). this is char count
  * monkey now tosses a coin to figure if he wants to add a hash tag&#8230; if yes, he tosses again to either use a random trending hashtag or a completely different one&#8230;
  * finally, the monkey, using the number of characters left, randomly hits the keyboard and makes a nonsense tweet&#8230;

this is much how i tweet at [@tiernano][2] <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />

anyway, using this as an idea, and adding in monkeys following each other depending on how they feel (more coin tossing) you could get a lot of tweets using some lower powered machines (worker nodes) and some beefy hardware&#8230; this is starting to sound like an interesting problem&#8230; now to figure out more&#8230; leave it with me&#8230;

 [1]: http://en.wikipedia.org/wiki/Infinite_monkey_theorem
 [2]: http://twitter.com/tiernano