---
title: "Using Taxonomies"
linktitle: "Usage"
date: "2014-05-26"
weight: 15
menu:
  main:
    parent: 'taxonomy'
prev: "/taxonomies/overview"
next: "/taxonomies/displaying"
---

## Defining taxonomies for a site

Taxonomies must be defined in the site configuration, before they can be
used throughout the site. You need to provide both the plural and
singular labels for each taxonomy.

Here is an example configuration in YAML that specifies two taxonomies.

Notice the format is **singular key** : *plural value*. 
### config.yaml

    ---
    taxonomies:
        tag: "tags"
        category: "categories"
        series: "series"
    ---

## Assigning taxonomy values to content

Once an taxonomy is defined at the site level, any piece of content
can be assigned to it regardless of content type or section.

Assigning content to an taxonomy is done in the front matter.
Simply create a variable with the *plural* name of the taxonomy
and assign all terms you want to apply to this content.

**taxonomy values are case insensitive**

### Front Matter Example (in JSON)

    {
        "title": "Hugo: A fast and flexible static site generator",
        "tags": [
            "Development",
            "Go",
            "fast",
            "Blogging"
        ],
        "categories" : [
            "Development"
        ],
        "series" : [
            "Go Web Dev"
        ],
        "slug": "hugo",
        "project_url": "http://github.com/spf13/hugo"
    }
