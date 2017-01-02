---
title: 'HowTo: Get around an NTLM Proxy (kind of)'
author: admin
layout: post
permalink: /howto-get-around-an-ntlm-proxy-kind-of/
dsq_thread_id:
  - 26007558
categories:
  - Uncategorized
---
Right. they have just installed an NTML Auth Proxy in work, and stuff like [Opera][1], [WBloggar][2] and other things cant get though it because of the NTML. so, i did some searching (IE and Mozilla works, but i really like opera, BTW) and found [APS Server][3]. Its an Authorization Proxy Server. basically, it connects to your proxy, authorizes its self (with your password) and then sets up a local port for you to use. then you just tell your apps with use standard proxies to connect to its port on local host, and heay presto, it works! handy. You need a copy of [Python][4], so it will work on windows, linux, mac, etc, and you need the package from the [APS Server website][3]. install python, then unpack the aps server package, and open your favourite text editior, edit the config file (fairly easy to under stand the docs there) and save it. then run the main.py file. if you have python installed properly, just run it from the command line (under windows). and it works! i am using it now to use w.bloggar on a NTML proxy. mozilla works with NTML, IE is now working using APS as the proxy, and i have just gotten opera running too! now, its not actually getting around the NTLM proxy. you still need to tell it your username and password, and your still blocked by stuff that the proxy has blocked, but its a start! bk_keywords: proxy

 [1]: http://www.opera.com
 [2]: http://www.wbloggar.com
 [3]: http://apserver.sourceforge.net/
 [4]: http://www.python.org