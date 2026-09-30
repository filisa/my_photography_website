# Nature — Art & Photography

A responsive portfolio website that shows my nature photography and watercolor paintings. I built it from scratch with plain HTML and CSS as part of my Responsive Web Design course at [Hyper Island](https://www.hyperisland.com/).

**Live site:** [my-art-and-photography.netlify.app](https://my-art-and-photography.netlify.app/)

---

## Pages

| Page | File | What's on it |
| --- | --- | --- |
| **Main** | `index.html` | Full-screen landing page with a nature photo background, a colour gradient overlay and a short welcome message. |
| **About** | `about.html` | A short introduction next to a cut-out portrait, with a large rotating "hej!" graphic in the background. |
| **Work** | `work.html` | A photo gallery on CSS Grid (animals, plants and winter landscapes). Some photos span two rows or columns, and they zoom in slightly on hover. |
| **Art** | `art.html` | A gallery of 18 watercolor paintings in a wrapping Flexbox layout. Each painting tilts slightly on hover. |

## Features

- **Responsive layout:** mobile-first breakpoint at `450px`. The galleries switch from one column on phones to a multi-column grid/flex layout on larger screens.
- **Fluid typography:** base font size scales with the viewport via `clamp(1.5rem, 2.5vw, 4rem)`.
- **Custom font:** [Big Shoulders](https://fonts.google.com/specimen/Big+Shoulders), self-hosted as a variable font with `@font-face`.
- **Design system:** colours, gradients, the font stack and the page animation are defined once as CSS custom properties in `:root`.
- **Animations:** every page fades in from black, the "hej!" graphic spins slowly, and the gallery images have hover effects.
- **Accessibility:**
  - Descriptive `alt` text on every image
  - Semantic HTML (`<nav>`, `<main>`, `<section>`, `<footer>`)
  - The page fade-in is turned off for users who set `prefers-reduced-motion`
- **Performance:**
  - Gallery images use `loading="lazy"`
  - Hero images are preloaded with `fetchpriority="high"`
  - Images were compressed to smaller file sizes

## Built with

- HTML5
- CSS3 (Grid, Flexbox, custom properties, media queries, keyframe animations, nesting)
- No frameworks, no JavaScript
- Hosted on [Netlify](https://www.netlify.com/)

## Project structure

```
my_photography_website/
├── index.html          # Main / landing page
├── about.html          # About me
├── work.html           # Photography gallery
├── art.html            # Watercolor gallery
├── styles.css          # All styles for every page
├── fonts/
│   └── Big_Shoulders/  # Self-hosted variable font + static weights
└── images/
    ├── art/            # Watercolor paintings (1–18.jpg)
    ├── DSCF*.jpg       # Photographs
    ├── hej.svg         # Rotating "hej!" graphic
    └── margarit.png    # Favicon
```

## Running it locally

There's no build step. Clone the repo and open `index.html` in your browser:

```bash
git clone <repo-url>
cd my_photography_website
open index.html        # macOS
# or start a small local server:
python3 -m http.server 8000
```

Then go to [http://localhost:8000](http://localhost:8000).

## Deployment

The site is a static site deployed with **Netlify** and is live at [my-art-and-photography.netlify.app](https://my-art-and-photography.netlify.app/).

## What I learned

- Building responsive layouts with CSS Grid and Flexbox
- Using media queries and `clamp()` for fluid, mobile-friendly design
- Organising styles with CSS custom properties and BEM-style class names
- Adding motion thoughtfully and respecting `prefers-reduced-motion`
- Optimising images for faster loading
- Deploying a static site with Netlify

## Author

**Margarita Nikulina**, frontend development student at Hyper Island, Stockholm. I love nature, watercolor painting and photography.

## License

All code, photographs and artwork © 2026 Margarita Nikulina, licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).

You may share and adapt this work for **non-commercial** purposes as long as you **give credit** and share it under the **same license**.
