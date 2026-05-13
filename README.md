# isaelanjos.github.io

This repository contains the **production build** of my personal portfolio: a single-page site presenting my background in **DevOps, cloud architecture and platform engineering**, technical focus areas, career timeline, and professional contact channels.

---

## Live site

After you deploy the contents of this folder (for example to **GitHub Pages** or any static host), add your public URL here, e.g. `https://<username>.github.io/<repository>/` or your custom domain.

---

## Tech stack

| Layer        | Details |
| ------------ | ------- |
| **Markup**   | Semantic HTML5 |
| **Styling**  | CSS3 (custom layout, responsive breakpoints, fixed section canvas where applicable) |
| **Behavior** | Vanilla JavaScript (no framework runtime) |
| **Icons**    | [Boxicons](https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css) via CDN — vector icons without bundling sprite assets in-repo |

Production assets in this folder are **minified** (HTML/CSS) and the script bundle is **minified and obfuscated** for a smaller payload and harder casual inspection of client-side logic.

---

## Additional resources

- **Contact** — Social and mail links are wired in JavaScript from a single configuration object; the contact block also references **IRA Soluções** for consulting and company inquiries (`https://www.irasolucoes.com.br`, `isael.anjos@irasolucoes.com.br`). There is **no** third-party form backend (e.g. Formspree); primary personal outreach is via **mailto** and linked profiles.

---

## Project layout (this build)

```
publish/
├── README.md
├── index.html              # Main page (minified)
└── assets/
    ├── style.min.css       # Minified stylesheet
    ├── script.min.js       # Minified + obfuscated application script
    └── profile.jpg         # Portrait asset
```

External stylesheets (Boxicons) are still loaded from the **unpkg** CDN as referenced in `index.html`.

---

## JavaScript capabilities

The script bundle powers:

1. **Contact deep links** — Elements marked with `data-contact` receive the correct `href` (email with prefilled subject, LinkedIn, GitHub, WhatsApp, Facebook, Instagram).
2. **Career journey modal** — Timeline dots open a modal with role-specific narrative text; backdrop and close controls; **Escape** closes the modal.
3. **Journey wire** — SVG path follows the horizontal timeline and updates on scroll/resize.
4. **Timeline scroll UX** — Edge affordances, smooth nudge on click, hover-driven scroll assist where supported, and alignment with `ResizeObserver` / font loading where available.
5. **Navigation** — Mobile menu toggle (hamburger ↔ close); **active section** highlighting in the header based on scroll position; **sticky** header after scrolling past a threshold; menu closes when a nav link is activated (after scroll).

These behaviors are implemented without a SPA framework, keeping the surface area small and hosting requirements limited to static file delivery.

---

## Responsiveness

The layout uses fluid typography, breakpoint-based rules, and a collapsible navigation pattern for smaller viewports so the experience remains usable on phones, tablets, and desktops.

---

## Version control & collaboration

Development history and collaboration are managed with **Git** and **GitHub** (or your chosen remote), so changes can be reviewed, tagged, and deployed in a repeatable way. This `publish/` tree is the **artifact** you upload to production; source files and the build pipeline typically live one level up in the same repository.

---

## Contributing

Issues and pull requests are welcome for typos, accessibility improvements, or constructive refactors. Please keep changes focused and describe the motivation in the PR body.

---

## Contact

- **Personal / general:** `isael.r.anjos@gmail.com`  
- **Company / consulting (IRA Soluções):** `isael.anjos@irasolucoes.com.br` — see also [irasolucoes.com.br](https://www.irasolucoes.com.br)  
- **LinkedIn:** [linkedin.com/in/isael-anjos-61265a130](https://www.linkedin.com/in/isael-anjos-61265a130/)

Prefer using the links on the live site when available.

---

Copyright © 2026 **Isael Anjos**. All rights reserved.
