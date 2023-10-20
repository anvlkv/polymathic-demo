+++
title="Global footer"
description="Footer content and out-links"
weight=11
[extra]
quick_step=5
navigation_level=1
[taxonomies]
features=["Getting started", "Customize", "Navigation"]
+++

# Global footer

Site global footer displays expanded version of the complete site navigation plus optional out-links.

## Footer out-links

You can add social out-links and more to your global footer. In your `config.toml` add:

```toml
    [extra.poly]
    social_outlink = [
        {href="https://www.linkedin.com/", title="LinkedIn", icon=false},
        {href="mailto:email@domain.com", title="Email", icon=false},
        {href="tel:+05890000111", title="0-589-0000111", icon=false},
    ]
```

To add an icons to links in footer add an [icon font](https://bulma.io/documentation/elements/icon/) to your project and set `icon="font-prefix icon-name"` in the link config. 

```toml
    [extra.poly]
    social_outlink = [
        {href="https://www.linkedin.com/", title="LinkedIn", icon="fas fa-linkedin"},
    ]
```