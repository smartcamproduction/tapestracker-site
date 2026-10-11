# tapestracker.com

Static site: home page, privacy policy (`/prywatnosc/`), terms (`/regulamin/`), account
deletion (`/usun-konto/`) and invite links (`/u/<nick>`, served by `404.html`).

`.well-known/` lets phones open invite links straight in the app:
- `assetlinks.json` — Android; PLACEHOLDER: SHA-256 of the signing key (`eas credentials -p android`;
  after Play launch also the key from Play Console → App integrity). Each fingerprint is a separate entry.
- `apple-app-site-association` — iOS; PLACEHOLDER: Apple Team ID (after joining Apple Developer).

Any static host works (GitHub Pages, Cloudflare Pages, Hostido FTP). `CNAME` and `.nojekyll`
are for GitHub Pages.
