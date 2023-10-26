+++
title="Styles"
description="Configure and extend the theme styles"
weight=13
[taxonomies]
features=["Customize"]
+++

# Styles

This theme uses [`normalize-scss`](https://www.npmjs.com/package/normalize-scss).

This theme uses [`animate.css`](https://www.npmjs.com/package/animate.css).

To customize theme styles you can define a configuration map. This will allow you to change all theme variables, along with those of [bulma](https://bulma.io/documentation/customize/variables/). 


## Styles config

First you would need to create a config map. For example `sass/_config.scss`. See [all variables](/docs/variables)

```scss
    @use "sass:map";

    $poly-config: (
        'font-family': 'Your font', serif,
        'primary': red,
    );

    $poly-config-dark: (
        text-darkness: 8%,
        background-lightness: 7%,
        primary: red
    );
```

## Adding font

To change a preloaded font set `font_url` and update your `$theme-config:("font-family": 'My font', monospace);`.

```toml
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

And if customizing, keeping the dark theme.

```scss
    @use './config';
    @use '../themes/polymathic/sass/polymathic.scss' with (
        // theme config
        $poly-config: config.$poly-config-dark,
    );
```


## Extending templates

Finally override theme default templates. For example `templates/base.html`

```html
    {% extends "polymathic/templates/base.html" %}
    {% block page_style %}
        <link rel="stylesheet" media="screen and (prefers-color-scheme: light)" href="{{ get_url(path='your-file-name.css') | safe }}" />
        <link rel="stylesheet" media="screen and (prefers-color-scheme: dark)" href="{{ get_url(path='your-file-name-dark.css') | safe }}" />
    {% endblock %}
```

