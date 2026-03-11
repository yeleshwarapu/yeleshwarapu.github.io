# yeleshwarapu.github.io

Portfolio site for **Arjun Yeleshwarapu**, third-year Mechanical Engineering student at UC Riverside (Class of 2027). The site documents work across thermal systems, fluid simulation, embedded controls, and data-driven engineering tools.

**Live:** [yeleshwarapu.github.io](https://yeleshwarapu.github.io)

---

## About

I'm focused on the intersection of thermal analysis and physical systems — particularly where simulation informs design and testing closes the loop. At **Highlander Racing FSAE Electric**, I lead the cooling subteam: developing MATLAB thermal models for the liquid cooling loop, scaling the team from 2 to 11 members, and owning the full design-to-test lifecycle for the 26E racecar's motor and inverter cooling architecture.

Last summer I interned at **Utthunga** (Houston, TX & Bengaluru, India) on the Asset Performance Management team — building parametric Python tools for pump performance curves, training a 96%-accurate pump health classifier on synthetic sensor data, running FEA thermal simulations in Altair SimLab, and shadowing DCS and APM engineering teams on-site.

Outside of coursework and team projects, I build software tools that sit at the edge of engineering and data science — the R'Cycle Co-Op cycling route planner and a modular home energy simulation being two recent examples.

---

## Tech Stack

The site is intentionally zero-dependency — no framework, no bundler, no npm. Everything runs in a single `index.html` file.

| Layer | Detail |
|---|---|
| **Markup** | Semantic HTML5 |
| **Styling** | Vanilla CSS with custom properties (design tokens for color, spacing) |
| **Scripting** | Vanilla ES6+ JavaScript — no libraries |
| **Fonts** | [Syne](https://fonts.google.com/specimen/Syne) (headings) + [DM Mono](https://fonts.google.com/specimen/DM+Mono) (body/mono) via Google Fonts |
| **Image CDN** | Cloudinary fetch URL transforms (`w_640,c_limit,q_auto,f_auto`) for the photo strip |
| **Project assets** | Self-hosted on GitHub Pages under `assets/` |
| **Hosting** | GitHub Pages — Jekyll disabled via `.nojekyll` |
| **Analytics** | None |

### Key implementation details

- **Custom cursor** — dual-layer (dot + ring) with `mix-blend-mode: exclusion` and a lerp-based ring follow animation via `requestAnimationFrame`
- **Parallax** — lightweight `scroll` listener driving `translateY` on hero background layers via `data-speed` attributes
- **Accordion** — height animation using measured `scrollHeight` rather than `max-height: 9999px`, avoiding layout jank
- **Slideshows** — `ExpSlideshow` class handles auto-advance with a progress bar, touch swipe, pause-on-hover, and dot navigation. Bidirectionally synced with the lightbox
- **Lightbox** — full-screen overlay with keyboard nav (`←` `→` `Esc`), touch swipe, backdrop blur, and auto-advance timer that resets on manual interaction
- **Scroll reveal** — `IntersectionObserver` with staggered `transition-delay` classes
- **SVG data visualizations** — all project chart visuals (pump curve, coolant temp, classifier output, heat exchanger temperature profile) are hand-coded inline SVGs with CSS `animate` draw-on effects
- **Photo strip** — mouse drag scroll via `mousedown`/`mousemove` delta with `scroll-snap-type: x mandatory`
- **Marquee** — pure CSS `@keyframes` animation, duplicated content for seamless loop

---

## Sections

### Hero
Full-viewport section with animated SVG heat lines (4 layered `<animate>` paths), a radial gradient background, a CSS grid overlay, ambient orbs, a live status indicator, and a scroll-bounce indicator. Parallax on background layers tied to `window.scrollY`.

### About
Two-column grid. Left: biography paragraphs and a 2×2 stats grid (team scaling, mass reduction, classifier accuracy, peak coolant temp). Right: skill tag groups organized by category (Software, Programming, Domain, Certifications) plus the SolidWorks CAD render of the 26E cooling loop.

### Experience
Accordion-style list of three roles. Each entry expands to reveal a description and an image slideshow:
- **Cooling Subteam Lead** — Highlander Racing FSAE Electric (Mar 2024 – Present)
- **Mechanical Engineering Intern** — Utthunga, Houston TX & Bengaluru India (Jun–Aug 2025)
- **President** — FIRST Robotics Competition Team 256 (Aug 2019 – Jun 2023)

### Projects
CSS grid layout with a featured full-width card and a 2-column grid below:
- **Liquid Cooling Loop — 26E Racecar** *(featured)* — MATLAB simulation, SolidWorks design, Arduino PWM fan control, inline SVG pump/system curve and coolant temp charts
- **Pump Performance Classifier** — scikit-learn Decision Tree, 96% accuracy, synthetic sensor data across vibration/temperature/pressure
- **Heat Exchanger Analysis Tool** — LMTD + ε-NTU methods, modular Python, Altair SimLab ECU thermal analysis
- **R'Cycle Co-Op** — Python cycling route planner scored against PM2.5, ozone, UV, shade, and loop geometry. Deployed on HuggingFace Spaces. Image slideshow with 4 city examples
- **Home Energy Dashboard** — Modular HVAC/EV/solar simulation with season-aware load profiles and interactive controls

### Photography
Horizontally scrollable drag strip of 21 photos. Images served through Cloudinary fetch transforms for automatic format/quality optimization. `scroll-snap-type` for discrete snapping, `grab`/`grabbing` cursor on drag.

### Contact
Two-column grid with a heading and four contact links (email, LinkedIn, GitHub, resume PDF download).

---

## File Structure

```
/
├── index.html                          # Entire site
├── .nojekyll                           # Disables Jekyll processing on GitHub Pages
└── assets/
    ├── images/                         # Project screenshots, CAD renders, lab photos
    │   ├── FINALLLRENDER.png           # SolidWorks cooling loop render
    │   ├── sanfrancisco20mi.png        # R'Cycle Co-Op route screenshots
    │   ├── waterloo10mi.png
    │   ├── seattlemobile.png
    │   ├── routequality.png
    │   └── YeleshwarapuArjun2026Resume-6.pdf
    └── photos/                         # Photography strip (DSCF*, AGDC*, film scans)
```

---

## Running Locally

No build step. Open directly or use any static file server:

```bash
# Python
python -m http.server 8000

# Node
npx serve .

# Or just open index.html in a browser
```

---

## Contact

| | |
|---|---|
| **Email** | ayele002@ucr.edu |
| **LinkedIn** | [arjun-yeleshwarapu](https://linkedin.com/in/arjun-yeleshwarapu/) |
| **GitHub** | [yeleshwarapu](https://github.com/yeleshwarapu/) |
| **Resume** | [PDF](https://yeleshwarapu.github.io/assets/images/YeleshwarapuArjun2026Resume-6.pdf) |
