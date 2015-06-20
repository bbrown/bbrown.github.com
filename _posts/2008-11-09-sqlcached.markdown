---
layout: post
title: SQLcached
date: '2008-11-09 17:48:08 -0700'
mt_id: 1397
blog_id: 1
post_id: 1397
basename: sqlcached
categories:
- technology
- programming
---
<p id="sqlcached-intro">
I have to agree with Dare Obasanjo's latest <a href="http://www.25hoursaday.com/weblog/2008/11/09/InMemoryCachingWhyWeCantJustTrustTheDatabaseToGetItRight.aspx">blog entry about in-memory caching</a>. After working on high-transaction, heavy database-using Web applications for the last nine years, there is one thing above all else that I have learned and taken to heart: <em>a Web application is only as good as its caching strategy</em>. My career has seen a progression from light to heavy cache usage and each new application has benefitted in scalability from that.
</p>
<p id="sqlcached-inspiration">
Dare's entry got me thinking: why couldn't the RDBMS itself incorporate a distributed, in-memory cache like <a href="http://www.danga.com/memcached/">memcached</a> or <a href="http://msdn.microsoft.com/en-us/data/cc655792.aspx">Project Velocity</a>? What if a Web application could basically eliminate the need for its own caching layer by relying solely on the database, which would then aggressively and algorithmically use one of the caching services to expand its memory-based caching?
</p>
<p id="sqlcached-benefits">
If the problem with query caching in MySQL or SQL Server is the amount of server RAM that can be installed, then distributed caching seems like the perfect solution. It's what the Web server layer uses: why not bring it down to the data layer. Moreover, given the common replication and clustering scenarios, there are likely idle database servers whose memory is already going unused for the most part. Putting a distributed caching system in place would put them in action while still keeping them ready for failovers.
</p>
<p id="sqlcached-objections">
The main objections I can see is that going to the database might cause an increase in network usage since some cache calls in the Web server layer would never leave the server and that the database would have to work to decide between file-level and cache-level access. But that would be minimal and the simplification it would engender on the Web application level would make the costs even less objectionable.
</p>
<p id="sqlcached-conclusion">
It's entirely possible that Project Velocity is being undertaken with exactly this thought in mind. (It's not clear that there's any movement afoot in MySQL AB towards this end&#x2014;at least from my cursory searches.) This idea would have to be implemented at the RDBMS level.
</p>
