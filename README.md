# Zeph app catalog

Published Zeph apps for the [Zeph](https://usezeph.com) companion. Same pattern as the skills catalog:

- **`index.json`** + **`index.json.sig`** — the signed registry the companion fetches (`apps_catalog_refresh` verifies the signature against the pinned key before trusting any entry).
- Each app version ships as a **GitHub Release** (`<id>-v<semver>`) carrying its signed **`.zeph-app`** bundle.

Apps are built + signed from the [zeph monorepo](https://github.com/zephclick/zeph) (`just zeph-tour-bundle`, `release apps --publish`). Pre-v1: dev-signed; production key rotation is tracked separately.
