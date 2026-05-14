# Agent Rules — Bean & Craft Coffee Project

## Authority of This File

This file is the single behavioral contract for every agent working on this project.
Read it fully at the start of every session.

---

## Core Principle

You execute what is specified. Maintain the "Nescafe-inspired" premium aesthetic at all times.
Consistency with existing design tokens and modular CSS structure is paramount.
Note: `login.html` is the primary entry point for the project.

---

## Design Standards

### 1. Color Palette (Nescafe Theme)
Always use the established design tokens in `Styles/tokens.css`:
- **Background (`--color-bg`):** #d9c5b2 (Creamy Latte)
- **Primary (`--color-primary`):** #4a2c2a (Coffee Brown)
- **Accent (`--color-accent`):** #8b4513 (Warm Cinnamon)
- **White/Surface (`--color-white`):** #eaddcf
- **Card Background (`--color-card-bg`):** #f5efe6

### 2. Typography
- **Headings:** "Playfair Display", serif. Use for `h1`, `h2`, `h3` and logo.
- **Body:** "Inter", sans-serif. Use for all readable text.
- **Logo/Nav Links:** Uppercase with refined letter-spacing (0.08em - 0.12em).

### 3. Header & Navigation
- **Header:** Glassmorphism style with blur (12px) and semi-transparent latte background.
- **Positioning:** Sticky at the top of the page.
- **Smooth Scrolling:** Always maintain `scroll-behavior: smooth` for anchor navigation.

---

## Technical Constraints

- **No JavaScript:** All interactivity must be achieved through CSS (transitions, hovers, states).
- **Modular CSS:** Styles must be kept in their respective files within the `Styles/` directory.
- **Image Assets:** All HD images must reside in the `photos/` folder.
- **Responsiveness:** Maintain full mobile and tablet compatibility via `Styles/responsive.css`.

---

## Handling Concerns

If you believe a decision is problematic or deviates from the established "Nescafe" brand:
Use this format:

    SECTION: [Name of the section or file]
    CONCERN: [Describe the problem you foresee]
    RECOMMENDATION: [What you suggest instead and why]

Do not proceed until the user confirms the direction.

---

## Reminder

You are an execution agent. Your role is precise, faithful implementation of the Bean & Craft Coffee brand identity.
When in doubt, check `Styles/tokens.css`.
