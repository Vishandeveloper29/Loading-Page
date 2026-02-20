# Loading Page

A clean, minimal animated loading screen built with pure HTML and CSS. It features a wave animation with cascading bars in a blue gradient palette and a centered full-viewport layout.

---

## Preview

Five vertical bars animate in a wave pattern with staggered delays, creating a smooth cascading effect. The color transitions from light to dark blue across the bars.

---

## Features

- Full-viewport centered layout using CSS Flexbox
- Smooth wave animation with 5 staggered bars
- Blue gradient color scheme (`#3675bc` → `#1b3b5e`)
- No JavaScript — pure HTML & CSS
- Lightweight and responsive

---

## File Structure

```
loading-page/
├── index.html    # Main HTML structure
└── style.css     # Styles and animation
```

---

## Getting Started

No build tools or dependencies required. Just open `index.html` in any modern browser.

```bash
git clone https://github.com/yourname/loading-page.git
cd loading-page
open index.html
```

---

## How It Works

### HTML Structure

The page has a single `.center` wrapper containing:
- `.loader` — placeholder element
- `.wave` — container with 5 `<span>` bars
- `<h1>` — "Loading..." label

### CSS Animation

Each `<span>` runs the `wave` keyframe animation, transitioning its height from `25px` to `75px` and back over `1s`. Each bar has a `0.1s` staggered delay, producing the wave effect.

```css
@keyframes wave {
  0%   { height: 25px; }
  50%  { height: 75px; }
  100% { height: 25px; }
}
```

### Color Palette

| Bar | Color | Delay |
|-----|-------|-------|
| Bar 1 | `#3675bc` | 0s |
| Bar 2 | `#2b5e96` | 0.1s |
| Bar 3 | `#265284` | 0.2s |
| Bar 4 | `#204671` | 0.3s |
| Bar 5 | `#1b3b5e` | 0.4s |

---

## Customization

- **Speed** — Change `1s` in `.wave span { animation: wave 1s ... }` to adjust animation speed.
- **Bar count** — Add/remove `<span>` elements and update the `nth-child` CSS rules accordingly.
- **Colors** — Update the `background-color` values in the `nth-child` selectors to match your brand.

---

## License

MIT License — free to use, modify, and distribute.
