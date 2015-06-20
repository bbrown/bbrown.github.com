---
layout: post
title: Making Widgets
date: '2006-02-24 21:30:00 -0700'
mt_id: 1087
blog_id: 1
post_id: 1087
basename: making-widgets
categories:
- go-daddy
- blogging-world
---
<p>So Wordpress now has <a href="http://wordpress.com/blog/2006/02/25/wordpress-widgets/">Widgets</a> and a sidebar editor, available depending on the theme. I tried to drag and drop like they said but I couldn't get it to work on Firefox 1.5 or IE6 on a stock Windows XP installation. Crazy!</p>
<p><a href="http://bbrown.info/images/34-25/old_sidebar.png"><img style="border:0;float:right;margin:5px;" src="http://app.onlinequickblog.com/images/34-25/old_sidebar.jpg" width="300" height="178" alt="View of the current Manage Sidebar screen for Quick Blog" /></a>This is especially timely for me since I've been working on a revision to <a href="http://www.godaddy.com/gdshop/blog/landing.asp">Quick Blog</a>'s Manage Sidebar functionality for our next release. I've always liked the current clickfest version pictured to the right. I spent a lot of time getting its Javascript just right. It's not easy to keep those little arrows looking just so as the components are moved through the list. In fact, there's some pretty sophisticated DOM scripting there because you're actually moving table rows within a table and between two separate tables.</p>
<p>The new version, frankly, rocks the Casbah.</p>
<p>This 1.2 release&#x2014;due soon&#x2014;is cram packed full of features. I seriously think that it is our biggest release ever (well, except for 1.0 because that let the cat out of the bag). We'll also soon have a public blog where we can really discuss things and give the  releases their due. I came up with the name that we're going to use for it, but it's provisional until we can come up with something better. Of course, I'll link to it here when it happens.</p>
<p>[UPDATE (2/26/2006): One of the commenters on that entry <a href="http://wordpress.com/2006/02/25/wordpress-widgets/#comment-1203">said</a>, "This is why Wordpress is lightyears ahead of the 'other guys'!" I have to suppose that that comment was out of ignorance.]</p>
<p>[UPDATE 2 (2/26/2006): <a href="http://andy.wordpress.com/2006/02/25/javascript-drag-and-drop-toolkits/">Looks like</a> the WP.com drag and drop is done using script.aculo.us. It really is a lovely library, but there are some quirks using it. My pet peeve is that there's no onDrop callback for the Sortable, even though there is one on the Droppable. I found an awesome suggestion to use the onMouseUp event.]
</p><p style="font-size:xx-small;">[The views expressed on this website/weblog are mine alone and do not necessarily reflect the views of Go Daddy Software, Inc.]</p>
