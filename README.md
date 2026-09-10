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
- Name: Savva / سافا, real logo wordmark ("SAVVA COFFEE") seen on cups in the
  café's own photos
- Address: Zubairah Al Roumiah, Bir Uthman, Madinah 42331, Saudi Arabia
- Instagram: `@savva_cafe` — bio: *"Specialty coffee ☕️ Saudi Arabia, madinah
  📍 'A day in savva is what you need to be savva'"*
- TikTok: `@savva_cafe` (exists, referenced by third-party "best cafes in
  Madinah" videos)
- Category: specialty coffee café, indoor **and** outdoor seating, children
  allowed, music present
- **Menu — real items**, from the client's own Instagram post/highlight
  screenshots (cropped into `img/`, app UI removed): Ice Hibiscus, Matcha
  Berry, Melon, Freddo, Blueberry Cheesecake, Cinnabon Danish, Madini
  Cookies, Kunafa. "Chocolate Caramel Cake" is our own descriptive label —
  the photo is real but no name was given for it anywhere.
- **Brand color** — the dark theme's green (`#2A331E` family) was sampled
  from the actual cup/logo color in the client's photos, not invented.

**Not confirmed — placeholders, do not treat as final:**
- Opening hours ("Daily · 5:00 PM – 12:00 AM") — from a third-party Arabic
  directory only, never confirmed against Google's own listing
- Phone / WhatsApp number — none found anywhere; footer shows "coming soon"
- Google's star rating and review count — the Maps page never rendered for
  us; nothing to quote
- **Prices** — not one price appears anywhere in any source material
  (Instagram, TikTok, Maps, directories). Every menu card intentionally
  shows no price; the hero's floating card says "Ask in-café for pricing."
  Do not add prices without getting them from the café directly.
- Typography (Baloo 2 / Baloo Bhaijaan 2) approximates the real logo's
  rounded "bubble-letter" look — it is not the café's actual brand font
  (we don't have that file).

**Do not launch this site publicly until hours, phone number, and prices are
confirmed by the café.**

## Third-party assets

- `anim/deliveryman-scooter.json` — "Deliveryman Riding scooter" Lottie
  animation by **nanoagency**, via [IconScout](https://iconscout.com/lottie-animations/deliveryman-riding-scooter).
  Downloaded by the client and used with on-page attribution in the Visit
  section (per IconScout's free-with-attribution license). Rendered with the
  `lottie-web` library, loaded from cdnjs.

## Editing content

Everything — copy, menu list, address, hours — lives inside `index.html`:
- `STRINGS` (near the top of the `<script>`) holds every UI string in both
  `en` and `ar`.
- `MENU_ITEMS` holds the menu cards (category, photo path, name/description
  keys) shown in the tabbed "Menu" section — photos live in `img/`.
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
