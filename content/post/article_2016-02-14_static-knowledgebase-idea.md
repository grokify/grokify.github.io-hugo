+++
author = "John Wang"
title = "Static Knowledgebase Idea"
date = "2016-02-14"
tags = [
    "devtools",
]
url = "/ideas/static-knowledgebase"
disqus_identifier = "/ideas/static-knowledgebase"
+++

I was recently thinking about developer-oriented knowledgebases and thought it would be a great idea to build a knowledgebase on a static documentation engine like [MkDocs](https://www.mkdocs.org/) or [Sphinx](https://www.sphinx-doc.org/en/master/). I imagine a project like this could be very useful to developer projects and would love to see it developed.

This could be done by adding a knowledgebase layout homepage with an added search capability to build out a service similar to Desk.com or Zendesk. Of course, it would be nice for those services to automatically take in data from sites like GitHub as well.

## Navigation

Unlike a blog which has articles listed by date, the top level navigation for the knowledgebase would be based on tag. Each tag would include it’s most popular articles and think link to the tag page for more articles. Each tag could be in a div box. It may be worthwhile to have some override for tag ordering beyond alphabetical.

## Search

At this time [Algolia](https://www.algolia.com/) provides free search for up to 10,000 records and 100,000 operations per month. That’s more than enough for sites to get started and popular sites can sign up for Algolia’s paid plans.

Of note, [Algolia does build a Jekyll plugin](https://github.com/algolia/algoliasearch-jekyll) so this could be similar but for MkDocs or Sphinx.

## Authoring and Version Control

The power of of building a knowledgebase off of a static blog generator is, of course, to allow developers to author in markdown stored on GitHub or another version control system.

## Summary

Static blog generators are popular with developers due to their simplicity and integration with services like GitHub. By enhancing a static blog generator to behave like a knowledgebase, developers can provide the knowledgebase experience users are accustomed to while supporting the authoring environment they are accustomed to.

While I think this is a great idea, I don’t have enough time to work on it now so if anyone is interested in this or knows of a project, please let me know :)