# Rod Navarro — Logo Designer Portfolio

A premium, modern, animated one-page portfolio built with **Vite + React + TypeScript**.

> Logo designer for digital creators. Dark mode, glassmorphism, Space Grotesk + Outfit fonts, custom cursor, grain texture, smooth scroll, fade-up reveals, parallax.

---

## 🚀 Quick Start

```bash
# Install dependencies
npm install

# Start dev server (http://localhost:5173)
npm run dev

# Type-check
npm run lint

# Production build → dist/
npm run build

# Preview the production build
npm run preview
```

---

## ☁️ Deploy

### Vercel (recommended — zero config)
1. Push this repo to GitHub.
2. Go to [vercel.com/new](https://vercel.com/new) and import the repo.
3. Vercel auto-detects Vite. Click **Deploy**.
4. Done — you get a `https://<project>.vercel.app` URL.

Or with the Vercel CLI:
```bash
npm i -g vercel
vercel        # preview deploy
vercel --prod # production deploy
```

### GitHub Pages
Add to `vite.config.ts`:
```ts
export default defineConfig({
  base: '/<repo-name>/',
  // ...
});
```
Then:
```bash
npm run build
npx gh-pages -d dist
```

### Netlify
Drag-and-drop the `dist/` folder onto [app.netlify.com/drop](https://app.netlify.com/drop).

---

## ✏️ Customizing the portfolio

All copy, services, work samples, testimonials, and FAQ items live in **one file**:

```
src/data/portfolio.ts
```

Edit the `portfolioData` object and save — Vite hot-reloads instantly.

### Add a work sample
1. Drop the image into `public/images/`.
2. Add an entry to `portfolioData.work`:
   ```ts
   { image: '/images/your-image.png', name: 'Project Name', type: 'Logo Design · 2025' }
   ```

### Change brand colors
Open `src/index.css` and edit the `:root` block:
```css
:root {
  --green: #4ade80;       /* primary accent */
  --green-deep: #16a34a;  /* secondary accent */
  --white: #ffffff;       /* contrast accent */
}
```

### Update contact email / links
In `src/data/portfolio.ts`:
```ts
email: 'you@yourdomain.com',
```

---

## 📁 Project structure

```
portfolio-shavon/
├── public/
│   ├── favicon.svg
│   └── images/            # logo work samples, portrait
├── src/
│   ├── components/        # (reserved for future component split)
│   ├── data/
│   │   └── portfolio.ts   # ⭐ all editable content
│   ├── hooks/
│   │   ├── useCountUp.ts
│   │   ├── useCustomCursor.ts
│   │   └── useReveal.ts
│   ├── App.tsx
│   ├── index.css
│   └── main.tsx
├── index.html
├── package.json
├── tsconfig.json
├── tsconfig.node.json
└── vite.config.ts
```

---

## 🎨 Features

- ✨ Dark mode with glassmorphism cards
- 🟢 Brand color gradient accents (configurable)
- 🔤 Space Grotesk + Outfit from Google Fonts
- 🖱️ Custom dot cursor with magnetic follower
- 🎞️ Smooth scroll, fade-up reveals, parallax
- 📱 Fully responsive
- ⚡ Fast Vite build, tree-shaken, type-safe

---

## 📜 License

MIT — use freely.
