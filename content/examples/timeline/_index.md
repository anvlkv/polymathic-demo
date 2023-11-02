+++
title="Timeline"
description="Timeline example"
template="timeline.html"
page_template="render-contents.html"
[taxonomies]
features=["Timeline", "Navigation", "Advanced"]
[extra.poly.page_asides]
content="""
# Timeline

This page demonstrates timeline entry.

See [timeline docs](/docs/timeline). 

See [parent timeline](/examples/timeline). 
"""
[extra.poly.timeline]
format="%b %Y"
content=[
  "examples/timeline/_index.md"
]
offset={count=1, url="#", text="Dummy offset"}
limit={count=10, url="#", text="Dummy limit"}
+++

# Timeline

This page demonstrates [timeline](/docs/timeline).

```md

    +++
    title="Timeline"
    description="Timeline example"
    template="timeline.html"
    [extra.poly.timeline]
    format="%b %Y"
    content=[
      "examples/timeline/_index.md"
    ]
    offset={count=4, url="/", text="Dummy offset"}
    limit={count=4, url="/", text="Dummy limit}
    +++

    # Timeline

    This page demonstrates [timeline](/docs/timeline).

```

Timeline content is generated using chat GPT.