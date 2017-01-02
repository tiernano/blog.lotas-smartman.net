---
title: emailing exceptions for remote testing
author: admin
layout: post
permalink: /emailing-exceptions-for-remote-testing/
dsq_thread_id:
  - 26011263
categories:
  - Uncategorized
---
Ok. Something I want in some of my applications, mainly web apps, is the ability for me to get an email when an unhandled exception is found, or any exception is found. So, here is some code I just hacked up as a test to show you how it works. Firstly, the actual exception handling code. The reason I made this into a function is because it will be called a lot in the web application, so a function will make life easer for me. 

<p class="MsoNormal" style="text-autospace:none">
  <span style="font-size:10.0pt;<br />
font-family:&quot;Courier New&quot;">&nbsp;</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp; <span style="color:blue">Public</span> <span style="color:blue">Function</span> EmailException(<span style="color:blue">ByVal</span> ex <span style="color:blue">As</span> Exception, <span style="color:blue">ByVal</span> sendto <span style="color:blue">As</span> <span style="color:blue">String</span>)</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">Dim</span> message <span style="color:blue">As</span> <span style="color:blue">New</span> MailMessage</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">Dim</span> server <span style="color:blue">As</span> <span style="color:blue">String</span> = "<b>InsertServerHere</b>" <span style="color:green">&#8216; this is the server your mail will be sent though. Change this to your server</span></span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">Dim</span> from <span style="color:blue">As</span> <span style="color:blue">String</span> = "<b>InsertEmailHere</b>" <span style="color:green">&#8216; this is the email address the message will come from. Change this to your email address</span></span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; message.Subject = "Caught Exception: " & ex.Message</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; message.From = from &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;message.BodyFormat = MailFormat.Html</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; message.Body = ex.Message & "<br>" & ex.StackTrace</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; message.To = sendto</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; SmtpMail.SmtpServer = server </span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; SmtpMail.Send(message)</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; MsgBox("caught exception and sent by email")</span>
</p>

<p class="MsoNormal" style="text-autospace:none">
  <span style="font-size:10.0pt;<br />
font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp; <span style="color:blue">End</span> <span style="color:blue">Function</span></span>
</p>

<p class="MsoNormal" style="text-autospace:none">
  &nbsp;
</p>

<p class="MsoNormal" style="text-autospace:none">
  As you can see in the function, it takes in the exception, and also an email address that the information will be sent to. There are some variables that need to be changed for this to work properly next is the test function I used. This is fairly basic. 2 input boxes take in 2 numbers and then return the value of the first one divided by the second one. I tried the first one as 4 and the second as 0 but no exception was thrown. It just returns infinity. So, then I tried 4 and h. the h caused an exception.
</p>

<p class="MsoNormal" style="text-autospace:none">
  &nbsp;
</p>

<p class="MsoNormal" style="text-autospace:none">
  <span style="font-size:10.0pt;<br />
font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp; <span style="color:blue">Private</span> <span style="color:blue">Sub</span> Form1_Load(<span style="color:blue">ByVal</span> sender <span style="color:blue">As</span> System.Object, <span style="color:blue">ByVal</span> e <span style="color:blue">As</span> System.EventArgs) <span style="color:blue">Handles</span> <span style="color:blue">MyBase</span>.Load</span>
</p>

<p class="MsoNormal" style="text-autospace:none">
  <span style="font-size:10.0pt;<br />
font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">Try</span></span>
</p>

<p class="MsoNormal" style="text-autospace:none">
  <span style="font-size:10.0pt;<br />
font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">Dim</span> i <span style="color:blue">As</span> <span style="color:blue">Integer</span> = InputBox("enter a number")</span>
</p>

<p class="MsoNormal" style="text-autospace:none">
  <span style="font-size:10.0pt;<br />
font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">Dim</span> j <span style="color:blue">As</span> <span style="color:blue">Integer</span> = InputBox("enter another number")</span>
</p>

<p class="MsoNormal" style="text-autospace:none">
  <span style="font-size:10.0pt;<br />
font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; MsgBox(i / j)</span>
</p>

<p class="MsoNormal" style="text-autospace:none">
  <span style="font-size:10.0pt;<br />
font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">Catch</span> ex <span style="color:blue">As</span> Exception</span>
</p>

<p class="MsoNormal" style="text-autospace:none">
  <span style="font-size:10.0pt;<br />
font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; EmailException(ex, "<b>insertemailaddresshere</b>") <span style="color:green">&#8216;the email address is where the email will be sent to. Change this to suit</span></span>
</p>

<p class="MsoNormal" style="text-autospace:none">
  <span style="font-size:10.0pt;<br />
font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">End</span> <span style="color:blue">Try</span></span>
</p>

<p class="MsoNormal" style="text-autospace:none">
  <span style="font-size:10.0pt;<br />
font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp; <span style="color:blue">End</span> <span style="color:blue">Sub</span></span>
</p>

<p class="MsoNormal" style="text-autospace:none">
  <span style="font-size:10.0pt;<br />
font-family:&quot;Courier New&quot;;color:blue">&nbsp;</span>
</p>

<p class="MsoNormal">
  So, hopefully this helps someone! Good luck and happy coding!
</p>