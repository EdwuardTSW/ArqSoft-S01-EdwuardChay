# Dk Bikes - Design System

## Direction & Feel

**Product:** Motorcycle catalog web app (ASP.NET Core MVC)

**Feel:** Dark, premium, automotive. Think showroom floor at night — polished surfaces, dramatic accent lighting, focused attention on the machines.

**Intent:** The user is a motorcycle enthusiast browsing a dealer catalog. They want to feel the power and prestige of each bike. The interface should feel like a luxury showroom, not a generic e-commerce site.

**Signature:** The dark glassmorphism cards with the red-to-black accent gradient. The subtle grid overlay on the background that fades out. The motorcycle badge positioned over the image like a showroom sticker.

---

## Color World

The physical space this product lives in: a premium motorcycle dealership showroom at night. Polished black floors, red accent lighting, chrome reflections, warm spotlights on the bikes.

**Palette (Dark Mode Only):**
- `#0a0a0f` - Deep showroom floor
- `#12121a` - Elevated surfaces (display stands)
- `#1c1c28` - Cards and panels
- `#262634` - Higher elevation (dropdowns, popovers)
- `#303040` - Highest elevation (tooltips, menus)
- `#e8e8ec` - Primary text (spotlight white)
- `#a0a0b0` - Secondary text (ambient light)
- `#707080` - Tertiary text (shadowed corners)
- `#505060` - Muted text (recessed areas)
- `#c41e3a` - Primary accent (brake caliper red)
- `#b8983d` - Gold accent (chrome warmth)

---

## Depth Strategy

**Borders-only with subtle backdrop blur.** No drop shadows in dark mode — they don't read well on dark backgrounds. Instead, use:
- Subtle rgba borders (`rgba(255,255,255,0.04)` to `rgba(255,255,255,0.14)`)
- Backdrop-filter blur for glassmorphism
- Surface elevation through lighter backgrounds (not shadows)
- Gradient overlays on cards for depth

**Elevation Scale (Dark Mode):**
- Level 0: `--surface-0` (#0a0a0f) - Base background
- Level 1: `--surface-100` (#12121a) - Cards, panels
- Level 2: `--surface-200` (#1c1c28) - Dropdowns, popovers
- Level 3: `--surface-300` (#262634) - Nested dropdowns
- Level 4: `--surface-400` (#303040) - Tooltips, highest

---

## Spacing System

**Base Unit:** 4px

```
--space-1: 0.25rem  (4px)
--space-2: 0.5rem   (8px)
--space-3: 0.75rem  (12px)
--space-4: 1rem     (16px)
--space-6: 1.5rem   (24px)
--space-8: 2rem     (32px)
--space-12: 3rem    (48px)
--space-16: 4rem    (64px)
```

**Usage:**
- Micro spacing: icon gaps, tight pairs → `--space-1` to `--space-2`
- Component spacing: within buttons, inputs, cards → `--space-3` to `--space-4`
- Section spacing: between related groups → `--space-6` to `--space-8`
- Major separation: between distinct areas → `--space-12` to `--space-16`

---

## Border Radius Scale

```
--radius-sm: 8px    (inputs, small buttons)
--radius-md: 14px   (buttons, badges)
--radius-lg: 20px   (cards)
--radius-xl: 28px   (large cards, panels)
--radius-full: 999px (pills, chips)
```

---

## Typography

**Font Family:** `'Inter', Segoe UI, system-ui, -apple-system, BlinkMacSystemFont, sans-serif`

**Hierarchy:**
- **Headlines:** Weight 900, tight letter-spacing (-0.06em), line-height 0.95
- **Body:** Weight 400-600, comfortable size, line-height 1.75
- **Labels/UI:** Weight 700-800, uppercase with letter-spacing (0.04em-0.2em)
- **Data/Numbers:** Weight 900, tabular numbers, letter-spacing -0.04em

---

## Key Component Patterns

### Moto Card
```
Background: linear-gradient(180deg, var(--surface-200), var(--surface-100))
Border: 1px solid var(--border-default)
Border-radius: var(--radius-xl) (28px)
Box-shadow: var(--shadow-lg)
Backdrop-filter: blur(14px)
Hover: translateY(-6px), border-color accent at 35% opacity
Transition: transform 0.3s cubic-bezier(0.34, 1.56, 0.64, 1)
```

### Filter Chip
```
Default: var(--surface-200), transparent border, var(--text-secondary)
Hover: var(--surface-300), var(--border-default), var(--text-primary)
Active: var(--accent), var(--accent), var(--text-primary), glow shadow
Border-radius: var(--radius-full)
```

### Button Primary
```
Background: linear-gradient(135deg, var(--accent), #991b1b)
Color: var(--text-primary)
Border-radius: var(--radius-full)
Box-shadow: 0 16px 40px var(--accent-glow)
Hover: translateY(-2px), brighten filter, larger shadow
```

### Form Control
```
Background: var(--surface-200)
Border: 1px solid var(--border-default)
Border-radius: var(--radius-lg) (20px)
Focus: var(--accent) border, 3px glow ring, var(--surface-300) bg
Hover: var(--border-strong), var(--surface-300)
```

### Detail Card
```
Background: linear-gradient(180deg, var(--surface-200), var(--surface-100))
Border: 1px solid var(--border-default)
Border-radius: var(--radius-xl)
Box-shadow: var(--shadow-lg)
Backdrop-filter: blur(14px)
```

---

## Accessibility

- Minimum contrast ratio: 4.5:1 for body text
- All interactive elements have `:focus-visible` states with 2-3px outline
- `prefers-reduced-motion` respected (animations disabled)
- `prefers-color-scheme` not used (app is dark-only by design)
- Semantic HTML structure maintained

---

## Animation

**Easing:** `cubic-bezier(0.34, 1.56, 0.64, 1)` for bouncy micro-interactions, `cubic-bezier(0.16, 1, 0.3, 1)` for fade-ins
**Durations:** 150-250ms for micro-interactions, 200-300ms for larger transitions
**Fade-in-up:** opacity 0→1, translateY(20px→0), 0.6s ease
**Stagger:** 50ms increments for card grids

---

## Background Effect

The signature background uses:
1. Base color: `--bg` (#0a0a0f)
2. Radial gradient 1: red accent at 6% opacity, top-left
3. Radial gradient 2: gold accent at 4% opacity, bottom-right
4. Subtle grid overlay: 48px grid with 1.2% white lines, fading to transparent at 85%

This creates the "showroom floor at night" atmosphere without being distracting.

---

## Logo Treatment

The Dk Bikes logo is displayed as an image in the navbar and footer:
- Navbar: 44px, with drop-shadow glow on hover
- Footer: 32px, smaller variant
- Both versions get scale(1.05) and enhanced glow on hover
- The logo's black background blends seamlessly with the dark UI

---

*Last updated: 2026-05-07*
