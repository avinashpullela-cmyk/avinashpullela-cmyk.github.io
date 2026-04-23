# Avinash Pullela — Portfolio

Personal portfolio website for **Avinash Pullela**, Senior Product Manager specialising in liquidity management, data products, and fintech. Live at [avinashpullela-cmyk.github.io](https://avinashpullela-cmyk.github.io).

## What's Inside

The site is a single-page portfolio covering:

- **Work** — In-depth case studies from Citi and Tata Steel: stress modelling platforms, data fabric infrastructure, and supply chain operations.
- **Ventures** — Side consulting work (Citac Inc.) connecting Indian precision-casting suppliers with North American buyers.
- **Projects** — Active personal projects being built in free time. Currently: a Food & Beverage Taste Profiler and a Personal Style Suggestion Engine.
- **Skills** — Domain expertise across product management, fintech, capital markets, data, and agile delivery.
- **Timeline** — 12+ year career history from engineering through to senior PM roles.

## Tech Stack

| Layer | Detail |
|---|---|
| Frontend | Vanilla HTML, CSS, JavaScript |
| Fonts | DM Sans (body), Playfair (headings) via Google Fonts |
| Styling | CSS custom properties, OKLch colour model, CSS Grid / Flexbox |
| Build | Custom asset bundler — fonts and assets are gzip-compressed and base64-embedded into `index.html` |
| Deploy | GitHub Pages via GitHub Actions (Jekyll Docker workflow) |

The entire site ships as a single `index.html` file with no runtime dependencies.

## Adding a New Side Project

Side projects are driven by a JavaScript array at the bottom of the `<script>` block inside `index.html`. To add a new project, append an object to the `PROJECTS` array:

```js
const PROJECTS = [
  // existing projects ...
  {
    icon: "🚀",                          // emoji shown on the card
    name: "Your Project Name",
    status: "building",                  // "active" | "building" | "idea"
    statusLabel: "Building",             // label shown in the badge
    description: "One or two sentences describing what you are building and why.",
    tags: ["Tag 1", "Tag 2", "Tag 3"]
  }
];
```

Save the file and push — GitHub Actions will redeploy automatically.

## Local Preview

Because the site is a self-contained HTML file you can preview it locally without any build step:

```bash
# Any static server works — e.g. Python's built-in one:
python3 -m http.server 8080
# Then open http://localhost:8080
```

## Deployment

Pushes to `main` trigger the GitHub Actions workflow at `.github/workflows/jekyll-docker.yml`, which builds the site with Jekyll and publishes it to GitHub Pages.

## Contact

- **Email:** avinash.pullela@gmail.com
- **LinkedIn:** [linkedin.com/in/avinashpullela](https://linkedin.com/in/avinashpullela)
- **Location:** Greater Toronto Area, Ontario
