# DESIGN.md: Moba Design System & Asset Specifications

Extracted from the live **moba.net** production site (theme `moba-theme`, stylesheet `app.44a499.css`) on 2026-10-09, using computed styles in the browser.
Purpose: give every AI agent (Claude, Copilot, Cursor) and every human builder one source of truth, so that internal tools, slides, web pages and documents look like Moba, not like a generic template.

> Status: **v0.1, unofficial.** Reverse-engineered from the public website, not from the official Moba brand guide. Check it against the Marketing brand book (logo usage, approved colours, photography) before anything external is published.

---

## 1. Brand essence

- **Positioning:** "Building Your Sustainable Egg Future". The tone is warm, trustworthy and engineering-proud, and it puts the customer first ("we create it *with you*").
- **Visual character:** calm light-grey canvas, deep navy type, one warm amber call to action and a bronze highlight word. The feel is premium industrial, not flashy tech.
- **Voice:** second person ("your challenges, our solutions"), short benefit-led headlines and concrete numbers ("1.2 million eggs a week"). Avoid hype words and exclamation marks.
- **Motif:** the egg. A small egg icon (`egg.svg`) is used as a list and link bullet, and a faint dotted grid sits in hero backgrounds.

## 2. Colour palette

| Token | Hex | Use |
|---|---|---|
| `--moba-navy` (primary) | `#002659` | Headings, body text, logo, outline buttons, focus ring, nav bar |
| `--moba-navy-deep` | `#112337` | Dark text and surfaces, footer details |
| `--moba-navy-light` | `#014589` | Start of the navy gradient |
| `--moba-slate` (body copy) | `#41586B` | Paragraph text in main content |
| `--moba-grey` | `#8698A2` | Secondary text, meta, dots pattern |
| `--moba-canvas` | `#F2F3F5` | Page background (not pure white) |
| `--moba-surface` | `#FFFFFF` | Cards, dropdowns |
| `--moba-border` | `#DEE2E6` | Hairlines, dividers |
| `--moba-amber` (CTA) | `#FCAF17` | Primary button background (text stays navy) |
| `--moba-bronze` | `#D7955E` to `#A77449` | Highlight word in headlines (gradient text) |
| `--moba-error` | `#C02B0A` | Form errors and required marks only |

**Gradients**
- Navy band (newsletter, banners): `linear-gradient(90deg, #014589, #002659)`
- Soft steel (footer, light sections): `linear-gradient(125deg, #A4B4BC -10%, #EFF0F3 58%)`
- Bronze highlight text: `linear-gradient(#D7955E, #A77449)`, applied to one key word only

**Rules**
- Use navy for text and amber for action. Amber is never used for text and never for large areas.
- Use at most **one** bronze highlight word per headline. Example: "Building Your **Sustainable** Egg Future".
- Use red only for errors, never for decoration.

## 3. Typography

| Role | Font | Weight | Size / line-height |
|---|---|---|---|
| H1 | **IBM Plex Serif** | 500 | 36px / 1.2 (mobile); scale up on desktop |
| H2 | IBM Plex Serif | 500 | 25px / 1.5 |
| H3 / card titles | **Ubuntu** | 500 | 16px / 1.2 |
| Eyebrow / lead (above H2) | Ubuntu | 500 | 16px, navy, sentence case |
| Body | Ubuntu | 400 | 18px / 27px (page), 16px / 27px (content blocks) |
| Nav links | Ubuntu | 400 | 16px / 24px |

- The headline pattern is serif (warm and established); the UI and body are a humanist sans (friendly and technical).
- Both fonts are free Google Fonts: `IBM Plex Serif` (500) and `Ubuntu` (400/500/700).
- Do not use all caps in headings and do not use monospace in customer-facing layouts.
- In Office and PowerPoint, fall back to **Georgia** for headings and **Segoe UI** for body if the fonts are not installed.

## 4. Spacing & layout

- **Spacing scale (px):** 8, 12, 16, 24, 32, 40, 52, 64, 80, 100 (`--Spacing__1` to `__10`)
- **Breakpoints (Bootstrap-based):** sm 676, md 768, lg 992, xl 1200, xxl 1400, xxxl 1600
- **Max content width:** 1500px
- **Grid:** 12 columns. Hero text is centred and generous whitespace is used between sections (64 to 100px).
- **Section rhythm:** eyebrow, then serif H2, then a short paragraph, then content (cards, carousel or table).

## 5. Components

**Buttons**
- *Primary:* amber `#FCAF17` background, navy text, pill shape (`border-radius: 50px`), padding `12px 16px`, Ubuntu 400 16px. It has a small navy circle with a white arrow on the right.
- *Secondary:* transparent background, 1px navy border, navy text, the same pill shape and arrow circle.
- Labels are verbs that start with the benefit, for example "Get in touch", "About Moba" and "View all customer stories".

**Cards** (product cards)
- White surface on a grey canvas, `border-radius: 10px`, **no shadow**, centred content, product render on top, then title and a short description followed by "Read more".

**Imagery**
- Real factory photography and product renders, plus landscapes for the sustainability story.
- The signature shape is **one large rounded corner**: the hero image uses `border-radius: 75px 0 0 0` (top-left only).
- An amber or orange colour block can sit partly behind an image as a graphic accent.

**Navigation**
- A thin navy top bar holds the quick links (Challenges · Products · Our Services · Refurbished).
- The main bar has the logo on the left and the amber "Get in touch" button plus a navy round menu button on the right.

**Carousel controls:** round navy buttons (`border-radius: 50%`).

## 6. Logo & assets

- Primary logo: `Moba_Egg_Industry_Solutions_Blauw_RGB.svg` (navy wordmark "MOBA" with the descriptor "Egg Industry Solutions").
- Favicon: `Moba-Favicon` (WordPress uploads).
- Always place the logo on a light background, and use a white version on navy. **Ask Marketing for the official white and mono versions.** Do not recolour the logo yourself.

## 7. Applying this outside the website

| Output | Guidance |
|---|---|
| **Internal web tools / dashboards** | Grey canvas, white cards (10px radius, no shadow), navy text, amber for the single primary action. Charts in navy, steel grey and amber; use bronze sparingly. |
| **Slides** | White or `#F2F3F5` background, serif title in navy and one bronze highlight word if needed. Use the navy gradient band only for section dividers. |
| **Documents / memos** | Serif headings in navy, Ubuntu (or Segoe UI) body in slate `#41586B`, thin `#DEE2E6` table rules. |
| **AI-generated output** | Agents should read this file first. Never invent new brand colours. When unsure, choose navy on light grey. |

## 8. CSS token block (copy-paste)

```css
:root {
  --moba-navy: #002659;
  --moba-navy-deep: #112337;
  --moba-navy-light: #014589;
  --moba-slate: #41586B;
  --moba-grey: #8698A2;
  --moba-canvas: #F2F3F5;
  --moba-surface: #FFFFFF;
  --moba-border: #DEE2E6;
  --moba-amber: #FCAF17;
  --moba-bronze-1: #D7955E;
  --moba-bronze-2: #A77449;
  --moba-error: #C02B0A;

  --font-heading: "IBM Plex Serif", Georgia, serif;
  --font-body: "Ubuntu", "Segoe UI", sans-serif;

  --radius-card: 10px;
  --radius-pill: 50px;
  --radius-hero: 75px 0 0 0;

  --gradient-navy: linear-gradient(90deg, #014589, #002659);
  --gradient-steel: linear-gradient(125deg, #A4B4BC -10%, #EFF0F3 58%);
}
```

## 9. Open points (to verify inside Moba)

- [ ] Compare with the official brand book from Marketing: colours, logo variants and photography rules.
- [ ] Is there an official PowerPoint/Word template? Add it to `design-system/`.
- [ ] Check the licence and availability of IBM Plex Serif and Ubuntu on managed Windows laptops.
- [ ] Decide on a dark mode for internal tools. **Until then, the design is light-only.**

## 10. Related files

- `design-system/tokens.css`: the same tokens as a ready-to-link stylesheet
- `.claude/skills/moba-web-page/SKILL.md`: step-by-step instructions for building an on-brand HTML page
- `tools/design-showcase/index.html`: a living demo of everything in this file
