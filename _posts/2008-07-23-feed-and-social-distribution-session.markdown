---
layout: post
title: Feed and Social Distribution Session
date: '2008-07-23 19:49:36 -0700'
mt_id: 1313
blog_id: 1
post_id: 1313
basename: feed-and-social-distribution-session
categories:
- web-tech
- blogging-world
- high-geekery
---
<p>
Talk with Jerry Cain, Ari Steinberg (Manager of News Feed Team), and Tom Whitnah.
</p>
<ul>
<li>Use the right channel to deliver the right message. Overview of the old ways of communication with users. Requests: when one user wants another user to take a specific action. Notifications: user-to-user to tell a user an action has been taken towards her, app-to-user to tell a user about something important to her from the application. Feed story: when a user wants to share actions they've taken.</li>
<li>Feed is the center of communication on Facebook. Old: single stream, not interactive, only 25 slots. New: top stories as highlights, multiple streams of news, more room for application stories to appear, commenting on stories.</li>
<li><code>feed.publishTemplatizedAction</code>: disaster, user-specific token sets made aggregation very difficult.</li>
<li>New methods: <code>feed.registerTemplateBundle</code> and <code>feed.publishUserAction</code></li>
<li>Allow template bundles to include several templates per story size, ranging from user-specific to more general. You can define different templates within a bundle to handle 1, 2, and many aggregated stories.</li>
<li>Before you launch your application, think about the sort of templates you're going to be using. Calling the API method only allows for one-line stories. Feed forms: <code>FB.Integration.showFeedDialog()</code></li>
<li>Great communications = happy users. Respect users' attention and their friends' attention.</li>
<li>Higher acceptance, lower ignore = more requests allocated.</li>
<li>Notifications: user-to-user, can be sent to any non-friends who are also users of the app; app-to-user, allocation is approximately seven per week per user.</li>
<li>More read, fewer hidden / spam = more notifications allocated.</li>
</ul>
<p>Q&amp;A</p>
<ul>
<li>Allow access to News Feed? Nope.</li>
<li>Handle instead of a bundle ID? Not yet.</li>
<li>Facebook applications versus Facebook Connect? No differentiation.</li>
<li>(me) Disclose allocations per user instead of aggregate? Can put it on the short-term roadmap, but wary of disclosing who is a tattletale.</li>
<li>Statistics data available via an API call? Someone was working on that but he didn't know the status of that work.</li>
<li>Set privacy in News Feeds? Not at this point but hopefully someday.</li>
<li>Timeline for new statistics to appear? In the next week or so.</li>
<li>Give visibility into an app's spamminess? Talked about it with the Reviews application but have found some spamminess within the Reviews application itself.</li>
<li>What kind of history for allocation reductions? Spamminess metrics last about a month.</li>
<li>Expand News Feed on friends to see more of a story? Haven't really thought it.</li>
<li>In stories themselves, possible to see how many times one was read in News Feed? Would like to, but not a high priority.</li>
<li>Add or view comments, available through API? Probably through fb:comments, not allow to add comments programmatically due to spam concerns.</li>
</ul>
