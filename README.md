# Gikomba Plug — website

Gikomba outfits & mitumba shoes, Nairobi. Order on WhatsApp, pay with M-Pesa.

The whole site is one file, `site/index.html`. No build step. **Only `site/` is published** (see `wrangler.jsonc`); it is served at the root of the domain.

## Before going live

These are still placeholders in `site/index.html`. Every order button is dead until they're filled:

| What | Where | Placeholder |
|---|---|---|
| WhatsApp number | `CONFIG.whatsappNumber` and the JSON-LD `telephone` | `2547XXXXXXXX` |
| M-Pesa till / paybill | `CONFIG.mpesa.number` | `XXXXXX` |
| Domain | canonical, `og:url`, `og:image`, JSON-LD | `yourdomain.co.ke` |
| Share image | `og:image` | `assets/img/og-image.jpg` (file doesn't exist yet; add it under `site/`) |
| Product photos | `PRODUCTS` (or the Google Sheet) | Unsplash stock — replace with photos of the actual items |
| Instagram / TikTok | `CONFIG.instagram`, `CONFIG.tiktok` | `@gikombaplug` — confirm the handles are claimed |

## Hosting

Cloudflare Workers static assets, connected to this repo. Once connected, every merge to `main` goes live in about a minute.
