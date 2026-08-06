# Office Profile

A personal professional profile page built with **HTML** and **CSS**.

## Overview

This project presents a personal profile card with contact information and a call-to-action button, styled with a clean, modern design system based on centralized design tokens.

## Features

- Responsive layout (mobile-friendly)
- Centralized design tokens (colors, typography, spacing, sizing, radii, effects, icons)
- Modular CSS architecture (tokens, global styles, components)
- WhatsApp contact button
- Contact information card

## Project Structure

```
office-profile/
├── index.html
├── README.md
├── assets/
│   ├── icons/
│   └── images/
├── css/
│   ├── main.css          # Entry point — imports all stylesheets
│   ├── token.css         # Design tokens (CSS custom properties)
│   ├── global.css        # Base and global styles
│   └── components/
│       ├── header.css    # Header and logo styles
│       └── hero.css      # Hero section and profile card styles
└── js/
```

## Getting Started

1. Clone or download the repository.
2. Open `index.html` in your browser.

No build step or dependencies are required.

## Design Tokens

All recurring values (colors, font sizes, weights, spacing, sizes, radii, shadows, icon sizes) are centralized in `css/token.css` as CSS custom properties under `:root`, making the theme easy to maintain and update.

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.