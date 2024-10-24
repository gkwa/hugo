---
title: "Introduction to Hugo"
date: "2013-07-01"
linktitle: "Introduction"
weight: 5
menu:
  main:
    parent: 'getting started'
next: '/overview/quickstart'
---

## What is Hugo?

Hugo is a general purpose website framework. Technically speaking, Hugo is
a static site generator. This means that unlike systems like Wordpress,
Ghost & Drupal which run on your web server expensively building a page
every time a visitor requests one, Hugo does the building when you create
your content. Since websites are viewed far more often then they are
edited, Hugo is optimized for website viewing while providing a great
writing experience. 

Sites built with hugo are extremely fast and very secure. Hugo sites can
be hosted anywhere including Heroku, GoDaddy, GitHub pages, S3
& Cloudfront and work well with CDNs. Hugo sites run without dependencies
on expensive run times like Ruby, Python or PHP and without dependencies
on any databases.

We think of Hugo as the ideal website creation tool. With nearly instant
built times and the ability to rebuild whenever a change is made Hugo
provides a very fast feedback loop. This is essential when you are
designing websites, but also very useful when creating content.  

## What does Hugo do?

In technical terms Hugo takes a source directory of markdown files and
templates and uses these as input to create a complete website. 

Hugo boasts the following features:

### General

  * Extremely fast built times (~1ms per page)
  * Completely cross platform: Runs on Mac OSX, Linux and Windows 
  * Easy [installation](/overview/installing)
  * Render changes [on the fly](/overview/usage) with [live reload](#) as you develop
  * Complete theme support
  * Host your site anywhere

### Organization

  * Straightforward [organization](/content/organization)
  * Support for [website sections](/content/sections)
  * Completely customizable [urls](/extras/urls)
  * Support for [categories](/indexes/category) and tags
  * Support for configurable [taxonomies](/indexes/overview) to create your own organization
  * Ability to [sort content](/content/ordering) as you desire
  * Automatic [table of contents](/extras/toc) generation
  * Dynamic menu creation
  * [pretty urls](/extras/urls) support
  * [permalink](/extras/permalinks) pattern support
  * [Aliases](/extras/aliases) (redirects)

### Content

  * Content written in [Markdown](/content/example)
  * Support for TOML, YAML and JSON metadata in [frontmatter](/content/front-matter)
  * Completely [customizable homepage](/layout/homepage)
  * Support for multiple [content types](/content/types)
  * Automatic and user defined [summaries](/content/summaries)
  * [shortcodes](/extras/shortcodes) to enable rich content inside of markdown
  * ["Minutes to Read"](/layout/variables) functionality
  * ["Wordcount"](/layout/variables) functionality

### Additional Features

  * Integrated Disqus comment support
  * Automatic [RSS](/layout/rss) creation
  * Support for go and amber templates
  * Syntax [highlighting](/extras/highlighting) powered by pygments

See what's coming next in the [roadmap](/meta/roadmap)

## Who should use Hugo?

Hugo is for people that prefer writing in a text editor over
a browser.

Hugo is for people who want to hand code their own website without
worrying about setting up complicated runtimes, dependencies and
databases. 

Hugo is for people building a blog, company site, portfolio, tumblog,
documentation, single page site or a site with thousands of
pages. 

## Why did you write Hugo?

I wrote Hugo ultimately for a few reasons. First I was disappointed with
wordpress, my then website solution. It rendered slowly. I couldn't create
content as efficiently as I wanted to and needed to be online to write
posts. The constant security updates and the horror stories of people's
hacked blogs. I hated how content was written in HTML instead of the much
simpler markdown. Overall I felt like it got in my way more than it helped
my from writing great content.

I looked at existing static site generators like Jekyll, Middle and Nanoc.
All had complicated dependencies to install and took far longer to render
my blog with hundreds of posts than I felt was acceptable. I wanted
a framework to be able to get rapid feedback while making changes to the
templates and the 5+ minute render times was just too slow. In general
they were also very blog minded and didn't have the ability to have
different content types and flexible urls.

I wanted to develop a fast and full featured website framework without
dependencies. The Go language seemed to have all of the features I needed
in a language. I began developing Hugo in Go and fell in love with the
language. I hope you will enjoy using (and contributing to) Hugo as much
as I have writing it.

## Next Steps

 * [Install Hugo](/overview/installing)
 * [Quick start](/overview/quickstart)
 * [Join the Mailing List](/community/mailing-list)
 * [Star us on Github](http://github.com/spf13/hugo)
