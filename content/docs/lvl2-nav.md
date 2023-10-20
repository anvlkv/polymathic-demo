+++
title="Deep navigation"
description="Customize navigation items on landing page and in global header submenus. Using Zola taxonomies"
weight=9
[extra]
navigation_level=2
[taxonomies]
features=["Navigation"]
+++

# Deep navigation (level 2)

To build richer navigation **sections** may have a list of taxonomies defined in their front matter:

```md
    +++
    [extra.poly]
    use_taxonomies= ["taxonomy_name", "another_taxonomy_name"]
    +++
```

Same taxonomies should be defined in your `config.toml`:

```toml
    taxonomies= [
        {name="taxonomy_name"},
        {name="another_taxonomy_name"}
    ]
```
