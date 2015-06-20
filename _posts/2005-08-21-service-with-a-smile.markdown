---
layout: post
title: Service with a Smile
date: '2005-08-21 03:47:47 -0700'
mt_id: 994
blog_id: 1
post_id: 994
basename: service-with-a-smile
categories:
- go-daddy
---
<br />The last few days I've had an opportunity to create two Windows services for the product I'm working on. I was surprised at how easy .NET makes these things. The hardest part was figuring out <a href="http://www.codeproject.com/dotnet/dotNETSCMDescription.asp">how to set the description</a> that shows up in the Services menu. The rest was just tricky business rules type stuff. Sadly, I didn't figure out a way to work <a href="http://www.15seconds.com/issue/031202.htm"><acronym title="Microsoft Message Queue">MSMQ</acronym></a> into the picture. Instead, I had to use SQL Server as a message queue since the stored procedures had to send the messages at various insertion points.<br /><br />Man, I wish I could just tell you what I was working on so I could actually provide more detail. All in due time, Mr. Brown. All in due time.<br /><br />[NOTE: The views expressed on this website/weblog are mine alone and do not necessarily reflect the views of Go Daddy Software, Inc.]<br /><br /><br />
