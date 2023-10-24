+++
title="Thumbnails"
description="Customize page and section thumbnails, create previews of your content"
weight=4
[taxonomies]
features=["Customize"]
+++

# Thumbnails

This theme renders previews of subsections and pages using its `sections.html` template.

If page or section defines a [hero image](/docs/hero-images/#hero-images) it will be used for thumbnail as well.

## Configure for entire section

To configure all page previews for one section in your `content/section/_index.md` add `page_thumbnails="value"`. Use `section_thumbnails="value"` to configure subsections. Possible values are:

- `"default"` card tile
- `"block"` block with title and description, hero image is used as block background if any
- `"banner"` banner tile with a hero image
- `"contents"` block with page content

```md
    +++
    title="Section title"
    [extra.poly]
    page_thumbnails="block"
    section_thumbnails="default"
    +++
```

## Override or set only for individual pages or subsections

```md
    +++
    title="Page title"
    [extra.poly]
    thumbnail="block"
    +++
```

## Make previews of specific pages or subsections appear larger inside their parent sections

```md
    +++
    title="Page title"
    [extra.poly]
    pop=true
    +++
```