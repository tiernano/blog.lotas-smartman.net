---
title: Stoping DDOS Attacks
author: admin
layout: post
permalink: /stoping-ddos-attacks/
dsq_thread_id:
  - 26003831
categories:
  - Uncategorized
---
[This article][1] on [Linux Journal][2] asks the question:

> <font class="content" color="#000000"><i>Considering how difficult they are to trace back to the original offender, if anyone is willing to do so, what might be an alternative means of ending DDOS attacks?</i></font>

It then states:

> <font class="content" color="#000000">On Thursday, February 20, 2003, at about 0130 GMT, the popular Live Journal site became the victim of a massive distributed denial-of-service attack. Live Journal staffers and upstream providers first tried to filter by IP, but they soon discovered what the "D" in DDOS means. After blocking about one quarter of the IP addresses on the Internet, they got on their load balancer and implemented some unknown but effective measures (repeated e-mails to them went unanswered). I can only assume these measures included some quality of service/rate limiting methods. Despite continued flooding, the site returned to usability after about four days of being somewhere between slow and totally unreachable. </font>

The article has some info about how to try and stop some types of DDOS attacks. It also states that if your DDOSed, your kind of screwed, because there&#8217;s not a lot to do. I did, however, [find this][3]. its an Apache 1.3 module that sees who is requesting pages from you, and if its more then 1 a second, it blocks them for a set amount of time. it sends a 403 error message. once a single 403 incident occurs, it blogs the IP address for 10 seconds.&nbsp; may be handy if you think your could be vulnerable to DDOS attacks, but aren&#8217;t we all?

 [1]: http://www.linuxjournal.com/article.php?sid=6749&mode=thread&order=0
 [2]: http://www.linuxjournal.com/
 [3]: http://www.networkdweebs.com/stuff/security.html