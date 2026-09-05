# small potatoes

Personal site for [paladinnx.github.io](https://paladinnx.github.io), built with [Eleventy](https://www.11ty.dev/).

## Local

Needs Node 18+.

```sh
npm install
npm start
```

Open http://localhost:8080. `npm run build` writes static files to `_site/`.

New posts go in `src/posts/` as Markdown files named `YYYY-MM-DD-slug.md`.

## GitHub Pages (required once)

GitHub will not publish this site until Pages is pointed at Actions instead of a branch (the old Jekyll setup).

1. Commit and push these files to `master`.
2. Open the repo on GitHub: **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **GitHub Actions** (not “Deploy from a branch”).
4. Open the **Actions** tab and confirm **Deploy to GitHub Pages** runs. The first run after step 3 should deploy.
5. If the workflow is waiting on approval, open **Settings → Environments → github-pages** and allow the `master` branch (or disable required reviewers).

After that, every push to `master` rebuilds and publishes https://paladinnx.github.io.

This repo is a user site (`username.github.io`), so it is served from `/`. Do not add `--pathprefix` unless you move it to a project repo.
