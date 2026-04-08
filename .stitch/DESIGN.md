# Design System — Giancarlo Banchi Portfolio

## 1. Identity

**Brand:** Giancarlo Banchi | PM Portfolio
**Voice:** Refined, precise, architectural. Confidence without noise.
**Aesthetic:** Editorial European portfolio — warm paper tones, structured typography, restrained detail.

---

## 2. Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| `--bg` | `#F4F1EB` | Page background — warm off-white/parchment |
| `--ink` | `#1A1917` | Primary text — near-black |
| `--ink-mid` | `#504E4B` | Body text, secondary labels |
| `--ink-light` | `#9A958F` | Captions, section labels, metadata |
| `--accent` | `#1D3557` | Navy — CTAs, active states, highlights |
| `--rule` | `#D8D3CB` | Dividers, borders, card outlines |
| `--white` | `#FDFCFA` | High-contrast backgrounds, buttons |
| `--hover-bg` | `#EDE9E2` | Row/card hover state |

---

## 3. Typography

| Role | Font | Spec |
|------|------|------|
| Display / Headings | Cormorant Garamond | Serif — weights 400 (italic) + 600. Used for names, section titles, hero text |
| Body / UI | Jost | Sans-serif — weights 300 (body), 400, 500. Used for nav, labels, paragraphs |

**Type scale:**
- Hero: `clamp(4rem, 11vw, 9.5rem)` — Cormorant 600
- Page title: `clamp(3.5rem, 9vw, 7.5rem)` — Cormorant 600
- Section heading: `clamp(1.8rem, 3.5vw, 2.8rem)` — Cormorant 600
- Card title: `1.35–1.5rem` — Cormorant 600
- Body: `0.88–0.92rem` — Jost 300, line-height 1.65–1.75
- Labels/caps: `0.62–0.72rem` — Jost 500, letter-spacing 0.14–0.2em, UPPERCASE

---

## 4. Layout Principles

- **Max width:** `1180px`, centered
- **Padding:** `clamp(1.25rem, 4vw, 2.5rem)` — fluid horizontal padding
- **Nav height:** `60px` — fixed top bar
- **Grid:** 1-column default; 2-column for about/contact panels; auto-fit cards for expertise
- **Borders as structure:** 1px `var(--rule)` lines define sections. No card shadows — borders only.
- **Vertical rhythm:** Sections padded `5–6rem` top/bottom, separated by `border-bottom`

---

## 5. Components

### Navigation
Fixed top bar, `60px` height. Logo (Cormorant 600, 1.05rem) left. Links right — Jost 500, 0.7rem, uppercase, 0.14em tracking. Active state: underline via `::after` pseudo-element in `--accent`.

### Buttons
- Primary: `background: var(--accent)`, white text, 1px border — hover inverts to transparent
- Secondary: transparent, `--ink-mid` text, `--rule` border — hover fills `--hover-bg`
- Padding: `0.75–0.8rem 1.6–1.8rem`. Font: Jost 500, 0.72rem, uppercase, 0.14em tracking.

### Section Labels
`0.65rem` Jost 500, uppercase, `0.2em` tracking, `--ink-light`. Followed by `::after` line (`max-width: 120px`, `--rule`). Pattern: `01 — Label Name`

### Cards / Grid
- Outlined grid with `border: 1px solid var(--rule)` wrapping cards
- Cards separated by inner borders (right + bottom)
- Number in top-left (`--ink-light`, 0.65rem)
- Hover: `background: var(--hover-bg)`

### Table Rows (Archive)
- Full-width list rows, `border-top/bottom: 1px solid var(--rule)`
- Hover: negative horizontal margin expansion + `--hover-bg`
- Columns: number / project info / client / status / year

### Status Pills
- `0.6rem` Jost 500, uppercase, 1px border
- `in-progress`: `--accent` color and border
- `completed`: `--ink-mid` color, `--rule` border

### Footer
Flex row, space-between. Logo (Cormorant) left, link list right. `--ink-light` links, hover to `--ink`.

---

## 6. Design System Notes for Stitch Generation

**USE THIS BLOCK IN EVERY STITCH PROMPT:**

```
Design system: editorial European portfolio.
Background: warm parchment #F4F1EB. Text: near-black #1A1917.
Accent color: navy #1D3557 for CTAs and highlights.
Dividers: 1px lines in #D8D3CB — no shadows, borders only.
Typography: Cormorant Garamond (serif, large display) + Jost (sans, UI/body).
Hero and page titles in large Cormorant Garamond italic+bold.
Labels: tiny uppercase Jost with wide letter-spacing.
Layout: structured, grid-based, generous whitespace.
Hover states: light warm fill #EDE9E2.
Fixed top nav, 60px, with logo left and links right.
Buttons: navy filled (primary) or transparent outlined (secondary).
Overall mood: refined, precise, architectural — not flashy.
```

---

## 7. Animation

- `fadeUp`: opacity 0→1, translateY 12–16px→0, 0.6–0.7s ease, staggered delays (0.2–0.55s)
- `fadeIn`: opacity 0→1, 0.5–0.6s
- Scroll reveal: IntersectionObserver adds `.visible` class, opacity/translateY transition 0.6s
- Pulse: availability dot glow, 2s infinite
