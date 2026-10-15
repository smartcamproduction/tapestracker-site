# tapestracker.com

Static site: home page, privacy policy (`/prywatnosc/`), terms (`/regulamin/`), account
deletion (`/usun-konto/`) and invite links (`/u/<nick>`, served by `404.html`).

`.well-known/` lets phones open invite links straight in the app:
- `assetlinks.json` — Android; holds the SHA-256 of the EAS keystore (same for all EAS builds;
  after Play launch also the key from Play Console → App integrity). Each fingerprint is a separate entry.
- `apple-app-site-association` — iOS; Apple Team ID XULP3L29B3 + bundle id.

Any static host works (GitHub Pages, Cloudflare Pages, Hostido FTP). `CNAME` and `.nojekyll`
are for GitHub Pages.

## Publishing

Hosted on GitHub Pages from the public repo `smartcamproduction/tapestracker-site` (only this
folder — the app repo stays private). After changing files here, commit and run from the repo root:

    bash scripts/publish-site.sh

(Merges with the published history instead of force-pushing.) DNS at Hostido: see docs/SETUP-DOMENA.md.
