---
layout: post
title: My First Feature
date: '2005-05-26 16:55:04 -0700'
mt_id: 914
blog_id: 1
post_id: 914
basename: my-first-feature
categories:
- go-daddy
---
<br />I finally finished my feature today. I actually finished it last Friday but we decided to take it in a different direction during the code review. It was the appropriate direction, so I just tossed out the <acronym title="User Interface">UI</acronym> elements and moved everything into the Windows service.<br /><br />I churned it out pretty quickly but ended up spending the last two days debugging an edge case. It turned out that the bug was present from the app's initial deployment but that the case had never come up. Unfortunately, my new feature would have caused it to come up occasionally so it had to be corrected before release. I implemented my feature&#x2014;fixing the old bug, tested out all the various permutations, and synchronized my code design document with the development.<br /><br />I presented the code design to my mentor and walked her through the code I changed. She approved of it, so we marked my feature done (insert <cite>Monster House</cite> "DONE" stamp and voiceover here). Well, it's actually just ready for <acronym title="Quality Assurance">QA</acronym> but I'm sure it'll pass through that with flying colors. *ahem* Of course.<br /><br />This little feature has enabled me to explore threading, Windows services, messaging, and the data layer. Not bad for my first feature. I also learned from my mentor that our boss welcomes suggestions for upcoming releases; that's right up my alley so I'm going to start pondering what my app needs.<br /><br />[NOTE: The views expressed on this website/weblog are mine alone and do not necessarily reflect the views of Go Daddy Software, Inc.]<br /><br /><br />
