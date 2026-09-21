# raindrop-medias-to-podcast

Publishing target for the video podcast feed built by
[raindrop-to-reader](https://github.com/ryderlee/raindrop-to-reader).

This repository holds no code. The `podcast.yml` workflow in that other
repository writes here:

| Path | What it is |
|---|---|
| `manifest.json` | The record of every candidate: published, skipped, and why. Written by the `discover` and `episode` jobs. |
| `feed.xml` | The RSS feed, rebuilt from the manifest on every run by the `assemble` job. Served by GitHub Pages. |
| Release assets | The media files themselves, one release per episode. |

Subscribe a podcast client to the `feed.xml` URL served by Pages.

## This repository is public

Anyone with the URL can fetch the feed, the manifest and the media. There is no
access control. That was a deliberate choice: GitHub Pages cannot serve a
private repository, and podcast clients cannot authenticate.
