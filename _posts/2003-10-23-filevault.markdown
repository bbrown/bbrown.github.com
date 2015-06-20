---
layout: post
title: FileVault
date: '2003-10-23 05:14:07 -0700'
mt_id: 596
blog_id: 1
post_id: 596
basename: filevault
---
<br />Apple's new version of <a href="http://www.apple.com/macosx/">Mac OS X</a> is going to provide a new feature called <a href="http://www.apple.com/macosx/features/filevault">FileVault</a>, an automatic, configurable system that encrypts and decrypts your entire home directory at login and logout. It uses <a href="http://csrc.nist.gov/encryption/aes/"><acronym title="Advanced Encryption Standard">AES</acronym></a>&#x2014;currently the most advanced encryption available that's not public key&#x2014;and a 2048-bit key!<br /><br />My initial thought at hearing this was that no one could possibly ever remember a 2048-bit key (256 characters, in other words, or 128 if using Unicode) and people would end up using "panther" or "edna" as their key, rendering the security easily breachable. A <a href="http://apple.slashdot.org/comments.pl?sid=83329&amp;cid=7290659">comment</a> over at <a href="http://apple.slashdot.org/article.pl?sid=03/10/23/1317220&amp;mode=thread&amp;tid=107&amp;tid=179&amp;tid=185&amp;tid=187&amp;tid=190">Slashdot</a> cleared up the matter. It turns out that the 2048-bit key is probably a one-way hash of a much smaller key, thus making the key virtually uncrackable. That's an elegant and awesome solution that makes me feel much more comfortable using it. Thanks, Apple!<br /><br />[UPDATE: I keep hearing the 150 new features figure being bandied about, but I never knew what those 150 were (aside from the big ones mentioned at every opportunity). Apple has since put up a <a href="http://www.apple.com/macosx/newfeatures/">page</a> listing each and every one of them. And my copy arrives tomorrow! Yeehaw.]<br /><br />[UPDATE (10/24/03): Oops, FileVault isn't 2048-bit encryption. It's only 128 bit. I think 2048-bit encryption would result in massive disk usage. My mistake.]<br /><br /><br />
