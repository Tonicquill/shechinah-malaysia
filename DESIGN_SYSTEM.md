# Shechinah Malaysia — Design System

> Built for single-file static site. All tokens defined as CSS custom properties.
> Date: 2026-05-07

## Color Palette

```css
--green: #669F38;       /* Signature — life, growth, programme identity */
--green-deep: #4A7A28;  /* Hover states, depth */
--gold: #F9A107;        /* CTA emphasis — action, hope, urgency */
--gold-deep: #D48900;   /* CTA hover */
--cream: #F4EEE6;       /* Warmth — quote blocks, founder section sparingly */
--ink: #111827;         /* Primary text, dark sections */
--ink-soft: #1F2937;    /* Secondary text, footer background */
--gray: #6B7280;        /* Body text */
--gray-light: #9CA3AF;  /* Labels, muted */
--gray-border: #E5E7EB; /* Borders, dividers */
--gray-bg: #F9FAFB;     /* Alt backgrounds */
--white: #FFFFFF;        /* Base */
```

**Rule:** Gold only for CTAs. Cream only for human-story blocks. Green is the through-line.

## Typography

| Role | Font | Weight | Size | Line-height | Letter-spacing |
|------|------|--------|------|-------------|----------------|
| Hero headline | Satoshi | 900 Black | clamp(44px, 7vw, 80px) | 0.98 | -0.035em |
| Section title | Satoshi | 700 Bold | clamp(30px, 4vw, 44px) | 1.1 | -0.02em |
| Card title | Satoshi | 800 ExtraBold | 16-20px | 1.2 | 0 |
| Body | System sans | 400 | 15-17px | 1.65-1.75 | 0 |
| Labels / Badges | Satoshi | 700 Bold | 10-12px | 1 | 0.1-0.2em (uppercase) |
| Stats numbers | Satoshi | 900 Black | 28-44px | 1 | -0.025em |
| Quotes | Satoshi | 500 Medium | 20-26px | 1.5 | 0 (italic) |
| Nav / Links | Satoshi | 500 Medium | 13-14px | 1 | 0 |

**Font stack:** `'Satoshi', -apple-system, BlinkMacSystemFont, sans-serif` for display
**Body fallback:** `-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif`
**Source:** `https://api.fontshare.com/v2/css?f[]=satoshi@900,700,500,400&display=swap`

## Spacing Scale

8px-based system. Common values:
- `4px` — tight gaps, icon-to-text
- `8px` — inline gaps
- `10px` — bento grid gap
- `14-16px` — button gaps
- `20-24px` — element bottom margins
- `28-36px` — headline bottom margins
- `40-48px` — stat gaps, section padding (mobile)
- `56-64px` — section padding
- `80-100px` — section padding (desktop)

## Layout

- **Max content width:** 1280px (container class)
- **Hero:** Full viewport, no max-width
- **Timeline:** Max 720px (readable line length)
- **Padding:** 40px sides desktop, 20px mobile
- **Grid:**
  - Ministries bento: `1.4fr 1fr 1fr`
  - Media: `repeat(3, 1fr)`
  - About: `1fr 1fr`
  - Footer: `2fr 1fr 1fr 1fr`

## Components

### Buttons
- Base: `padding: 15px 36px; border-radius: 10px; font-weight: 700`
- Primary: gold bg + ink text → gold-deep hover + lift + glow shadow
- Outline: white border 30% opacity + white text → full white hover
- Green: green bg + white text → deep green hover + lift + green glow
- Active: `scale(0.97)` press effect

### Cards
- Default: white bg, 1px #F3F4F6 border, 14px radius
- Hover: subtle shadow + darker border
- Featured (flagship): no border, green-tinted bg, photo + overlay content

### Dividers
- Batik SVG: 48px height, 12% opacity, green + gold paths
- Wave pattern using Q-bezier curves
- Diamond pattern variant for variety

## Motion

| Element | Method | Timing |
|---------|--------|--------|
| Scroll reveal | Intersection Observer + CSS transition | 0.8s cubic-bezier(0.16,1,0.3,1) |
| Stagger cascade | transition-delay increments (0.1s × n) | Up to 0.5s total |
| Counter animate | requestAnimationFrame with easeOutCubic | 2s duration |
| Button hover | transform + box-shadow transition | 0.25s cubic-bezier(0.16,1,0.3,1) |
| Nav border | transition on scroll class toggle | 0.3s |
| Scroll indicator | CSS keyframes infinite bounce | 2s loop |

## Responsive Breakpoints

- **768px:** Stack grids to single column, reduce type sizes, collapse padding
- **1024px:** Adjust hero content padding
- **Mobile nav:** Links hidden (future: hamburger menu)

## Divider Variants

3 unique batik-inspired patterns rotate between sections:
1. Double wave (green main + gold accent)
2. Diamond dash pattern
3. Single wave with staggered gold highlights

Each 48px tall, 12% opacity, purely decorative (aria-hidden).
