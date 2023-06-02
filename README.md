# Hyas SEO

Official SEO integration for Hyas.

## Status

[![npm (scoped)](https://img.shields.io/npm/v/@hyas/seo?style=flat-square)](https://www.npmjs.com/package/@hyas/seo)

## Installation

```bash
npm i @hyas/seo -D
```

## Setup

Add to `./config/_default/module.toml`:

```toml
[[mounts]]
  source = "node_modules/@hyas/seo/layouts"
  target = "layouts"

[[mounts]]
  source = "layouts"
  target = "layouts"
```

Add to `./config/_default/config.toml`:

```toml
title = "Hyas"
enableRobotsTXT = true

[social]
  twitter = "gethyas"
```

Add to `./config/_default/params.yml`:

```bash
seo:
  description: "Build your next web project with the official Bootstrap starter for Hyas."
  generate:
    title: true
    meta: true
    twitter: true
    og: true
    jsonld:
      article: true
      breadcrumbs: true
  title_tag:
    separator: "|"
    home_text: "Bootstrap Starter"
  og_article_types: [post, posts, blog, news, article, articles, event, events, course, courses]
  jsonld_article_types: [article, articles]
  jsonld_news_article_types: [news, updates]
  jsonld_blog_posting_types: [post, posts, blog]
  image: "/images/kris-mikael-krister-aGihPIbrtVE-unsplash.jpg" 
  private: false
```

## Usage

See the Hyas docs: [SEO](https://gethyas.com/docs/reference-guides/seo/)


## Credits

This npm package is based on the Hugo module:

- [future-wd/hugo-seo](https://github.com/future-wd/hugo-seo)
