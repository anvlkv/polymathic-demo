+++
title="Landing page"
description="content/_index.md and templates/index.html"
weight=3
+++

Theme builds landing page using title, description and contents from `content/_index.md`, extended version of site [global navigation](/navigation).

For example:

```markdown

    +++
    title="Add a title"
    description="Optional description"
    [extra]
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