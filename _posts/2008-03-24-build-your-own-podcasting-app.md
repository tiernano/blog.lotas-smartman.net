---
title: Build your own PodCasting App
author: admin
layout: post
permalink: /build-your-own-podcasting-app/
dsq_thread_id:
  - 26015421
  - 26015421
categories:
  - Uncategorized
---
Ok, well, i wont be showing you how to, but its a step in the right direction! First, MSDN has an article showing you [how to record and play sound using the WaveForm Audio Interface][1]. this will allow you to record your podcast into a WAV file. Next, there is the [C# MP3 compressor][2], which will convert your WAV File to your MP3. 

then with the help of the [MP3 ID3v1 editor][3] you can set your ID3 data, rename your file the way you want (still looking to embed album art into the MP3 its self, like iTunes does). and then upload it. 

There are other things you can do with this. For example, with the help of [Windows Media Audio Compressor][4]&nbsp;you can build WMAs and also MP3s, and have both formats. You could have low bit rate audio (say 32 ro 64k) available on HTTP downloads (using, lets say, [Amazon S3][5] or [Libsyn][6]) and higher quality versions (96 and 128k) available on BitTorrent using something like [BTSharp][7]&nbsp;with the help of S3 again.

this could work&#8230;. <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />

 [1]: http://msdn2.microsoft.com/en-us/library/aa446573.aspx
 [2]: http://www.codeproject.com/cs/media/MP3Compressor.asp
 [3]: http://www.codeproject.com/useritems/ID3v1_Editor.asp
 [4]: http://www.codeproject.com/managedcpp/WmaCompressor.asp
 [5]: http://www.amazon.com/s3
 [6]: http://www.libsyn.com/
 [7]: http://www.mono-project.com/Bitsharp