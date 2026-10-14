# Sixgree plugins

Plugins add features to [Sixgree](https://sixgree.com), the app that maps your professional network. You install them from inside the app: **Settings → Plugins**, turn on **Enable plugins**, then **Browse**. Each one shows what it does and what it risks before anything is installed, and nothing installs without your yes.

This repo holds the official plugin list (`catalog.json`) and the packages it points to (`packages/`).

## The plugins

| Plugin | What it does |
|---|---|
| **Auto scan** (`auto-scan`) | Reads the circles of people you know on LinkedIn by itself: it turns the pages on its own. Also brings Auto scan, Auto connect, Check for new and Dev mode. |
| **Manual scan** (`manual-scan`) | Reads those circles while you page through them yourself: you scroll each page and click Next, and it reads as you go, with chimes. |

Install either one or both. With only Manual scan, every circle scan is by hand.

## Read this before installing a scanner

Both scanners read LinkedIn pages with **your own account**, in Chrome on your computer. LinkedIn's User Agreement doesn't allow automated tools, and **LinkedIn can restrict accounts that use them**. Heavy days and fast paging are what get noticed: a few hundred search pages in a day, or pages loaded seconds apart.

The scanners keep a daily budget and stop the moment LinkedIn pushes back. Even with every limit lifted, Dev mode stops at 250 search pages a day. Use them slowly, on an account you're prepared to have restricted.

A plugin runs its own code on your computer, with the same access as Sixgree.

## For plugin makers

The package format (`.sgplugin`, a zip with a manifest listing every file by sha256) and the list format are documented in the app's repo, in `docs/PLUGINS.md`. The scanner packages here are built from the scanner's source in the app's repo, with `npm run build:plugins -- --catalog <base-url>`.

## License

MIT.
