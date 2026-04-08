# Giancarlo Banchi — PM Portfolio Site

## 1. Site Vision

A refined, editorial portfolio website for Giancarlo Banchi, a Milan-based project manager. Minimal, typographically-driven design influenced by architectural practice. Warm parchment tones, structured layouts, navy accents. Communicates precision and credibility without flash.

## 2. Stitch Project ID

_Not yet created — run Stitch to generate the first screen and populate `.stitch/metadata.json`._

## 3. Tech Stack

- Static HTML/CSS/JS — no framework
- Google Fonts: Cormorant Garamond + Jost
- Deployed on Vercel (see `.vercel/project.json`)
- No build step — files served directly from root

## 4. Sitemap

| Page | File | Status |
|------|------|--------|
| Home | `index.html` | [x] Built |
| Archive | `archive.html` | [x] Built |
| About | `about.html` | [x] Built |
| Contact | `contact.html` | [x] Built |

## 5. Roadmap

_All core pages are complete. Items below are enhancements for future iterations:_

- [ ] Case study detail page (`case-study.html`) — deep-dive on a single project
- [ ] Services page — explicit breakdown of PM engagement types and pricing
- [ ] Print/PDF CV download integration

## 6. Creative Freedom

Ideas for future Stitch-generated screens:

- **Case Study Template** — full-page project deep-dive: hero banner, challenge/approach/outcome sections, metrics, team credits
- **Services Page** — three-column engagement model breakdown with scope, timeline, and pricing tiers
- **Process Page** — visual walkthrough of Giancarlo's PM methodology (phases, tools, deliverables)
- **404 Page** — on-brand error page with navigation back to home
- **Thank You / Confirmation** — post-contact submission state page

## 7. Navigation Structure

```
Home (index.html)
├── Archive (archive.html)
├── About (about.html)
└── Contact (contact.html)
```

All pages share the same fixed top nav. Active page is indicated with a navy underline `::after` element.
