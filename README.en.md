[Русский](README.md) | [English](README.en.md)

# ByeByeDPI Manual

The documentation consists of Markdown files and images. After a change is pushed to the [repository](https://github.com/BDManual/ByeByeDPI-Manual), GitHub Actions builds them into the [byebyedpi.xyz](https://byebyedpi.xyz) website.

## Prerequisites

For local work, install:

1. [Hugo Extended](https://gohugo.io/installation/)
2. [Git](https://git-scm.com/downloads)
3. [Go](https://go.dev/doc/install) - used to download the Hextra theme

[Fork the repository](https://github.com/BDManual/ByeByeDPI-Manual/fork) and clone your fork, replacing `<YOUR_USERNAME>` with your GitHub username:

```bash
git clone https://github.com/<YOUR_USERNAME>/ByeByeDPI-Manual.git
cd ByeByeDPI-Manual
```

For a small correction, you can skip the local setup: open the relevant file in [`content`](content), click **Edit this file**, and propose the change through a Pull Request.

## Working with Hugo

Run this command in the repository directory:

```bash
hugo server -D
```

Hugo downloads the Hextra theme on the first run. When the site is ready, open [http://localhost:1313/](http://localhost:1313/). File changes will appear automatically.

Pages are stored in [`content/docs`](content/docs):

- `.ru.md` - Russian version;
- `.en.md` - English version.

Create both language files when adding a page. Follow the existing page structure and start each file with:

```yaml
---
title: Page title
weight: 9
---
```

The `weight` determines the page order in the sidebar.

## Text and image requirements

- Check spelling, punctuation, and whether the instructions work.
- Update the Russian and English versions together when possible.
- New image names must contain only lowercase Latin letters, digits, and hyphens: `proxy-settings.png`.
- Put images in [`static/images`](static/images) and insert them as `![Description](/images/proxy-settings.png)`.
- Capture only the relevant part of the screen, hide personal information, and compress excessively large files.

## Submitting changes

Before submitting, make sure the site builds without errors:

```bash
hugo --minify
```

Push the changes to your fork and click **Create Pull Request** in the GitHub interface. The Pull Request will either be accepted or receive review comments. Push corrections to the same branch and they will automatically appear in the existing Pull Request.

## Disclaimer

> **Use this material at your own risk.**

DPI bypass behavior depends on the ISP, time, and target resources. The materials are provided for educational purposes. Use them legally and only on networks where you have permission.
