# pocketdev releases

Signed APK builds of **pocketdev** — agentic coding from your phone, against a desktop
sandbox. The source lives in a private repository; this one carries binaries only.

## Install

1. Install [Obtainium](https://github.com/ImranR98/Obtainium).
2. Add app → `https://github.com/hans-e-yang/pocketdev-releases`.
3. Install the first APK manually from the release page, then let Obtainium handle
   updates.

## Verify

Every release publishes the APK and a `SHA256SUMS.txt`. Updates must be signed with the
same key, or Android will refuse to install them.

```
Signing certificate SHA-256:
39:74:A8:46:15:A9:29:DE:2A:4F:A1:D6:D5:5D:90:31:9D:FC:16:ED:2D:14:76:5C:55:BE:DF:63:09:20:75:29
```

```bash
apksigner verify --print-certs pocketdev-<version>.apk
```

## What's in a release

- `pocketdev-<version>.apk` — signed release build, package `dev.pocketdev.app`
- `SHA256SUMS.txt` — checksums

Built by GitHub Actions from a tagged commit. No source, no secrets, no configuration.
