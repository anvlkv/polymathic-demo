+++
title="Thumbnails"
description="Customize page and section thumbnails, create previews of your content"
weight=4
[taxonomies]
features=["Customize"]
+++

# Thumbnails

This theme renders previews of subsections and pages using its `sections.html` template.

If page or section defines a [hero image](/docs/hero-images/#hero-images) it can be used for thumbnail as well.

## Configure for entire section

To render all page previews for one section in your `content/section/_index.md` add `page_thumbnails="default"`. Possible values are:

- `default` tile
- `block` block with title and description, hero image is used as block background if any
- `hero` tile with a hero image
- `banner` banner tile with a hero image
- `contents` renders block with page content

```md
    +++
    title="Section title"
    [extra.poly]
    page_thumbnails="default"
    +++
```

## Override or set only for individual pages

```md
    +++
    title="Page title"
    [extra.poly]
    thumbnail="block"
    +++
```

## Make previews of specific pages appear larger inside sections

```md
    +++
    title="Page title"
    [extra.poly]
    pop=true
    +++
```