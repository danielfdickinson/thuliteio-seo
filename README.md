# Hyas SEO

Official SEO integration for Hyas.

## Status

[![npm (scoped)](https://img.shields.io/npm/v/@hyas/seo?style=flat-square)](https://www.npmjs.com/package/@hyas/seo)

## Installation

```bash
npm i @hyas/seo
```

## Setup

Add mounts to `./config/_default/module.toml`:

```toml
[[mounts]]
  source = "node_modules/@hyas/seo/layouts"
  target = "layouts"

[[mounts]]
  source = "layouts"
  target = "layouts"
```

Add settings to `./config/_default/hugo.toml`:

```toml
title = "Hyas"
enableRobotsTXT = true

[social]
  twitter = "gethyas"
```

Set parameters in `./config/_default/params.toml`:

```toml
# Hugo
title = "My Docs"
description = "Congrats on setting up a new Doks project!"
images = ["cover.png"]

# SEO (@hyas/seo)
[seo]
  [seo.title]
    separator = " | "
    suffix = ""
  [seo.favicons]
    sizes = []
    icon = "favicon.png" # favicon.png (default)
    svg_icon = "favicon.svg" # favicon.svg (default)
    mask_icon = "mask-icon.svg" # mask-icon.svg (default)
    mask_icon_color = "white" # white (default)
```

## How to use

See the Hyas documentation:

- [SEO](https://docs.gethyas.com/guides/integrations-guide/seo/)

## Credits

This npm package is based on:

- [Hugo SEO](https://gitlab.com/hugo-modules/hugo-seo)
