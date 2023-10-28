+++
title="Taxonomies"
description="Customize and supercharge Zola taxonomies"
weight=14
[extra]
navigation_level=4
[taxonomies]
features=["Advanced", "Customize", "Navigation"]
+++

# Taxonomies

This theme allows you to customize how taxonomies are displayed and how they sort pages

## taxonomy_preview_count `config.toml`

You can additionally customize how many items are displayed in `taxonomy_list.html`

```toml
    [extra.poly]
    taxonomy_preview_count=8 # default is 3
```

## Configuration `taxonomies.yaml` 

This theme supports customizing taxonomies by loading additional config. You can create your `taxonomies.yaml` in your project root or any other file supported by Zola's `load_data`. Note, `zola serve` won't update on changes in this file unless you put it in a `static` folder or trigger update by making changes elsewhere in a watched file. 

```yaml
    taxonomy_kind: # name of your taxonomy
      title: Your title # custom title
      description: Description # optional description
      content: | # optional content for taxonomy_list.html
        ### Some title

        Content supports markdown
      sort_by: path # default sort_by for pages when showing this taxonomy see available page variable here https://www.getzola.org/documentation/templates/pages-sections/
      reverse: false # whether to apply | reverse filter to sorted pages
      terms: # order of terms, specify only top ones or all
        - Term name # select term by name for ordering
        - title: Another term # select term by name for ordering and customization
          description: Term description # optional description
          content: | # optional content for taxonomy_single.html
             ### Some title

             Content supports markdown
          sort_by: "extra.my_property" # override default sort for specific term
          reverse: true # override sort_by reverse
    another_taxonomy: # and so on...
      title: Custom title 2 
```

## taxonomy_config_path `config.toml`

You may use any other file as long as it has the same structure as the one above

```toml
    [extra.poly]
    taxonomy_config_path="path/to/your-file.yaml" # or leave out `./taxonomies.yaml` is the default
```