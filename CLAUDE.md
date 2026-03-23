# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.
# Portfolio Project Brief

## What this is
A personal portfolio for Achinthya Hemachandra — a senior product 
professional (8 years experience) open to both PM and PMM roles.
The portfolio must work for two audiences simultaneously:
- A recruiter skimming for 20 seconds — the home page scroll tells 
  the complete story without any clicking required
- A hiring manager spending 15 minutes — deep dive pages provide 
  proof and strategic thinking

## Site structure
- Home (index.html) — fully scrollable, self-contained story
- Work index (work.html) — 3 case study cards linking to subpages
- Enphase case study (enphase.html)
- Digite case study (digite.html)  
- Sony case study (sony.html)
- AI & Ways of Working (ai.html)
- Contact (contact.html)

## Home page scroll order
1. Hero — positioning headline, dual PM/PMM label, two CTAs
2. At a glance — 3 company cards (Enphase, Digite, Sony), each 
   clickable to full case study
3. What I bring — 2x2 grid of 4 capability themes
4. How I work with AI — condensed 3-block preview, links to ai.html
5. A little more about me — 2-3 sentence human layer
6. Contact strip — email, LinkedIn, resume downloads (PM + PMM)

## Case study page structure (same template for all 3)
Each case study follows exactly this four-part structure:
1. The situation — context and stakes
2. My bet — the strategic decision and reasoning (this is the 
   most important section — it must lead with thinking, not action)
3. What I did — execution, decisions, tradeoffs
4. What changed — outcomes and learning

## Tone
Confident and calm. Substance over flash. Warm but not casual. 
Written like a thoughtful senior practitioner, not a marketing deck.
Never use superlatives. Never use "passionate about" or "excited to".

## Content
All content will be provided per page. Do not invent or assume 
experience. Only use what is explicitly given.

## Build approach
Build one page at a time. Start with index.html (home page).
Always check Design.md before making any styling decisions.
When in doubt on design, do less — whitespace is preferable 
to filler.

## Project Overview

This is a **static HTML portfolio** for a senior product professional. There is no build system, package manager, or framework — all pages are self-contained `.html` files that run directly in a browser. Each subfolder typically contains a `code.html` (the page) and a `screen.png` (reference screenshot).

## Running Pages

Open any `code.html` directly in a browser. No server, build step, or install is required. Tailwind CSS is loaded via CDN (`cdn.tailwindcss.com`) and configured inline via a `<script id="tailwind-config">` block in each file.

## Tech Stack

- **CSS:** Tailwind CSS via CDN with a custom theme extending Material Design 3 color tokens
- **Fonts:** `Newsreader` (display/headlines) and `Inter` (body/labels) from Google Fonts
- **Icons:** Material Symbols Outlined from Google Fonts

## Design System

The authoritative design reference is `Design.md`. All HTML files must adhere to it. Key rules:

### Color Tokens (Tailwind class names)
| Token | Hex | Use |
|---|---|---|
| `surface` / `background` | `#fcf9f4` | Page background (warm off-white) |
| `surface-container-low` | `#f6f3ee` | Full-width section breaks |
| `surface-container-lowest` | `#ffffff` | Raised cards/floating elements |
| `on-surface` | `#1c1c19` | All body text (never use pure black) |
| `primary` | `#005247` | Deep teal — primary CTAs, accents |
| `primary-container` | `#1a6b5e` | Gradient endpoint, secondary fills |
| `primary-fixed` | `#a6f1e0` | Subtle highlights behind key text |
| `tertiary` | `#6e3b00` | Amber — high-intent CTAs ("Contact Me") |
| `on-surface-variant` | `#3f4946` | Secondary/supporting text |

### Typography
- **Headlines/Display:** `font-headline` (Newsreader serif), `text-6xl`/`text-7xl`, `leading-[1.1]`
- **Body:** `font-body` (Inter), `text-xl` at `leading-relaxed` (1.7)
- **Labels/Metadata:** `font-label` (Inter), `text-[11px]`, `uppercase`, `tracking-[0.2em]` — use for "ROLE", "DATE", "RESULT" etc.

### Critical Rules
- **No divider lines.** Section breaks use background color shifts only. If a wash is needed, use `primary-container` at 15% opacity.
- **No pure black.** Always use `on-surface` (`#1c1c19`) for text.
- **No decorative blobs or mesh gradients.** Increase headline size instead of adding filler.
- **No heavy shadows.** Use `shadow` with `24px` blur, `0px` offset, `4%` opacity (`on-surface` color).
- **Cards:** No borders, no dividers. `spacing-10` (3.5rem) internal padding. Hover transitions background from `surface-container` → `surface-container-high`.
- **Nav:** Glassmorphism — `bg-surface/80 backdrop-blur-md`.
- **Primary CTA gradient:** `linear-gradient(135deg, #005247, #1a6b5e)`.
- **Max content width:** `max-w-[780px] mx-auto`.

### Elevation (Stacked Paper)
Place `surface-container-lowest` cards on `surface-container-low` backgrounds for natural "ghost" elevation — no explicit shadows needed.
