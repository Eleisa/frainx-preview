---
publishDate: 2026-08-10T00:00:00Z

title: 'Customize Your Astro Template: Colors, Fonts, Logo'

excerpt: Customize the AstroWind Astro template to your brand. Light and dark colors, fonts, logo, favicons, header and footer, and tokens for your own components.

image: 'https://images.unsplash.com/photo-1709803056954-aff96d0faf1c?auto=format&fit=crop&w=2070&q=80'

imageAlt: Steps painted in different colors against a blue sky

category: Documentation

tags:
  - astro
  - tailwind css
  - theme
---

Customizing the AstroWind template to your brand is a handful of files, and none of them is inside a component you would rather not touch. The demo is blue, uses Inter and says "AstroWind" everywhere; this guide goes through what to change, in the order most projects need it. If you have not created the project yet, start with the [getting started guide](/get-started-website-with-astro-tailwind-css).

## What you'll change

- The color palette, for light and dark mode, in one file.
- The fonts, self-hosted through Astro's Fonts API.
- The logo, the favicons and the default social share image.
- The header menu, the header button and the footer.
- The tokens your own components and any shadcn/ui blocks will use.

## Change the theme colors (light and dark)

`src/components/CustomStyles.astro` declares the palette as CSS variables, once for light mode under `:root` and once for dark mode under `.dark`:

```css
:root {
  --aw-color-primary: rgb(1 97 239);
  --aw-color-secondary: rgb(1 84 207);
  --aw-color-accent: rgb(109 40 217);
  --aw-color-text-heading: rgb(0 0 0);
  --aw-color-text-default: rgb(16 16 16);
  --aw-color-text-muted: rgb(16 16 16 / 66%);
  --aw-color-bg-page: rgb(255 255 255);
}

.dark {
  --aw-color-primary: rgb(1 97 239);
  /* … */
  --aw-color-bg-page: rgb(8 9 10);
}
```
