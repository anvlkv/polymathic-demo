+++
title="Title and description"
description="Using title and description fields from your page's front-matter"
weight=3
[taxonomies]
features=["Rich content"]
+++

# Title and description

The theme uses `title` and `description` properties from your content's front-matter. 

```md
    +++
    title="Add a title"
    description="Optional description"
    +++
```

Additional titles may be created from taxonomies names, this only happens when using [shared taxonomies](/navigation). The theme does it by turning `my_taxonomy` into `My Taxonomy`. If you use those, you may like to double check for any oddly looking titles. Feel free to create an (issue)[https://github.com/anvlkv/polymathic/issues] in case you can not solve the odd title or encounter problems with translated content. 