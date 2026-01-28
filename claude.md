# RobotReady Landing Page - Project Documentation

This document provides complete documentation for modifying content, colors, and integrations without touching layout code.

---

## Quick Reference: Where to Edit

| What to Change | File | Location |
|----------------|------|----------|
| **Colors** | `styles.css` | Lines 20-45 (`:root` CSS variables) |
| **Typography** | `styles.css` | Lines 50-75 (font tokens) |
| **Spacing** | `styles.css` | Lines 80-95 (space tokens) |
| **Page copy** | `index.html` | See Content Map below |
| **Logo** | `index.html` | Line 30 (nav__logo section) |
| **HubSpot form** | `index.html` | Line 175 (#hubspot-form div) |
| **Navigation links** | `index.html` | Lines 35-38 |
| **Hero background** | `styles.css` | Lines 220-230 (.hero::before) |

---

## Content Map

All editable content is organized below with its exact location in `index.html`.

### Company Information

| Content | Current Value | Location |
|---------|---------------|----------|
| Company Name | RobotReady | Nav logo, `<title>`, footer copyright |
| Meta Description | "RobotReady is the trusted authority..." | `<head>` meta tag |
| Copyright | © 2025 RobotReady. All rights reserved. | Footer |

### Mission Statement (Verbatim - Do Not Alter)

```
RobotReady is the trusted authority for humanoid robotics readiness, helping organizations make confident decisions about timing, deployment, and the operational changes required for successful deployment.
```

**Location:** Hero section `<h1>` element

### Tagline

```
Be ready before you deploy.
```

**Location:** Hero section `.hero__tagline` paragraph

### Navigation

| Label | Anchor | Location |
|-------|--------|----------|
| About | #about | .nav__link |
| Expertise | #expertise | .nav__link |
| Insights | #insights | .nav__link |
| Contact | #contact | .nav__cta button |

### Hero CTAs

| Button | Label | Action | Class |
|--------|-------|--------|-------|
| Primary | Get Started | Scrolls to #contact | btn--primary |
| Secondary | Learn More | Scrolls to #approach | btn--secondary |

### Our Approach Section

| Tile | Title | Description |
|------|-------|-------------|
| 1 | Assess | Evaluate operational readiness across facility, process, people, and systems. |
| 2 | Plan | Define the deployment pathway and sequence operational changes. |
| 3 | Guide | Support execution, change management, and organizational alignment. |

### What We Do Section

```
- Humanoid readiness assessment across facility, process, people, safety, and controls
- Deployment planning and operational change roadmapping
- Vendor-agnostic guidance with no robot sales or OEM preference
- Risk framing and decision support around timing and rollout
- Internal alignment across operations, engineering, safety, IT/OT, and quality
- Defining what to measure during pilots to learn quickly and scale safely
```

### Who It's For Section

**Column 1: Manufacturing & Operations Leaders**
```
Operations, engineering, continuous improvement, plant leadership, safety, and IT/OT teams evaluating humanoid deployment.
```

**Column 2: Robotics OEMs & Innovators**
```
Teams seeking readiness feedback loops and clear pilot success criteria for customer deployments.
```

### Credibility Strip

```
- Product-agnostic
- Readiness-first
- Operator-aware
- Deployment decision support
```

### CTA Band

| Element | Content |
|---------|---------|
| Headline | Assess readiness. Reduce surprises. |
| Supporting text | A short engagement can clarify timing, risks, and required operational changes. |
| Button | Get in Touch → #contact |

### Contact Section

| Element | Content |
|---------|---------|
| Title | Get in Touch |
| Intro | Tell us what you're evaluating and what constraints you're facing. |

### Footer

| Element | Content |
|---------|---------|
| Copyright | © 2025 RobotReady. All rights reserved. |
| Email | hello@getrobotready.com |
| LinkedIn | https://linkedin.com/company/robotready |

---

## Theme Tokens Reference

All visual properties are controlled via CSS custom properties in `styles.css`. Edit values in the `:root` block only.

### Color System (Based on RobotReady Logo)

```css
/* Background colors - deep blue-black tones */
--color-background: #0a0e14;         /* Deep dark blue-black */
--color-panel: #131a24;              /* Dark blue panel */
--color-panel-elevated: #1a2432;     /* Elevated panel (hover states) */

/* Text colors - cool white/gray tones */
--color-text: #f0f4f8;               /* Near-white with cool tint */
--color-text-muted: #8a9bae;         /* Blue-gray for secondary text */
--color-text-subtle: #5a6a7a;        /* Subtle blue-gray for hints */

/* Border colors */
--color-border: #1e2a3a;             /* Dark blue-gray borders */
--color-border-hover: #2a3a4a;       /* Borders on hover */

/* Accent colors - warm orange for CTAs */
--color-accent: #e05a2b;             /* Warm orange - primary CTA */
--color-accent-hover: #f06a3b;       /* Accent hover state */
--color-accent-active: #c04a1b;      /* Accent active/pressed state */

/* Brand colors - logo blue */
--color-brand: #2d9cdb;              /* Logo blue - for highlights */
--color-brand-light: #56b3e6;        /* Lighter brand blue */
--color-brand-dark: #1a7ab8;         /* Darker brand blue */

/* Secondary accent - uses brand blue */
--color-secondary: #2d9cdb;          /* Brand blue as secondary */
--color-secondary-hover: #56b3e6;    /* Secondary hover */

/* Focus states (accessibility) */
--color-focus: #2d9cdb;              /* Focus ring - brand blue */
--color-focus-outline: rgba(45, 156, 219, 0.4);  /* Focus glow */
```

### Typography

```css
/* Font stack */
--font-sans: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, ...;

/* Font weights */
--font-weight-normal: 400;
--font-weight-medium: 500;
--font-weight-semibold: 600;
--font-weight-bold: 700;

/* Font sizes */
--font-size-xs: 0.75rem;     /* 12px */
--font-size-sm: 0.875rem;    /* 14px */
--font-size-base: 1rem;      /* 16px */
--font-size-lg: 1.125rem;    /* 18px */
--font-size-xl: 1.25rem;     /* 20px */
--font-size-2xl: 1.5rem;     /* 24px */
--font-size-3xl: 2rem;       /* 32px */
--font-size-4xl: 2.5rem;     /* 40px */
--font-size-5xl: 3rem;       /* 48px */

/* Line heights */
--line-height-tight: 1.1;
--line-height-snug: 1.25;
--line-height-normal: 1.5;
--line-height-relaxed: 1.625;
```

### Spacing Scale

```css
--space-xs: 0.25rem;     /* 4px */
--space-sm: 0.5rem;      /* 8px */
--space-md: 1rem;        /* 16px */
--space-lg: 1.5rem;      /* 24px */
--space-xl: 2rem;        /* 32px */
--space-2xl: 3rem;       /* 48px */
--space-3xl: 4rem;       /* 64px */
--space-4xl: 6rem;       /* 96px */
--space-5xl: 8rem;       /* 128px */
```

### Layout

```css
--container-max-width: 1140px;
--container-padding: 1.5rem;
--nav-height: 72px;
```

### Button Styles

Primary button (accent-colored):
```css
.btn--primary {
  background-color: var(--color-accent);
  color: var(--color-text);
  border-color: var(--color-accent);
}
```

Secondary button (outline):
```css
.btn--secondary {
  background-color: transparent;
  color: var(--color-text);
  border-color: var(--color-border);
}
```

---

## How To: Common Tasks

### Replace the Logo

1. Open `index.html`
2. Find the comment: `<!-- LOGO PLACEHOLDER: Replace this div... -->`
3. Replace the `<span class="nav__logo-text">RobotReady</span>` with:
   ```html
   <img src="assets/logo.svg" alt="RobotReady" class="nav__logo-img">
   ```
4. Add logo styles to `styles.css` if needed:
   ```css
   .nav__logo-img {
     height: 32px;
     width: auto;
   }
   ```

### Add HubSpot Form

1. Open `index.html`
2. Find `<div id="hubspot-form">`
3. Delete the fallback form (everything from `<!-- FALLBACK FORM -->` to `<!-- END FALLBACK FORM -->`)
4. Paste your HubSpot embed code inside the `#hubspot-form` div:
   ```html
   <script charset="utf-8" type="text/javascript" src="//js.hsforms.net/forms/embed/v2.js"></script>
   <script>
     hbspt.forms.create({
       region: "na1",
       portalId: "YOUR_PORTAL_ID",
       formId: "YOUR_FORM_ID"
     });
   </script>
   ```

### Add Hero Background Image

1. Place your image in an `assets/` folder
2. Open `styles.css`
3. Find `.hero::before` (around line 220)
4. Update the `background-image` property:
   ```css
   background-image:
     linear-gradient(to bottom, rgba(13, 13, 13, 0.85), rgba(13, 13, 13, 0.95)),
     url('assets/hero-bg.jpg');
   ```

### Change the Accent Color

1. Open `styles.css`
2. Find the color tokens in `:root` (around line 30)
3. Update these three values:
   ```css
   --color-accent: #YOUR_COLOR;
   --color-accent-hover: #YOUR_LIGHTER_COLOR;
   --color-accent-active: #YOUR_DARKER_COLOR;
   ```

### Use Inter Font Instead of System Fonts

1. Open `index.html`
2. Uncomment the Google Fonts link in `<head>`:
   ```html
   <link rel="preconnect" href="https://fonts.googleapis.com">
   <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
   <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
   ```
3. Open `styles.css`
4. Update the font-sans variable:
   ```css
   --font-sans: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
   ```

### Update Footer Contact Information

1. Open `index.html`
2. Find the `<footer>` section at the bottom
3. Update:
   - Email: `href="mailto:your@email.com"`
   - LinkedIn: `href="https://linkedin.com/company/your-company"`
   - Copyright year or company name

---

## File Structure

```
/RobotReady
├── index.html      # Main HTML page
├── styles.css      # All styles with theme tokens
├── claude.md       # This documentation file
└── assets/         # (Create as needed)
    ├── logo.svg    # Logo file
    └── hero-bg.jpg # Hero background image
```

---

## Accessibility Notes

- All colors meet WCAG AA contrast requirements
- Focus states are visible on all interactive elements
- Semantic HTML structure (nav, main, section, footer)
- Form inputs have associated labels
- Images require alt text when added
- Navigation is keyboard accessible

---

## Design Principles

1. **Calm, confident, conservative** - No hype language or startup aesthetics
2. **Premium whitespace** - Generous spacing, minimal visual noise
3. **High contrast** - Near-white on near-black for readability
4. **Restrained color** - Single warm accent for CTAs only
5. **Product-agnostic** - No mention of specific robot vendors or products
6. **Technically sophisticated audience** - Skip the basics, speak to operators

---

## Version History

| Version | Date | Notes |
|---------|------|-------|
| 1.0 | 2025-01-27 | Initial landing page build |
