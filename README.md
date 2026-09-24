# Ralue Editor corresponding source

Ralue Editor is Ralue's modified build of Collabora Online. Collabora Online is
primarily licensed under the Mozilla Public License 2.0 (MPL-2.0). This
directory provides the corresponding source information and ordered patch
series for the exact editor build distributed by Ralue.

Ralue is an independent product and is not affiliated with, endorsed by, or
sponsored by Collabora Productivity Ltd. Collabora and LibreOffice names and
marks belong to their respective owners.

## Exact release

- Ralue image: `ralue/editor:mvp-26.04.2.9`
- Ralue source tag: `ralue-editor-mvp-26.04.2.9-source-offer`
- Ralue source commit: `c82544ae`
- Browser revision: `c84e02f6a1`
- Upstream repository: `https://github.com/CollaboraOnline/online.mirror.git`
- Upstream commit: `2229109277f4b443dd1eb5df11c5e59f74d1a45d`

## Reconstruct the modified source

Clone the upstream source, check out the immutable revision, and apply every
patch in lexical order:

```bash
git clone --filter=blob:none https://github.com/CollaboraOnline/online.mirror.git ralue-editor
cd ralue-editor
git checkout 2229109277f4b443dd1eb5df11c5e59f74d1a45d
git am /path/to/career-hub/open-source/ralue-editor/patches/*.patch
```

The patch series includes the modified MPL-covered files plus the Ralue build
and deployment files needed to produce the release. The exact engine image,
digest and browser revision are recorded in `UPSTREAM.lock`. Verify downloaded
patches against `PATCHES.sha256` before applying them.

## Licensing and notices

The modified covered source remains available under MPL-2.0. Preserve the
upstream `COPYING`, `README.FILENOTICES.md`, per-file notices, source history,
and third-party notices in `browser/LICENSE`. Files in the larger Career Hub
application that do not contain MPL-covered code retain their own licensing.

This package is an engineering compliance measure, not legal advice. Questions
about source availability can be sent to `support@ralue.app`.
