---
layout: post
title: Ch-Ch-Ch-CheckBot
date: '2008-09-30 03:33:23 -0700'
mt_id: 1369
blog_id: 1
post_id: 1369
basename: ch-ch-ch-checkbot
categories:
- high-geekery
- go-daddy
---
<p>
Yesterday I released my latest project at work. I call it CheckBot and it is a Windows service that pulls down messages from a third-party service, checks them for domain names, and replies with whether those domain names are available. I built it using a plugin architecture, so adding third-party services is a breeze.
</p>
<p>
The first plugin was Twitter. A Twitter user just has to follow <a href="http://twitter.com/domaincheck">domaincheck</a> and then send that bot account a domain name through the direct messaging system. Within seconds, CheckBot will respond with its availability and include a link to register it on GoDaddy.com if it is available.
</p>
<p>
I am very proud of this application because I did it fairly quickly and I like the simplicity of the design. There was only one bug that came up during testing and it was both minor and quickly resolved. This sort of thing is exactly the reason why I love my job and the Gadgets Team I lead.
</p>
<p style="font-size:xx-small;">
[The views expressed on this website/weblog are mine alone and do not necessarily reflect the views of Go Daddy Software, Inc.]
</p>
