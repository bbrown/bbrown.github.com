---
layout: post
title: Blogging Outside Yourself
date: '2006-10-16 15:53:00 -0700'
mt_id: 1154
blog_id: 1
post_id: 1154
basename: blogging-outside-yourself
categories:
- go-daddy
- blogging-world
---
<p>
Just finished deploying the latest release of <a href="http://www.godaddy.com/gdshop/blog/landing.asp">Quick Blog</a> today and boy was it a fun development cycle. My feature was implementing the <a href="http://www.xmlrpc.com/metaWeblogApi">MetaWeblog API</a>. This API, if you don't know, allows you to blog from a variety of tools instead of being constrained to the admin interface provided by your blogging engine.
</p>
<p>
Now, obviously I'm a big fan of my chosen blogging engine but sometimes it's nice to have options and a change of scenery. The <a href="http://en.wikipedia.org/wiki/MetaWeblog">MetaWeblog API</a>, along with the MovableType API, the Blogger API, and the Atom Publishing API, sets a standard around which software developers and blog publishers can collaborate. The collaboration is unavoidable because the API specification is a steaming pile.
</p>
<p>
Like <a href="http://diveintomark.org/archives/2002/10/08/in_praise_of_evolvable_formats">all specs Winerian</a>, the ambiguity rapidly becomes evident as you get down to work. I first implemented the specification as written. Fire up <a href="http://ecto.kung-foo.tv/">Ecto</a> and see what happens. XmlRpcFaultException. Lovely. Look at <a href="http://ecto.kung-foo.tv/archives/001401.php" title="Oh what a ass saver!">the Logging Console</a> and step through the debugger. Ahh, I took the spec one way and Ecto took it the other. Try another client and see that usage has cemented on Ecto's way. Nice. Continue with each MetaWeblog endpoint.
</p>
<p>
In the end, though, it was a lot of fun because now we integrate well with Windows Live Writer, Flickr, and Google Docs. We might implement the other APIs at some point but I don't know that they give us anything that we don't already have. I've pored over their specs and it's mostly just more of the same&#x2014;each implemented slightly differently, varying in names, inputs, or outputs. It really feels like the feed wars all over again; I've just never seen a compelling reason to pick one over the other except that the non-Winerian specifications are universally rigorous and easier to implement.
</p>
<p style="font-size:xx-small;">[The views expressed on this website/weblog are mine alone and do not necessarily reflect the views of Go Daddy Software, Inc.]</p>
