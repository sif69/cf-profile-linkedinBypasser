# cf-profile-linkedinBypasser

Lightweight static page that instantly redirects to a Codeforces profile and supplies an Open Graph preview image so LinkedIn shows a nice card instead of blocking the URL.

## What it does

* Serves a minimal `index.html` with Open Graph meta tags and a `meta refresh` redirect to `https://codeforces.com/profile/sif_69`.
* `preview.jpg` in the same folder is used as the `og:image` so social previews (LinkedIn/Twitter) render a thumbnail.

## Repo files

* `index.html` — redirect + OG meta tags (main file)
* `preview.jpg` — image used by `og:image` (place in same folder, case-sensitive)
* `README.md` — you (now) reading this

## Deploy (GitHub Pages)

1. Put `index.html` and `preview.jpg` at repo root.
2. Go to **Settings → Pages**.
3. Under **Source**, choose `main` branch and `/ (root)` folder. Save.
4. Wait ~1 minute, then visit `https://<your-username>.github.io/<repo-name>/` — the page will redirect to the Codeforces profile and LinkedIn should show the preview card.

Notes:

* Make sure `preview.jpg` filename and case exactly match `og:image` in `index.html`.
* If you prefer a JavaScript redirect instead of meta-refresh, replace the meta tag with `window.location.replace('https://codeforces.com/profile/sif_69')` inside a tiny script.
* Add `<meta name="viewport" content="width=device-width,initial-scale=1">` for mobile friendliness.

## Troubleshooting

* No image in preview: check filename, commit, and wait for GitHub Pages to rebuild.
* Page not enabled: enable Pages source in Settings (see Deploy steps).

## License

MIT — do what you want, credit's nice but not required.

---

Made by `sif69` — ping me on GitHub if you want tweaks.
