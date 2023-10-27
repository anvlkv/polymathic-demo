+++
title="Breadcrumbs"
weight=10
[taxonomies]
features=["Navigation", "Default"]
[extra]
navigation_level=5
+++

# Breadcrumbs

By default the theme will render breadcrumbs on every page, section, taxonomy kind, and term, except the `index.html`

## Disable

You can disable breadcrumbs in your `config.toml`

```toml
    [extra.poly]
    breadcrumbs=false
```

## Extend

When extending `themes/polymathic/layout.html` or any of it descendants you may want to add breadcrumbs as following

```html
    {% extends "themes/polymathic/layout.html" %}

    {% block breadcrumbs %}
      {% if config.extra.poly.breadcrumbs -%}
        {% set root_section = get_section(path="_index.md", metadata_only=true) %}
        {% set links = ["/", path1, path2, currentPath...] %}
        {%- set titles = [root_section.title, title1, title2, currentTitle...] -%}
        {{navigation::breadcrumbs(links=links, titles=titles)}}
      {% endif %}
    {% endblock %}
```