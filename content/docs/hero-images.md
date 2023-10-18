+++
title="Hero images"
description="Use images to emphasize your pages and sections"
weight=7
+++

# Hero images

Every **page** and **section** may have a hero image. Hero image is used by the theme and for Open Graph meta `og:image`. Hero image is defined in content front matter. You can specify path to one of your static paths, page or section assets. 

```md
    +++
    [extra]
    [extra.poly]
    hero="my-hero-image.png"
    +++
```

Fallback `og:image` (one for entire site) can be configured in your `config.toml` and must point to a static file
    
```toml
    [extra]
    [extra.poly]
    og_image= "/og.png"
```

Theme resizes and optimizes hero and social images using Zola's `resize_image()`.