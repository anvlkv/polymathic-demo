+++
title="Page asides"
description="Navigation within and across pages, additional content"
weight=4
[taxonomies]
features=["Navigation", "Customize", "Default"]
[extra]
navigation_level=4
+++

# Page asides

By default every page will try to render an `aside` with navigation:

- between next and previous pages within the same section
- between next and previous pages within the same taxonomy term (for every page term and taxonomy)
- to taxonomy-lists of its' taxonomies (with `render=true`)

An empty aside won't be rendered.


## Configure for entire section

You can configure default aside for all pages in a section

```md
    +++
    title="Section title"
    [extra.poly.page_asides]
    section=true
    term=true
    taxonomy=true
    content="Plain text"
    toc=true
    +++

    Section content
```

### Section aside

While sections do have visible `aside` rendered it's not configurable. Section renders its `_index.md` content to its aside, which expands to full page if the section has no descendants.

## Configure or override for individual pages

Disabling all default behavior

```md
    +++
    title="Page title"
    [extra.poly]
    aside=false
    +++
```

Disabling some default behavior

```md
    +++
    title="Page title"
    [extra.poly.aside]
    section=false # hide page navigation between next and previous pages within the same section
    term=true # render page navigation between next and previous pages within the same taxonomy term
    taxonomy=false # hide page navigation to taxonomy-lists of its' rendered taxonomies
    +++
```

### Additional content in aside

You can display additional text in the page aside by setting

```md
    +++
    title="Page title"
    [extra.poly.aside]
    content="Plain text aside content"
    +++

    Main content
```

Or hide the section aside content

```md
    +++
    title="Page title"
    [extra.poly.aside]
    content=false # disable section aside content for this page
    +++

    Main content
```

### Displaying table of contents `toc` in page aside

Besides all default navigation you can add table of contents to the current page aside


```md
    +++
    title="Page title"
    [extra.poly.aside]
    toc=true
    +++
```