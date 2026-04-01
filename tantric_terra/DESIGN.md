# Design System Strategy: The Sensorial Editorial

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Sacred Editorial."** 

This system transcends the utilitarian nature of standard web design to create a digital sanctuary. We are not building a dashboard; we are curating a mindful journey. By leveraging intentional asymmetry, high-contrast typography scales, and a rejection of rigid "boxy" containers, the design system mirrors the fluidity and organic nature of tantra and holistic well-being. We break the "template" look by treating the screen as a physical canvas where photography, typography, and layered surfaces breathe together in a rhythmic, intentional dance.

## 2. Colors: Tonal Depth & The "No-Line" Rule
Our palette is a sophisticated transition of earth-born pigments. The goal is to create warmth through depth, not through decoration.

### The "No-Line" Rule
**Explicit Instruction:** Use of 1px solid borders for sectioning or containment is strictly prohibited. 
In this design system, boundaries are felt, not drawn. Define sections solely through:
*   **Background Shifts:** Transitioning from `surface` (#fff8f6) to `surface-container-low` (#fef1ec).
*   **Tonal Nesting:** A `surface-container-highest` (#ede0db) card sitting on a `surface-container` (#f8ebe6) background.

### Surface Hierarchy & Nesting
Treat the UI as layered sheets of fine, textured paper. 
*   **Base:** `background` (#fff8f6) for the primary reading experience.
*   **Secondary Context:** `surface-container-low` (#fef1ec) for supplementary content.
*   **Focus Elements:** Use `primary-container` (#734f40) with `on-primary-container` (#f4c3b0) text for high-impact callouts or banners.

### Glass & Gradient Rules
To elevate the "professional" and "spiritual" feel:
*   **Glassmorphism:** For navigation overlays or floating action elements, use `surface` colors at 80% opacity with a `backdrop-blur` of 20px. This allows the organic photography to bleed through the UI, maintaining a sense of presence.
*   **Signature Gradients:** For primary CTAs and hero section accents, apply a subtle linear gradient from `primary` (#59382a) to `secondary` (#83523b) at a 135-degree angle. This adds "soul" and a tactile, sun-drenched quality to the interface.

## 3. Typography: The Elegant Voice
Typography is the primary vehicle for the brand’s "calming yet professional" authority.

*   **The Heroic Serif (Noto Serif):** Used for all `display` and `headline` levels. This conveys wisdom, heritage, and the "High-End Editorial" feel. 
    *   *Styling Note:* Use wide letter-spacing (-0.02em) and generous line-heights (1.2 - 1.4) to allow the words to breathe.
*   **The Modern Foundation (Plus Jakarta Sans):** Used for `title`, `body`, and `label` levels. This provides a clean, contemporary contrast to the serif, ensuring high legibility for long-form holistic guidance.
*   **Visual Hierarchy:** Large `display-lg` (3.5rem) should often be paired with a much smaller `label-md` (0.75rem) in all-caps above it to create a sophisticated, magazine-style header.

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are often too "digital." We utilize ambient light and tonal shifts.

*   **The Layering Principle:** Instead of shadows, use the Spacing Scale (specifically `spacing-8` and `spacing-12`) to create literal distance between elements, letting the color shifts between `surface-container` tiers do the work of separation.
*   **Ambient Shadows:** For elements that *must* float (e.g., a "Book Now" modal), use an extra-diffused shadow: `box-shadow: 0 20px 40px rgba(115, 79, 64, 0.08)`. Note the use of a tinted shadow (using the `primary` hue) rather than black or grey.
*   **The "Ghost Border" Fallback:** If accessibility requires a stroke, use `outline-variant` (#d5c3bd) at 15% opacity. It should be a suggestion of a line, not a hard stop.

## 5. Components: Bespoke Elements

### Buttons
*   **Primary:** `primary` (#59382a) background with `on-primary` (#ffffff) text. Shape: `rounded-sm` (0.125rem) for a refined, slightly architectural feel. No heavy rounding.
*   **Tertiary (Text-Only):** Use `primary` text with a 1px underline in `secondary_fixed_dim`. The underline should be offset by 4px to feel like a vintage editorial link.

### Cards & Lists
*   **The Organic Card:** Cards should never have borders. Use `surface-container-highest` with a `rounded-lg` (0.5rem) corner. 
*   **Separation:** Forbid divider lines. Separate list items using `spacing-4` (1.4rem) vertical padding and a subtle change in background color on hover.

### Inputs & Forms
*   **Aesthetic:** Fields are "Open-Style." Only a bottom border using `outline-variant` at 40% opacity. 
*   **Focus State:** The bottom border transitions to `primary` (#59382a) with a subtle `surface-tint` glow.

### Signature Component: The "Mindful Reveal"
*   Use high-quality photography as a background within a `surface-container-low` section, partially obscured by an overlapping `surface` text card using an asymmetrical offset (e.g., `-spacing-16` margin).

## 6. Do's and Don'ts

### Do:
*   **Do** embrace negative space. If a layout feels "full," add `spacing-20` (7rem) of padding.
*   **Do** use asymmetrical image placements. Align text to the left and images to the far right, allowing them to bleed off the edge of the screen.
*   **Do** use the "Tonal Layering" principle for all hierarchy needs before reaching for a shadow.

### Don't:
*   **Don't** use 100% black (#000000) for text. Use `on-surface` (#201a18) to maintain a soft, earthy vibration.
*   **Don't** use sharp, 90-degree corners for large containers. Use `rounded-md` as a minimum to keep the "feminine and soft" promise.
*   **Don't** use standard "icon-plus-text" horizontal grids. Experiment with stacking and overlapping icons over images to create depth.
*   **Don't** use high-contrast dividers. If you feel the need for a line, use a wide spacing gap instead.