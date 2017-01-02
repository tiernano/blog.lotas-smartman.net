---
title: Creating Datatables and filling them with what ever you want
author: admin
layout: post
permalink: /creating-datatables-and-filling-them-with-what-ever-you-want/
dsq_thread_id:
  - 26009429
categories:
  - Uncategorized
---
<div class="Section1">
  <p class="MsoNormal" style='text-autospace:none'>
    I was looking for code for making a data table which I could fill with what ever information I wanted to fill it with, and then use it for what ever I want to use it for. Its mainly because some of the things I&rsquo;m working on are in multiple tables and even using an inner joins don&rsquo;t help. So, this way I can create a datatable with the information I want in it, return it via either a webservice or what ever, and it works grand. The following is the code im using.
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    &nbsp;
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;<font color="blue"><span style='color:blue'>Dim</span></font> dt <font color="blue"><span style='color:blue'>As</span></font> <font color="blue"><span style='color:blue'>New</span></font> DataTable <font color="green"><span style='color:green'>&#8216; create an empty table</span></font></span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <font color="blue"><span style='color:blue'>Dim</span></font> row <font color="blue"><span style='color:blue'>As</span></font> DataRow <font color="green"><span style='color:green'>&#8216; new row</span></font></span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <font color="blue"><span style='color:blue'>Dim</span></font> list <font color="blue"><span style='color:blue'>As</span></font> <font color="blue"><span style='color:blue'>New</span></font> ArrayList <font color="green"><span style='color:green'>&#8216; array list that holds the row information</span></font></span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <font color="blue"><span style='color:blue'>Dim</span></font> i <font color="blue"><span style='color: blue'>As</span></font> <font color="blue"><span style='color:blue'>Integer</span></font></span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <font color="blue"><span style='color:blue'>For</span></font> i = 0 <font color="blue"><span style='color:blue'>To</span></font> 6 <font color="green"><span style='color: green'>&#8216; create 7 colums in the row</span></font></span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; list.Add(<font color="blue"><span style='color:blue'>New</span></font> DataColumn(i)) <font color="green"><span style='color:green'>&#8216;create the new colum</span></font></span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; dt.Columns.Add(list(i)) <font color="green"><span style='color:green'>&#8216; name the row as the value of i</span></font></span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <font color="blue"><span style='color:blue'>Next</span></font></span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <font color="blue"><span style='color:blue'>For</span></font> i = 0 <font color="blue"><span style='color:blue'>To</span></font> 200 <font color="green"><span style='color:green'>&#8216; now create 201 rows and add them to the table</span></font></span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <font color="blue"><span style='color:blue'>Dim</span></font> myRow <font color="blue"><span style='color:blue'>As</span></font> DataRow</span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="green"><span style='color:green'>&#8216; Create a new DataRow.</span></font></span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; myRow = dt.NewRow()</span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <font color="blue"><span style='color:blue'>Dim</span></font> z <font color="blue"><span style='color:blue'>As</span></font> <font color="blue"><span style='color:blue'>Integer</span></font></span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <font color="blue"><span style='color:blue'>For</span></font> z = 0 <font color="blue"><span style='color:blue'>To</span></font> 6 <font color="green"><span style='color: green'>&#8216; put data in each colum</span></font></span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; myRow(z) = i</span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <font color="blue"><span style='color:blue'>Next</span></font></span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; dt.Rows.Add(myRow)</span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; dt.AcceptChanges() <font color="green"><span style='color:green'>&#8216; accept the changes in the table</span></font></span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <font color="blue"><span style='color:blue'>Next</span></font></span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; dt.AcceptChanges() <font color="green"><span style='color:green'>&#8216; accept the changes again, just in case</span></font></span>
  </p>
  
  <p>
    <span style=';font-family: "Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; DataGrid1.DataSource = dt <font color="green"><span style='color:green'>&#8216; set the datasource of the datagrid to the table</span></font></span>
  </p>
  
  <p>
    <span style=';font-family: "Courier New"'>After reading the code, I think there could be a quicker way of doing the following code:</span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <font color="blue"><span style='color:blue'>For</span></font> i = 0 <font color="blue"><span style='color:blue'>To</span></font> 6 <font color="green"><span style='color: green'>&#8216; create 7 colums in the row</span></font></span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; list.Add(<font color="blue"><span style='color:blue'>New</span></font> DataColumn(i)) <font color="green"><span style='color:green'>&#8216;create the new colum</span></font></span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; dt.Columns.Add(list(i)) <font color="green"><span style='color:green'>&#8216; name the row as the value of i</span></font></span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&<br /> nbsp;&nbsp;&nbsp;&nb<br /> sp;&nbsp;&nbsp;&nbsp; <font color="blue"><span style='color:blue'>Next</span></font></span>
  </p>
  
  <p>
    <span style=';font-family: "Courier New"'>Replace the code with:</span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <font color="blue"><span style='color:blue'>For</span></font> i = 0 <font color="blue"><span style='color:blue'>To</span></font> 6 <font color="green"><span style='color: green'>&#8216; create 7 colums in the row</span></font></span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; dt.Columns.Add(<font color="blue"><span style='color:blue'>New</span></font> DataColumn(i)) <font color="green"><span style='color:green'>&#8216; name the row as the value of i</span></font></span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    <span style=';font-family:"Courier New"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <font color="blue"><span style='color:blue'>Next</span></font></span>
  </p>
  
  <p class="MsoNormal" style='text-autospace:none'>
    Not sure if it speeds up anything, but in theory it should. You could also remove the list variable. Hope this helps someone!
  </p>
</div>