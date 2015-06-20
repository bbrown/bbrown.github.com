---
layout: post
title: Microsoft Distributed Cache Services née Velocity
date: '2008-06-07 20:17:25 -0700'
mt_id: 1293
blog_id: 1
post_id: 1293
basename: microsoft-distributed-cache-services-ne-velocity
categories:
- high-geekery
- net-development
---
<p>
Microsoft has unveiled its new project code-named <a href="http://msdn.microsoft.com/en-us/data/cc655792.aspx">Velocity</a> {<a href="http://www.25hoursaday.com/weblog/2008/06/06/VelocityADistributedInMemoryCacheFromMicrosoft.aspx">via</a>}, which is a .NET version of memcached for the Microsoft orbit. It's not at this point baked into the OS or IIS, but it's a start.
</p>
<p>
It's got some additional features that go beyond memcached. One of the great things about memcached is its simplicity and limited feature set. It doesn't worry about security and it's essentially a glorified hashtable. For example, it offers named cache stores, regions within those caches, object searching, and different concurrency models. I can envision a lot that such functionality would get me if I were to replace memcached with it.
</p>
<p>
But I'm most curious as to the future of this project and its official position. If it's going to become a supported technology and/or officially bundled, then I'd be willing to invest the effort in switching. But if it's a one-off and never gets much attention, then I'd rather stick with the power horse that is memcached. There's plenty of hope listed in <a href="http://blogs.msdn.com/velocity/archive/2008/06/04/project-velocity-ctp1-features.aspx">their future feature list</a>. I'm subscribed to the blog and I will be following this project closely.
</p>
