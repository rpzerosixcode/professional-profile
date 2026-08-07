# Office Profile

Professional profile page built with **HTML** and **CSS**, with no dependencies or build steps. Presents contact information, skills and a WhatsApp call-to-action, with a responsive design based on centralized design tokens.

## Technologies

- **HTML5** — semantic and accessible markup
- **CSS3** — design tokens, responsive layout with `clamp()` and media queries
- **Font Awesome 7** — icons (via CDN)
- **Google Fonts (Inter)** — typography (via CDN)

## Features

- Responsive layout that adapts to any screen size
- Profile card with contact information
- WhatsApp contact button
- Clickable `tel:` and `mailto:` links
- Skills grid with progress bars
- Centralized design tokens for easy maintenance
- Modular CSS architecture (tokens → globals → components)
- `prefers-reduced-motion` support
- Accessibility: skip link, `aria-label`s, `role="progressbar"` and visible focus

## Project Structure

```
office-profile/
├── index.html                      # Main page
├── README.md
├── LICENSE
├── assets/                         # Static assets (empty; ready for use)
│   ├── icons/
│   └── images/
├── css/
│   ├── main.css                    # Entry point — imports all styles
│   ├── token.css                   # Design tokens (CSS custom properties)
│   ├── global.css                  # Base styles, shared divider, accessibility
│   └── components/
│       ├── header.css              # Header and logo
│       ├── hero.css                # Hero section and profile card
│       ├── skills.css              # Skills grid and progress bars
│       └── footer.css              # Footer
└── js/                             # Reserved for future scripts (empty)
```

## Getting Started

1. Clone or download the repository.
2. Open `index.html` in your browser.

No build step, dependencies or configuration required.

## Design Tokens

All recurring values (colors, typography, spacing, sizing, radii, effects, icons) are centralized in `css/token.css` as CSS custom properties under `:root`. Heading fonts use `clamp()` for a fluid type scale between mobile and desktop.

## Responsiveness

Breakpoints are defined per component:

| Component | Behavior |
|---|---|
| Header | Font and letter-spacing shrink below 480px |
| Hero | Stacks vertically below 900px; CTA becomes full-width below 420px |
| Skills | Grid 3 → 2 → 1 columns at 1199px / 640px |
| Footer | Stacks and centers below 480px |

## Accessibility

- **Skip link** — "Skip to content" lets keyboard users jump past the header
- **Decorative icons** — marked with `aria-hidden="true"`; interactive icons keep a descriptive `aria-label`
- **Skill bars** — expose `role="progressbar"` with `aria-valuenow/min/max`
- **Visible focus** — all interactive elements have a `:focus-visible` ring
- **Reduced motion** — animations and smooth scrolling disabled with `prefers-reduced-motion: reduce`

## Maintenance

- Add new styles in `css/components/` and import them in `css/main.css`
- Reuse design tokens from `css/token.css` instead of hard-coded values
- Keep component semantics when changing classes
- Preserve ARIA attributes when modifying the HTML

## License

Licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.