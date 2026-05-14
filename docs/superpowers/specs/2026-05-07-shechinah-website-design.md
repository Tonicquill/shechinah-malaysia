# Shechinah JB Website — Design Spec

> Date: 2026-05-07
> Status: Approved, built
> Source: Original WordPress site (Wayback Machine) + Kimi prototype + 2024-2025 news research

## Architecture

Single-file static HTML + inline CSS. No framework, no build step, no JavaScript dependency beyond vanilla DOM APIs. Served as static file. Follows loheksem pattern.

**File:** `index.html` — complete self-contained site

**Font delivery:** Satoshi from CDN (api.fontshare.com), falls back to system sans stack

## Section Map

1. **Nav** — Fixed, backdrop-blur, transparent border → solid on scroll. Logo + 4 links + Donate CTA
2. **Hero** — Full-bleed dark gradient background + overlay. Centered text: "Giving Hope, Restoring Dignity" with green/gold/white color spans. Subtext, dual CTAs, 4-stat strip embedded at bottom. Scroll indicator arrow
3. **Ministries** — Asymmetric bento grid (1.4fr 1fr 1fr). Halfway House flagship spans 2 rows with photo placeholder. 4 other programmes in clean bordered cards
4. **Quote Block** — Cream background. James Issachar's real words from The Star (Sep 2025) as pull-quote with attribution
5. **About / Founder** — 2-column: photo placeholder + text about James, 10+ years, registration details, The Star coverage
6. **Timeline** — Vertical line timeline, 7 milestones 2018-2026 with green dots and dates
7. **Media** — 3-column grid: The Star Sep 2025, Community Spotlight Dec 2025, Local Press Jan 2024
8. **Donate CTA** — Dark full-width section, gold accent label, big headline, dual CTAs
9. **Footer** — 4-column grid: brand + programmes + connect + support. Copyright bar

Between major sections: batik-inspired geometric SVG dividers (Malaysian identity, subtle)

## Design Direction: Modern Movement × Malaysian Soul

- **Font:** Satoshi single family, weight-driven hierarchy (900/700/500/400)
- **Base:** White-dominant, cream only for quote block
- **Hero:** Full-bleed cinematic, text over dark overlay
- **Color:** Olive green #669F38 (signature), gold #F9A107 (CTA emphasis), ink #111827 (text), cream #F4EEE6 (warmth sparingly)
- **Layout:** Anti-generic — no 3 equal cards, no centered CTAs in body sections, asymmetric grids
- **Texture:** Batik-inspired SVG patterns between sections
- **Quotes:** Real James Issachar quotes with publication attribution

## Anti-Generic Rules Applied

1. No 3 equal cards — asymmetric bento grid, flagship 2× tile
2. No Inter/Roboto/Poppins — Satoshi only, weight-driven
3. No purple/neon/dark mode — white base, green signature, gold CTA
4. No emoji icons — geometric SVG dividers + real photos (when available)
5. Hero not centered-on-white — cinematic full-bleed with overlay
6. Real quotes from The Star with attribution
7. Stats embedded in hero, not generic card strip
8. Batik-inspired geometric dividers for Malaysian identity

## Content Sources

- Original WordPress site via Wayback Machine (Dec 2024 snapshot)
- The Star coverage (Sep 2025, Dec 2025)
- Community news (flood relief Jan 2024, Wesak outreach May 2024)
- Kimi prototype for structure reference

## Image Strategy

Currently using honest gray placeholders with text labels. Real Shechinah photography needed:
- Hero background: James with Halfway House residents
- Halfway House tile: Taman Rinting shelter
- About section: James Issachar portrait
- Media cards: publication mastheads

Placeholders are intentional — honest > fake. Replace when real photos sourced.

## Technical

- CSS custom properties for all design tokens
- Intersection Observer for scroll reveals (no framework)
- requestAnimationFrame for counter animations
- CSS-only animations (transitions, keyframes)
- Mobile-responsive: stacked layouts, smaller type, adjusted spacing
- nav-height CSS variable for scroll offset calculations
- Backdrop-filter for nav glass effect

## Next Steps

1. Source real photography from James / Shechinah archives
2. Add actual donation link/URL
3. Add social media links
4. Consider Malay language version
5. Add contact form section
