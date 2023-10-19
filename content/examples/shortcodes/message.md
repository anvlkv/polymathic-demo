+++
title="message"
description="Bulma message component. A side note for your content"
[taxonomies]
features=["Rich content"]
+++

```md
    {%/* message() */%}

    Message body

    ## with markdown

    {%/* end */%}
```

{% message() %}

Message body

## with markdown

{% end %}

```md
    {%/* message(title="Message title") */%}

    Message body

    ## with markdown

    {%/* end */%}
```

{% message(title="Message title") %}

Message body

## with markdown

{% end %}