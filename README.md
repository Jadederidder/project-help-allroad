# project-help-allroad

Public marketing page for the **All Road Premium Bundle** — Volkswagen Financial Services South Africa's embedded armed response, medical, licence, fines and RAF service operated by Project Help (Pty) Ltd.

**Live:** https://allroad.projecthelp.co.za

## Stack

Single-file static site, no build process. Same pattern as `project-help-vw-sales` and `auto-pedigree-dashboard`.

```
docs/
  index.html          single self-contained HTML (CSS + JS inline)
  img/                product images and lifestyle photography
  CNAME               allroad.projecthelp.co.za
.github/workflows/
  deploy_pages.yml    GitHub Pages deploy (push to main on docs/**, or manual)
```

GitHub Pages source is set to **GitHub Actions** (not "Deploy from a branch"). The deploy workflow auto-fires on any push to `main` that touches `docs/**`, and can be manually triggered via `gh workflow run deploy_pages.yml --ref main`.

## Content updates

To update copy or pricing:

1. Edit `docs/index.html` directly. All content is in one file.
2. Push to `main`. Pages rebuild fires automatically; live within 1–2 minutes.

To swap or add images:

1. Drop the new asset into `docs/img/` (web-optimized — JPEG for photography, PNG for transparent product mockups).
2. Reference it in `index.html` via `<img src="img/your-asset.jpg" alt="...">`.

## DNS

`allroad.projecthelp.co.za` CNAME → `jadederidder.github.io` (set at the registrar before Pages will validate the custom domain).

## Brand

- **VW navy:** `#1F3864` (primary)
- **Brochure red:** `#D93832` (accents on key words like "Help", "Armed")
- **Silver bg:** `#F5F6F8`
- **Display font:** Bricolage Grotesque
- **Body font:** Manrope

Both fonts loaded from Google Fonts.

## Service contact details (in footer)

- Membership Administration: **010 597 0855** / `allroad@projecthelp.co.za`
- RAF Claims Hotline: **010 012 6402** (Mon–Fri 08:30–16:30)

## App links

- App Store: https://apps.apple.com/za/app/premium-help/id6747082773
- Google Play: https://play.google.com/store/apps/details?id=com.zqpremiumhelp&hl=en
