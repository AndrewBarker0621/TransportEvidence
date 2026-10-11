# Transport Evidence — company website

Static site for [transportevidence.com](https://transportevidence.com/): AI-driven traffic modelling, simulation and optimisation at city scale.

## Pages

| File | Purpose |
| --- | --- |
| `index.html` | Landing page: hero, problem, what we do, how it works, use cases, team, contact |
| `product.html` | The workflow in depth, deliverables, human-oversight table, illustrative example, approach and data handling |
| `use-cases.html` | Six use cases (question → what we model → what you get) and who we work with |
| `about.html` | Mission, founders' full profiles and selected publications |
| `contact.html` | Email CTA, what to include, pilot offer, FAQ |
| `privacy.html` | Privacy statement |
| `404.html` | Not-found page (GitHub Pages serves it automatically) |

Supporting files: `styles.css`, `main.js` (mobile menu, footer year), `favicon.svg`, `images/` (logo, founder photos, `og.jpg` share image, `aws.svg` and `claude.svg` text wordmarks for the "Supported by" strip), `sitemap.xml`, `robots.txt`, `.nojekyll`, `CNAME`.

All pages share the same header and footer markup. When you change the navigation or footer, apply the change to every page. `404.html` uses absolute paths (`/styles.css`) because GitHub Pages serves it for any missing URL, including nested ones.

Every page carries a Content-Security-Policy meta tag that allows only the site's own files plus Google Fonts. If you add analytics, a form service or any other third-party script, add its host to that tag (on every page) or the browser will block it.

## Things to fill in

- **Ricardo's photo**: replace `images/xinyu-wang.svg` with a photo (square crop, about 900×900) and update the two `<img>` tags that reference it (`index.html`, `about.html`).
- **Illustrative figures**: the "See it in action" table on the landing page and the lane-closure example on the product page use synthetic numbers and generic street names. Replace them with a real open-data demonstration when one exists, and keep the "illustrative" label until then.
- **Claims to confirm**: deliverables (`product.html`), pilot offer and the FAQ answers (`contact.html`), and the data-handling wording (`product.html`, `privacy.html`) describe the intended way of working. Review them before launch.

## Deploying on GitHub Pages

1. Push this folder to a GitHub repository.
2. Settings → Pages → Source: *Deploy from a branch*, branch `main`, folder `/ (root)`.
3. Keep the `CNAME` file so the site is served at `transportevidence.com` (DNS must point to GitHub Pages).
