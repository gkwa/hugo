---
title: "Taxonomy Terms Template"
linktitle: "Taxonomy Terms"
date: "2014-05-21"
weight: 60
aliases: ["/indexes/lists/","/doc/indexes/", "/extras/indexes"]
menu:
  main:
    parent: 'layout'
prev: "/templates/homepage"
next: "/templates/views"
---

A unique template is needed to create a list of the terms for a given
taxonomy. This is different from the [list template](/templates/list/)
as that template is a list of content, where this is a list of meta data.

## Which Template will be rendered?
Hugo uses a set of rules to figure out which template to use when
rendering a specific page.

Hugo will use the following prioritized list. If a file isn’t present
than the next one in the list will be used. This enables you to craft
specific layouts when you want to without creating more templates
then necessary. For most sites only the \_default file at the end of
the list will be needed.

A Taxonomy Terms List will be rendered at /`PLURAL`/

* /layouts/taxonomy/`SINGLE`.terms.html
* /layouts/\_default/terms.html

If that neither file is found in either the /layouts or /theme/layouts
directory than hugo will not render the taxonomy terms pages. It is also
common for people to render taxonomy terms lists on other pages such as
the homepage or the sidebar (such as a tag cloud) and not have a
dedicated page for the terms.

## Variables

Taxonomy Terms pages are of the type "node" and have all the [node
variables](/templates/variables/) and [site
variables](/templates/variables/) available to use in the templates. 

Taxonomy Terms pages will additionally have:

**.Data.Singular** The singular name of the taxonomy <br>
**.Data.Plural** The plural name of the taxonomy<br>
**.Data.Terms** The taxonomy itself<br>
**.Data.Terms.Alphabetical** The Terms alphabetized<br>
**.Data.Terms.ByCount** The Terms ordered by popularity<br>

## Example terms.html file

List pages are of the type "node" and have all the [node
variables](/templates/variables/) and [site
variables](/templates/variables/) available to use in the templates.

This content template is used for [spf13.com](http://spf13.com).
It makes use of [partial templates](/templates/partials). The list of indexes
templates cannot use a [content view](/templates/views) as they don't display the content, but
rather information about the content.

This particular template lists all of the Tags used on
[spf13.com](http://spf13.com) and provides a count for the number of pieces of
content tagged with each tag.

.Data.Terms is an map of terms => [contents]

    {{ template "partials/header.html" . }}
    {{ template "partials/subheader.html" . }}

    <section id="main">
      <div>
       <h1 id="title">{{ .Title }}</h1>

       <ul>
       {{ $data := .Data }}
        {{ range $key, $value := .Data.Terms }}
        <li><a href="{{ $data.Plural }}/{{ $key | urlize }}"> {{ $key }} </a> {{ len $value }} </li>
        {{ end }}
       </ul>
      </div>
    </section>

    {{ template "partials/footer.html" }}


## Ordering

Hugo can order the meta data in two different ways. It can be ordered by the
number of content assigned to that key or alphabetically.


## Example indexes.html file (alphabetical)

    {{ template "partials/header.html" . }}
    {{ template "partials/subheader.html" . }}

    <section id="main">
      <div>
       <h1 id="title">{{ .Title }}</h1>
       <ul>
       {{ $data := .Data }}
        {{ range $key, $value := .Data.Terms.Alphabetical }}
        <li><a href="{{ $data.Plural }}/{{ $value.Name | urlize }}"> {{ $value.Name }} </a> {{ $value.Count }} </li>
        {{ end }}
       </ul>
      </div>
    </section>
    {{ template "partials/footer.html" }}

## Example indexes.html file (ordered)

    {{ template "partials/header.html" . }}
    {{ template "partials/subheader.html" . }}

    <section id="main">
      <div>
       <h1 id="title">{{ .Title }}</h1>
       <ul>
       {{ $data := .Data }}
        {{ range $key, $value := .Data.Terms.ByCount }}
        <li><a href="{{ $data.Plural }}/{{ $value.Name | urlize }}"> {{ $value.Name }} </a> {{ $value.Count }} </li>
        {{ end }}
       </ul>
      </div>
    </section>

    {{ template "partials/footer.html" }}

