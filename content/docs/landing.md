+++
title="Landing page"
description="content/_index.md and templates/index.html"
weight=3
[taxonomies]
features=["Navigation", "Rich content"]
[extra]
navigation_level=0
+++

Theme builds landing page using title, description and contents from `content/_index.md`, expanded version of site [global navigation](/docs/lvl1-nav) and [deep navigation](/docs/lvl2-nav).

For example:

```markdown

    +++
    title="Add a title"
    description="Optional description"
    [extra.poly]
    hero="hero.png"
    +++

    # My landing page content

    Hello word

    <form>
    
    {{/* field(type="email",name="email",label="Subscribe") */}}
    {{/* formButtons(submit="Subscribe") */}}

    </form>


```