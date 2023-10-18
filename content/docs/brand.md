+++
title="Brand"
description="Customize your favicons, titles, and font"
weight=1
+++

# Brand

## favicon

You can add multiple favicons by specifying them in `config.toml`

```toml
    [extra]
    [extra.poly]
    favicon = [
        {rel = "icon", type = "image/x-icon", size = "", path = "/favicon.ico"},
        {rel = "apple-touch-icon", type = "image/png", size = "180x180", path = "/favicon/apple-touch-icon.png"},
        {rel = "icon", type = "image/png", size = "32x32", path = "/favicon/favicon-32x32.png"},
    ]
```

## Name

Name, app name, or brand name `app_name`

```toml
    [extra]
    [extra.poly]
    app_name = "your app name"
```

## Logo

```toml
    [extra]
    [extra.poly]
    logo = "/your-logo.png"
```

##  Include a font url

```toml
    [extra]
    [extra.poly]
    font_url = "https://fonts.googleapis.com/css2?family=AR+One+Sans:wght@400;700&display=swap"
```

## webmanifest

Whether to include a webmanifest file and path to it.

```toml
    [extra]
    [extra.poly]
    manifest = "/webmanifest.json"
```

## og:image fallback

Fallback `og:image` (one for entire site) can be configured in your `config.toml` and must point to a static file

```toml
    [extra]
    [extra.poly]
    og_image= "/og.png"
```