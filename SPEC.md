# SPEC.md — Urban Shibuya Style Guide

## Concept

**Urban Shibuya** is a modern minimalist Japanese streetwear aesthetic that channels the raw energy of Shibuya Crossing — the organized chaos of neon lights, bold typography, and unapologetic contrast. It's the visual language of Tokyo's youth culture: sharp, confident, and effortlessly cool. This style guide defines the design system for an anime + clothing ecommerce brand that blends Japanese streetwear boldness with the clean precision of editorial fashion.

The aesthetic is **nocturnal Tokyo energy** — think black asphalt reflections, bold red stoplights, the white glow of convenience stores, and splashes of yellow taxi lights cutting through the darkness.

---

## Design Philosophy

1. **Bold Contrast** — Maximum impact through black/white foundations with strategic red accents
2. **Editorial Precision** — Clean layouts with sharp hierarchy, inspired by high-fashion lookbooks
3. **Streetwear Edge** — Urban texture, bold type, unapologetic presence
4. **Japanese Minimalism** — Every element earns its place; no visual noise

---

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| `--color-black` | `#0D0D0D` | Primary background, dominant surfaces |
| `--color-white` | `#F5F5F0` | Primary text on dark, light backgrounds |
| `--color-red` | `#E63946` | Primary accent, CTAs, highlights |
| `--color-gray` | `#9E9E9E` | Secondary text, muted elements |
| `--color-yellow` | `#FFD60A` | Secondary accent, badges, special callouts |

### Color Meanings

- **Black (#0D0D0D)** — Power, sophistication, the night sky over Tokyo
- **Off-White (#F5F5F0)** — Clean space, breathing room, the calm before the storm
- **Bold Red (#E63946)** — Energy, urgency, the Shibuya crossing signal
- **Warm Gray (#9E9E9E)** — Balance, supporting text, subtle depth
- **Accent Yellow (#FFD60A)** — Highlights, special items, the neon glow of Tokyo taxis

---

## Typography

### Font Stack

- **Headings:** `'Bebas Neue', Impact, Haettenschweiler, sans-serif`
  - All caps, track-tight, maximum impact
  - Use for hero text, section headers, product names
  
- **Body:** `'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif`
  - Clean, modern, highly readable
  - Use for descriptions, UI text, form labels

### Type Scale

| Token | Size | Line Height | Weight | Usage |
|-------|------|-------------|--------|-------|
| `--text-hero` | clamp(3rem, 10vw, 8rem) | 0.9 | 400 | Hero headlines |
| `--text-h1` | clamp(2rem, 5vw, 4rem) | 1.1 | 400 | Page titles |
| `--text-h2` | clamp(1.5rem, 3vw, 2.5rem) | 1.2 | 400 | Section headers |
| `--text-h3` | clamp(1.25rem, 2vw, 1.75rem) | 1.3 | 500 | Card titles |
| `--text-body` | 1rem | 1.6 | 400 | Body copy |
| `--text-small` | 0.875rem | 1.5 | 400 | Captions, metadata |
| `--text-xs` | 0.75rem | 1.4 | 500 | Badges, labels |

### Letter Spacing

- Headings: `0.02em` to `0.05em` (tight, impactful)
- Body: `0` (natural flow)
- ALL CAPS elements: `0.15em` (breathing room between letters)

---

## Design Tokens (CSS Custom Properties)

### Colors

```css
--color-black: #0D0D0D;
--color-white: #F5F5F0;
--color-red: #E63946;
--color-gray: #9E9E9E;
--color-yellow: #FFD60A;
```

### Spacing Scale

| Token | Value | Usage |
|-------|-------|-------|
| `--space-xs` | 0.25rem | Tight spacing, icon gaps |
| `--space-sm` | 0.5rem | Small gaps, padding |
| `--space-md` | 1rem | Standard spacing |
| `--space-lg` | 1.5rem | Section padding |
| `--space-xl` | 2rem | Large gaps |
| `--space-2xl` | 4rem | Section margins |
| `--space-3xl` | 6rem | Hero spacing |

### Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `--radius-sm` | 2px | Subtle rounding |
| `--radius-md` | 4px | Buttons, inputs |
| `--radius-lg` | 8px | Cards, containers |

### Shadows

| Token | Value | Usage |
|-------|-------|-------|
| `--shadow-sm` | 0 2px 4px rgba(0,0,0,0.3) | Subtle elevation |
| `--shadow-md` | 0 4px 12px rgba(0,0,0,0.4) | Cards |
| `--shadow-lg` | 0 8px 24px rgba(0,0,0,0.5) | Modals, hero elements |
| `--shadow-red` | 0 0 20px rgba(230,57,70,0.4) | Red glow effect |

### Transitions

| Token | Value | Usage |
|-------|-------|-------|
| `--transition-fast` | 150ms ease | Micro-interactions |
| `--transition-base` | 250ms ease | Standard transitions |
| `--transition-slow` | 400ms ease | Dramatic effects |

---

## Component Specifications

### Buttons

#### Primary Button
- Background: `--color-white`
- Text: `--color-black`
- Padding: 1rem 2.5rem
- Border: 2px solid `--color-white`
- Hover: Background `--color-red`, border `--color-red`, text white
- Text: UPPERCASE, letter-spacing 0.15em

#### Secondary Button
- Background: transparent
- Text: `--color-white`
- Border: 2px solid `--color-white`
- Hover: Background `--color-white`, text `--color-black`

#### Accent Button
- Background: `--color-red`
- Text: `--color-white`
- Hover: Background `--color-yellow`, text `--color-black`

### Cards

#### Product Card
- Background: `--color-black`
- Border: 1px solid rgba(255,255,255,0.1)
- Hover: Border `--color-red`, shadow `--shadow-red`
- Image aspect ratio: 4:3
- Content: Product image, title (h3), price, "Add to Cart" button

#### Featured Card (Large)
- Full-width or half-width
- Background: gradient overlay on image
- Large typography overlay
- CTA button

### Badges

- `--badge-new`: Yellow background, black text
- `--badge-sale`: Red background, white text
- `--badge-limited`: White background, black text

### Navigation

- Background: `--color-black` with slight transparency
- Logo: Left-aligned, bold
- Links: Right-aligned, uppercase, letter-spacing 0.1em
- Hover: Red underline animation
- Mobile: Hamburger menu with slide-in drawer

### Footer

- Background: `--color-black`
- Three-column layout: Links, Newsletter, Social
- Top border: 2px solid `--color-red`
- Newsletter input with red CTA

### Form Elements

#### Input
- Background: rgba(255,255,255,0.05)
- Border: 1px solid `--color-gray`
- Focus: Border `--color-red`
- Text: `--color-white`
- Placeholder: `--color-gray`

#### Checkbox/Radio
- Custom styled with red accent
- Smooth transition on check

---

## Layout System

### Grid

- Desktop: 12-column grid, 24px gutter
- Tablet: 8-column grid, 20px gutter
- Mobile: 4-column grid, 16px gutter

### Container

- Max-width: 1400px
- Padding: 1.5rem (mobile), 3rem (desktop)
- Centered with auto margins

### Section Spacing

- Section padding: `--space-2xl` vertical
- Component gaps: `--space-lg`
- Related items: `--space-md`

---

## Visual Assets

### Imagery Style
- High contrast, editorial photography
- Urban Tokyo backdrops preferred
- Desaturated with selective color pops
- Anime character art with clean lines

### Icon Style
- Line icons, 2px stroke
- Monochrome or white
- Geometric, minimal

### Decorative Elements
- Diagonal lines and angles
- Bold borders
- Red accent lines
- Glitch effects (subtle)

---

## Animation & Interactions

### Hover Effects
- Cards: Border color shift to red, subtle scale (1.02)
- Buttons: Background color transition, 250ms
- Links: Red underline slide-in from left

### Page Transitions
- Fade-in for content sections
- Staggered animation for product grids

### Micro-interactions
- Button press: Scale down to 0.98
- Add to cart: Pulse animation
- Badge pulse on new items

---

## Responsive Breakpoints

| Breakpoint | Width | Layout Adjustments |
|------------|-------|-------------------|
| Mobile | < 640px | Single column, stacked nav |
| Tablet | 640px - 1024px | 2-column grids |
| Desktop | > 1024px | Full layout, 3-4 column grids |

---

## Usage Guidelines

### Do
- Use black backgrounds for impact sections
- Pair red accents sparingly for maximum effect
- Keep text concise and bold
- Use ALL CAPS for headings
- Maintain generous white space

### Don't
- Overuse red — it loses impact
- Mix with decorative, ornate fonts
- Clutter layouts with too many elements
- Use gradient backgrounds (except overlays)

---

*Version 1.0 — Urban Shibuya Design System*