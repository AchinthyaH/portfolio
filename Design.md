# The Portfolio Design System: Editorial Confidence

This design system is a bespoke framework crafted for the senior product professional. It rejects the frantic, "attention-economy" patterns of modern SaaS in favor of an **unhurried, editorial experience**. It is designed to feel like a high-end monograph—intentional, authoritative, and deeply personal.

---

## 1. Creative North Star: "The Digital Monograph"
The guiding principle of this system is **The Digital Monograph**. Unlike a standard resume or "grid-of-cards" portfolio, this system treats every page as a curated exhibition.

We break the "template" look through:
* **Intentional Asymmetry:** Utilizing the 12-column grid to create wide gutters and offset text blocks, suggesting a layout that was hand-set by an editor.
* **Tonal Depth:** Replacing harsh lines with shifts in warm neutrals.
* **Typographic Gravity:** Using extreme scale shifts between oversized serif headlines and meticulous, tracked-out labels to create a sense of hierarchy and "breath."

---

## 2. Color & Surface Architecture
The palette is rooted in warmth. We avoid "pure" whites or grays, opting instead for a "paper and ink" feel that reduces eye strain and conveys seniority.

### Surface Hierarchy & Nesting
To move beyond a flat digital feel, we use a **Stacked Paper** methodology. Instead of using lines to separate thoughts, use the following tiering:
* **Base Layer (`surface` / #fcf9f4):** The canvas. Used for the primary page background.
* **Lowered Sections (`surface-container-low` / #f6f3ee):** Use for full-width section breaks to denote a change in topic (e.g., shifting from "Case Study" to "Testimonials").
* **Raised Elements (`surface-container-lowest` / #ffffff):** Used for interactive cards or floating elements to create a soft, natural "pop" against the warm base.

### The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid lines to section off content. Boundaries must be defined by background color shifts. If a visual break is required, use `primary_container` (#1a6b5e) at 15% opacity as a soft wash, not a stroke.

### Signature Textures
For primary CTAs or hero headers, use a subtle **linear gradient** transitioning from `primary` (#005247) to `primary_container` (#1a6b5e) at a 135-degree angle. This adds a "silk-screened" depth that flat hex codes cannot achieve.

---

## 3. Typography: The Editorial Voice
The typography is the core of this system's "confidence." It pairs the intellectual weight of a humanist serif with the functional clarity of a modern sans-serif.

* **Display & Headlines (Newsreader/Playfair):** These are the "voice." Set at `display-lg` (3.5rem) with a tight `line-height: 1.2`. Do not be afraid of word-wrapping; let the type be the hero.
* **Body (Inter/DM Sans):** The "logic." Set at 18px with a generous `line-height: 1.7`. This ensures long-form case studies feel "unhurried" and legible.
* **Labels:** Set in Inter, `label-sm` (11px), uppercase, with `letter-spacing: 0.1em`. Use these for metadata (e.g., "ROLE," "DATE," "RESULT") to provide a technical, disciplined counterpoint to the organic serif headlines.

---

## 4. Elevation & Depth
We reject the heavy, "fuzzy" drop shadows of 2010s design. Depth is achieved through **Tonal Layering** and **Ambient Light**.

* **The Layering Principle:** Place a `surface-container-lowest` card on a `surface-container-low` background. This creates a "ghost" elevation that feels integrated into the page.
* **Ambient Shadows:** For floating menus or modals, use a shadow with a `24px` blur, `0px` offset, and `4%` opacity using the `on_surface` color (#1c1c19). This mimics the soft shadow of paper on a desk.
* **Glassmorphism:** For top navigation bars, use `surface` at 80% opacity with a `20px` backdrop-blur. This allows the high-end typography of the content to bleed through as the user scrolls, maintaining a sense of place.

---

## 5. Components

### Buttons
* **Primary:** Filled with `primary` (#005247). 4px radius. Type: `label-md` (bold).
* **Secondary (The "Amber Accent"):** Use `tertiary` (#6e3b00) for high-intent CTAs (e.g., "Contact Me"). This warm amber provides a sophisticated "spark" against the cool teal.
* **Ghost:** No border. `on_surface` text with a subtle background shift to `surface-container-high` on hover.

### Cards
* **Constraint:** No borders. No dividers.
* **Structure:** Use `spacing-10` (3.5rem) of internal padding. Group content using vertical whitespace from the Spacing Scale.
* **Hover:** Transition the background from `surface-container` to `surface-container-high`.

### Input Fields
* **Style:** Minimalist. Only a bottom border of `outline_variant` at 20% opacity.
* **Focus:** Transition the bottom border to `primary` (#005247) at 1px thickness. No "glow" effects.

### Narrative Lists
* Used for career history. Forbid the use of divider lines. Instead, use a 2-column layout where the "Label" (Date) sits in a narrow left column and the "Title/Body" (Role/Description) sits in a wider right column, separated by `spacing-8`.

---

## 6. Do's and Don'ts

### Do
* **Do** use extreme whitespace. If a section feels finished, add another `spacing-12` (4rem) of padding.
* **Do** use "Optical Centering." On the 780px max-width grid, allow images to occasionally "bleed" out of the container by 40px to break the box.
* **Do** use `primary_fixed` (#a6f1e0) for very subtle background highlights behind important text snippets.

### Don't
* **Don't** use 100% black. Always use `on_surface` (#1c1c19) for text to maintain the warm, organic feel.
* **Don't** use decorative blobs or mesh gradients. If the page feels "empty," increase the font size of the headlines rather than adding "fluff."
* **Don't** use standard 12px "body small" for anything other than labels. Small text feels timid; this system is confident.