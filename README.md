# zabuton-app.github.io

The organization landing page for the 座布団 (zabuton) app series,
served at <https://zabuton-app.github.io/>.

It acts as an index of released zabuton apps, linking to each app's own
site (`/meguri/`, `/kizami/`, …), GitHub repository, and latest release.

## Structure

- `index.html` — the whole page: markup, styles, and a small script that
  fetches each app's latest release tag from the GitHub API
- `assets/` — the zabuton brand image and app icons (copied from each
  app's `docs/assets/icon.png`)

## Development

The site is a single static page with no build step. Preview it locally:

```bash
python -m http.server -d .
```

## Adding an app

1. Copy the app's icon into `assets/<romaji-name>.png`
2. Add an app card to the `.apps` grid in `index.html`, following the
   existing cards (kanji display name, romaji name, description, website
   and GitHub links, and a `data-repo` attribute for the release tag)

## Deployment

GitHub Pages serves the `main` branch root automatically — pushing to
`main` deploys the site.
