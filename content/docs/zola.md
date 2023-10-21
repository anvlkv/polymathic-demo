+++
title="Zola content"
description="Default styles applied to your content"
weight=2
[extra]
quick_step=2
[taxonomies]
features=["Getting started", "Rich content"]
+++

# Zola content

## Typography

This theme applies minimal default styling to content from your site's `content/`. All headings and subheadings extend appropriate bulma typography classes.

```md
    +++
    title="Page title"
    +++

    Next follows typography preview.

    # Typography title 1  <!-- .title.is-1 -->

    ## Typography title 2  <!-- .title.is-2.subtitle -->
    
    ### Typography title 3  <!-- .title.is-3.subtitle -->

    #### Typography title 4  <!-- .title.is-4.subtitle -->

    ...
```

## Bulma components

Beyond that you can use Bulma components in your content. This theme does not import all of them by default. See [more components](/docs/adding-more-components). Components are aligned with the theme or [your configuration](/docs/styles).

```md
    +++
    title="Page title"
    +++

    <div class="buttons">
        <button class="button is-primary">Primary</button>
        <button class="button is-link">Link</button>
    </div>
```