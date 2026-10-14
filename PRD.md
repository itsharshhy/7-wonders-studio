# PRD — 7 Wonders Studio Website

| | |
|---|---|
| **Client** | 7 Wonders Studio — Unisex Salon |
| **Location** | Shop No. 4, Ground Floor, Libra Tower, Hill Road, Bandra West, Mumbai 400050 (opp. St. Stanislaus High School) |
| **Instagram** | [@7wondersstudioofficial](https://www.instagram.com/7wondersstudioofficial/) |
| **Document status** | Draft v1 — for pitch |
| **Prepared by** | Aspersh Upadhyay & Harsh Yadav |
| **Last updated** | October 2026 |

---

## 1. Background

7 Wonders Studio is a unisex hair, skin and grooming salon on Hill Road, Bandra West — one of Mumbai's most competitive salon streets (Lakmé, Jean-Claude Biguine, Shivas and A'Kreations are all within walking distance). Today the studio's online presence is Instagram plus third-party listings (Justdial, aggregators). It has no website of its own, so:

- People who search "salon Bandra West" land on aggregator pages that also list competitors.
- There is no single place that shows services, location, hours and a way to book.
- The brand's look is set by whatever a listing site shows, not by the studio.

## 2. Goal

Give 7 Wonders a premium, minimal website that makes it look like the best salon on Hill Road, and turns visitors into booked appointments.

### Success metrics (first 90 days after launch)

| Metric | Target |
|---|---|
| Booking requests (WhatsApp / form) from the website | 30+ per month |
| "Get directions" and "Call" taps | Tracked and growing month on month |
| Google Business Profile → website clicks | Tracked from week 1 |
| Mobile Lighthouse performance score | ≥ 90 |
| Ranking for "unisex salon Bandra West" / "salon Hill Road Bandra" | Page 1 on Google |

## 3. Audience

1. **Bandra & Khar locals (25–45)** — want a reliable regular stylist nearby. Need: services, prices, easy booking.
2. **Brides and occasion clients** — planning ahead, compare portfolios. Need: work samples, trust, a consultation.
3. **Men's grooming clients** — want sharp cuts and beard work without a "ladies parlour" feel. Need: clear "for him" positioning.
4. **Walk-by / new-to-area** — found it on Google Maps. Need: hours, phone, directions in one tap.

## 4. Brand & design direction

- **Feel:** minimal, editorial, quietly luxurious. References: *M/Coupe* (giant wordmark, black-and-white photography) and *Lumière* (split hero, serif headline with an italic accent word).
- **Concept — "The Seven Wonders":** the menu is organised as seven signature disciplines, numbered I–VII. This turns the name into the structure of the site and is easy to remember.
- **Typography:**
  - Display / wordmark — *Italiana* (thin, high-contrast caps)
  - Headlines — *Cormorant Garamond*, with italic rose-taupe accent words
  - Body & labels — *Jost* (geometric, spaced uppercase labels)
- **Colour modes:** three switchable modes — Warm (bone `#F5F3EF`, default), Light (gallery white `#FFFFFF`) and Dark (ink `#121110`) — sharing a rose-taupe accent. The visitor's choice is remembered.
- **Photography:** black-and-white or desaturated, real studio and client work. Stock photos in the demo are placeholders only.

## 5. Scope

### Phase 1 — Demo landing page (this repo, done)
Single page used to pitch the client.

| Section | Content |
|---|---|
| Header | Monogram, nav (Services, Studio, Journal, Visit), "Book a visit" button, mobile menu |
| Hero | "Seven ways to feel wonderful." + intro, 2 CTAs, 3 quick facts, portrait photo with address card |
| Wordmark band | Full-width studio photo + giant "7 / WONDERS" wordmark |
| The Seven Wonders | I Cut & Style · II Colour · III Hair Rituals · IV Skin · V Hands & Feet · VI Grooming · VII Occasion & Bridal |
| Studio | About copy + Consult → Craft → Care process |
| Promise | Full-width quote band |
| Journal | 4-tile Instagram grid + follow link |
| Visit & Book | Address, landmark, hours, phone, directions; booking form that opens a pre-filled WhatsApp message |
| Footer | Wordmark, location, Instagram |

### Phase 2 — Full website (v1 launch)

**Pages:** Home · Services & Prices · Bridal · Gallery · About / Team · Contact · Privacy

**Features (must-have):**
1. Full service menu with starting prices, durations and gender filter (Him / Her / All).
2. Booking — WhatsApp booking (launch) → upgrade to real online booking (calendar slots, stylist choice, SMS/WhatsApp confirmations).
3. Click-to-call, click-to-WhatsApp and Google Maps on every page (sticky mobile bar).
4. Gallery of real before/after work, filterable by service.
5. Team page — stylists with speciality and photo.
6. Google reviews pulled onto the site (rating + latest reviews).
7. Local SEO: `HairSalon` / `LocalBusiness` schema, Google Business Profile link, Bandra-focused page titles and copy.
8. Analytics: GA4 + events for book, call, WhatsApp, directions.

**Nice-to-have (Phase 3):**
- Bridal enquiry form with date and function details.
- Gift cards / packages (e.g., "Pre-wedding package", "Monthly grooming").
- Offers & seasonal campaigns page (Diwali, wedding season).
- Membership / loyalty ("7th visit on us" — ties to the name).
- Instagram feed embed that auto-updates.
- Hindi / Marathi language toggle.
- Retail product shop.

### Out of scope (v1)
Payments, customer accounts, POS / inventory integration.

## 6. Functional requirements

| ID | Requirement | Priority |
|---|---|---|
| F1 | Every page shows a booking action within one tap on mobile | Must |
| F2 | Booking form validates name + phone, then hands off to WhatsApp with a pre-filled message | Must |
| F3 | Services data lives in one editable file / CMS so the owner can update prices | Must |
| F4 | Address links open Google Maps; phone links open the dialler | Must |
| F5 | Gallery images lazy-load and are served as WebP/AVIF | Must |
| F6 | Owner can change hours, offers and photos without a developer | Should (CMS) |
| F7 | Online slot booking with confirmations | Could (Phase 3) |

## 7. Non-functional requirements

- **Performance:** LCP < 2.5s on 4G; total page weight < 1.5 MB on first load.
- **Responsive:** designed mobile-first — most salon traffic in India is on phones.
- **Accessibility:** WCAG 2.1 AA contrast, keyboard navigation, alt text, reduced-motion support.
- **SEO:** semantic HTML, meta + Open Graph tags, sitemap, `LocalBusiness` structured data.
- **Hosting:** Vercel or Netlify (free/low-cost tier), custom domain with HTTPS.
- **Theme:** light + dark mode.

## 8. Recommended tech stack (Phase 2)

| Layer | Choice | Why |
|---|---|---|
| Framework | Next.js (or Astro) | Fast static pages, great SEO, easy to grow |
| Styling | Tailwind CSS or plain CSS with the tokens in this demo | Keeps the design system consistent |
| CMS | Sanity or Decap CMS | Owner edits services, prices, gallery |
| Booking | WhatsApp → later Fresha / Zenoti / custom (Supabase) | Start simple, upgrade when volume justifies it |
| Hosting | Vercel | Free tier, instant deploys from GitHub |
| Analytics | GA4 + Vercel Analytics | Track bookings and calls |

## 9. Content needed from the client

- [ ] Correct brand name usage ("7 Wonders Studio" vs "7 Wonder Studio")
- [ ] Logo files (vector if available)
- [ ] Phone / WhatsApp number
- [ ] Opening hours (and weekly off, if any)
- [ ] Full service list with starting prices
- [ ] 15–30 high-resolution photos: studio interior, team, client work (or permission to use Instagram posts)
- [ ] Team names, roles, specialities
- [ ] Year founded, story, anything that sets them apart (products used, certifications)
- [ ] Google Business Profile access (for reviews + SEO)
- [ ] Domain preference (e.g., `7wondersstudio.in`)

## 10. Timeline (Phase 2)

| Week | Milestone |
|---|---|
| 1 | Kick-off, content collection, sitemap sign-off |
| 2 | Design of all pages (desktop + mobile) |
| 3–4 | Build, CMS setup, content entry |
| 5 | QA, SEO setup, analytics, client review |
| 6 | Launch + handover training |

## 11. Open questions

1. Do they want online payments / deposits for bridal bookings?
2. Do they already use salon software (Zenoti, Fresha, Salonist) we should integrate with?
3. Is there a second location planned?
4. Who will update the site — owner, front desk, or us on a retainer?
