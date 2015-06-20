---
layout: post
title: Spampossible
date: '2005-01-29 16:13:59 -0700'
mt_id: 844
blog_id: 1
post_id: 844
basename: spampossible
categories:
- high-geekery
---
<br />Today I had a thought about a way to solve (or, more realistically, limit) email spam. I was thinking that my new blog, <a href="http://www.foundontheweb.org/">Found on the Web</a>, could use my email address on it for feedback, comment, or link suggestions. But I didn't want to just put my email address out there so I would need a way to protect it from acquisition by spammers.<br /><br />My idea is the idea of an expiring email address. Basically, you would post an email address that was only good for that day and the next day. After that, all email to that address would go into /dev/null. The tricky thing is to actually implement it: you couldn't have an email address like <a href="mailto:bill-01-30-2005@bbrown.info">bill_01-30-2005@bbrown.info</a> because it would be easily guessable and would thus allow the spammer to project valid email addresses into the future.<br /><br />So I thought about using some encryption algorithm to store an encrypted version of the expiration date in the email address. So you'd get something like <a href="mailto:info_7097997XGDASD9@bbrown.info">info_7097997XGDASD9@bbrown.info</a> that would indicate to the mail client (or the mail server depending on your preference) when to stop accepting emails to that account number.<br /><br />The main problem with that approach is that such an email address is no longer usable to a person since you can't memorize it and you can't effectively communicate it over the phone. You're never going to get around ugly URLs because encryption isn't pretty. Further, these email addresses would be machine generated and are not intended for general audiences.<br /><br />The key for the algorithm should be something that every mail client already has, like your email account password.<br /><br />My only concern is that this would encourage spammers to send out their unsolicited commercial even quicker. Instead of spending time collecting lists of potential marks, they would just send out their emails as soon as they find an address.<br /><br /><br />
