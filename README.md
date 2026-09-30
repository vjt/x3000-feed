# x3000-feed

apk package feed for the OpenWrt GL-X3000 images published at
[vjt/openwrt-glinet-x3000](https://github.com/vjt/openwrt-glinet-x3000/releases).

It is served by GitHub Pages from the `gh-pages` branch at
<https://vjt.github.io/x3000-feed/>. It provides:

- `kmods/<release>/` — every kernel module for that release's kernel, so
  `apk add kmod-<name>` works. Modules only install on the release they were
  built for.
- `custom/` — the custom packages baked into those images, so they can be
  updated with `apk` instead of a reflash.

Images from the first release that carries the feed onwards already list both
URLs in `/etc/apk/repositories.d/x3000feed.list` and trust the signing key.
There is nothing to configure.

The `gh-pages` branch is rewritten on every publish; do not base anything on
its history.
