# fitOS public site (GitHub Pages)

A tiny static site that fitOS needs on the public internet:

- `spotify/` — the Spotify **redirect URI** ("bounce" page). Spotify only accepts https (or
  loopback) redirects and fitos-server is plain http on the LAN, so Spotify sends the phone here
  and the page forwards `code` / `state` / `error` to fitos-server. Edit `FITOS` in
  `spotify/index.html` if the server isn't at `http://10.0.10.10:7210`.
- `index.html`, `privacy.html`, `pt.html` — the public home and privacy pages Google asks for
  before the YouTube OAuth app can be published.

Publish: copy this folder to a GitHub repo named `fitos` (or any name), Settings → Pages →
Deploy from branch → `main` / root. The site is then `https://<you>.github.io/fitos/`, and the
redirect URI is `https://<you>.github.io/fitos/spotify/`. See docs/research/spotify.md.
