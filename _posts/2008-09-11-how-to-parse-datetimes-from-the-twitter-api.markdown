---
layout: post
title: How to Parse DateTimes from the Twitter API
date: '2008-09-11 15:23:00 -0700'
mt_id: 1340
blog_id: 1
post_id: 1340
basename: how-to-parse-datetimes-from-the-twitter-api
categories:
- web-tech
- programming
- net-development
---
<p>
If you were wanting to interact with the Twitter API under .NET, you might find yourself trying to convert a date value from the XML results over to a DateTime in your code. Twitter uses a weird format for their dates—<code>Thu Sep 04 11:09:28 +0000 2008</code>—that doesn't get converted properly with just a good ol' <code>DateTime.Parse</code>. You could spend a lot of time iteratively trying to figure out the correct format to use. <b>Or</b>, you could just use the following (my free gift to you, dear Twitter-API-consuming reader):
</p>
<code>
DateTime.ParseExact((directMessage.SelectSingleNode("//created_at").InnerText), "ddd MMM dd HH:mm:ss zzzz yyyy", CultureInfo.InvariantCulture, DateTimeStyles.AdjustToUniversal);
</code>
<p>
<code>directMessage</code> here is an <code>XmlNode</code> representing a single direct message extracted from a <a href="http://apiwiki.twitter.com/REST+API+Documentation#directmessages">list of direct messages</a>. I found this out after many iterations since all of the .NET libraries for Twitter just punt on this conversion.
</p>
