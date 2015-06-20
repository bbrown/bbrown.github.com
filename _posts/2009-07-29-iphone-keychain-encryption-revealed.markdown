---
layout: post
title: iPhone Keychain Encryption Revealed
date: '2009-07-29 23:04:58 -0700'
mt_id: 1412
blog_id: 1
post_id: 1412
basename: iphone-keychain-encryption-revealed
categories:
- mac-os-x
---
<p>
I just got the definitive word on the algorithm that the iPhone uses to encrypt Keychain items and it's Triple-DES. I was flabbergasted that they didn't go with AES since a) there's hardware acceleration for AES-128 on the 3G and AES-256 on the 3GS; b) the Keychain APIs are wildly different from the Mac OS X ones; and c) Triple-DES has been deprecated for new secure applications for years now.
</p>
