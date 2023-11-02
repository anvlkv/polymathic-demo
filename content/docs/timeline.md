+++
title="Timeline"
description="Organize your content into timeline. Timeline template and extra"
weight=4
[taxonomies]
features=["Navigation", "Timeline", "Advanced"]
[extra]
navigation_level=5
+++

# Timeline

Polymathic comes with template for building timelines from your content. Timeline renders **pages** according to their parent section's `page_thumbnails` or page `thumbnail`.

> Timeline may behave unexpectedly when rendering overlapping time spans. Feel free to [open an issue or propose your solution](https://github.com/anvlkv/polymathic/issues).

## Add a timeline page front-matter

Add a page where you want to display the timeline. It can be a section or page.

Specify sections or individual pages to be included in the timeline in `[extra.poly.timeline]` `content`.

Use the `template="timeline.html"` in your content 

```md
    +++
    title="Timeline title"
    template="timeline.html"
    [extra.poly.timeline]
    content=[
      "section/_index.md", # pages from section
      "section/subsection/_index.md", # pages from subsection 
      "another-section/some-page/index.md", # and a page
    ]
    +++

    Content displayed in aside
```

### Format dates

See [chrono](https://docs.rs/chrono/0.4.31/chrono/format/strftime/index.html) for format specification

```md
    +++
    title="Timeline title"
    template="timeline.html"
    [extra.poly.timeline]
    format="%Y-%m-%d %H:%M"
    content=[
      ...
    ]
    +++
```

### Reverse

```md
    +++
    title="Timeline title"
    template="timeline.html"
    [extra.poly.timeline]
    reverse=true
    +++
```

### Limiting and offsetting

Limit the size of timeline or offset it.

`[extra.poly.timeline] limit` limits the number of entries in timeline and adds a button to end of the timeline. You can configure count, text, and next url.

`[extra.poly.timeline] offset` offsets the start of entries in timeline and adds a button before the timeline. You can configure count, text, and previous url.

You would need to define separate content entries for each segment of the timeline

```md
    +++
    title="Timeline title"
    template="timeline.html"
    [extra.poly.timeline]
    offset={ count=4, url="/timeline/0", text="previous" }
    limit={ count=4, url="/timeline/2", text="next" }
    +++
```


## Add dates to all timeline pages

Add `date` in [front matter](https://www.getzola.org/documentation/content/page/#front-matter) of the page or use the filename date.

Template will throw an error if there's no date.

## Span timestamps

`date` is always used for sorting.

Set `[extra.poly.timeline] start_date`, then page `date` will be treated as `end_date`.

Set `[extra.poly.timeline] end_date`, then page `date` will be treated as `start_date`.

Set `[extra.poly.timeline] end_date` and `[extra.poly.timeline] start_date`, `date` property will be only used for sorting the timeline.

```md 
    +++
    title="My page"
    date=2023-10-31
    [extra.poly.timeline] 
    start_date=2023-10-01
    end_date=2023-11-01
    +++
```

## Vague dates

When the actual date is vague like "2020's" you can set `[extra.poly.timeline]` `vague` of your page to `true` or a `"string"`.

Then dates are still used for ordering and positioning but timeline displays your custom value or nothing on that segment instead of formatted date.

```md 
    +++
    title="My page"
    date=2023-10-31
    [extra.poly.timeline] 
    vague="Once upon a time"
    +++
```