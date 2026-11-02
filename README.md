# Business Evaluation (static site for GitHub Pages)

- `evaluation/index.html`: the evaluation. Talks to the `momentum-roadmap` Worker (`API_URL` at the top of its script).
- `index.html`: root of the subdomain, forwards to themomentumcycle.com. Future lead magnets go in sibling folders.

## Before going live
1. Set `TURNSTILE_SITE_KEY` (currently Cloudflare's always-pass test key).
2. Stage names, descriptions and questions are copied from the Worker's `src/index.js`. If you edit them
   there, copy them here too (the Worker's copy is the one that scores).

## Custom domain
1. Repo → Settings → Pages: deploy from `main`, root folder.
2. Add a `CNAME` file containing only the subdomain (e.g. `go.themomentumcycle.com`).
3. Squarespace → Domains → DNS: CNAME record, host = the subdomain part (e.g. `go`), value = `zkrunyon-ui.github.io`.
4. GitHub → your profile Settings → Pages → Verify the domain (prevents takeover), then tick "Enforce HTTPS".

## values/
The Values Assessment (`values/index.html`), API = the `tmc-values` Worker. The values list in the page is
generated from `../Values Assessment/src/copy.js`; if you edit labels there, regenerate the page.
Same Turnstile site key as the evaluation.

## Photo credits
- assets/together-trail.jpg (values): the hero photo from themomentumcycle.com (Unsplash).
- assets/summit-path.jpg (evaluation): Pascal Debrunner on Unsplash, https://unsplash.com/photos/eiLiKk5Zsgs (Unsplash License: free to use, no attribution required).
