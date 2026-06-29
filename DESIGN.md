---
name: Cyber-Circuit Aesthetic
colors:
  surface: '#131313'
  surface-dim: '#131313'
  surface-bright: '#3a3939'
  surface-container-lowest: '#0e0e0e'
  surface-container-low: '#1c1b1b'
  surface-container: '#201f1f'
  surface-container-high: '#2a2a2a'
  surface-container-highest: '#353534'
  on-surface: '#e5e2e1'
  on-surface-variant: '#e5bcc5'
  inverse-surface: '#e5e2e1'
  inverse-on-surface: '#313030'
  outline: '#ac878f'
  outline-variant: '#5c3f46'
  surface-tint: '#ffb1c4'
  primary: '#ffb1c4'
  on-primary: '#65002e'
  primary-container: '#ff4a8d'
  on-primary-container: '#590028'
  inverse-primary: '#ba005b'
  secondary: '#dcfdff'
  on-secondary: '#00373a'
  secondary-container: '#00f1fd'
  on-secondary-container: '#006a6f'
  tertiary: '#00e639'
  on-tertiary: '#003907'
  tertiary-container: '#00a827'
  on-tertiary-container: '#003205'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#ffd9e1'
  primary-fixed-dim: '#ffb1c4'
  on-primary-fixed: '#3f001a'
  on-primary-fixed-variant: '#8f0044'
  secondary-fixed: '#6ff6ff'
  secondary-fixed-dim: '#00dce6'
  on-secondary-fixed: '#002022'
  on-secondary-fixed-variant: '#004f53'
  tertiary-fixed: '#72ff70'
  tertiary-fixed-dim: '#00e639'
  on-tertiary-fixed: '#002203'
  on-tertiary-fixed-variant: '#00530e'
  background: '#131313'
  on-background: '#e5e2e1'
  surface-variant: '#353534'
typography:
  display-lg:
    fontFamily: sora
    fontSize: 64px
    fontWeight: '800'
    lineHeight: '1.1'
    letterSpacing: -0.02em
  display-lg-mobile:
    fontFamily: sora
    fontSize: 40px
    fontWeight: '800'
    lineHeight: '1.1'
  headline-lg:
    fontFamily: sora
    fontSize: 32px
    fontWeight: '700'
    lineHeight: '1.2'
    letterSpacing: 0.05em
  headline-md:
    fontFamily: sora
    fontSize: 24px
    fontWeight: '700'
    lineHeight: '1.2'
  body-lg:
    fontFamily: spaceMono
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
  body-md:
    fontFamily: spaceMono
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.6'
  label-sm:
    fontFamily: jetbrainsMono
    fontSize: 12px
    fontWeight: '500'
    lineHeight: '1.0'
    letterSpacing: 0.1em
spacing:
  unit: 4px
  gutter: 24px
  margin-desktop: 64px
  margin-mobile: 16px
  container-max: 1440px
---

## Brand & Style
The design system is engineered for the high-octane world of digital content creation, blending **Cyberpunk** grit with high-fidelity functionalism. It targets an audience that thrives in digital subcultures, gaming, and creative tech. The UI evokes a "terminal-of-the-future" feeling—high-performance, slightly dangerous, and intensely immersive.

The style is a hybrid of **Cyber-Brutalism** and **Glassmorphism**. It utilizes heavy contrast, sharp geometric cuts, and luminous "light-bleed" effects to simulate a physical HUD (Heads-Up Display). The interface should feel like a living machine, utilizing motion and light to guide the user through complex workflows.

## Colors
This design system operates exclusively in a high-contrast dark mode to maximize the impact of neon luminescence.

- **Deep Obsidian (#050505):** The foundation. Used for large surface areas to create an "infinite void" effect.
- **Neon Pink (#ff007f):** Action and energy. Reserved for primary calls-to-action, critical alerts, and brand highlights.
- **Electric Cyan (#00f3ff):** Information and telemetry. Used for secondary actions, data visualization, and links.
- **Acid Green (#00ff41):** Status and success. Used for system confirmations, "Online" indicators, and terminal-style accents.
- **Functional Alpha:** Use semi-transparent versions of these colors (10-20% opacity) for background washes and glass panels.

## Typography
Typography is split between aggressive, geometric display faces and technical, monospaced functional text.

- **Headlines:** Use **Sora** in extra-bold weights. All-caps is preferred for primary navigation and display headers to enhance the futuristic, industrial feel.
- **Body Text:** Use **Space Mono**. This maintains the "hacker" aesthetic while ensuring readability for long-form content. 
- **System Labels:** Use **JetBrains Mono** for metadata, timestamps, and small UI labels. These should often be uppercase with increased letter spacing to mimic serial numbers or hardware tags.

## Layout & Spacing
The layout follows a rigid 12-column grid but encourages "breaking" the grid with absolute-positioned decorative elements (like scanline overlays). 

- **Grid:** Use a fluid grid with generous gutters (24px) to allow components to breathe despite their high visual weight.
- **Rhythm:** All spacing must be multiples of 4px. Use larger gaps (48px+) between distinct sections to prevent the high-contrast elements from feeling cluttered.
- **Asymmetry:** Encourage slight horizontal offsets or diagonal alignments in layout containers to reinforce the "glitch" aesthetic.

## Elevation & Depth
Depth is not achieved through realistic shadows, but through **light emission** and **transparency**.

- **Z-Axis Hierarchy:** Higher elevation elements do not cast black shadows; they emit a colored glow (drop-shadow with 15-30px blur using the component’s accent color at 30% opacity).
- **Glassmorphism:** Use `backdrop-filter: blur(20px)` on semi-transparent panels. This creates a sense of "layered HUD" windows over a digital background.
- **Scanlines:** A global overlay of 1px horizontal lines (black at 5% opacity) should be applied to the entire viewport or specific "active" panels to simulate a CRT monitor.

## Shapes
The shape language is strictly **geometric and sharp**. Avoid all rounded corners.

- **Angled Cuts:** Use CSS `clip-path` to create 45-degree "dog-ear" cuts on the corners of buttons and containers.
- **Borders:** Containers should have 1px solid borders. Use "double borders" (a 1px border with a 2px offset secondary border) for primary containers.
- **Dividers:** Horizontal rules should often terminate in a small square or a 45-degree angled tip rather than a flat end.

## Components
- **Buttons:** Sharp corners with a 45-degree cut on the top-right and bottom-left. Primary buttons use a solid Neon Pink fill with a Cyan "outer glow" on hover.
- **Input Fields:** Deep Obsidian background with a 1px Cyan bottom border. On focus, the border flashes Acid Green and a subtle scanline animation scrolls through the input area.
- **Cards/Panels:** Semi-transparent (80% opacity) Obsidian background with heavy backdrop blur. A 1px border in Cyan or Pink is mandatory. Add decorative "L-shaped" corner brackets to reinforce the frame.
- **Chips/Tags:** Monospace text enclosed in a solid block of color with the text knocked out in Obsidian. Use for categories or status tags.
- **Glitch Elements:** On hover or state change, components should briefly "glitch"—a rapid 2px horizontal displacement combined with a momentary color shift to secondary accents.
- **Data Visuals:** Progress bars should be segmented (blocky) rather than smooth gradients, mimicking old-school loading sequences.