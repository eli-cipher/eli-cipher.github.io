# ELI CIPHER // SAT-LINK — Portfolio

Satellite communications & offensive space cybersecurity portfolio.
Single-file vanilla HTML/CSS/JS — no build step, $0 stack.

## Stack

| Layer | Tool |
|---|---|
| 3D hero | Three.js (CDN) — dot-sphere Earth, 3 orbiting satellites, RF beams, starfield |
| Animation | GSAP + ScrollTrigger (CDN) — boot wipe, scroll reveals, pinned attack chain |
| Icons | Lucide (CDN) + inline SVGs for brand icons (removed from Lucide) |
| Fonts | Google Fonts — Space Grotesk / JetBrains Mono |
| Extras | Live ISS position (api.wheretheiss.at, no key) · Canvas RF spectrum · command palette |

## Features

- Boot sequence loader → wipes into hero
- **Clickable satellites** — each opens a project "payload manifest"
- `sudo hack` easter egg (type it anywhere)
- Footer command palette: `help`, `whoami`, `projects`, `skills`, `contact`, `flag`, `clear`
- Pinned scroll "attack chain": Recon → Signal Acquisition → Protocol Analysis → Exploitation → Intercept & Flag
- Light/dark theme toggle (persisted)
- Custom crosshair cursor (desktop only), RF spectrum widget, live ISS telemetry
- `prefers-reduced-motion` + mobile fallbacks (no pin, paused render loops offscreen)

## Run locally

Open `index.html` directly, or serve:

```bash
python3 -m http.server 8000
```

## Deploy

**GitHub Pages** — push this folder to a repo → Settings → Pages → deploy from `main` (root).
`404.html` is included and served automatically.

**Netlify Drop** — drag the folder onto [app.netlify.com/drop](https://app.netlify.com/drop).

## Files

```
index.html   ← the whole site
404.html     ← themed not-found page
og-cover.png ← social link preview image
```

## Maintenance notes

- Brand social icons are inline SVGs (Lucide dropped brand icons — do not re-add via `data-lucide`)
- `data-lucide="code-xml"` (renamed from `code-2` in newer Lucide)
- Render loops pause when offscreen/tab hidden; canvases render one static frame under reduced motion
- Update the two `wu-soon` writeup cards (`href="#"`) when the SATCOM posts go live
