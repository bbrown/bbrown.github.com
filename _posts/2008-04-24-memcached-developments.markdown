---
layout: post
title: Memcached Developments
date: '2008-04-24 01:00:18 -0700'
mt_id: 1275
blog_id: 1
post_id: 1275
basename: memcached-developments
categories:
- technology
- net-development
---
<p>
Today I discovered that there's a new <a href="http://www.splinedancer.com/memcached-win32/">port of memcached for Windows</a>! This one reflects memcached v1.2.4, which <a href="http://www.danga.com/memcached/news.bml">added</a> a bunch of new features like multi-get, append/prepend, and check and set. This is a huge release even though it's in beta and is the first pass from the new maintainer. I am especially happy because I was considering putting in some time to do the port myself; I wasn't looking forward to it since I'd have to learn C++ and it'd take me awhile.
</p>
<p>
I also found the <a href="http://code.google.com/p/beitmemcached/">BeIT memcached client library</a>, which purports to improve on <a href="http://www.codeplex.com/EnyimMemcached/">Enyim</a>. I haven't had a chance to try it out yet, but I like the embeddable, lightweight nature of its code. It supports a few commands that Enyim doesn't so I'm going to give it a try. Enyim had a couple quirks that we found and worked around so I'm always willing to find a more straightforward framework if possible. I don't understand the hashing issues enough to ascertain which is using the better-performing or more consistent algorithm so I don't have a preference on that front.
</p>
<p>
All in all, these were two very welcome developments. It's never been a better time to be a memcached fan in the .NET world!
</p>
