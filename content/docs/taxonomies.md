+++
title="Taxonomies"
description="Customize and supercharge Zola taxonomies"
weight=14
[taxonomies]
features=["Advanced", "Customize", "Navigation"]
+++

# Taxonomies

This theme supports customizing taxonomies by loading additional config. You can create your `taxonomies.yaml` in your project root or any other file supported by Zola's `load_data`

## taxonomy_config_path `config.toml`

```toml
    [extra.poly]
    taxonomy_config_path="path/to/your-file.yaml" # or leave out `./taxonomies.yaml` is the default
```

## taxonomy_preview_count `config.toml`

You can additionally customize how many items are displayed in `taxonomy_list.html`

```toml
    [extra.poly]
    taxonomy_preview_count=8 # default is 3
```

## Configuration `taxonomies.yaml` 


```yaml
    [taxonomy name]: 
      title: Your title
      description: Description
      content: |
        ### Some title

        Content supports markdown
      sort_by: title # default sort_by for taxonomy pages
      terms: 
        - Term name # select term by name for ordering
        - title: Another term # select term by name for ordering and customization
          description: Term description
          content: |
             ### Some title

             Content supports markdown
          sort_by: "extra.my_property"
```

