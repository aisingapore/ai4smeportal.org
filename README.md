# ai4smeportal.org

Redirect-only site. Every request to **ai4smeportal.org**, on any path (e.g. `ai4smeportal.org/look-ai`), is sent to **https://ai4sme.org/**.

## Stack

Plain static HTML, no build step. Hosted on **GitHub Pages**.

## Files

| File | Purpose |
|------|---------|
| `index.html` | Redirects `ai4smeportal.org/` to https://ai4sme.org/ |
| `404.html` | GitHub Pages serves this for any other path, so `ai4smeportal.org/*` also redirects |
| `CNAME` | Tells GitHub Pages the custom domain is `ai4smeportal.org` |
| `.nojekyll` | Serve files as-is, skip Jekyll processing |

GitHub Pages can't do server-side 301s, so the redirect is done with an instant meta refresh plus `location.replace()`.

## Run locally

```bash
open index.html
```

