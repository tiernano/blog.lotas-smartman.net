---
title: 'Some MotorLoggr news: XMPP, Twitter, OpenID'
author: admin
layout: post
permalink: /some-motorloggr-news-xmpp-twitter-openid/
dsq_thread_id:
  - 26016576
  - 26016576
categories:
  - Uncategorized
---
So, I finally got my SQL server up and running for [MotorLoggr][1]. Still nothing there, but if you would like to play with an Alpha version, drop me a mail at <motorloggr@gmail.com>. Anyway, I have been playing with some cool stuff for the last while, and I though I should post some interesting links.

First off, [Twitter][2]. I have been using Twitter for ages, and I see that the likes of [IWantSandy][3] is using it for taking notes, etc. So, I had a look at their [API][4], and managed to get a C# app reading data easily. all you have to do is call an authenticated HTTP page (see the API under Direct Message Methods) and you can get back JSON, XML, RSS or Atom. very nice and easy. Only problem with it is its polled&#8230;

That&#8217;s where XMPP comes in! I have been playing with AG Software&#8217;s [agsmpp-SDK][5]. with literally just a couple of lines of code, you can build an app that talks directly to XMPP. What&#8217;s [XMPP][6]? Its the protocol that [GTalk][7], [Jabber][8], etc, talk. pretty cool stuff&#8230; will be looking at a bot that you can chat to and add data. I may also look into using [Windows Live Agents for Windows Live Messenger][9]&#8230;

Finally, [OpenID][10]. This is something I have been very interested in for a while now. There is a [Membership provider based on OpenID][11], which I would like to play around with&#8230; Lets see what I can actually implement&#8230; <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />

 [1]: http://www.motorloggr.com
 [2]: http://www.twitter.com
 [3]: http://www.iwantsandy.com/
 [4]: http://groups.google.com/group/twitter-development-talk/web/api-documentation
 [5]: http://www.ag-software.de/index.php?page=agsxmpp-sdk
 [6]: http://www.xmpp.org/
 [7]: http://www.google.com/talk/
 [8]: http://www.jabber.org/
 [9]: http://dev.live.com/agents/default.aspx
 [10]: http://www.openid.net
 [11]: http://code.google.com/p/dotnet-membership-provider/