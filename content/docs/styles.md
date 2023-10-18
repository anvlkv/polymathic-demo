+++
title="Styles"
description="Configure and extend the theme styles"
weight=13
+++

# Styles

This theme uses [`scss-reset`](https://www.npmjs.com/package/scss-reset).

To customize theme styles you can define a configuration map. This will allow you to change all theme variables, along with those of [bulma](https://bulma.io/documentation/customize/variables/). 

## Styles config

First you would need to create a config map. For example `sass/_config.scss`

```scss
    @use "sass:map";

    $poly-config: (
        'font-family': 'Your font', serif,
        'primary': red,
    );
```

## Adding font

To change a preloaded font set `font_url` and update your `$theme-config:("font-family": 'My font', monospace);`.

```toml
    [extra]
    [extra.poly]
    font_url="https://font.hosting.com"
```

## Use theme styles with config

Last step for this template is to use the theme with provided config. For example `sass/your-file-name`

```scss
    @use './config';
    @use '../themes/polymathic/sass/polymathic.scss' with (
        // theme config
        $poly-config: config.$poly-config,
        // bulma variables
        $warning: red,
        $desktop: 1080px
    );
```


## Extending templates

Finally override theme default templates. For example `templates/base.html`

```html
    {% extends "polymathic/templates/base.html" %}
    {% block page_style %}
        <link rel="stylesheet" href="{{ get_url(path='your-file-name.css') | safe }}" />
    {% endblock %}
```

