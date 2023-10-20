+++
title="Global navigation"
description="Customize navigation items on landing page and in global header"
weight=8
[extra]
quick_step=4
navigation_level=0
[taxonomies]
features=["Getting started", "Navigation"]
+++

# Global navigation (level 1)


To enable global navigation add to your `config.toml` the paths to **pages** and **sections** which you want to include. The paths in `menu_order` should reflect actual paths to your content.

```toml
    [extra.poly]
    menu_order = [
        "resume/_index.md",
        "projects/_index.md",
        "contact.md"
    ]
```
