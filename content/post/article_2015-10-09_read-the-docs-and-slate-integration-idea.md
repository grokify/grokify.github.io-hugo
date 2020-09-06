+++
author = "John Wang"
title = "Read the Docs and Slate Integration Idea"
date = "2015-10-09"
tags = [
    "devtools",
]
url = "/ideas/readthedocs-slate-integration"
disqus_identifier = "/ideas/readthedocs-slate-integration"
+++

[Read the Docs](https://readthedocs.org/) and [Slate](https://github.com/slatedocs/slate) are two great open source documentation tools. Each has advantages with Read the Docs supporting repo-based documentation and Slate supporting 3-column layout. These advantages make both very useful for documenting SDKs. Given that each has their own strengths, it would be great to be able to use these together. Here’s an idea for single sourcing content and publishing into both.

## Situation

Read the Docs is powerful because it allows documentation to reside directly in a SDK repository. As such, the docs and be versioned exactly with the SDK and it includes nice themes and navigation. However, as it is tied to the repo, it is necessarily limited when it comes to reading documentation across repos which is Slate’s strong suit.

While Slate is good at managing documentation across langauges in its 3-column layout, manually updating this content requires different SDK maintainers to continually monitor, contribute to and update the multi-language Slate repo.

## Proposal

The idea is that SDK authors could author content in Read the Docs format using markdown. When certain tags are added to code snippets those would automatically get merged into a Slate markdown file. This way developers can stay focused on working on their language-specific SDKs while documentation staff can own collection of and normalizing that data until it is fit for release.

## Summary

Documentation is hte life blood of developer programs and it behooves programs to use the best apps available to them. Read the Docs and Slate are two such tools and as such it would be great to see them work together in a seamless fashion.

