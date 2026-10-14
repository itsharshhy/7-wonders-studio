# 7 Wonders Studio — Website

Demo landing page for **7 Wonders Studio**, a unisex salon on Hill Road, Bandra West, Mumbai.
Minimal, editorial, luxury direction — built to pitch the full website to the client.

**Live demo:** https://7-wonders-studio-hiharshhyadav-4472.vercel.app

## What's here
```
index.html      → the landing page (HTML + CSS + JS in one file, no build step)
docs/PRD.md     → product requirements for the full website
docs/PITCH.md   → how to present it to the client, packages, objections
```

## Run it
Open `index.html` in a browser. That's it.

Or serve it locally:
```bash
npx serve .
```

## Deploy (free)
- **Vercel:** `npx vercel` in this folder, or import the GitHub repo at vercel.com/new.
- **GitHub Pages:** Repo → Settings → Pages → Deploy from branch `main`, folder `/`.

## Placeholders to replace before showing the client
| Where | What |
|---|---|
| `index.html` → `WHATSAPP_NUMBER` | Studio's WhatsApp number (digits only, with 91) |
| `index.html` → Visit section | Phone number and opening hours (marked `TODO`) |
| All `<img>` tags | Free-licence Unsplash demo photos → swap for real studio / Instagram photos |

Photos show in black and white and turn to colour on hover. If an image fails to load, the frame shows a designed fallback, so the page never looks broken.

## Design system
- **Fonts:** Italiana (wordmark), Cormorant Garamond (headlines), Jost (body/labels) — Google Fonts
- **Three colour modes** (switcher in the header, choice is remembered):
  - **Warm** (default) — bone `#F5F3EF`, ink `#171514`, accent `#9E776B`
  - **Light** — gallery white `#FFFFFF`, ink `#0E0E0E`, accent `#8C6A60`
  - **Dark** — ink `#121110`, bone text `#EEE9E2`, accent `#C9A093`
- Responsive down to 360px, respects reduced motion.

## Credits
Concept, design and build by [Aspersh Upadhyay](https://github.com/aspershupadhyay) & Harsh Yadav.

## Next
See `docs/PRD.md` — Phase 2 moves this to Next.js/Astro with a CMS, gallery, prices and online booking.
