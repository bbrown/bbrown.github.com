---
layout: post
title: Web.config and Virtual Directories
date: '2008-02-21 09:49:57 -0700'
mt_id: 1262
blog_id: 1
post_id: 1262
basename: web-config-and-virtual-directories
categories:
- net-development
---
<p>At work today, I ran into some trouble trying to set up a virtual directory as an application in IIS. My two applications, the parent and the child, occupied different locations in the filesystem, had separate app pools, and different app names. Due to the inheritance of Web.config, though, the HTTP modules defined in the parent app were throwing configuration exceptions in the child app even though the child app never referenced any of the HTTP modules. </p> <p>I thought about adding an httpModule section to the child app's Web.config with a remove call, but that seemed klunky to me. Frantic Google searching wasn't giving any better solutions. Following the link chains from blog entry to blog entry to comments to more blog entries, I stumbled upon the answer: </p> <blockquote><code>&lt;location inheritinchildapplications="false"&gt;<br />&#xA0; &lt;system.web&gt;<br />&#xA0;&#xA0; &lt;httpmodules&gt;<br />&#xA0;&#xA0;&#xA0; …<br />&#xA0;&#xA0; &lt;/httpmodules&gt;<br />&#xA0; &lt;/system.web&gt;<br />&lt;/location&gt;</code><cite><a href="http://aspadvice.com/blogs/ssmith/archive/2006/08/21/HttpModule-Breaks-SubApplications-Problem-Solved.aspx">source</a></cite> </blockquote> <p>Of course! This breaks the inheritance chain and it only touches the parent app's Web.config. </p>
