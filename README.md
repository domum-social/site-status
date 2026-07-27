# Domum Social status site

The static status page for [Domum Social](https://domum.social), served by
GitHub Pages so it stays reachable when the instance itself is not.

Extracted from `domum-ops` at `roles/mastodon/files/status-site`, history intact.

## Updating

Edit `index.html`: set the timestamp and text under `.current`, and move the
previous entry to the top of `.history`. Push to `main`; Pages redeploys.

```
date -u
```

## Files

| File | Purpose |
|------|---------|
| `index.html` | The page — current status and history |
| `status.css` | Styling; `.current` / `.history` sections, red text for error states |
| `domum_logo.svg` | Logo |
| `favicon.ico` | Favicon |

## Custom domain

`status.domum.social` is served from here once its DNS record points at
GitHub Pages and a `CNAME` file containing `status.domum.social` is committed
to the repository root.
