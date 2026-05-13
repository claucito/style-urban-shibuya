# 🏯 Urban Shibuya — Design System

> Modern minimalist Japanese streetwear aesthetic for anime + clothing ecommerce

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)

---

## Concept

**Urban Shibuya** channels the raw energy of Tokyo's Shibuya Crossing — the organized chaos of neon lights, bold typography, and unapologetic contrast. It's the visual language of Japanese youth culture: sharp, confident, and effortlessly cool.

This design system is built for an anime + streetwear ecommerce brand that blends:
- 🎌 Japanese streetwear boldness
- ✨ Editorial fashion precision  
- 🌃 Nocturnal Tokyo energy
- ⚡ Anime-inspired dynamism

---

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| **Black** | `#0D0D0D` | Primary background, dominant surfaces |
| **Off-White** | `#F5F5F0` | Primary text, light backgrounds |
| **Bold Red** | `#E63946` | Primary accent, CTAs, highlights |
| **Warm Gray** | `#9E9E9E` | Secondary text, muted elements |
| **Accent Yellow** | `#FFD60A` | Secondary accent, badges, special callouts |

### Color Meanings

- **Black (#0D0D0D)** — Power, sophistication, the night sky over Tokyo
- **Off-White (#F5F5F0)** — Clean space, breathing room, the calm before the storm  
- **Bold Red (#E63946)** — Energy, urgency, the Shibuya crossing signal
- **Warm Gray (#9E9E9E)** — Balance, supporting text, subtle depth
- **Accent Yellow (#FFD60A)** — Highlights, special items, the neon glow of Tokyo taxis

---

## Typography

### Font Stack

```css
/* Headings — Bold, Impactful */
font-family: 'Bebas Neue', Impact, Haettenschweiler, sans-serif;

/* Body — Clean, Modern */
font-family: 'DM Sans', -apple-system, BlinkMacSystemFont, sans-serif;
```

### Type Scale

| Class | Size | Usage |
|-------|------|-------|
| `.text-hero` | clamp(3rem, 10vw, 8rem) | Hero headlines |
| `h1` | clamp(2rem, 5vw, 4rem) | Page titles |
| `h2` | clamp(1.5rem, 3vw, 2.5rem) | Section headers |
| `h3` | clamp(1.25rem, 2vw, 1.75rem) | Card titles |
| `.text-body` | 1rem | Body copy |
| `.text-small` | 0.875rem | Captions, metadata |

---

## Quick Start

### 1. Include Fonts

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=DM+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
```

### 2. Include Styles

```html
<link rel="stylesheet" href="styles.css">
```

### 3. Start Building

```html
<body class="has-navbar">
  <nav class="navbar">...</nav>
  
  <section class="hero">...</section>
  
  <section class="products-section">
    <div class="grid grid-cols-4">
      <article class="card">...</article>
    </div>
  </section>
</body>
```

---

## Components

### Buttons

```html
<!-- Primary — White with red hover -->
<button class="btn btn-primary">Shop Now</button>

<!-- Secondary — Outline -->
<button class="btn btn-secondary">Learn More</button>

<!-- Accent — Red background -->
<button class="btn btn-accent">Add to Cart</button>

<!-- Ghost — Minimal -->
<button class="btn btn-ghost">View Details</button>

<!-- Sizes -->
<button class="btn btn-sm">Small</button>
<button class="btn btn-lg">Large</button>
<button class="btn btn-full">Full Width</button>
```

### Cards

```html
<article class="card">
  <div class="card-image">
    <span class="badge badge-new">New</span>
    <img src="..." alt="Product">
  </div>
  <div class="card-content">
    <h3 class="card-title">Product Name</h3>
    <p class="card-text">Description here</p>
    <div class="card-price">¥4,800</div>
    <a href="#" class="btn btn-accent btn-full btn-sm">Add to Cart</a>
  </div>
</article>
```

### Badges

```html
<span class="badge badge-new">New</span>
<span class="badge badge-sale">-20%</span>
<span class="badge badge-limited">Limited</span>
<span class="badge badge-hot">Hot</span>
```

### Hero Section

```html
<section class="hero">
  <div class="hero-background">
    <img src="hero.jpg" alt="">
  </div>
  <div class="container">
    <div class="hero-content">
      <span class="hero-eyebrow">New Season 2026</span>
      <h1 class="hero-title">
        Tokyo Street
        <span class="accent">Revolution</span>
      </h1>
      <p class="hero-description">Description...</p>
      <div class="hero-actions">
        <a href="#" class="btn btn-primary">Shop Now</a>
        <a href="#" class="btn btn-secondary">View Lookbook</a>
      </div>
    </div>
  </div>
</section>
```

### Forms

```html
<div class="form-group">
  <label class="form-label">Email</label>
  <input type="email" class="form-input" placeholder="Enter email">
</div>

<label class="form-check">
  <input type="checkbox" class="form-check-input">
  <span class="form-check-label">Remember me</span>
</label>
```

### Navigation

```html
<nav class="navbar">
  <div class="navbar-container">
    <a href="#" class="navbar-logo">Urban<span>Shibuya</span></a>
    <ul class="navbar-nav">
      <li><a href="#" class="navbar-link">Home</a></li>
      <li><a href="#" class="navbar-link">Collection</a></li>
    </ul>
    <div class="navbar-actions">
      <a href="#" class="navbar-icon"><i class="fas fa-search"></i></a>
      <a href="#" class="navbar-icon"><i class="fas fa-shopping-bag"></i></a>
    </div>
    <button class="navbar-toggle">
      <span></span><span></span><span></span>
    </button>
  </div>
</nav>
```

---

## CSS Custom Properties

All design tokens are defined as CSS variables:

```css
:root {
  /* Colors */
  --color-black: #0D0D0D;
  --color-white: #F5F5F0;
  --color-red: #E63946;
  --color-gray: #9E9E9E;
  --color-yellow: #FFD60A;
  
  /* Spacing */
  --space-xs: 0.25rem;
  --space-sm: 0.5rem;
  --space-md: 1rem;
  --space-lg: 1.5rem;
  --space-xl: 2rem;
  --space-2xl: 4rem;
  --space-3xl: 6rem;
  
  /* Typography */
  --font-heading: 'Bebas Neue', Impact, sans-serif;
  --font-body: 'DM Sans', sans-serif;
  
  /* Transitions */
  --transition-fast: 150ms ease;
  --transition-base: 250ms ease;
  --transition-slow: 400ms ease;
  
  /* Shadows */
  --shadow-sm: 0 2px 4px rgba(0,0,0,0.3);
  --shadow-md: 0 4px 12px rgba(0,0,0,0.4);
  --shadow-lg: 0 8px 24px rgba(0,0,0,0.5);
  --shadow-red: 0 0 30px rgba(230, 57, 70, 0.5);
}
```

---

## Layout Classes

### Grid System

```html
<div class="grid grid-cols-4 gap-lg">
  <!-- 4 columns on desktop, 2 on tablet, 1 on mobile -->
</div>

<div class="grid grid-cols-3"><!-- 3 columns --></div>
<div class="grid grid-cols-2"><!-- 2 columns --></div>
<div class="grid grid-cols-1"><!-- 1 column --></div>
```

### Container

```html
<div class="container">
  <!-- Centered, max-width 1400px, responsive padding -->
</div>
```

### Section Spacing

```html
<section class="section">...</section>        <!-- 6rem vertical padding -->
<section class="section-sm">...</section>     <!-- 4rem vertical padding -->
<section class="section-lg">...</section>     <!-- 8rem vertical padding -->
```

---

## Utility Classes

### Text

```html
<span class="text-red">Red text</span>
<span class="text-yellow">Yellow text</span>
<span class="text-gray">Gray text</span>
<span class="text-uppercase">UPPERCASE</span>
<span class="text-center">Centered</span>
```

### Spacing

```html
<div class="mb-md">margin-bottom: 1rem</div>
<div class="mb-xl">margin-bottom: 2rem</div>
<div class="mt-lg">margin-top: 1.5rem</div>
<div class="p-md">padding: 1rem</div>
<div class="gap-md">gap: 1rem</div>
```

### Display

```html
<div class="flex">display: flex</div>
<div class="flex-col">flex-direction: column</div>
<div class="items-center">align-items: center</div>
<div class="justify-between">justify-content: space-between</div>
<div class="hidden">display: none</div>
```

---

## Animation Classes

```html
<div class="animate-fadeIn">Fades in</div>
<div class="animate-fadeInUp">Fades in and moves up</div>
<div class="animate-slideInLeft">Slides in from left</div>
<div class="animate-slideInRight">Slides in from right</div>

<!-- Staggered delays -->
<div class="animate-fadeInUp delay-100">100ms delay</div>
<div class="animate-fadeInUp delay-200">200ms delay</div>
<div class="animate-fadeInUp delay-300">300ms delay</div>
```

---

## Browser Support

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

---

## License

MIT © 2026 Urban Shibuya

---

## Files

```
style-urban-shibuya/
├── SPEC.md        # Full design specification
├── styles.css     # Complete CSS with custom properties
├── index.html     # Showcase page with all components
└── README.md      # This file
```