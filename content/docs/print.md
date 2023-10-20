+++
title="Print"
description="Customize print stylesheets"
weight=15
[taxonomies]
features=["Customize", "Advanced"]
+++

# Print

This theme comes with basic support for print media. You can customize or override print styles `themes/polymathic/sass/print.scss`.

See [styles for general approach](./styles.md).

```html
    {% extends "polymathic/templates/base.html" %}
    {% block print_style %}
        <link rel="stylesheet" media="print" href="{{ get_url(path='your-print-file-name.css') | safe }}" />
    {% endblock %}
```

