+++
title="Implementation"
description="Showing section with a hero tile"
[taxonomies]
features=["Rich content", "Customize", "Navigation"]
+++

### `content/section/_index.md`

```md
    +++
    title="Section with hero"
    description="Hero section tile"
    [extra.poly]
    hero="DALL-E-2023-10-18_18.46.38_jungle_tropic_happiness_painting_wax_pastel.png"
    +++

    This section shows a hero tile as its preview


```

### `content/section/page.md`

```md 
    +++
    title="Implementation"
    description="Showing section with a default tile"
    +++

    ### `content/section/_index.md`

    ```md
        +++
        title="Section with hero"
        description="Hero section tile"
        [extra]
        [extra.poly]
        hero="DALL-E-2023-10-18_18.46.38_jungle_tropic_happiness_painting_wax_pastel.png"
        +++

        This section shows a hero tile as its preview


    ```

    ### `content/section/page.md`

    ...
```