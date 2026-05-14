# ☕ BeanCraft Coffe — Frontend Build Plan

_Format: HTML + CSS Only | Audience: AI Agent | Phase-Based Execution_

---

## 📑 Table of Contents

1. [🎨 Global Design Tokens](#-global-design-tokens)
2. [📁 File Structure](#-file-structure)
3. [🚀 Phase 1 — Foundation: Tokens, Reset & Layout System](#-phase-1--foundation-tokens-reset--layout-system)
4. [🧭 Phase 2 — Navigation & Hero Section](#-phase-2--navigation--hero-section)
5. [🛍️ Phase 3 — Product Section & Explore Section](#%EF%B8%8F-phase-3--product-section--explore-section)
6. [⭐ Phase 4 — Bestseller Section & Testimonials Section](#-phase-4--bestseller-section--testimonials-section)
7. [🤝 Phase 5 — Subscribe Section, Trusted By & Footer](#-phase-5--subscribe-section-trusted-by--footer)
8. [📱 Phase 6 — Responsive Behavior](#-phase-6--responsive-behavior)
9. [✅ Master Acceptance Checklist](#-master-acceptance-checklist)

---

## 🎨 Global Design Tokens

> **Note:** Every agent session must include this block as the authoritative reference.

```css
/* Colors */
--color-background: #faf6f1;
--color-primary: #4a2c2a;
--color-secondary: #d4a96a;
--color-accent: #6b7f5e;
--color-text-dark: #1e1e1e;
--color-text-muted: #7a6a5a;
--color-white: #ffffff;
--color-card-bg: #f5efe6;
--color-border: #e8ddd0;

/* Typography */
--font-heading: "Playfair Display", serif;
--font-body: "Inter", sans-serif;

--font-size-xs: 0.75rem;
--font-size-sm: 0.875rem;
--font-size-base: 1rem;
--font-size-md: 1.125rem;
--font-size-lg: 1.5rem;
--font-size-xl: 2rem;
--font-size-2xl: 2.75rem;
--font-size-3xl: 3.5rem;

/* Spacing */
--spacing-xs: 4px;
--spacing-sm: 8px;
--spacing-md: 16px;
--spacing-lg: 24px;
--spacing-xl: 40px;
--spacing-2xl: 64px;
--spacing-3xl: 96px;

/* Shape */
--radius-sm: 4px;
--radius-md: 8px;
--radius-lg: 16px;
--radius-full: 9999px;

/* Elevation */
--shadow-card: 0 2px 12px rgba(74, 44, 42, 0.08);
--shadow-hover: 0 4px 20px rgba(74, 44, 42, 0.14);

/* Layout */
--max-width: 1200px;
--gutter: 24px;
```

---

## 📁 File Structure

> **Note:** All agents must respect this structure. Do not create files outside it.

```text
/bean-craft/
├── index.html
└── css/
    ├── tokens.css          ← Phase 1
    ├── layout.css          ← Phase 1
    ├── nav.css             ← Phase 2
    ├── hero.css            ← Phase 2
    ├── products.css        ← Phase 3
    ├── explore.css         ← Phase 3
    ├── bestseller.css      ← Phase 4
    ├── testimonials.css    ← Phase 4
    ├── subscribe.css       ← Phase 5
    ├── trusted.css         ← Phase 5
    ├── footer.css          ← Phase 5
    └── responsive.css      ← Phase 6
```

---

## 🚀 Phase 1 — Foundation: Tokens, Reset & Layout System

### Agent Task

Build the CSS foundation that all future phases depend on.
**Output:** okens.css, layout.css, and the base index.html shell.
_No visible sections are produced in this phase beyond a warm cream background._

### okens.css

Define all CSS custom properties using the exact variable names from the Global Design Tokens block above.

Apply a CSS reset:

- `box-sizing: border-box` on all elements via the universal selector
- Zero margin and padding on `html` and `body`
- `max-width: 100%` on `img` elements
- `display: block` on `img`

Apply base body styles:

- `background-color: var(--color-background)`
- `font-family: var(--font-body)`
- `color: var(--color-text-dark)`
- `line-height: 1.6`
- `-webkit-font-smoothing: antialiased`

### layout.css

Define the following utility and structural classes:

- .container
  - max-width: var(--max-width)
  - margin: 0 auto
  - padding-inline: var(--gutter)

- .section
  - padding-block: var(--spacing-3xl)

- .grid
  - display: grid
  - grid-template-columns: repeat(12, 1fr)
  - gap: var(--gutter)

- .grid-2 — shortcut for repeat(2, 1fr)
- .grid-3 — shortcut for repeat(3, 1fr)
- .grid-4 — shortcut for repeat(4, 1fr)

- .flex-center
  - display: flex
  - lign-items: center
  - justify-content: center

- .text-center
  -     ext-align: center

- .sr-only
  - Accessibility utility: positions element off-screen without display:none

### index.html shell

- **DOCTYPE**: html5, lang="en"
- **Meta**: charset UTF-8, viewport with width=device-width, initial-scale=1
- **Title**: Bean & Craft Coffee
- **Google Fonts link**: Playfair Display (weights 400, 700) and Inter (weights 400, 500, 600)
- **Link all CSS files in this exact order**:
  okens.css → layout.css →
  av.css → hero.css → products.css → xplore.css → estseller.css → estimonials.css → subscribe.css → rusted.css → ooter.css →
  esponsive.css

Body must contain the following semantic shell — empty, no content yet:

```html
<header class="site-header"></header>
<main>
  <section class="hero-section"></section>
  <section class="products-section"></section>
  <section class="explore-section"></section>
  <section class="bestseller-section"></section>
  <section class="testimonials-section"></section>
  <section class="subscribe-section"></section>
  <section class="trusted-section"></section>
</main>
<footer class="site-footer"></footer>
```

### 🛑 Constraints

- No JavaScript
- No visible output beyond the background color
- Variable names must match the Global Design Tokens block exactly — future phases depend on them

---

## 🧭 Phase 2 — Navigation & Hero Section

### Agent Context

Phase 1 is complete. okens.css, layout.css, and the index.html shell exist.
**Task:** Build the navigation bar and hero section.
**Output:**
av.css, hero.css, and filled HTML inside .site-header and .hero-section.

_Paste the Global Design Tokens block at the top of this prompt as your reference._

### Navigation — .site-header

### HTML structure inside:

```html
<header class="site-header">
  <nav class="navbar">
    <div class="navbar__container container">
      <a class="navbar__logo" href="#">Bean & Craft Coffee</a>
      <ul class="navbar__links">
        <li><a href="#">Shop</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Brewing Guide</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
      <div class="navbar__cta">
        <button class="btn-primary" type="button">Shop Now</button>
      </div>
    </div>
  </nav>
</header>
```

### CSS — av.css:

- .site-header
  - position: sticky, op: 0, z-index: 100
  - ackground: var(--color-background)
  - order-bottom: 1px solid var(--color-border)

- .navbar\_\_container
  - display: flex, lign-items: center, justify-content: space-between
  - height: 72px

- .navbar\_\_logo
  - ont-family: var(--font-heading)
  - ont-size: var(--font-size-lg)
  - color: var(--color-primary)
  - ont-weight: 700, ext-decoration: none

- .navbar\_\_links
  - display: flex, gap: var(--spacing-xl)
  - list-style: none, margin: 0, padding: 0

- .navbar\_\_links a
  - ont-size: var(--font-size-sm)
  - color: var(--color-text-muted)
  -     ext-decoration: none
  -     ransition: color 0.2s — hover color: var(--color-primary)

- .btn-primary _(shared button component, define here, reuse in all sections)_
  - ackground: var(--color-primary)
  - color: var(--color-white)
  - padding: 10px 22px
  - order-radius: var(--radius-full)
  - ont-size: var(--font-size-sm)
  - ont-weight: 600
  - order: none, cursor: pointer
  -     ransition: opacity 0.2s — hover: opacity: 0.88

### Hero Section — .hero-section

Content:

- **Headline**: "Handcrafted Coffee, Brewed with Soul"
- **Subheadline**: "Discover small-batch roasted coffee beans sourced ethically and crafted for your perfect morning ritual."
- **Primary CTA button**: "Shop Now"
- **Secondary CTA**: "Explore Beans" (text link style)
- **Image**: placeholder div or img with a warm coffee lifestyle image

### HTML structure inside :

```html
<section class="hero-section">
  <div class="container">
    <div class="hero__inner">
      <div class="hero__content">
        <h1 class="hero__headline">Handcrafted Coffee, Brewed with Soul</h1>
        <p class="hero__subheadline">...</p>
        <div class="hero__actions">
          <button class="btn-primary" type="button">Shop Now</button>
          <a class="btn-text" href="#">Explore Beans</a>
        </div>
      </div>
      <div class="hero__visual">
        <div class="hero__image-wrapper">
          <img src="images/hero.jpg" alt="Freshly roasted coffee beans" />
        </div>
      </div>
    </div>
  </div>
</section>
```

### CSS — hero.css:

- .hero-section
  - min-height: 90vh
  - ackground: var(--color-background)
  - display: flex, lign-items: center
  - padding-block: var(--spacing-2xl)

- .hero\_\_inner
  - display: grid
  - grid-template-columns: 1fr 1fr
  - gap: var(--spacing-2xl)
  - lign-items: center

- .hero\_\_headline
  - ont-family: var(--font-heading)
  - ont-size: var(--font-size-3xl)
  - color: var(--color-primary)
  - line-height: 1.15, ont-weight: 700
  - margin-bottom: var(--spacing-md)

- .hero\_\_subheadline
  - ont-size: var(--font-size-md)
  - color: var(--color-text-muted)
  - line-height: 1.7, max-width: 480px
  - margin-bottom: var(--spacing-xl)

- .hero\_\_actions
  - display: flex, gap: var(--spacing-md), lign-items: center

- .btn-text
  - color: var(--color-primary)
  - ont-weight: 600, ont-size: var(--font-size-sm)
  -     ext-decoration: underline
  - cursor: pointer

- .hero\_\_image-wrapper
  - width: 100%, spect-ratio: 4 / 5
  - order-radius: var(--radius-lg)
  - overflow: hidden
  - ackground: var(--color-card-bg)
  - ox-shadow: var(--shadow-card)

- .hero\_\_image-wrapper img
  - width: 100%, height: 100%, object-fit: cover

### 🛑 Constraints

- No JavaScript
- .btn-primary styles defined here are the shared component used across all phases
- Hero image wrapper must hold its aspect ratio without JavaScript

---

## 🛍️ Phase 3 — Product Section & Explore Section

### Agent Context

Phases 1 and 2 are complete. Navigation and hero are built.
**Task:** Build the Product Section and Explore Section.
**Output:** products.css, xplore.css, and filled HTML inside .products-section and .explore-section.

_Paste the Global Design Tokens block at the top of this prompt as your reference._

### Product Section — .products-section

Content — 3 product cards:

1. Ethiopian Light Roast | | "Bright and floral with citrus notes." | Badge: Freshly Roasted
2. Colombian Medium Roast | | "Smooth, balanced, and chocolatey." | Badge: Bestseller
3. Brazil Dark Roast | | "Bold, rich, and full-bodied." | Badge: Limited Roast

### HTML structure:

```html
<section class="products-section">
  <div class="container">
    <div class="section-header">
      <span class="section-label">Our Collection</span>
      <h2 class="section-title">Freshly Roasted, Ready to Brew</h2>
    </div>
    <div class="products-grid">
      <div class="product-card">
        <div class="product-card__image"><img src="..." alt="..." /></div>
        <span class="product-card__badge">Freshly Roasted</span>
        <h3 class="product-card__name">Ethiopian Light Roast</h3>
        <p class="product-card__description">
          Bright and floral with citrus notes.
        </p>
        <div class="product-card__footer">
          <span class="product-card__price"></span>
          <button class="btn-outline" type="button">Add to Cart</button>
        </div>
      </div>
      <!-- Repeat for remaining 2 cards -->
    </div>
  </div>
</section>
```

### CSS — products.css:

- .products-section
  - ackground: var(--color-background)
  - padding-block: var(--spacing-3xl)

- .section-header
  -     ext-align: center, margin-bottom: var(--spacing-2xl)

- .section-label
  - display: block
  - ont-size: var(--font-size-xs)
  - ont-weight: 600, letter-spacing: 0.12em
  -     ext-transform: uppercase
  - color: var(--color-accent)
  - margin-bottom: var(--spacing-sm)

- .section-title
  - ont-family: var(--font-heading)
  - ont-size: var(--font-size-2xl)
  - color: var(--color-primary)

- .products-grid
  - display: grid
  - grid-template-columns: repeat(3, 1fr)
  - gap: var(--spacing-xl)

- .product-card
  - ackground: var(--color-card-bg)
  - order-radius: var(--radius-lg)
  - overflow: hidden
  - ox-shadow: var(--shadow-card)
  -     ransition: box-shadow 0.2s — hover: var(--shadow-hover)

- .product-card\_\_image
  - width: 100%, spect-ratio: 1 / 1
  - ackground: var(--color-border)
  - overflow: hidden
  - Inner img: width: 100%, height: 100%, object-fit: cover

- .product-card\_\_badge
  - display: inline-block
  - ackground: var(--color-primary), color: var(--color-white)
  - ont-size: var(--font-size-xs), ont-weight: 600
  - padding: 4px 12px
  - order-radius: var(--radius-full)
  - margin: var(--spacing-md) var(--spacing-md) 0

- .product-card\_\_name
  - ont-family: var(--font-heading)
  - ont-size: var(--font-size-lg)
  - color: var(--color-primary)
  - padding: var(--spacing-sm) var(--spacing-md) 0

- .product-card\_\_description
  - ont-size: var(--font-size-sm)
  - color: var(--color-text-muted)
  - line-height: 1.6
  - padding: var(--spacing-xs) var(--spacing-md) var(--spacing-md)

- .product-card\_\_footer
  - display: flex, justify-content: space-between, lign-items: center
  - padding: var(--spacing-md)
  - order-top: 1px solid var(--color-border)

- .product-card\_\_price
  - ont-size: var(--font-size-md), ont-weight: 600
  - color: var(--color-primary)

- .btn-outline _(shared component, define here)_
  - ackground: transparent
  - order: 1.5px solid var(--color-primary)
  - color: var(--color-primary)
  - padding: 8px 16px
  - order-radius: var(--radius-full)
  - ont-size: var(--font-size-xs), ont-weight: 600
  - cursor: pointer
  - Hover: fill background with var(--color-primary), color var(--color-white)

### Explore Section — .explore-section

#### Content — 3 explore cards:

1. **Sourcing** | "Ethically sourced from trusted farms worldwide."
2. **Roasting** | "Small-batch roasting to preserve peak flavor."
3. **Brewing** | "Inspiration and guides for your perfect cup."

### HTML structure:

```html
<section class="explore-section">
  <div class="container">
    <div class="section-header">
      <span class="section-label">Discover</span>
      <h2 class="section-title">Explore Coffee Crafted for Everyday Moments</h2>
    </div>
    <p class="explore__intro">
      A warm and inviting selection of coffees made for people who value taste,
      ritual, and quality.
    </p>
    <div class="explore-grid">
      <div class="explore-card">
        <div class="explore-card__icon"></div>
        <h3 class="explore-card__title">Sourcing</h3>
        <p class="explore-card__text">
          Ethically sourced from trusted farms worldwide.
        </p>
      </div>
      <!-- Repeat for Roasting and Brewing -->
    </div>
  </div>
</section>
```

### CSS — xplore.css:

- .explore-section
  - ackground: var(--color-card-bg)
  - padding-block: var(--spacing-3xl)

- .explore\_\_intro
  - ont-size: var(--font-size-md)
  - color: var(--color-text-muted)
  - line-height: 1.7, ext-align: center
  - max-width: 600px, margin: 0 auto var(--spacing-2xl)

- .explore-grid
  - display: grid
  - grid-template-columns: repeat(3, 1fr)
  - gap: var(--spacing-xl)

- .explore-card
  - ackground: var(--color-background)
  - order-radius: var(--radius-lg)
  - padding: var(--spacing-xl)
  -     ext-align: center
  - ox-shadow: var(--shadow-card)
  -     ransition: box-shadow 0.2s — hover: var(--shadow-hover)

- .explore-card\_\_icon
  - width: 48px, height: 48px
  - ackground: var(--color-primary)
  - order-radius: var(--radius-full)
  - margin: 0 auto var(--spacing-md)

- .explore-card\_\_title
  - ont-family: var(--font-heading)
  - ont-size: var(--font-size-lg)
  - color: var(--color-primary)
  - margin-bottom: var(--spacing-sm)

- .explore-card\_\_text
  - ont-size: var(--font-size-sm)
  - color: var(--color-text-muted)
  - line-height: 1.6

---

## ⭐ Phase 4 — Bestseller Section & Testimonials Section

### Agent Context

Phases 1–3 are complete. Product and Explore sections are built.
**Task:** Build the Bestseller Section and Testimonials Section.
**Output:** estseller.css, estimonials.css, and filled HTML inside .bestseller-section and .testimonials-section.

_Paste the Global Design Tokens block at the top of this prompt as your reference._
_.btn-primary and .btn-outline are already defined in previous CSS files — do not redefine them._

### Bestseller Section — .bestseller-section

Content — 2 featured bestseller cards:

1. Colombian Medium Roast | | "Our most popular blend — smooth, balanced, and endlessly satisfying." | Badge: #1 Bestseller
2. Ethiopian Light Roast | | "A bright and delicate roast with floral, citrus complexity." | Badge: Staff Pick

### HTML structure:

```html
<section class="bestseller-section">
  <div class="container">
    <div class="section-header">
      <span class="section-label">Most Loved</span>
      <h2 class="section-title">Our Bestsellers</h2>
    </div>
    <div class="bestseller-grid">
      <div class="bestseller-card">
        <div class="bestseller-card__image"><img src="..." alt="..." /></div>
        <span class="bestseller-card__badge">#1 Bestseller</span>
        <div class="bestseller-card__content">
          <h3 class="bestseller-card__name">Colombian Medium Roast</h3>
          <p class="bestseller-card__description">Our most popular blend...</p>
          <div class="bestseller-card__footer">
            <span class="bestseller-card__price"></span>
            <button class="btn-primary" type="button">Shop Now</button>
          </div>
        </div>
      </div>
      <!-- Repeat for second card -->
    </div>
  </div>
</section>
```

### CSS — estseller.css:

- .bestseller-section
  - ackground: var(--color-background)
  - padding-block: var(--spacing-3xl)

- .bestseller-grid
  - display: grid
  - grid-template-columns: repeat(2, 1fr)
  - gap: var(--spacing-2xl)

- .bestseller-card
  - ackground: var(--color-card-bg)
  - order-radius: var(--radius-lg)
  - overflow: hidden
  - ox-shadow: var(--shadow-card)
  - display: flex, lex-direction: column

- .bestseller-card\_\_image
  - width: 100%, spect-ratio: 16 / 9
  - ackground: var(--color-border), overflow: hidden
  - Inner img: width: 100%, height: 100%, object-fit: cover

- .bestseller-card\_\_badge
  - display: inline-block
  - ackground: var(--color-accent), color: var(--color-white)
  - ont-size: var(--font-size-xs), ont-weight: 700
  - letter-spacing: 0.08em, ext-transform: uppercase
  - padding: 6px 14px
  - order-radius: var(--radius-full)
  - margin: var(--spacing-lg) var(--spacing-lg) 0

- .bestseller-card\_\_content
  - padding: var(--spacing-lg)
  - lex: 1, display: flex, lex-direction: column

- .bestseller-card\_\_name
  - ont-family: var(--font-heading)
  - ont-size: var(--font-size-xl)
  - color: var(--color-primary)
  - margin-bottom: var(--spacing-sm)

- .bestseller-card\_\_description
  - ont-size: var(--font-size-base)
  - color: var(--color-text-muted)
  - line-height: 1.7, lex: 1
  - margin-bottom: var(--spacing-lg)

- .bestseller-card\_\_footer
  - display: flex, justify-content: space-between, lign-items: center
  - order-top: 1px solid var(--color-border)
  - padding-top: var(--spacing-md)

- .bestseller-card\_\_price
  - ont-size: var(--font-size-lg), ont-weight: 700
  - color: var(--color-primary)

### Testimonials Section — .testimonials-section

#### Content — 3 testimonial cards:

1. "The smoothest coffee I've ever had. It feels like a café experience at home." — Sarah K.
2. "Every roast feels thoughtful and rich in flavor." — Mark T.
3. "I've tried many brands and Bean & Craft is now my daily ritual." — James L.

### HTML structure:

```html
<section class="testimonials-section">
  <div class="container">
    <div class="section-header">
      <span class="section-label">What Customers Say</span>
      <h2 class="section-title">Loved by Coffee Drinkers</h2>
    </div>
    <div class="testimonials-grid">
      <div class="testimonial-card">
        <div class="testimonial-card__stars">★★★★★</div>
        <blockquote class="testimonial-card__quote">
          "The smoothest coffee I've ever had..."
        </blockquote>
        <p class="testimonial-card__author">Sarah K.</p>
      </div>
      <!-- Repeat for remaining 2 cards -->
    </div>
  </div>
</section>
```

### CSS — estimonials.css:

- .testimonials-section
  - ackground: var(--color-card-bg)
  - padding-block: var(--spacing-3xl)

- .testimonials-grid
  - display: grid
  - grid-template-columns: repeat(3, 1fr)
  - gap: var(--spacing-xl)

- .testimonial-card
  - ackground: var(--color-background)
  - order-radius: var(--radius-lg)
  - padding: var(--spacing-xl)
  - ox-shadow: var(--shadow-card)
  - display: flex, lex-direction: column, gap: var(--spacing-md)

- .testimonial-card\_\_stars
  - color: var(--color-secondary)
  - ont-size: var(--font-size-md)
  - letter-spacing: 2px

- .testimonial-card\_\_quote
  - ont-family: var(--font-heading)
  - ont-size: var(--font-size-md)
  - color: var(--color-primary)
  - line-height: 1.7, ont-style: italic
  - lex: 1, margin: 0

- .testimonial-card\_\_author
  - ont-size: var(--font-size-sm)
  - ont-weight: 600
  - color: var(--color-text-muted)

---

## 🤝 Phase 5 — Subscribe Section, Trusted By & Footer

### Agent Context

Phases 1–4 are complete. All primary content sections are built.
**Task:** Build the three closing sections of the page.
**Output:** subscribe.css, rusted.css, ooter.css, and filled HTML inside the three remaining sections and footer.

_Paste the Global Design Tokens block at the top of this prompt as your reference._

### Subscribe Section — .subscribe-section

#### Content:

- **Headline**: "Join Our Coffee Circle"
- **Supporting text**: "Get brewing tips, new blends, and exclusive offers."
- **Email input placeholder**: "Enter your email"
- **Button**: "Subscribe"

### HTML Structure

```html
<section class="subscribe-section">
  <div class="container">
    <div class="subscribe__inner">
      <h2 class="subscribe__headline">Join Our Coffee Circle</h2>
      <p class="subscribe__text">
        Get brewing tips, new blends, and exclusive offers.
      </p>
      <div class="subscribe__form">
        <input
          type="email"
          class="subscribe__input"
          placeholder="Enter your email"
        />
        <button type="button" class="subscribe__btn">Subscribe</button>
      </div>
    </div>
  </div>
</section>
```

### CSS — `subscribe.css`

- .subscribe-section
  - ackground: var(--color-primary)
  - padding-block: var(--spacing-3xl)

- .subscribe\_\_inner
  -     ext-align: center, max-width: 560px
  - margin: 0 auto

- .subscribe\_\_headline
  - ont-family: var(--font-heading)
  - ont-size: var(--font-size-2xl)
  - color: var(--color-white)
  - margin-bottom: var(--spacing-sm)

- .subscribe\_\_text
  - ont-size: var(--font-size-md)
  - color: rgba(255, 255, 255, 0.72)
  - margin-bottom: var(--spacing-xl)

- .subscribe\_\_form
  - display: flex, gap: var(--spacing-sm), justify-content: center

- .subscribe\_\_input
  - lex: 1, max-width: 320px
  - padding: 14px 20px
  - order-radius: var(--radius-full)
  - order: 1.5px solid transparent
  - ont-size: var(--font-size-base)
  - ackground: var(--color-white)
  - color: var(--color-text-dark)
  - outline: none
  - Focus: order-color: var(--color-secondary)

- .subscribe\_\_btn
  - ackground: var(--color-secondary)
  - color: var(--color-primary)
  - ont-weight: 700, ont-size: var(--font-size-base)
  - padding: 14px 28px
  - order-radius: var(--radius-full)
  - order: none, cursor: pointer
  - Hover: slight darkening of background

### Trusted By Section — .trusted-section

#### Content:

- **Label**: "Trusted by coffee lovers and local cafés"
- **Five partner names rendered as styled text:** Roast & Co. | Morning Brew Co. | The Daily Grind | Artisan Café | Grounds & Grace

### HTML structure:

```html
<section class="trusted-section">
  <div class="container">
    <p class="trusted__label">Trusted by coffee lovers and local cafés</p>
    <div class="trusted__logos">
      <span class="trusted__logo-item">Roast & Co.</span>
      <span class="trusted__logo-item">Morning Brew Co.</span>
      <span class="trusted__logo-item">The Daily Grind</span>
      <span class="trusted__logo-item">Artisan Café</span>
      <span class="trusted__logo-item">Grounds & Grace</span>
    </div>
  </div>
</section>
```

### CSS — rusted.css:

- .trusted-section
  - ackground: var(--color-background)
  - padding-block: var(--spacing-2xl)
  - order-top: 1px solid var(--color-border)

- .trusted\_\_label
  -     ext-align: center
  - ont-size: var(--font-size-xs), ont-weight: 600
  - letter-spacing: 0.1em, ext-transform: uppercase
  - color: var(--color-text-muted)
  - margin-bottom: var(--spacing-xl)

- .trusted\_\_logos
  - display: flex, justify-content: center, lign-items: center
  - lex-wrap: wrap, gap: var(--spacing-2xl)

- .trusted\_\_logo-item
  - ont-family: var(--font-heading)
  - ont-size: var(--font-size-md), ont-weight: 700
  - color: var(--color-border)
  - opacity: 0.7
  - letter-spacing: 0.05em

### Footer — .site-footer

#### Content (4 columns):

- **Column 1** — Brand: logo name, tagline "Freshly roasted, always crafted with care.", copyright
- **Column 2** — Shop: Ethiopian Light Roast, Colombian Medium Roast, Brazil Dark Roast
- **Column 3** — Company: About, Brewing Guide, Contact
- **Column 4** — Support: Shipping, Returns, Privacy Policy, Terms

### HTML structure:

```html
<footer class="site-footer">
  <div class="container">
    <div class="footer__grid">
      <div class="footer__col footer__col--brand">
        <span class="footer__logo">Bean & Craft Coffee</span>
        <p class="footer__tagline">
          Freshly roasted, always crafted with care.
        </p>
      </div>
      <div class="footer__col">
        <h4 class="footer__col-title">Shop</h4>
        <ul class="footer__links">
          <li><a href="#">Ethiopian Light Roast</a></li>
          <li><a href="#">Colombian Medium Roast</a></li>
          <li><a href="#">Brazil Dark Roast</a></li>
        </ul>
      </div>
      <div class="footer__col">
        <h4 class="footer__col-title">Company</h4>
        <ul class="footer__links">
          <li><a href="#">About</a></li>
          <li><a href="#">Brewing Guide</a></li>
          <li><a href="#">Contact</a></li>
        </ul>
      </div>
      <div class="footer__col">
        <h4 class="footer__col-title">Support</h4>
        <ul class="footer__links">
          <li><a href="#">Shipping</a></li>
          <li><a href="#">Returns</a></li>
          <li><a href="#">Privacy Policy</a></li>
          <li><a href="#">Terms</a></li>
        </ul>
      </div>
    </div>
    <div class="footer__bottom">
      <p>© 2024 Bean & Craft Coffee. All rights reserved.</p>
    </div>
  </div>
</footer>
```

### CSS — ooter.css:

- .site-footer
  - ackground: var(--color-primary)
  - color: var(--color-white)
  - padding-block: var(--spacing-3xl)

- .footer\_\_grid
  - display: grid
  - grid-template-columns: 2fr 1fr 1fr 1fr
  - gap: var(--spacing-2xl)

- .footer\_\_logo
  - ont-family: var(--font-heading)
  - ont-size: var(--font-size-lg), ont-weight: 700
  - color: var(--color-white), display: block
  - margin-bottom: var(--spacing-sm)

- .footer\_\_tagline
  - ont-size: var(--font-size-sm)
  - color: rgba(255, 255, 255, 0.6)
  - line-height: 1.6, max-width: 240px

- .footer\_\_col-title
  - ont-size: var(--font-size-xs), ont-weight: 700
  - letter-spacing: 0.12em, ext-transform: uppercase
  - color: var(--color-secondary)
  - margin-bottom: var(--spacing-md)

- .footer\_\_links
  - list-style: none, margin: 0, padding: 0

- .footer\_\_links a
  - display: block
  - ont-size: var(--font-size-sm)
  - color: rgba(255, 255, 255, 0.65)
  -     ext-decoration: none
  - margin-bottom: var(--spacing-sm)
  - Hover: color: var(--color-white)

- .footer\_\_bottom
  - order-top: 1px solid rgba(255, 255, 255, 0.15)
  - margin-top: var(--spacing-2xl)
  - padding-top: var(--spacing-lg)
  -     ext-align: center
  - ont-size: var(--font-size-xs)
  - color: rgba(255, 255, 255, 0.4)

---

## 📱 Phase 6 — Responsive Behavior

### Agent Context

Phases 1–5 are complete. The full desktop layout is built across all sections.
**Task:** Add all responsive breakpoints. No new sections are created.
**Output:**
esponsive.css — this file is already linked last in index.html from Phase 1.

_Paste the Global Design Tokens block at the top of this prompt as your reference._

_All class names used here already exist in prior CSS files. This file only overrides values at given breakpoints._

### Breakpoints

- **Tablet**: max-width: 1024px
- **Mobile**: max-width: 768px
- **Small mobile**: max-width: 480px

### Tablet — @media (max-width: 1024px)

**Navigation**:

- .navbar\_\_links: gap: var(--spacing-lg)
- .navbar\_\_links a: ont-size: var(--font-size-xs)

**Hero**:

- .hero\_\_inner: grid-template-columns: 1fr — stack columns
- .hero-section: ext-align: center
- .hero\_\_subheadline: max-width: 100%
- .hero\_\_actions: justify-content: center
- .hero\_\_visual: max-width: 480px, margin: 0 auto

**Products**:

- .products-grid: grid-template-columns: repeat(2, 1fr)

**Explore**:

- .explore-grid: grid-template-columns: repeat(2, 1fr)

**Bestseller**:

- .bestseller-grid: grid-template-columns: 1fr

**Testimonials**:

- .testimonials-grid: grid-template-columns: repeat(2, 1fr)

**Subscribe**:

- .subscribe\_\_form: lex-direction: column, lign-items: center
- .subscribe\_\_input: max-width: 100%

**Footer**:

- .footer\_\_grid: grid-template-columns: 1fr 1fr, gap: var(--spacing-xl)

### Mobile — @media (max-width: 768px)

**Navigation**:

- .navbar\_\_links: display: none
- .navbar\_\_logo: ont-size: var(--font-size-md)

**Hero**:

- .hero\_\_headline: ont-size: var(--font-size-2xl)
- .hero-section: min-height: auto, padding-block: var(--spacing-2xl)

**Products**:

- .products-grid: grid-template-columns: 1fr

**Explore**:

- .explore-grid: grid-template-columns: 1fr

**Testimonials**:

- .testimonials-grid: grid-template-columns: 1fr

**Subscribe**:

- .subscribe\_\_headline: ont-size: var(--font-size-xl)

**Trusted By**:

- .trusted\_\_logos: gap: var(--spacing-xl)

**Footer**:

- .footer\_\_grid: grid-template-columns: 1fr
- .footer\_\_col--brand: ext-align: center
- .footer\_\_tagline: max-width: 100%

### Small Mobile — @media (max-width: 480px)

- .hero\_\_headline: ont-size: var(--font-size-xl)
- .section-title: ont-size: var(--font-size-xl)
- .hero\_\_actions: lex-direction: column, width: 100%
- .btn-primary: width: 100%, ext-align: center
- .btn-text: width: 100%, ext-align: center
- .subscribe\_\_btn: width: 100%
- .container: padding-inline: var(--spacing-md)

---

## ✅ Master Acceptance Checklist

### 🏗️ Foundation

- [ ] All CSS variables defined in okens.css with exact names from the Global Design Tokens block
- [ ] CSS reset applied: box-sizing, margin, padding, img max-width
- [ ] Base body styles use design tokens
- [ ] Container, grid, and utility classes functional in layout.css
- [ ] All CSS files linked in correct order in index.html
- [ ] Google Fonts (Playfair Display + Inter) loaded

### 🧭 Navigation

- [ ] Navbar is sticky at top, height 72px
- [ ] Logo uses Playfair Display and --color-primary
- [ ] Links styled and spaced correctly
- [ ] CTA button matches .btn-primary spec

### Hero Coffe

- [ ] Headline uses Playfair Display at --font-size-3xl
- [ ] Two-column layout: text left, image right
- [ ] Both CTAs present and correctly styled
- [ ] Image wrapper maintains aspect ratio with border-radius and shadow

### 🛍️ Product Section

- [ ] Section label, headline, and 3-column grid present
- [ ] All 3 product cards render with image, badge, name, description, price, and CTA
- [ ] Card hover shadow transition applied

### 🔍 Explore Section

- [ ] 3-column explore card grid present
- [ ] Each card has icon placeholder, title, and text
- [ ] Section background uses --color-card-bg for visual rhythm separation

### ⭐ Bestseller Section

- [ ] 2-column grid with larger card format
- [ ] Accent-colored badge (--color-accent) distinguishes from standard product cards
- [ ] Each card has image, name, description, price, and "Shop Now" CTA

### 💬 Testimonials Section

- [ ] 3-column grid present
- [ ] Each card has stars (--color-secondary), italic quote, and author name
- [ ] Section background uses --color-card-bg

### ✉️ Subscribe Section

- [ ] Section background uses --color-primary (deep brown)
- [ ] White headline and muted supporting text
- [ ] Email input and button side by side on desktop
- [ ] Button is ype="button" — no form tag used

### 🤝 Trusted By Section

- [ ] Five partner names rendered in muted monochrome style
- [ ] Logos centered in a flex row
- [ ] Section has top border using --color-border

### 🦶 Footer

- [ ] 4-column grid: brand (2fr), shop, company, support
- [ ] Brand column has logo, tagline
- [ ] All link groups present with correct items
- [ ] Copyright bar in .footer\_\_bottom
- [ ] Section background uses --color-primary

### 📱 Responsive

- [ ] Tablet (1024px): 2-column grids, stacked hero
- [ ] Mobile (768px): all grids single column, nav links hidden
- [ ] Small mobile (480px): full-width buttons, reduced headline sizes
- [ ] No horizontal scroll at any breakpoint
- [ ] Tap targets adequately sized on mobile
