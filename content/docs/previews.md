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

To render all your previews as blocks in your `content/section/_index.md` add `page_block=true`

```md
    +++
    title="Section title"
    [extra.poly]
    page_block=true
    +++
```

## Override or set only for individual pages

```md
    +++
    title="Page title"
    [extra.poly]
    block=false
    +++
```

## Make previews larger

```md
    +++
    title="Page title"
    [extra.poly]
    pop=true
    +++
```