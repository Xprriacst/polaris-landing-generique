# Design System Specification: The Ethereal Navigator

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Ethereal Navigator."** 

Moving away from the rigid, boxy constraints of traditional SaaS dashboards, this system treats the interface as a vast, open sky. It is designed to feel weightless, expansive, and highly intentional. We achieve a "High-End Editorial" feel by prioritizing white space as a functional element rather than a void. By utilizing intentional asymmetry—such as offset hero typography and overlapping translucent containers—we break the "template" look to create an experience that feels bespoke and curated.

## 2. Color Philosophy & The Layering Principle
The palette is rooted in light and atmosphere. We utilize a "Tonal Depth" strategy rather than structural line-work to define the interface.

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders for sectioning or containment. Boundaries must be defined solely through background color shifts or subtle tonal transitions.
*   **Surface:** `#f7f9fb` (The base "sky")
*   **Surface-Container-Low:** `#f2f4f6` (Subtle grouping)
*   **Surface-Container-Lowest:** `#ffffff` (The "active" focal point)

### Surface Hierarchy & Nesting
Instead of a flat grid, treat the UI as a series of physical layers—like stacked sheets of fine paper. 
*   **Layer 1 (Background):** `surface`
*   **Layer 2 (Sectioning):** `surface-container-low`
*   **Layer 3 (Component/Card):** `surface-container-lowest`

### The "Glass & Gradient" Rule
To elevate the primary blue (`#004ac6`) from a standard utility color to a premium brand element, use **Signature Textures**. 
*   **Primary CTA:** Apply a subtle linear gradient from `primary` (#004ac6) to `primary-container` (#2563eb) at a 135-degree angle.
*   **Floating Elements:** Utilize Glassmorphism. Set the container to a semi-transparent `surface-container-lowest` (alpha 70%) with a `backdrop-blur` of 20px.

## 3. Typography: The Editorial Voice
The typography is the "Polaris" (the Guiding Star) of the system. We use a dual-font approach to balance mathematical precision with human elegance.

*   **Display & Headlines (Lexend):** Used for high-impact moments. Lexend’s expanded character width provides an immediate sense of "breathing room."
    *   *Styling Tip:* Apply `-0.02em` letter spacing for `display-lg` to maintain density, but use `+0.05em` for `headline-sm` to lean into the premium editorial look.
*   **Body & Labels (Inter):** Used for functional clarity. Inter provides the "architectural" foundation.
    *   *Styling Tip:* Increase line-height to 1.6 for `body-lg` to ensure the "Ethereal" feel persists even in text-heavy sections.

**Typography Scale Highlights:**
*   **Display-LG:** 3.5rem (Lexend) - The "Hero" voice.
*   **Headline-MD:** 1.75rem (Lexend) - Section anchors.
*   **Title-SM:** 1rem (Inter, Medium) - High-utility UI text.
*   **Label-MD:** 0.75rem (Inter, Bold, All-Caps) - Used with `+0.1em` letter spacing for a "Swiss-style" technical aesthetic.

## 4. Elevation & Depth
In this design system, shadows are not used to create "pop"—they are used to simulate soft, natural ambient light.

*   **Ambient Shadows:** For floating elements, use a three-step shadow stack.
    *   *Layer 1:* 0px 4px 20px (4% opacity of `on-surface`)
    *   *Layer 2:* 0px 10px 40px (2% opacity of `on-surface`)
*   **The "Ghost Border" Fallback:** If a border is required for accessibility (e.g., high-contrast mode), use `outline-variant` (#c3c6d7) at **15% opacity**. Never use 100% opaque borders.
*   **Roundedness:** A signature of this system is the "Organic Curve." 
    *   **Default:** `1rem` (16px) for standard components.
    *   **Large (lg):** `2rem` (32px) for main content containers and hero sections.

## 5. Signature Components

### Buttons (The "Polaris" Interaction)
*   **Primary:** Gradient fill (`primary` to `primary-container`), `1rem` corner radius, and a subtle white inner-glow (top-only, 1px, 20% opacity).
*   **Secondary:** `surface-container-high` background with `on-surface` text. No border.
*   **Tertiary:** Transparent background. On hover, transition to `surface-container-low`.

### Cards & Information Architecture
*   **Forbid Dividers:** Do not use `<hr>` tags or lines to separate content. Use the **Spacing Scale** (32px or 48px gaps) or a shift from `surface` to `surface-container-low` to define boundaries.
*   **Photorealism:** When using imagery, apply `xl` (3rem) corner radius. Use a subtle `outline-variant` (10% opacity) inner stroke to ensure the image feels "seated" in the UI.

### Input Fields
*   **State:** Default inputs use `surface-container-low` background. 
*   **Focus State:** Shift to `surface-container-lowest` with a 2px "Ghost Border" of `primary` at 40% opacity. This creates a soft "aura" rather than a hard ring.

## 6. Do's and Don'ts

### Do:
*   **Use Asymmetry:** Offset your headlines to the left while keeping body text centered in a narrower column to create an editorial layout.
*   **Embrace the Void:** If a screen feels "empty," add more padding rather than more features.
*   **Tint Your Neutrals:** Ensure your "on-surface" text (#191c1e) is used for body text, but use "on-surface-variant" (#434655) for secondary metadata to create hierarchy.

### Don't:
*   **Don't use 100% Black:** It breaks the "Ethereal" softness. Use `on-surface`.
*   **Don't use sharp corners:** Even the smallest chip must have at least a `sm` (0.5rem) radius.
*   **Don't crowd the margins:** Ensure a minimum of 40px padding on all major container edges to maintain the premium feel.