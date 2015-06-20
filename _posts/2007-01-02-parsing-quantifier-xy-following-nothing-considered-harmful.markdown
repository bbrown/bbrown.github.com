---
layout: post
title: Parsing Quantifier {x,y} Following Nothing Considered Harmful
date: '2007-01-02 12:37:00 -0700'
mt_id: 1181
blog_id: 1
post_id: 1181
basename: parsing-quantifier-xy-following-nothing-considered-harmful
categories:
- net-development
---
<!-- google_ad_section_start -->
<p>
If you normally do a <code>Regex.Escape(string)</code> in C# to get some text ready for use as a regular expression, be aware that a string like <code>^Lijit&#xA0;(+http://www.lijit.com/)$</code> will be escaped like so <code>^Lijit\&#xA0;\(+http://www\.lijit\.com/\)$</code> instead of <code>^Lijit\&#xA0;\(<b>\</b>+http://www\.lijit\.com/\)$</code> as you would expect.
</p>
<p>
Using that "escaped" regular expression will result in an ArgumentException along the lines of <code>parsing "^Lijit&#xA0;(+http://www.lijit.com/)$" - Quantifier {x,y} following nothing.</code> That message is virtually <a href="http://www.google.com/search?q=parsing%20Quantifier%20%7Bx%2Cy%7D%20following%20nothing.">un-Google-able</a> until now.
</p>
<p>
The .NET exception occurs, I think, because the parser just doesn't understand the unescaped quantifier being next to an escaped control character. I believe that the escaping misses it because it uses that same parser because the plus sign is definitely one of the characters that the <code>Escape</code> method can handle.
</p>
<!-- google_ad_section_end -->




