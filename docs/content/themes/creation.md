+++
title = "Creating a Theme"
weight = 50
date = 2014-05-12T10:09:17Z
prev = "/themes/customizing"
next = "/templates/overview"

[menu]
  [menu.main]
    parent = "themes"
+++

Hugo has the ability to create a new theme in your themes directory for you
using the `hugo new` command.

`hugo new theme [name]`

This command will initialize all of the files and directories a basic theme
would need. Hugo themes are written in the go template language. If you are new
to Go, the [go template primer](/templates/primer/) will help you get started.

## Theme Components

A theme consists of templates and static assets such as javascript and css
files. Themes can also optionally provide [archetypes](/content/archetypes)
which are archetypal content types used by the `hugo new` command.

### Layouts

Hugo is built around the concept that things should be as simple as possible.
Fundamentally website content is displayed in two different ways, a single
piece of content and a list of content items. With Hugo a theme layout starts
with the defaults. As additional layouts are defined they are used for the
content type or section they apply to. This keeps layouts simple, but permits
a large amount of flexibility.

### Single Content

The default single file layout is located at `layouts/_default/single.html`.


### List of Contents

The default list file layout is located at `layouts/_default/list.html`


### Static

Everything in the static directory will be copied directly into the final site
when rendered. No structure is provided here to enable complete freedom. It is
common to organize the static content into 

    /css
    /js
    /img

The actual structure is entirely up to you, the theme creator, on how you would like to organize your files.


### Archetypes

If your theme makes use of specific keys in the front matter it is a good idea
to provide an archetype for each content type you have. Archetypes follow the
[guidelines provided](/content/archetypes).

