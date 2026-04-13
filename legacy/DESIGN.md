# Design System Document: Institutional Heritage & Digital Elegance

## 1. Overview & Creative North Star
The visual identity for **Instituto Bilingüe República de Italia** is built upon the Creative North Star of **"The Modern Archivist."** 

This design system rejects the "template-heavy" look of typical educational portals in favor of a bespoke, editorial experience. It balances the weight of academic tradition with the fluidity of modern digital interactions. We achieve this through "Intentional Asymmetry"—placing heavy serif headlines against vast white space and using overlapping tonal surfaces to create depth. The goal is to evoke the feeling of a high-end academic journal: serious, prestigious, and meticulously organized, yet breathing with contemporary light.

---

## 2. Colors: Tonal Depth over Structural Lines
Our palette is deeply rooted in institutional identity, but its application must be sophisticated.

### Palette Strategy
- **Primary (`#005dac`):** Used for core branding and high-importance UI elements.
- **Secondary (`#1b6d24`):** Reserved for growth-oriented actions, success states, and subtle heritage accents.
- **Tertiary/Alert (`#b61b1f`):** To be used sparingly for critical alerts or specific symbolic highlights.
- **Neutral/Surface Strategy:** We use a refined range of whites and greys (`surface-container-lowest` to `highest`) to build a tactile environment.

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders to separate sections. Structure must be defined solely through:
1. **Background Color Shifts:** E.g., a `surface-container-low` section transitioning into a `surface` background.
2. **Intentional White Space:** Using the spacing scale to create "invisible boundaries."

### Signature Textures & Glassmorphism
To add "soul" to the interface:
- **Subtle Gradients:** Use a linear gradient from `primary` to `primary-container` for hero call-to-actions to avoid a "flat" commercial look.
- **The Glass Rule:** Floating navigation or modal overlays must use semi-transparent `surface` colors with a `backdrop-filter: blur(20px)`. This integrates the UI layers rather than stacking them like stickers.

---

## 3. Typography: Editorial Authority
The contrast between Noto Serif and Work Sans creates a "Newspaper vs. System" hierarchy.

- **Display & Headlines (Noto Serif):** These are our "Heritage" anchors. Use `display-lg` for hero moments with tight letter-spacing and `headline-md` for section entries. Their role is to provide the "Institutional Voice."
- **Body & Titles (Work Sans):** These are our "Functional" anchors. Work Sans provides a clean, neutral balance that ensures readability in dense academic content.
- **Visual Hierarchy Tip:** Use high-contrast sizing. A large `display-sm` headline next to a small, wide-tracked `label-md` creates a premium editorial feel that standard "middle-of-the-road" sizing cannot achieve.

---

## 4. Elevation & Depth: Tonal Layering
We do not use shadows to create "pop"; we use layers to create "presence."

- **The Layering Principle:** Depth is achieved by stacking `surface-container` tiers. 
    - *Example:* Place a `surface-container-lowest` card on top of a `surface-container-low` section. The subtle shift in hex code creates a "lift" that feels like heavy cardstock resting on a desk.
- **Ambient Shadows:** If a floating element is functionally required (e.g., a dropdown), shadows must be extra-diffused. 
    - *Spec:* `box-shadow: 0 12px 40px rgba(0, 28, 58, 0.06);` (using a tinted version of `on-primary-fixed` at very low opacity).
- **The Ghost Border:** If a boundary is required for accessibility, use the `outline-variant` token at **15% opacity**. Never use 100% opaque borders.

---

## 5. Components

### Buttons & Interaction
- **Primary Button:** Solid `primary` fill, `on-primary` text. Rounding: `DEFAULT (0.25rem)`. No border.
- **Secondary Button:** `surface-container-highest` background with `primary` text. This feels more "integrated" than an outlined button.
- **Tertiary Button:** Text-only with a subtle `primary` underline on hover.

### Cards & Lists
- **The Divider Ban:** Cards must not have border lines or internal divider lines. Use `surface-container-lowest` for the card body and vertical padding to separate list items.
- **Entry Animations:** List items should stagger-fade in vertically to reinforce the "Archivist" feel of being carefully presented.

### Input Fields
- **Style:** Use "Soft Fields." A `surface-container-low` background with a `Ghost Border` that becomes a 2px `primary` bottom-border on focus. This mimics the feeling of filling out a prestigious physical form.

### Academic Highlights (Unique Component)
- **Heritage Badge:** A small, square-shouldered chip using `secondary` (Green) with `on-secondary` text, used to denote official institutional announcements or bilingual status.

---

## 6. Do's and Don'ts

### Do:
- **Use "Breathing Room":** If you think a section has enough padding, add 16px more. Prestige is signaled by the luxury of space.
- **Respect the Serif:** Use Noto Serif for all titles that represent the "voice" of the Institute.
- **Tint your Shadows:** Ensure any elevation uses a blue-tinted shadow to remain consistent with the `primary` color story.

### Don't:
- **Don't use Rounded Corners:** Avoid `full` or `xl` roundness. Stay strictly within `DEFAULT (0.25rem)` to maintain a serious, architectural tone.
- **Don't use Pure Black:** Text should always be `on-surface` (`#1b1c1c`) or `text` (`#333333`), never `#000000`, to keep the palette soft and academic.
- **Don't Overuse Red:** The `tertiary` red is an alert or a symbol. Overusing it will break the "Minimalist/Serious" personality and create unnecessary visual stress.

---

## 7. Token Reference Summary

| Property | Token / Value | Application |
| :--- | :--- | :--- |
| **Corner Radius** | `DEFAULT: 0.25rem` | All buttons, inputs, and cards. |
| **Surface (Base)** | `#fbf9f8` | Main page background. |
| **Surface (Card)** | `#ffffff` | Floating content over base. |
| **Primary** | `#1976d2` | Brand headers, primary actions. |
| **Headlines** | `Noto Serif` | Display and section titles. |
| **Body** | `Work Sans` | All functional and reading text. |
| **Border** | `outline-variant @ 15%` | Only when functionally necessary. |