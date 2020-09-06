+++
author = "John Wang"
title = "Bitcoin Is Now Supported in Encode::Base58::GMP"
date = "2013-05-02"
tags = [
    "encoding",
]
url = "/bitcoin/now-supported-in-encode-base58-gmp"
disqus_identifier = "/bitcoin/now-supported-in-encode-base58-gmp"
draft = false
+++

Base58 is a human-readable, protocol-safe encoding useful for case-sensitive encodings in cross-application situations such as URLs, databases, file systems, full-text indexes and others.

<!--more-->

It was popularized by [Flickr](https://www.flickr.com/groups/api/discuss/72157616713786392) and also used by [Bitcoin](https://en.bitcoin.it/wiki/Base58Check_encoding) and Grokbase. Back in 2011, I open sourced Base58 libraries using the [GNU MP Big Num Library (GMP)](https://gmplib.org/) for [Perl](https://metacpan.org/pod/Encode::Base58::GMP) and [Ruby](https://rubygems.org/gems/base58_gmp) to create Base58 encodings. At the time, the Ruby library supported Bitcoin, Flickr and GMP alphabets while the Perl library only supported the Flickr and GMP alphabets. With [Encode:Base58::GMP](https://metacpan.org/pod/Encode::Base58::GMP) version 1.0, the Perl library now also supports the Bitcoin alphabet for decoding and encoding as well as conversion from and to the Flickr and GMP alphabets. Grokbase uses the Flickr alphabet so there’s no need for a separate library in the code.

In addition to Bitcoin support, the Perl library has now added a base58_from_to() function to generically transcode Base58 strings and has updated the md5_base58() function to create strings padded with leading zero values. The change to md5_base58() is not backward compatible so this is something to consider for an upgrade.

For a bit of background, the reason Encode::Base58::GMP did not support Bitcoin in earlier releases is that I utilize the transliteration operator for the conversion and Perl does not support variables with the transliteration operator which I was using for implmentations in other languages at the time (Ruby, PHP, and Python). At the time, I didn’t find a solution to this other than hand-writing each conversion which I wanted to avoid so I left it out. Coincident to the recent Bitcoin activity, [a bug report](https://rt.cpan.org/Public/Bug/Display.html?id=84565) and blog comment were posted requesting this feature so I decided to look at this again. This time, I found the Perl solution is to use eval with optional pre-compile. I implemented the eval which looked clean but, in the end, I decided to release the hardcoded tr version.

Thanks to the Perl community for [Metacpan](https://metacpan.org/), [RT](https://rt.cpan.org/Public/), [Distzilla](http://dzil.org/) and [CPAN Testers](http://www.cpantesters.org/distro/E/Encode-Base58-GMP.html#Encode-Base58-GMP-1.00) for making this update easy. Also thanks to Ingy for writing [Test::Base](https://metacpan.org/pod/Test::Base) which makes Data Driven Testing a pleasure. If you are interested in Test::Base, this distribution includes an example of using external files in `t/03_md5-base58.t`.

Version 1.00 is now on CPAN so have fun.

