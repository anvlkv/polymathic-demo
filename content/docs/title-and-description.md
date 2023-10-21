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

Additional titles may be created from taxonomies names, this only happens when using [shared taxonomies](/docs/lvl1-nav). The theme does it by turning `my_taxonomy` into `My Taxonomy`. If you use those, you may like to [customize how your taxonomies are](/docs/taxonomies/#configuration-taxonomiesyaml) displayed.