# yeleshwarapu.github.io

Personal portfolio site for Arjun Yeleshwarapu — ME student at UC Riverside focused on thermal systems, cooling loop design, and energy optimization.

**Live site:** [yeleshwarapu.github.io](https://yeleshwarapu.github.io)

---

## Stack

Plain HTML, CSS, and vanilla JS — no frameworks, no build step, no dependencies.

- **Fonts:** Syne + DM Mono via Google Fonts
- **Images:** Cloudinary CDN for photo strip, GitHub-hosted assets for project images
- **Hosting:** GitHub Pages (static, Jekyll disabled via `.nojekyll`)

---

## Structure

```
/
├── index.html              # Entire site — single file
├── .nojekyll               # Disables Jekyll on GitHub Pages
└── assets/
    ├── images/             # Project photos, CAD renders, screenshots
    ├── photos/             # Photography strip images
    └── images/*.pdf        # Resume
```

---

## Sections

| Section | Description |
|---|---|
| Hero | Name, tagline, animated heat lines |
| About | Background, skills, stats, CAD render |
| Experience | Accordion with image slideshows — Highlander Racing, Utthunga, FRC |
| Projects | Grid — FSAE cooling loop, pump classifier, heat exchanger tool, R'Cycle Co-Op, home energy dashboard |
| Photography | Draggable horizontal photo strip |
| Contact | Email, LinkedIn, GitHub, resume download |

---

## Running Locally

No build step required — just open `index.html` in a browser, or serve it with any static server:

```bash
npx serve .
# or
python -m http.server 8000
```

---

## Contact

- **Email:** ayele002@ucr.edu
- **LinkedIn:** [arjun-yeleshwarapu](https://linkedin.com/in/arjun-yeleshwarapu/)
- **GitHub:** [yeleshwarapu](https://github.com/yeleshwarapu/)
