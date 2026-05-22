# Milo Madolora — Portfolio (Issue I)

Single-file editorial portfolio at `index.html`, deployed to GitHub Pages at https://milomadatu.github.io/.

## Stack

- Vanilla HTML + inline `<style>`. No build step, no JS framework.
- Google Fonts CDN: **Playfair Display** (headlines, italics) + **Inter** (body, labels).
- Static assets:
  - `index.html` — entire site
  - `favicon.svg`
  - `LMAClassof2026Website.png` — screenshot for the Web section
  - `photos/` — JPGs used in the Photography section
  - `projects/lma/` and `projects/ivc/` — coursework PDFs (+ one `.pptx`, one `.xlsx`)
- Deployed via GitHub Pages from `main` branch. No CI; pushes auto-deploy in 30–60s.

## Design system

Color tokens (declared as CSS custom properties on `:root`):
- `--paper: #f6f2ea` — page background (cream)
- `--ink: #111111` — primary text
- `--ink-soft: #3a3a3a` — secondary text
- `--muted: #6b6660` — captions, kickers, micro-labels
- `--accent: #8a1c1c` — drop caps, section numbers, hover, pullquote drop cap
- `--rule: #111111` — horizontal rules

Typography:
- Headlines / italic pullquotes: Playfair Display, 700–900
- Body / micro-labels (uppercase): Inter, 400–600
- Drop cap on `.lede::first-letter` for editorial feel

Layout:
- Single `.wrap` container, max-width 1200px, side padding 32px (20px on mobile)
- Sections are numbered `00`–`06` (About → Contact), then a Colophon back-matter block
- Each `.section-head` is a grid: section-num (Playfair italic, accent) + kicker (uppercase Inter) + section-title (Playfair 700)
- Two-column body via `.two-col` (1fr 2fr): a lede on the left, two-column prose (`.columns`) on the right

Tile grid (used in Video and Photography sections):
- 12-column grid (`.tiles { display: grid; grid-template-columns: repeat(12, 1fr); }`)
- Span helpers: `.span-4 / .span-6 / .span-8 / .span-12`
- Aspect helpers: `.tile-wide` (16:9), `.tile-tall` (3:4), `.tile-natural` (image's own ratio)
- Tile images use `position: absolute; object-fit: cover` to fill the aspect-constrained tile

## Content conventions

- **Voice**: third-person lede ("Milo Madolora grew up..."), first-person columns ("I was always surrounded by culture..."). The lede always uses third person; the column paragraphs always use first person. Keep this split.
- **Placeholders**: `<span class="todo">[...]</span>` (yellow highlight in browser, monospace). One remains in the file — see "Open follow-ups" below.
- **External links**: `target="_blank" rel="noopener"`. Display label first, URL implicit.
- **Captions**: `<strong>Title</strong> &mdash; descriptive line.` Don't put a period inside the `<strong>`.
- **Pull-quote attribution**: lives inside `.by` span which uppercase-transforms via CSS.

## Hard rules for writing on this site

These come from explicit corrections Milo has given. Honor them.

1. **Preserve names exactly.** Don't "fix" what looks like a typo. The pullquote in About is attributed to "LeBron Jame's favorite saying" — that is a real person Milo knows, **not** the basketball player LeBron James. Type names exactly as Milo provides them; if something looks like a typo, ask before changing.
2. **Don't overclaim authorship.** Milo did not hand-code the LMA Class of 2026 site (https://milomadatu.github.io/lma-class-of-2026). AI built the code; Milo conceived the project, curated all 101 senior bios + headshots, and shipped it. Do not use phrases like "hand-coded," "built from scratch," "wrote the frontend," or "designed in Figma" unless Milo explicitly confirms. Safe verbs: *built, shipped, made, ran, deployed, curated, organized.*
3. **Don't invent metrics.** For the Vietnamese Film Festival internship — or any real work — do not fabricate audience sizes, post counts, follower counts, or engagement numbers. If specificity needs a number, mark it as a TODO placeholder for Milo to fill in. Use scope descriptors, tool names, and verbs instead.
4. **Don't add quote transitions between sections.** They were tried, they caused awkward vertical whitespace, they were removed. Don't re-add.

## Key facts (anchors)

- **Milo Madolora** — senior at LMA, Class of 2026
- **Headed to Northeastern University**, fall 2026, studying **Business Administration**
- **From**: Irvine, CA → **To**: Boston, MA
- **Vietnamese-Filipino American family** — identity is the throughline of his creative work
- **Photo kit**: Canon G16, Nikon D3100, Leica mini II (both film and digital)
- **Video software**: Adobe Premiere
- **Emails**: madolora.m@northeastern.edu (primary), mkmadolora@gmail.com (personal)
- **Socials**: `@milomadatu` on Instagram and YouTube; `milomadatu` on GitHub; `milo-madolora` on LinkedIn

## Project / content anchors

Marketing:
- **Vietnamese Film Festival** — Summer 2025 marketing internship; pills are Brand Strategy · Social Media · Graphic Design · Content Strategy
- **Filipino Club at LMA** — founded by Milo
- **Siply** — Marketing & Branding for a student-run beverage startup
- **VitaPearls Virtual Enterprise** — Sales Representative for a healthier-boba VE
- **M&N Detailing** — branding & content for a local detailing shop

Web:
- **LMA Class of 2026 archive** at `milomadatu.github.io/lma-class-of-2026` — 101 seniors, photos + bios + class stats; framed around **Information Architecture · Editorial Direction · GitHub Pages** (not code)

Video (5 YouTube videos):
- Featured: Class of 2026 Senior Video (`iP06NzZrDZA`)
- Senior Denim Dinner (`vWTp99aXQNU`)
- Where Will I Be in 10 Years? (`XZDrVbRJ7_A`)
- The Challenger (`8n-IYu4Jq9Q`) — uses `hqdefault.jpg`, no maxres available
- Josue Guzman (`DdzFOMR6LMY`) — uses `hqdefault.jpg`, no maxres available

Photography (6 images):
- IMG_0412.jpg — Crescent Bay, 2026 (hero)
- IMG_0059.jpg — Golden hour, after a tradeshow DJ set
- IMG_0136.jpg — Karaoke night (the only portrait-orientation photo)
- DSC_0278.jpg — Backyard, blue hour
- IMG_0100.jpg — NFC Championship Watch Party, 2026 (at SoFi-ish stadium)
- IMG_0284.jpg — Senior Day, LMA Track & Field, Class of 2026

## Specific content gotchas

- **CycleBright** is a combined light + dashcam built for ebikes — not just a generic "cycling concept."
- **Miss Mia** (in the tattoos paper) is a front-office staff member at Legacy Magnet Academy.
- **"How Digital Photography is Changing the World"** is about digital cameras broadly, not smartphone cameras specifically.
- **"Wear It Forward"** = connecting one non-profit's surplus textiles with a non-profit that needs them. Not generic clothing donation.
- **"Wandering Through the Demands of Life"** = an essay built around a Spotify playlist — the songs sequenced as a narrative on the daily demands of being a person.

## Section structure (top → bottom)

| # | Section | Notes |
|---|---|---|
| Masthead | "The Portfolio · 2026 · Issue I" + identity statement | identity line is the masthead-sub italic. |
| 00 | About | third-person lede leading with cultural identity, then three first-person column paragraphs, then LeBron pullquote |
| 01 | Video | 5 clickable YouTube thumbnails (1 hero + 2×2). All open YouTube in new tab. |
| 02 | Photography | 6 images: hero + (wide + portrait) + 3 small wides |
| 03 | Marketing | VFF internship block + "On Campus & Freelance" list block |
| 04 | The Web | LMA Class of 2026 archive — IA/Editorial/Pages pills, real screenshot |
| 05 | School Projects | grouped LMA (9 items) and IVC (3 items), each with italic one-sentence description |
| 06 | Contact | two emails, social links, "Currently" line |
| Colophon | Credits · Set in · Next Issue (TBD — from Boston) | back-matter, slightly darker beige background |

## Open follow-ups

- **`[number, e.g. 20+]` placeholder** in the VFF marketing bullet — Milo asked to keep this slot open to fill in a real figure later.
- **Coursework section sort** is currently the order files were dropped in. Milo asked to be reminded that he wants it re-sorted "optimally" — possibilities: alphabetical, chronological (by term), by topic, or curated strongest-first. Ask which axis before re-sorting.

## Deployment

```bash
git add -A
git commit -m "<message>"
git push
```

Pushes to `main` on `milomadatu/milomadatu.github.io`. GitHub Pages auto-deploys within ~30–60 seconds. Live URL: https://milomadatu.github.io/.

No staging environment. Push only after the change has been visually verified in `index.html` locally (open the file directly in a browser).
