# fixingflatware.com

The umbrella / manifesto site for **Fixing Flatware** — a small studio
un-bloating the everyday software you rely on. CUTLR is the first tool.

Static site. Everything lives in `public/` and is deployed as-is.

## Develop

```bash
./dev.sh          # serves public/ on http://localhost:8080
```

## Deploy

Push to `main` → GitHub Actions (`.github/workflows/deploy.yml`) publishes
`public/` to **GitHub Pages**. Custom domain **fixingflatware.com** is attached
once purchased (`public/CNAME`); `fixingflatware.xyz` 301-redirects to it.

One-time repo setting: **Settings → Pages → Source = "GitHub Actions"**.
