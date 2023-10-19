+++
title="Implementation"
description="Showing section with a default tile"
[taxonomies]
features=["Rich content", "Customize", "Navigation"]
+++

### `content/section/_index.md`

```md
   +++
    title="Section pop with hero"
    description="Hero section pop tile"
    [extra.poly]
    hero="DALL-E-2023-10-18_18.46.38_jungle_tropic_happiness_painting_wax_pastel.png"
    pop=true
    +++

    This section shows a pop hero tile as its preview


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
        title="Section pop with hero"
        description="Hero section pop tile"
        [extra]
        [extra.poly]
        hero="DALL-E-2023-10-18_18.46.38_jungle_tropic_happiness_painting_wax_pastel.png"
        pop=true
        +++

        This section shows a pop hero tile as its preview


    ```

    ### `content/section/page.md`

    ...
```