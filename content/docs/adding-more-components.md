+++
title="More Bulma components"
description="Include more or all Bulma components in your styles"
weight=14
+++

# More components

## Import all

This theme does not import all bulma components. Should you need more components, you may `@use` the `themes/polymathic/sass/all_bulma.scss`. If you're not using any style customization then simply link to `all_bulma.css` file. See [extending templates](./stles/#extending-templates).

## Import components one by one

Given you have [already created your styles config and scss file using the theme](./styles.md/#use-theme-styles-with-config). You can import more components after the `@use` statement. Use the theme path `@import "themes/polymathic/node_modules/bulma/{path to component}.sass"`.