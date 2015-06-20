---
layout: post
title: Transactions
date: '2005-06-06 01:01:41 -0700'
mt_id: 924
blog_id: 1
post_id: 924
basename: transactions
categories:
- net-development
---
<br />Not that <a href="http://www.superdotnet.com/Article.aspx?ArticleID=191">transactions in .NET</a> were super hard, but .NET 2.0 is going to have a <a href="http://www.microsoft.com/downloads/details.aspx?familyid=AAC3D722-444C-4E27-8B2E-C6157ED16B15&amp;displaylang=en">System.Transaction</a> library. <a href="http://wesnerm.blogs.com/net_undocumented/2005/06/c_data.html">Transactions</a> will be invoked with a <code>using</code> statement, which I think is an amazingly elegant way to do them.<br /><br />Wesner Moise thinks that people will forget the commit call, but I don't. I think if you have the desire to make a transaction, you probably won't have forgotten that you're in the transaction by the time you've done your SQL. That may just be me, though.<br /><br /><br />
