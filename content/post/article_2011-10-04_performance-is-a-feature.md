+++
author = "John Wang"
title = "Performance is a Feature"
date = "2011-10-04"
tags = [
    "performance",
]
url = "/performance/is-a-feature"
disqus_identifier = "/performance/is-a-feature"
+++

The phrase “Performance is a Feature” has been growing in popularity. Lately, it’s importance for me is underlined by the fact the most common response I get from showing off my early-stage mailing list archive, Grokbase, is that “it’s fast.” I first heard this idea similarly phrased in [Google’s Think Quartlerly](https://mashable.com/2011/03/24/think-quarterly/) and then in [Jeff Atwood’s Coding Horror](https://blog.codinghorror.com/performance-is-a-feature/) which was [covered on Hacker News](https://news.ycombinator.com/item?id=2676673). Matt Brittin, managing director of Google for UK and IE ops said it like this:

<!--more-->

> At Google, we often think that speed is the forgotten ‘killer application’ – the ingredient that can differentiate winners from the rest. We know that the faster we deliver results, the more useful people find our service.

I’ve worked in some high-performance environments (enterprise search for billion+ document archives) and written benchmark reports so I know performance is important; however, this got me thinking, sure “we” (those in the know) know that performance is important, but what about the meta-question, why is it important to say it is important?

# Motivation

For me, the strongest reason for talking about Performance as a Feature is that it can help motivate and focus development. This is important because performance can be vitally important and yet be difficult to achieve and result in little to show using metrics such as lines of code and visible features. Indeed, a product screen shot can look exactly the same after a 100x speed up.

The reason performance can be hard to achieve is three fold.

## Performance is Mentally Challenging

Often times, performance is an architectural problem-solving exercise and not the mere act of taking a requirement and executing on it. Additionally, often times you need to taken into account many domain-specific properties in order to fully optimize the system. So you may need to understand the problem space in detail, come up with a solution, and then communicate / convince others that the design should be accepted even before you get started coding.

## Performance is not Greenfield

Once you come up with a good solution, often times you cannot just implement it as you are improving an existing process. The new solution needs to integrate into the existing solution and either be a drop-in replacement or change the code around it. Like repainting a car after it gets dinged, the affected code can be much larger than the immediate problem. Further, if data conversion is needed, once the new code has been implemented, the conversion process may take longer than development or deployment.

## Performance is Hard to See

Finally, it can be hard to tell your peers what you accomplished if what you accomplished was a performance improvement since there is nothing to see. To complicate matters, you are not necessarily working on a new product or even a new feature. Indeed, you may be just speeding up someone else's creative work. That the speed-up itself is what makes the work useful at all may be hard to convey. Here, metrics tell the best story to other developers but to people using the app, it may be simply fast.

# Summary

As developers, we like to see the fruits of our labor and this often means working on new features that are visible and we can talk about. However, when talking to users, often times the first thing they notice and talk about may be your app’s performance. So when developing an app, it is important to remember, that:

Performance is not just any feature, it may be a killer feature.

Have you had to implement performance features? What were the challenges you faced?

