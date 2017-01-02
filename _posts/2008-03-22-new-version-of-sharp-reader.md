---
title: New version of Sharp Reader
author: admin
layout: post
permalink: /new-version-of-sharp-reader/
dsq_thread_id:
  - 26004197
categories:
  - Uncategorized
---
<table cellSpacing="2" cellPadding="2" width="100%" border="0">
  <tr>
    <td style="font-family: Verdana,Sans-serif; font-size: 10pt">
      <p>
        <a style="color: #66c; text-decoration: none" href="http://aspnetweblog.com/"></p> 
        
        <p>
          Scott</a> wrote, of Luke writing:
        </p>
        
        <blockquote>
          <p>
            <a style="color: #66c; text-decoration: none" href="http://blog.lotas-smartman.net/wp-content/uploads/2008/03/SharpReader0901.zip"></p> 
            
            <p>
              SharpReader 0.9.0.1</a> has been released. This version has the
            </p>
            
            <p>
              following changes:
            </p>
            
            <ul>
              <li>
                Added a "File | Open" menu-item.
              </li>
              <li>
                Added a "File | Subscribe" menu-item.
              </li>
              <li>
                Mark updated items in <i>italics</i>.
              </li>
              <li>
                Added a label before the address text box; ALT-D selects <p>
                  address text box.
                </p>
              </li>
              
              <li>
                Fixed KeepAlive bug that sometimes kept connections open too <p>
                  long.
                </p>
              </li>
              
              <li>
                Fixed bug in proxy authentication.
              </li>
              <li>
                Better retry-mechanism for failed webrequests.
              </li>
              <li>
                Fixed infinite post-threading.
              </li>
              <li>
                Fixed unnecessary ListView refresh issue.
              </li>
              <li>
                Added debug-statements at app-startup to find Win98/WinME <p>
                  problems. If you&#8217;re running Win98 or WinME, please try to run
                </p>
                
                <p>
                  SharpReader and send me the sharpreader.log file after it fails.
                </p>
                
                <p>
                  Hopefully this will give me some more information that may help
                </p>
                
                <p>
                  resolve this bug.
                </p>
              </li>
              
              <li>
                Open links in external browser now always goes to the system <p>
                  default browser.
                </p>
              </li>
              
              <li>
                implement <p>
                  <a style="color: #66c; text-decoration: none" href="http://www.pocketsoap.com/weblog/2003/04/1202.html"></p> 
                  
                  <p>
                    Simon Fell&#8217;s BlogThis plugin interface</a>. If you save your
                  </p>
                  
                  <p>
                    plugin into a "plugins" subdirectory, SharpReader will find the
                  </p>
                  
                  <p>
                    plugin and make it available in the listview popup menu
                  </p>
                  
                  <p>
                    (shortcut ^B). Simon&#8217;s
                  </p>
                  
                  <p>
                    <a style="color: #66c; text-decoration: none" href="http://www.pocketsoap.com/weblog/2003/04/1205.html"></p> 
                    
                    <p>
                      last drop of Relaxer</a> uses this plugin mechanism to post to
                    </p>
                    
                    <p>
                      RESTLog. <b>Make sure you do NOT put IBlogThis itself in the</p> 
                      
                      <p>
                        plugins directory as this causes .NET to load this interface
                      </p>
                      
                      <p>
                        twice. Since SharpReader will use one copy of IBlogThis and your
                      </p>
                      
                      <p>
                        plugin another, SharpReader will not be able to find the plugin
                      </p>
                      
                      <p>
                        (because it will implement the wrong copy of IBlogThis)</b></li> </ul> 
                        
                        <p>
                          &nbsp;
                        </p>
                        
                        <p>
                          [<a style="color: #66c; text-decoration: none" href="http://www.hutteman.com/weblog/2003/04/17.html#000067">Luke</p> 
                          
                          <p>
                            Hutteman&#8217;s public virtual MemoryStream</a>]
                          </p></blockquote> 
                          
                          <p>
                            Well, read the above. Great work Luke.
                          </p>
                          
                          <p>
                            BTW, this was post was made with the ASPNETWebLog
                          </p>
                          
                          <p>
                            <a style="color: #66c; text-decoration: none" href="http://www.pocketsoap.com/weblog/2003/04/1202.html"></p> 
                            
                            <p>
                              BlogThis</a> Plugin..its not perfect (OK, its not even close, but it
                            </p>
                            
                            <p>
                              works pretty well). You can get it
                            </p>
                            
                            <p>
                              <a style="color: #66c; text-decoration: none" href="http://tripleasp.net/blogcode/ASPNETWebLogPlugin.zip"></p> 
                              
                              <p>
                                here</a>.
                              </p>
                              
                              <p>
                                [<a style="color: #66c; text-decoration: none" href="http://aspnetweblog.com/posts/5751.aspx">ScottW&#8217;s</p> 
                                
                                <p>
                                  ASP.NET WebLog</a>] </td> </tr> </table> 
                                  
                                  <p>
                                    Hmmmm. this BlogThis idea is pretty cool. pity it only works with with
                                  </p>
                                  
                                  <p>
                                    ASPWeblogs. I have movable type and would like to use this. hopefully someone
                                  </p>
                                  
                                  <p>
                                    reads this and works on some code! hehe!
                                  </p>