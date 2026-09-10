# Savva — Website

A bilingual (English / Arabic, full RTL) one-page site for **Savva** (سافا), a
specialty coffee house in Madinah, Saudi Arabia. Single self-contained
`index.html` — no build step, no framework.

## What's real vs. placeholder

Built from two sources only: a Google Maps pin and the `@savva_cafe`
Instagram profile. Both were hard to verify directly (the Maps page needs a
browser to render, Instagram blocks unauthenticated scraping), so this list
is intentionally conservative.

**Confirmed:**
- Name: Savva / سافا
- Address: Zubairah Al Roumiah, Bir Uthman, Madinah 42331, Saudi Arabia
- Instagram: `@savva_cafe` — bio: *"Specialty coffee ☕️ Saudi Arabia, madinah
  📍 'A day in savva is what you need to be savva'"*
- TikTok: `@savva_cafe` (exists, referenced by third-party "best cafes in
  Madinah" videos)
- Category: specialty coffee café, indoor **and** outdoor seating, children
  allowed, music present

**Not confirmed — placeholders, do not treat as final:**
- Opening hours ("Daily · 5:00 PM – 12:00 AM") — from a third-party Arabic
  directory only, never confirmed against Google's own listing
- Phone / WhatsApp number — none found anywhere; footer shows "coming soon"
- Google's star rating and review count — the Maps page never rendered for
  us; nothing to quote
- All menu items and every price — no real menu was available. The Menu
  section lists **generic, universally-safe specialty-coffee drink names**
  (Espresso, Cappuccino, Cold Brew, Mango Smoothie, etc.) with no prices
  attached — not Savva's actual named items
- Interior style, brand colors, and every visual in the "Atmosphere" section
  — the whole visual identity (dark espresso palette, gold accent, canvas
  particle animation, gradient "mood" panels) is our own proposed design,
  not derived from any real branding or photo

**Do not launch this site publicly until hours, phone number, and menu are
confirmed by the café.**

## Editing content

Everything — copy, drink list, address, hours — lives inside `index.html`:
- `STRINGS` (near the top of the `<script>`) holds every UI string in both
  `en` and `ar`.
- `DRINKS` holds the drinks-menu items (category, icon, name/description
  keys) shown in the tabbed "Menu" section.
- `MAPS_URL` is the one Google Maps link used by both "Get Directions"
  buttons.

## Sources used during research

- https://www.instagram.com/savva_cafe/
- https://www.tiktok.com/@savva_cafe
- https://venuewise.com/venue/savva-cafe-madinah/cafe
- https://experiencemedina.com/سافا-كافيه-المدينة/ (fetch failed; hours came
  from a search-engine summary of this page only, not a direct quote)
- Google Maps pin given by the client (never successfully rendered by our
  tooling — someone should open it directly to confirm rating/hours/phone)

## Running it

Just open `index.html` in a browser. No install, no build.
