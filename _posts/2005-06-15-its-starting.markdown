---
layout: post
title: It's Starting
date: '2005-06-15 14:46:54 -0700'
mt_id: 939
blog_id: 1
post_id: 939
basename: its-starting
categories:
- go-daddy
---
<br />Today I started development on the app I've been designing for the last couple weeks. I had forgotten that feeling of starting from scratch. That moment where you're done preparing documentation and you open up VisualStudio.NET, create a new solution, and think, "What now?"<br /><br />So I did what any normal developer does. I procrastinated by building out framework level stuff: logging, components, and subsystems. Then I got tired of that and actually started working on the HTML prototype. I think I've got the basics of a really great design.<br /><br />Oh and one thing I learned that might be helpful for someone out there. If you're trying to get <a href="http://logging.apache.org/log4net/">log4net</a> working and you just want a simple test to make sure everything's working, remember that the <a href="http://logging.apache.org/log4net/release/sdk/log4net.Appender.TraceAppender.html">TraceAppender</a> is not the <a href="http://logging.apache.org/log4net/release/sdk/log4net.Appender.AspNetTraceAppender.html">AspNetTraceAppender</a>. I spent quite awhile wondering why the heck nothing came up in the trace even though log4net was showing that it was configured and all the loggers were at the levels I specified.<br /><br />[NOTE: The views expressed on this website/weblog are mine alone and do not necessarily reflect the views of Go Daddy Software, Inc.]<br /><br /><br />
