---
layout: post
title: Online Outlining
date: '2005-06-17 15:52:12 -0700'
mt_id: 943
blog_id: 1
post_id: 943
basename: online-outlining
categories:
- web-tech
---
<br />I can't believe I never mentioned <a href="http://www.sproutliner.com/">Sproutliner</a> before. It's a free, online outlining web app that's surprisingly robust. It gets even better because its creator <a href="http://glenmurphy.com/blog/2005/05/sproutliner-open-sourced.html">open-sourced it</a> recently. I liked the hosted option, but it's very openness made me unable to use it for sensitive matters. Now I can host it on my own site, put it behind some authentication, and use it to my heart's content.<br /><br />It took a little doing because I didn't install it into the root of my domain. The developer made it so that every link and reference was root relative, <em>i.e.</em>, "/<em>some-path</em>/<em>some-file</em>.php". There were a lot of those references, so it took awhile to hunt them down&#x2014;a global replace didn't work, unfortunately&#x2014;and make them plain ol' relative.<br /><br /><br />
