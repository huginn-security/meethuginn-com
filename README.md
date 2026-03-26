# meethuginn.com

Public-facing website for the Huginn Security Platform.

## Structure

```
scanner/index.html    — Scanner transparency & opt-out page
index.html            — Landing page (placeholder)
```

## Deployment

Designed for static hosting: GitHub Pages, Cloudflare Pages, or any CDN.

The scanner page fetches live scanner IPs from the Huginn platform API at runtime (`GET /api/v1/scanner-ips`). Update `API_BASE` in `scanner/index.html` if the platform runs on a different domain.

## DNS

- `meethuginn.com` — points to this site
- `scanner-*.sensors.meethuginn.com` — rDNS on sensor IPs, resolves to this site
