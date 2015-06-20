---
layout: post
title: That's Another Way to Go About It
date: '2008-09-12 15:46:00 -0700'
mt_id: 1341
blog_id: 1
post_id: 1341
basename: thats-another-way-to-go-about-it
categories:
- programming
- net-development
---
<p>
I generally don't like to showcase other's inelegant code, but <a href="http://code.google.com/p/twitterizer/source/browse/trunk/Twiterizer.Framework/TwitterRequest.cs#sl_svn22_256">this</a> couldn't be more timely given yesterday's <a href="http://bbrown.info/2008/09/11/how-to-parse-datetimes-from-the-twitter-api.aspx">Twitter <code>created_at</code> parsing tip</a>. There's always more than one way to do something, I guess.
</p>
<code>
</code><pre>       private static DateTime ParseDateString(string DateString)<br />        {<br />            Regex re = new Regex(@"(?&lt;DayName&gt;[^ ]+) (?&lt;MonthName&gt;[^ ]+) (?&lt;Day&gt;[^ ]{1,2}) ↵<br />            (?&lt;Hour&gt;[0-9]{1,2}): (?&lt;Minute&gt;[0-9]{1,2}): (?&lt;Second&gt;[0-9]{1,2}) ↵<br />            (?&lt;TimeZone&gt;[+-][0-9]{4}) (?&lt;Year&gt;[0-9]{4})");<br />            Match CreatedAt = re.Match(DateString);<br />            DateTime parsedDate = DateTime.Parse(<br />                string.Format(<br />                    "{0} {1} {2} {3}:{4}:{5}",<br />                    CreatedAt.Groups["MonthName"].Value,<br />                    CreatedAt.Groups["Day"].Value,<br />                    CreatedAt.Groups["Year"].Value,<br />                    CreatedAt.Groups["Hour"].Value,<br />                    CreatedAt.Groups["Minute"].Value,<br />                    CreatedAt.Groups["Second"].Value));<br /><br />            return parsedDate;<br />        }</pre>
<p>
For me, the lesson here is to <i>know your libraries</i> and always assume that someone else has done it better than you already. It then becomes a quest to find that better solution to the problem.
</p>
