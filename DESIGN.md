# Design System Specification: The Boardroom Editorial

## 1. Overview & Creative North Star
### Creative North Star: "The Academic Executive"
This design system moves beyond the typical corporate dashboard. It is an editorial-first experience that blends the prestige of the University of Minnesota with the sharp, high-stakes atmosphere of a professional boardroom. We reject the "standard grid" in favor of **Intentional Asymmetry**. By utilizing significant negative space and overlapping architectural layers, we create a digital environment that feels curated, not generated.

The aesthetic leverages the provided logo's handshake—a symbol of partnership and professional closure—to drive a "Solidarity & Structure" layout theme. Expect heavy, authoritative typography paired with ethereal, layered surfaces.

---

## 2. Colors: Tonal Depth & Soul
We are departing from flat blocks of color. The palette is anchored in Maroon and Gold, but it is executed through sophisticated tonal transitions.

### The Palette
- **Primary Maroon (#7A0019):** Used as the grounding force. Use `primary` (#51000D) for deep text and `primary_container` (#7A0019) for high-impact brand moments.
- **Secondary Gold (#FFCC33):** Our "Illumination" color. Use `secondary_container` (#FECB32) for highlights and `on_secondary_container` (#705600) for readable accents.
- **Surface Neutrals:** A range of warm, paper-like tones from `surface_container_lowest` (#FFFFFF) to `surface_dim` (#ECD5D4).

### The "No-Line" Rule
**Borders are strictly prohibited for sectioning.** We do not use 1px lines to separate content. Boundaries must be defined solely by background shifts. 
*   *Example:* Place a `surface_container_low` sidebar against a `surface` background. The shift in tone is the divider.

### The Glass & Gradient Rule
To provide visual "soul," use subtle radial gradients for hero sections, transitioning from `primary` (#51000D) to `primary_container` (#7A0019). For floating navigation or executive summaries, utilize **Glassmorphism**: 
*   **Surface:** `surface_bright` at 80% opacity.
*   **Backdrop Blur:** 12px to 20px.

---

## 3. Typography: The Editorial Voice
We utilize **Manrope** for its geometric clarity and modern professional weight. The hierarchy is designed to read like a high-end financial journal.

| Level | Size | Weight | Usage |
| :--- | :--- | :--- | :--- |
| **Display-LG** | 3.5rem | 800 | Rare, hero-only statements. Negative letter-spacing (-0.02em). |
| **Headline-LG** | 2rem | 700 | Primary section headers. Direct and authoritative. |
| **Title-MD** | 1.125rem | 600 | Card titles and sub-headings. |
| **Body-LG** | 1rem | 400 | Standard reading text. Increased line-height (1.6) for legibility. |
| **Label-MD** | 0.75rem | 700 | Caps-only. Used for metadata and overlines. |

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are largely replaced by **The Layering Principle**.

- **Surface Nesting:** Depth is achieved by stacking. Place a `surface_container_highest` (#F5DDDC) element inside a `surface_container_low` (#FFF0EF) parent to create a recessed, "carved" look.
- **Ambient Shadows:** For high-level modals or floating action buttons, use "Shadow-as-Light." 
    - **Color:** Use `on_surface` (#251818) at 6% opacity.
    - **Blur:** 40px - 60px.
    - **Offset:** Y: 20px.
- **The "Ghost Border" Fallback:** If accessibility requires a stroke (e.g., in high-contrast modes), use `outline_variant` (#E0BFBE) at **15% opacity**. Never 100%.

---

## 5. Components

### Buttons: The Executive Action
- **Primary:** `primary` background with `on_primary` text. Use `md` (0.375rem) corner radius. No border.
- **Secondary (The Gold Standard):** `secondary_container` background. This is used for "Win" actions or "Close Deal" buttons.
- **Tertiary:** Text-only in `primary_fixed_variant` (#8D1324) with an underline that appears only on hover.

### Cards & Lists: Editorial Blocks
- **Cards:** Forbid divider lines. Separate content using `body-sm` labels and 24px vertical padding (from the spacing scale). Use `surface_container_low` for the card body against a `surface` background.
- **Input Fields:** Use `surface_container_highest` for the field fill. The "Ghost Border" (15% opacity) only appears on focus.

### Additional Signature Components
- **The "Boardroom" Stat-Hero:** A massive `display-md` number in `primary` with a small `label-sm` descriptor in `secondary` gold. No box—just floating editorial data.
- **Partner Chips:** Using the handshake motif, chips should have `full` roundedness and use `secondary_fixed` (#FFDF92) backgrounds.

---

## 6. Do's and Don'ts

### Do
- **Do** use intentional asymmetry. Align a headline to the far left and the body text to a secondary grid column on the right.
- **Do** use the `secondary_fixed_dim` (#F2C025) for subtle highlights in text (background-highlights).
- **Do** ensure 4.5:1 contrast ratios by using `on_primary_fixed` on top of light containers.

### Don't
- **Don't** use 1px solid black or grey borders.
- **Don't** use default Material Design "Elevation 1" shadows; they are too harsh for this aesthetic.
- **Don't** clutter the screen. If a section feels crowded, double the white space. The "Boardroom" aesthetic requires breathing room to feel expensive.