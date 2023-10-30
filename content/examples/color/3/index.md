+++
title="Cyan"
template="example-3-index.html"
weight=3
[extra.poly]
hero="hero.png"
+++


### `sass/my-color.scss`

```scss

@use "sass:map";

$poly-config: (
  "primary-color": aqua,
  "mono-range": 45,
);

@use "../themes/polymathic/sass/polymathic.scss" with (
  $poly-config: $poly-config
);

```


### `templates/examples-base.html`

```html

{%/* import "polymathic/templates/macros/util.html" as util */%}
{%/* extends "polymathic/templates/index.html" */%}

{%/* block page_meta */%}
  {{/* util::content_meta(content=page) */}}
{%/* endblock */%}

{%/* block page_style */%}
  {%/* block example_style */%}
    <!-- example styles here -->
  {%/* endblock */%}
{%/* endblock */%}

{%/* block content */%}
  <nav class="navbar">
    <div class="navbar-brand">
      {%/* set anc = get_section(path = page.ancestors|last) */%}
      <a class="navbar-item" href="{{/*anc.path*/}}">
        Return to: {{/*anc.title*/}}
      </a>
      <h5 class="navbar-item">
        Now viewing: {{/*page.title*/}}
      </h5>
    </div>
    <div class="navbar-menu">
      <div class="navbar-end">
        <div class="navbar-item">
          <div class="buttons">
            {%/* if page.lower */%}
              <a href="{{/*page.lower.path*/}}" class="button is-light">
                Previous: {{/*page.lower.title*/}}
              </a>
            {%/* endif */%}
            {%/* if page.higher */%}
              <a href="{{/*page.higher.path*/}}" class="button is-primary">
                Next: {{/*page.higher.title*/}}
              </a>
            {%/* endif */%}
          </div>
        </div>
      </div>
    </div>
  </nav>
  {{/*super()*/}}
{%/* endblock */%}

{%/* block modals %} {%/*endblock*/%}
```

### `templates/my-example.html`

```html

{%/* extends "example-base.html" */%}

{%/* block example_style */%}
  <link rel="stylesheet" media="screen and (prefers-color-scheme: light)" href="{{ get_url(path='your-file-name.css') | safe }}" />
  <link rel="stylesheet" media="screen and (prefers-color-scheme: dark)" href="{{ get_url(path='your-file-name-dark.css') | safe }}" />
{%/* endblock */%}
```