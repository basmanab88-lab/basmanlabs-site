# basmanlabs-site

Static brand-level site for **basmanlabs.com** — hosts the homepage, privacy policy, and terms of service that are required for Google OAuth verification of all Basman Labs products.

## Files

- `index.html` — brand landing page
- `privacy.html` — privacy policy (shared across all products)
- `terms.html` — terms of service (shared across all products)
- `demo-video-script.md` — script for the HandyMan OAuth demo video

## Deploy

1. Create new Vercel project pointing to this folder
2. Vercel auto-detects static site — no build step
3. Set custom domain: `basmanlabs.com` (+ `www.basmanlabs.com`)
4. Point DNS at Vercel (automatic instructions in Vercel dashboard)

## Subdomains for individual products

- `handyman.basmanlabs.com` → existing `handyman/web` Vercel deployment (update that project's custom domain)
- `t-800.basmanlabs.com` → existing `t-800` Vercel deployment (optional)
- Future: `crm.basmanlabs.com`, etc.

## Google OAuth verification checklist

For each product that uses Google OAuth:

1. ✅ Homepage public at a `basmanlabs.com` URL
2. ✅ Privacy policy at `basmanlabs.com/privacy.html`
3. ✅ ToS at `basmanlabs.com/terms.html`
4. ✅ Verify domain in Google Search Console (one-time, covers all subdomains)
5. ⬜ Record demo video per `demo-video-script.md`, upload to YouTube Unlisted
6. ⬜ Submit OAuth verification in Google Cloud Console
