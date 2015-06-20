---
layout: post
title: Revisiting the Past
date: '2007-01-26 22:43:00 -0700'
mt_id: 1198
blog_id: 1
post_id: 1198
basename: revisiting-the-past
categories:
- programming
- net-development
- go-daddy
---
<p>
Today I finally had the chance to revisit <a href="http://bbrown.info/2005/08/21/service-with-a-smile-2.aspx">the first service</a> I ever wrote. I christened it Pingarooni and it handles all the outgoing trackbacks and pings for <a href="http://www.godaddy.com/gdshop/blog/landing.asp">Quick Blog</a>. It's been a long time since I've been in a position to re-examine early code done in a state of relative ignorance&#x2014;I've been coding in ASP.NET for so long that my code is generally something of which I'm quite proud.
</p>
<p>
But I had never created a Windows service. The only non-Web application I'd ever created was <a href="http://sourceforge.net/projects/logzipper/">a console application</a>&#x2014;certainly a world apart. I didn't really know what I was doing so my code evinced a certain textbook formality that subsequent services I wrote had thankfully shed. The flow of it was horrendous and I'm surprised it lasted as long as it did.
</p>
<p>
Here are the things I learned in revising it:
</p>
<ul>
<li>Make your service work on batches at a time. By doing so, you'll be able to see progress and some freak error will only affect a small number of work items.</li>
<li>Make the service work on discrete work units so that many instances of the service can be run in parallel.</li>
<li>Make the service update the database to report its progress as soon as possible. At the least, it should report every batch if not throughout the batch.</li>
<li>Make the service run continuously if possible, stopping only when an OnStop event is raised. If the work load is neverending, there's no sense in pausing between runs.</li>
<li>Make the service use plugins along <a href="http://en.wikipedia.org/wiki/Command_pattern">command pattern</a> lines to define its work. If possible, these plugins should be put into a separate assembly or module so that additional plugins can be introduced with a simple restart of the service.</li>
</ul>
<p style="font-size:xx-small;">
The views expressed on this website/weblog are mine alone and do not necessarily reflect the views of Go Daddy.com Software, Inc.
</p>
