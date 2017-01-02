---
title: Anti Spam tools
author: admin
layout: post
permalink: /anti-spam-tools/
dsq_thread_id:
  - 26015995
categories:
  - Uncategorized
---
Running your own mail server at home has its benefits, but also can be a bit of a pain. Most ISP&#8217;s now offer some sort of Spam and Virus Filtering. When you run it your self, you need to do this your self. Over the last couple of days I have been playing with 2 different packages for filtering spam and viruses from your email. 

The main one I have been using is a Windows based app that sits between your Router and your mail server. Its called [No Spam Today][1] and so far so good.&nbsp;instead of port 25 being forwarded directly to your mail server, you set it up to hit this machine first. it then runs some checks on the email (spam assassin, attachment blocking, etc) and then if the email passes, it forwards it to your real server, which then passes it to the user. If the email is spam, there is the option of dropping it immediately, or filtering it, but I use the option of flagging it as spam in the header, and then get Outlook to filter that to a spam folder.

The other option I have looked into is [ProxMox Mail Gateway][2]. its a Linux based solution which does pretty much the same as above. I have ProxMox installed in Virtual Server, running on the network, but I haven&#8217;t configured it fully yet, so its not in production.

The difference between the 2 is price. ProxMox has a free version, which you can install on any old hardware, and setup in a matter of minutes (if you read the manual, which I haven&#8217;t fully). NoSpamToday is the same, but it installs on a Windows Machine, so no formatting of machines needed. Its also not free. Its $200 (at time of writing) for a 10 user license. Since I only have 2 real email accounts (3 if you include Administrator and Postmaster accounts) 10 licenses is over kill. There are paid versions of ProxMox, and they charge by the domain, not the users. your talking EUR399 for a single domain license for the standard edition, or 2 grand for the Pro. And then, virus protection is an extra 269EUR and that&#8217;s for 50 users&#8230; 

I really should be gratefully though. So far, since installing NoSpamToday, it has blocked:

  * 1000 emails which done exist on the domain (I have a list of email addresses I am using in a list. there are better ways, but I haven&#8217;t configured them yet&#8230;
  * 100 emails where allowed though the first check, of which 70 where marked as spam!
  * another 150 emails where ignored due to a delay filter (email processing is paused, and if the sender disconnected before time runs out, its considered spam. most normal, non spam email servers will wait).

Not bad for 3 days of processing! <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" /></p> 

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:8a03c820-e79c-4522-ab97-f2b81fb6d2ed" style="padding-right:0px;display:inline;padding-left:0px;padding-bottom:0px;margin:0px;padding-top:0px;">
  Technorati Tags: <a href="http://technorati.com/tags/Anti%20Spam" rel="tag">Anti Spam</a>, <a href="http://technorati.com/tags/NoSpamToday" rel="tag">NoSpamToday</a>, <a href="http://technorati.com/tags/ProxMox" rel="tag">ProxMox</a>, <a href="http://technorati.com/tags/Exchange" rel="tag">Exchange</a>
</div>

 [1]: http://www.nospamtoday.com/
 [2]: http://www.proxmox.com/cms_proxmox/en/products/mail-gateway/