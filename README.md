# Graduate Attributes Self-Assessment

**Live tool: https://drdukegledhill.github.io/GraduateAttributes/**

A lightweight, single-page web tool for students to self-assess their development across the University of Huddersfield's seven Graduate Attributes. No accounts, no server, no data storage — progress is encoded directly in a bookmarkable URL.

## Graduate Attributes

| Attribute | Description |
|---|---|
| Self-motivated | Ability to do what needs to be done without being prompted |
| Commercially aware | Understanding of the wider environment organisations operate in |
| Enterprising | Adapting thinking and behaviour to changing circumstances |
| Resilient | Driven, resolute, and able to deal positively with challenges |
| Effective collaborator | Working well with others and effective interpersonal skills |
| Confident leader | Enthusing a group and motivating them towards a shared goal |
| Globally & socially aware | Welcoming new perspectives and anticipating external impacts |

## How it works

Students visit the page and rate themselves 1–5 on each attribute. The radar/spider chart updates in real time as they answer. On saving, the browser URL updates to encode their scores — they bookmark it and return later for subsequent assessments.

Up to **5 assessments** can be completed across the academic year. Each new assessment adds another layer to the radar chart, making development over time visible at a glance.

Once two assessments are saved, an **Assessment / Progress** tab switcher appears at the top of the page. The Progress tab shows:

- **Score trends** — a line chart tracing each attribute across all completed assessments, with a colour-coded legend
- **Progress so far** — a side-by-side score grid for quick comparison

Switching back to the Assessment tab always presents a clean form for the next round. A **dark/light mode** toggle (☀️/🌙) in the header switches themes, with the preference saved in the browser.

### URL format

Each assessment is stored as a 7-digit string (one digit per attribute, 1–5):

```
index.html?v1=3452341
index.html?v1=3452341&v2=4563452
```

No data ever leaves the student's browser.

## Hosting

The tool is designed to be served via **GitHub Pages** from the `/docs` folder.

1. Push this repository to GitHub
2. Go to **Settings → Pages**
3. Set source to **Deploy from branch → `main` → `/docs`**
4. The tool will be available at `https://<username>.github.io/<repo>/`

## Development

The tool is a single self-contained HTML file at `docs/index.html` with no build step or dependencies beyond a CDN-hosted copy of [Chart.js](https://www.chartjs.org/).

To run locally, open `docs/index.html` directly in a browser or serve with any static file server:

```bash
npx serve docs
```

## Licence

[Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)](LICENSE)

© Dr Duke Gledhill. Free to use and adapt for non-commercial educational purposes with attribution.
