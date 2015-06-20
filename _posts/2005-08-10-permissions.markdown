---
layout: post
title: Permissions
date: '2005-08-10 08:17:10 -0700'
mt_id: 984
blog_id: 1
post_id: 984
basename: permissions
categories:
- go-daddy
- net-development
---
<br />I've spent the last few days working out a permission model for the application I'm developing. I've always wanted to use bits and bitwise operators for some sort of authorization system and it's everything I ever thought it would be.<br /><br />What's really cool is that I've encapsulated the permissions to the user object so that all my fellow developers have to do to use it is call <code>User.CheckPermissions</code> and then pass in the desired enumeration values. It returns a true or false. .NET makes it terribly easy, requiring nothing more than the <a href="http://dotnet.org.za/armand/articles/168.aspx">Flag attribute</a> on the enumeration and setting the enumeration values to powers of 2.<br /><br />What's more, thanks to the ease of bitwise operation, they can pass in several permissions in bitwise AND/OR formation. This makes for an <strong>incredibly</strong> powerful authorization system. In other words, my co-workers can say <code>User.CheckPermissions(Permissions.CanDoThis &amp; Permissions.CanDoThat)</code> and find out whether the user can do both this and that. Having just spent the last day or two actually implementing permissions throughout the app, I can say that this is very intuitive and clear.<br /><br />There's some other little nifty features, but I can't go into them unfortunately.<br /><br />[NOTE: The views expressed on this website/weblog are mine alone and do not necessarily reflect the views of Go Daddy Software, Inc.]<br /><br /><br />
