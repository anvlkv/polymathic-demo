+++
title="Shortcodes"
description="Shortcodes provided with the theme"
weight=12
[taxonomies]
features=["Rich content", "Forms"]
+++

# Shortcodes

Polymathic includes several simple shortcodes. To use in your Zola content.

## message

```md
    {%/* message(title="message title") */%}

    Some body content

    ### supports markdown

    {%/* end */%}
```

## heroCard

When used with images `alt` attribute is either provided to the shortcode or derived from file name.

```md
    {%/* heroCard(hero="my-page-asset.png", banner=true, href="/some-page") */%}

    Some body content

    ### supports markdown

    {%/* end */%}
```

## assetCard

When used with images `alt` attribute is either provided to the shortcode or derived from file name.

```md
    {%/* assetCard(image="my-page-asset.png") */%}

    Some body content

    ### supports markdown

    {%/* end */%}
```

## assetGallery

Renders grid with all assets of current page or section

```md

    {{assetGallery(exclude=["some.png"],titles=false)}}
```

## field

```md
    {{/* field(name="field-name") */}}
```

## formButtons

```md
    {{/* formButtons(cancel="Some text") */}}
```