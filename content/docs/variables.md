+++
title="Variables"
description="All Sass variables"
weight=14
[taxonomies]
features=["Customize"]
+++

# Sass variables

See [styles config](/docs/styles#styles-config) for more details on customization.

## Default

```scss
  $poly-primary: map.get($poly-config, "primary-color") or #7257bc !default;
  $poly-black: map.get($poly-config, "black") or #222 !default;
  $poly-white: map.get($poly-config, "white") or #fdfdfd !default;
  $poly-font-family: map.get($poly-config, "font-family") or "AR One Sans",
  $poly-font-family-print: map.get($poly-config, "font-family-print") or serif !default;
  $poly-ui-transition-time: map.get($poly-config, "ui-transition-time") or 250ms !default;
  $poly-ui-transition-fn: map.get($poly-config, "ui-transition-fn") or ease-out !default;
  $poly-body-size: map.get($poly-config, "body-size") or 16px !default;
  $poly-body-size-print: map.get($poly-config, "body-size-print") or $poly-body-size * .82 !default;
  $poly-darkness: map.get($poly-config, "text-darkness") or 90%;
  $poly-accent-saturation: map.get($poly-config, "accent-saturation") or 70%;
  $poly-lightness: map.get($poly-config, "background-lightness") or 99%;
  $poly-saturation: map.get($poly-config, "background-saturation") or 5%;
  $poly-text-saturation: map.get($poly-config, "text-saturation") or 10%;
  $poly-mono-range: map.get($poly-config, "mono-range") or 30;
  $_level: map.get($poly-config, "a11y-contrast") or "AA";
  $poly-background: map.get($poly-config, "background-color");
  $poly-text: map.get($poly-config, "text-color");
  $poly-link: map.get($poly-config, "link-color");
  $poly-info: map.get($poly-config, "info-color");
  $poly-info-dark: map.get($poly-config, "info-color-dark") or
  $poly-info-light: map.get($poly-config, "info-color-light") or
  $poly-link-dark: map.get($poly-config, "link-color-dark") or
  $poly-link-light: map.get($poly-config, "link-color-light") or
  $poly-grid-pop: map.get($poly-config, "grid-pop-size") or .75rem !default;
  $poly-hero-text-shadow: map.get($poly-config, "hero-text-shadow") or 0 .1em .15em rgba($poly-black, .75) !default;
  $poly-hero-hover-background: map.get($poly-config, "hero-hover-background") or linear-gradient(
    to bottom,
    rgba($poly-link-light, 0),
    rgba($poly-link-light, 0.25) 7%,
    rgba($poly-link-light, 0.95)
  ) !default;
  $poly-navigation-blocks-grid: map.get($poly-config, "navigation-blocks-grid") or (
    mobile: 2,
    tablet: 2,
    desktop: 3,
    widescreen: 4,
    fullhd: 4 
  ) !default;
```

## Dark

Besides all variables from `$poly-config` the `$poly-config-dark` also has following defaults

```scss
    $black: map.get($poly-config-dark, "black") or $poly-white !default;
    $black-bis: map.get($poly-config-dark, "black-bis") or darken($poly-white, 7%) !default;
    $black-ter: map.get($poly-config-dark, "black-ter") or darken($poly-white, 14%) !default;

    $grey-darker: map.get($poly-config-dark, "grey-darker") or
      darken($poly-white, 21%) !default;
    $grey-dark: map.get($poly-config-dark, "grey-dark") or darken($poly-white, 29%) !default;
    $grey: map.get($poly-config-dark, "grey") or darken($poly-white, 48%) !default;
    $grey-light: map.get($poly-config-dark, "grey-light") or
      lighten($poly-black, 100% - 71%) !default;
    $grey-lighter: map.get($poly-config-dark, "grey-lighter") or
      lighten($poly-black, 100% - 86%) !default;
    $grey-lightest: map.get($poly-config-dark, "grey-lightest") or
      lighten($poly-black, 100% - 93%) !default;

    $white-ter: map.get($poly-config-dark, "white-ter") or
      lighten($poly-black, 100% - 96%) !default;
    $white-bis: map.get($poly-config-dark, "white-bis") or
      lighten($poly-black, 100% - 98%) !default;
    $white: map.get($poly-config-dark, "white") or $poly-black !default;
```