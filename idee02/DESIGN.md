# Design System Document: The Grounded Sanctuary

## 1. Overview & Creative North Star
**Creative North Star: The Grounded Sanctuary**

This design system is a rejection of the frantic, high-contrast digital world. It is built to evoke the physical sensation of entering a high-end massage studio: the scent of cedar, the weight of linen, and the stillness of a stone-walled room. 

We move beyond "standard" UI by embracing **Editorial Asymmetry**. Instead of a rigid, centered grid, we use intentional shifts in alignment and generous, "wasteful" white space to signal luxury. This system is masculine in its strength and stability, but deeply gentle in its execution. We prioritize "presence" over "conversion," trusting that a calm user is a converted user.

---

## 2. Colors: Tonal Earth & Warm Light
The palette is strictly warm. There are no cold greys or clinical blues. Every hex code is chosen to mimic natural materials—terracotta, sand, and ochre.

### The "No-Line" Rule
**Standard 1px borders are strictly prohibited for sectioning.** 
Visual boundaries must be created through background shifts. To separate the hero from the content, transition from `surface` (#fcf9f4) to `surface-container-low` (#f6f3ee). This creates a "felt" boundary rather than a "seen" one, maintaining the artisanal flow of the layout.

### Surface Hierarchy & Nesting
Treat the interface as physical layers of fine paper. 
*   **Base:** `surface` (#fcf9f4)
*   **Sectioning:** `surface-container` (#f0ede8)
*   **Cards/Floating Elements:** `surface-container-lowest` (#ffffff) to create a subtle "lift" against the creamier backgrounds.

### The "Glass & Gradient" Rule
For floating navigation or modal overlays, use **Glassmorphism**. Apply `surface-bright` at 70% opacity with a `24px` backdrop-blur. This ensures the warm tones of the background bleed through, maintaining the "warm light" mood. For primary CTAs, use a subtle linear gradient from `primary` (#883528) to `primary_container` (#a64c3e) to give the element a soft, rounded, 3D volume—mimicking a smooth river stone.

---

## 3. Typography: The Editorial Voice
Our typography pairing creates a dialogue between tradition (the Serif) and modernity (the Sans).

*   **Headings (Noto Serif):** Used for all `display` and `headline` roles. This font carries the "Artisanal" and "Trustworthy" weight. Use `display-lg` (3.5rem) with `letterSpacing: "-0.02em"` for hero statements to create a sophisticated, compressed look.
*   **Body (Manrope):** Used for `title`, `body`, and `label` roles. Manrope’s geometric but humanist curves provide a "Clean" and "Professional" counterpoint to the organic Serif.
*   **The Hierarchy Strategy:** We use extreme scale. Pair a `display-lg` headline with a `body-md` subheader. The vast difference in size creates a high-end editorial feel found in luxury magazines.

---

## 4. Elevation & Depth
In this system, depth is achieved through **Tonal Layering** rather than shadows.

*   **The Layering Principle:** To highlight a "Treatment Card," do not add a shadow. Instead, place a `surface-container-lowest` (#ffffff) card on top of a `surface-container` (#f0ede8) background. The 2% difference in luminance provides a sophisticated, architectural lift.
*   **Ambient Shadows:** If a floating element (like a booking FAB) requires a shadow, use the `on-surface` color (#1c1c19) at **4% opacity** with a blur of `32px` and a Y-offset of `8px`. This mimics the soft, diffused glow of a shaded lamp.
*   **The "Ghost Border":** If accessibility requires a border (e.g., in input fields), use the `outline-variant` (#dac1b8) at **20% opacity**. It should be felt as a suggestion of a shape, not a hard enclosure.

---

## 5. Components

### Buttons (The Tactile Touch)
*   **Primary:** Filled with `primary` (#883528), text in `on_primary` (#ffffff). Shape: `rounded-DEFAULT` (0.25rem). The slight roundness feels intentional and architectural, avoiding the "pill" shape which can feel too tech-focused.
*   **Tertiary:** No background. Use `notoSerif` for the text with an underline in `secondary_fixed_dim` (#f9ba76) set at 3px thickness, offset by 4px.

### Input Fields (The Quiet Request)
*   **Style:** No container boxes. Use a simple `surface-container-highest` (#e5e2dd) bottom bar (2px). Labels should use `label-md` in `on_surface_variant`. 
*   **Focus State:** The bottom bar transitions to `primary` (#883528).

### Cards & Lists (The Breathable Grid)
*   **Rule:** Forbid divider lines. Use `spacing.12` (4rem) to separate list items.
*   **Layout:** Use asymmetrical padding. A card might have `padding-left: 2rem` and `padding-right: 4rem` to create a sense of organic movement.

### Signature Component: The "Therapy Detail" Card
A layout designed for treatment descriptions.
*   **Background:** `surface_container_low`.
*   **Typography:** `headline-sm` (Noto Serif) aligned to the top-left, with `body-md` (Manrope) aligned to the bottom-right, separated by significant `spacing.20` (7rem). This creates a luxurious "slow" reading experience.

---

## 6. Do's and Don'ts

### Do:
*   **Do** use `spacing.24` (8.5rem) for vertical margins between major sections. The layout must feel "slow."
*   **Do** use images with "Warm Light" filters—think sun-drenched linen and soft-focus stone textures.
*   **Do** embrace asymmetry. It’s okay for a text block to be offset from the center to create a custom, human feel.

### Don't:
*   **Don't** use pure #000000. Use `on_surface` (#1c1c19) for all "black" text to keep the warmth.
*   **Don't** use sharp, 0px corners. Use `rounded-DEFAULT` or `rounded-md` to maintain a "gentle" touch.
*   **Don't** crowd the interface. If a screen feels "efficient," it’s likely too cluttered for this system. Increase the whitespace.