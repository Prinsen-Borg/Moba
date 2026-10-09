---
name: moba-web-page
description: Use when asked to build any HTML web page, one-pager, internal tool, dashboard or demo for Moba. Produces a single self-contained, on-brand page that follows DESIGN.md.
metadata: owner IT & Digital Transformation · version 0.1
---

## Goal
One self-contained `index.html` that a Moba colleague would recognise as Moba at first glance. It should be clear, calm and premium industrial, and it should work on a phone.

## Steps
1. **Read the rules.** Read `DESIGN.md` and `design-system/tokens.css`. Copy the `:root` token block into the page (single-file pages) or link `tokens.css` (pages inside this repo).
2. **Define the page's single job.** Write one sentence: who reads it and what they should do or know afterwards. Every section must serve that job.
3. **Load the fonts.** Use Google Fonts `IBM Plex Serif` (500) and `Ubuntu` (400/500/700), with the fallbacks from the tokens.
4. **Build the structure** using the Moba section rhythm: *eyebrow* (Ubuntu 500, 16px) → *serif H2* → short paragraph → content (cards, table, chart).
5. **Build the hero:**
   - grey canvas `#F2F3F5` with the faint dotted grid;
   - centred serif H1 with at most **one** bronze gradient word;
   - one amber primary button and at most one navy outline secondary button.
6. **Style the components:**
   - Cards: white, `10px` radius, **no shadow**.
   - Buttons: pills with a small navy arrow circle.
   - Images: the signature `75px` top-left corner.
   - Band sections: the navy gradient.
   - Footer: the steel gradient.
7. **Use real content.** Use Moba product names, units (eggs/hour, cases/hour) and terms. Never use lorem ipsum. Label example data as "Example".
8. **Check before you hand it over** (see Never and Gotchas below).

## Output
- `tools/<page-name>/index.html`, plus a 3-line `README.md` in the same folder (purpose, owner, date).
- One HTML file with inline CSS/JS. External requests go only to Google Fonts.

## Example
Request: "Make a page showing our IT initiatives." The result has the eyebrow "IT & Digital Transformation" above the H1 "Our **Digital** Roadmap". It then shows one card per initiative (ERP, MyMoba, Telephony, AI) with status chips, and a navy band with the next three milestones.

## Never
- Never invent colours outside the palette. Amber is for actions only and never for text.
- Never use shadows on cards, purple or blue "tech" gradients, emoji as section markers or all-caps headings.
- Never use stock phrases like "cutting-edge", "revolutionary" or "seamless".
- Never put confidential figures, personal data or secrets into a page (see AGENTS.md §5).
- Never use horizontal scrolling on a 400px-wide phone.

## Gotchas
- Navy text on amber passes contrast, but white on amber does **not**. Keep button text navy.
- Bronze gradient text needs `-webkit-background-clip: text` plus a solid `color` fallback.
- Ubuntu renders noticeably wider than Segoe UI. Test the fallback so headings don't wrap badly on Windows laptops without the font.
- The design is light-only for now (DESIGN.md §9). Set `color-scheme: light` and an explicit body background.
