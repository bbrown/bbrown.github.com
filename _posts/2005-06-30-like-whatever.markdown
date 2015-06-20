---
layout: post
title: LIKE @whatever
date: '2005-06-30 05:32:02 -0700'
mt_id: 950
blog_id: 1
post_id: 950
basename: like-whatever
categories:
- net-development
---
<br />Phew, just spent some time trying to get a parameter to work with a LIKE and wildcards in the WHERE clause of a SELECT. I'm creating a stored procedure for SQL Server 2000.<br /><br />For example, I wanted something like this:<br /><br />SELECT * FROM table WHERE no_column_in_particular LIKE '%@param%'<br /><br />But it would always return all the rows, so I knew that I was getting doing something like "LIKE '%%'" I tried all sorts of different methods like wrapping the parameter in brackets. I finally found the answer in <a href="http://66.102.7.104/search?q=cache:sqlforums.windowsitpro.com/web/forum/messageview.aspx%3Fcatid%3D66%26threadid%3D20344%26enterthread%3Dy" title="I had to use the Google Cache version because I couldn't get the forum itself to come up.">this SQL Server Magazine forum entry</a>.<br /><br />The solution is to use string concatenation or add it to the parameter before running the SELECT:<br /><br />SELECT * FROM table WHERE no_column_in_particular LIKE '%' + @param + '%'<br /><br />Or:<br /><br />SET @param = '%' + @param + '%'<br /><br />I'm not sure if the former is considered dynamic SQL in crafting the plan, but if it is then the latter might be higher performing. IANADBA.<br /><br /><br />
