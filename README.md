# Updated Mercury Interactive

Client-only WebGL interactive for Mercury: single `index.html` with an inline ES module and Three.js loaded via import map (no build step). Curriculum, NGSS alignment, and product links are in [`Standards.md`](Standards.md).

**Production:** [https://content-interactives.github.io/updated-mercury](https://content-interactives.github.io/updated-mercury)

---

## Architecture

| Layer | Implementation |
|--------|----------------|
| Rendering | `THREE.WebGLRenderer` + scene graph |
| Modules | `importmap` → `three@0.162.0` and `three/addons/` from unpkg |
| UI | HTML/CSS overlays, Font Awesome 6.5 (CDN) |

---

## Repository layout

| Path | Role |
|------|------|
| `index.html` | Shell, styles, main module script, import map |
| `package.json` | `npx http-server -p 8083` for local dev |
| `Flexi_Telescope.svg` | Branding asset |

---

## Local development

```bash
npm install
npm run dev
```

Serves on **8083**. Use HTTP, not `file://`.

---

## Deployment

GitHub Pages or any static host; keep paths relative to repo root.
