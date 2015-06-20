---
layout: post
title: Introducing the New Facebook Profile & More Session
date: '2008-07-23 17:22:48 -0700'
mt_id: 1312
blog_id: 1
post_id: 1312
basename: introducing-the-new-facebook-profile-more-session
categories:
- web-tech
- blogging-world
- high-geekery
---
<p>
Talk by Ruchi Sanghvi and Josh Elman. Here are my rough notes on the presentation:
</p>
<ul>
<li>The never-ending profile was the motivation behind the redesign.</li>
<li>Emphasizing feeds: increases engagement and encourage content creation</li>
<li>Simpler, cleaner profiles: easier profile navigation, clearer identity, more control</li>
<li>More control over profile: users decide about tabs, when to publish, and look of stories</li>
<li>"It all starts with the Wall": feed, publisher, profile boxes</li>
<li>Stories: one-line, short, or full (up to 500x700). Done with feed forms, using FBML or Javascript.</li>
<li>Publisher: different versions for user and friends, </li>
<li>Info tab: deep integration with structured information, should represent information about what the user's done. Info stuff is enabled through canvas page button using FBML or Javascript.</li>
<li>Tabs: provides the richest expression, hybrid of a profile box and canvas page (solely FBML, no advertising), no caching, 760 pixels wide, no autoplay, fb:visible-to-owner</li>
<li>Profile boxes: profile_main -&gt; narrow, on Wall, wide and narrow appear on Boxes tab, Bookmarks will be migrated, must manually add a bookmark otherwise.</li>
<li>New permissions/lack of adding: reduces friction. First access provides user ID, friends, pic and names, publish feed stories, send requests. Add require_login to links to trigger permissions solicitation.</li>
</ul>
<p>
Q&amp;A:
</p>
<ul>
<li>How do users first get into the app if they're not adding?: About page much more static.</li>
<li>Should apps offer all integration points and let users decide or pick some?: Both, but mostly the latter.</li>
<li>Is user info going to be available to all? Still limited to privacy settings.</li>
<li>What can the Publisher do?: Rehashed already shown options</li>
<li>Smiley app? Uses shared preferences, which has been available for 9 months</li>
<li>Can you detect whether a user is in new profile? Yes, part of API.</li>
<li>Widened Wall, is it final? Yes.</li>
<li>(from me) Extended permissions, is the Wiki list definitive? Yes.</li>
<li>Engagement metrics, what are they? Bunch of them. User can reorder boxes.</li>
<li>What are these info sections? Not a mini-feed, opposite of one. More for static information. Button on canvas page shows example, the user allows it, adds it to profile, and edits inline.</li>
<li>What new stats will be available, users who have added tabs? Yes.</li>
<li>Logged in user for tabs is viewer or user? Viewer. Tabs focus should be on the user.</li>
</ul>
