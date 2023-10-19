+++
title="Install"
description="Adding Zola theme, installing dependencies"
weight=0
[taxonomies]
features=["Getting started"]
+++

# Install

Once you already have Zola installed and ran `zola init`, then run from your project directory

    $ git init
    $ git submodule add https://github.com/anvlkv/polymathic themes/polymathic

You will also need [npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) installed, then run

    $ npm --prefix themes/polymathic install

For those using netlify deployments config is available here

    $ cp themes/polymathic/netlify.toml netlify.toml

In your `config.toml` Set Zola theme to polymathic

```toml
    theme = "polymathic"
```