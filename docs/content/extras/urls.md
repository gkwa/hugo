---
title: "URLs"
date: "2014-01-03"
aliases:
  - "/doc/urls/"
weight: 70
notoc: true
menu:
  main:
    parent: 'extras'
prev: "/extras/toc"
next: "/community/mailing-list"
---

## Pretty Urls

By default Hugo will create content with 'pretty' urls. For example
content created at /content/extras/urls.md will be rendered at
/content/extras/urls/index.html and accessible at /content/extras/urls. No
no standard server side configuration is required for these pretty urls to
work.

If you would like to have uglyurls you are in luck. Hugo supports the
ability to create your entire site with ugly urls. Simply use the
`--uglyurls=true` flag on the command line.

If you want a specific piece of content to have an exact url you can
specify this in the front matter under the url key. See [Content
Organization](/content/organization/) for more details. 

## Canonicalization

By default, all relative URLs encountered in the input will be canonicalized
using `baseurl`, so that a link `/css/foo.css` becomes
`http://yoursite.example.com/css/foo.css`.

Setting `canonifyurls` to `false` will prevent this canonicalization.

Benefits of canonicalization include fixing all URLs to be absolute, which may
aid with some parsing tasks.  Note though that all real browsers handle this
client-side without issues.

Benefits of non-canonicalization include being able to have resource inclusion
be scheme-relative, so that http vs https can be decided based on how this
page was retrieved.
