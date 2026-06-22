# evansmorgan.com

Personal portfolio — Morgan Evans, Staff Experience Designer at Adobe.

Built with [Astro](https://astro.build) + [Tailwind CSS 4](https://tailwindcss.com).

## Local development

```bash
npm run dev       # dev server at http://localhost:4321
npm run build     # production build → dist/
npm run preview   # preview the production build locally
```

## Project structure

```
src/
  components/
    Nav.astro               # top nav
    Footer.astro            # footer (dynamic copyright year)
  layouts/
    Layout.astro            # base shell (nav + footer)
    ProjectLayout.astro     # case study template (back button, hero, lightbox)
  pages/
    index.astro             # home — project cards
    about.astro             # about page
    manticore.astro         # collaborative photography case study
    photoshop-desktop.astro # photoshop desktop case study (password protected)
    photoshop-phone.astro   # photoshop mobile case study (password protected)
  styles/
    global.css              # design tokens + base styles

public/
  MorganEvans_Resume.pdf    # ← replace with latest resume (keep filename)
  favicon.ico / favicon.svg
  img/
    manticore/              # collaborative photography images
    photoshop-desktop/      # ← add desktop project images here
    photoshop-phone/        # ← add mobile project images here
```

## Changing passwords

Protected case study passwords are set at the top of `src/pages/index.astro`:

```js
const PS_DESKTOP_PASSWORD = 'your-password';
const PS_PHONE_PASSWORD   = 'your-password';
```

Only the SHA-256 hash is embedded in the HTML — plaintext never appears in source.

## Deploying

Connect this repo to [Vercel](https://vercel.com) or [Netlify](https://netlify.com) — both detect Astro automatically with no extra config needed.
