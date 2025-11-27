# KobuBox Site

This repository contains the Hugo site for the KobuBox project.

Warning: It's mostly and AI fever dream for now, but it's something I wanted to get myself motivated!

## Prerequisites

- Install Hugo (extended version recommended). On macOS with Homebrew:

```bash
brew install hugo
```

## Running the site locally

From the root of this repo:

```bash
hugo server -D
```

Then open the URL Hugo prints (usually http://localhost:1313) in your browser.

## Custom theme

The site uses a custom theme located in `themes/kobubox` with a soft, cozy, "squishmallow" inspired design.

Most of the homepage content is rendered directly in `themes/kobubox/layouts/index.html`. You can tweak copy and structure there, or later move sections into content files and partials as the project grows.
