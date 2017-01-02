---
title: Modified code for making SQL select statments quickly
author: admin
layout: post
permalink: /modified-code-for-making-sql-select-statments-quickly/
dsq_thread_id:
  - 26009617
categories:
  - Uncategorized
---
Ok. the following code is something i use a fair amount. There would be something in a table with information in it like the following:  


> 45,43,56,77,22,33</p>
This would repesent, lets say as an example, an order for a user. so the user would have bought them products in a single purchase. To get the information about the products, i send that string into a function that splits it and returns a SQL statement. Now, the following code includes a button for testing it. If you see any better ways of doing this, please post a reply!  


> <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;;color:blue">Private</span><span style="font-size:10.0pt;font-family:&quot;Courier New&quot;"> <span style="color:blue">Sub</span> Button1_Click(<span style="color:blue">ByVal</span> sender <span style="color:blue">As</span> System.Object, <span style="color:blue">ByVal</span> e <span style="color:blue">As</span> System.EventArgs) <span style="color:blue">Handles</span> Button1.Click</span> 
> 
> <p class="MsoNormal" style="text-autospace: none">
>   <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; MsgBox(test(";1;2;3;4;5;"))</span>
> </p>
> 
> <p class="MsoNormal" style="text-autospace: none">
>   <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp; <span style="color:blue">End</span> <span style="color:blue">Sub</span></span>
> </p>
> 
> <p class="MsoNormal" style="text-autospace: none">
>   <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp; <span style="color:blue">Private</span> <span style="color:blue">Function</span> test(<span style="color:blue">ByVal</span> list <span style="color:blue">As</span> <span style="color:blue">String</span>) <span style="color:blue">As</span> <span style="color:blue">String</span></span>
> </p>
> 
> <p class="MsoNormal" style="text-autospace: none">
>   <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">Dim</span> sql <span style="color:blue">As</span> <span style="color:blue">String</span></span>
> </p>
> 
> <p class="MsoNormal" style="text-autospace: none">
>   <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; sql = "select * from products where productid = "</span>
> </p>
> 
> <p class="MsoNormal" style="text-autospace: none">
>   <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">Dim</span> seperator <span style="color:blue">As</span> <span style="color:blue">String</span> = ""</span>
> </p>
> 
> <p class="MsoNormal" style="text-autospace: none">
>   <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">Dim</span> x <span style="color:blue">As</span> Array</span>
> </p>
> 
> <p class="MsoNormal" style="text-autospace: none">
>   <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">Dim</span> i <span style="color:blue">As</span> <span style="color:blue">Integer</span></span>
> </p>
> 
> <p class="MsoNormal" style="text-autospace: none">
>   <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; x = Split(list, ";")</span>
> </p>
> 
> <p class="MsoNormal" style="text-autospace: none">
>   <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">For</span> i = 0 <span style="color:blue">To</span> x.Length &#8211; 1</span>
> </p>
> 
> <p class="MsoNormal" style="text-autospace: none">
>   <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">If</span> x(i) <> "" <span style="color:blue">Then</span></span>
> </p>
> 
> <p class="MsoNormal" style="text-autospace: none">
>   <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; sql += seperator & x(i)</span>
> </p>
> 
> <p class="MsoNormal" style="text-autospace: none">
>   <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; seperator = " or productid =&nbsp; "</span>
> </p>
> 
> <p class="MsoNormal" style="text-autospace: none">
>   <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">End</span> <span style="color:blue">If</span></span>
> </p>
> 
> <p class="MsoNormal" style="text-autospace: none">
>   <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">Next</span></span>
> </p>
> 
> <p class="MsoNormal" style="text-autospace: none">
>   <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">Return</span> sql</span>
> </p>
> 
> <p class="MsoNormal" style="text-autospace: none">
>   <span style="font-size:10.0pt;font-family:&quot;Courier New&quot;">&nbsp;&nbsp;&nbsp; <span style="color:blue">End</span> <span style="color:blue">Function</span></span>
> </p>

Hope this helps!