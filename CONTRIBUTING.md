# Adding New Research

## Folder structure

Each research report lives in its own folder at the repo root:

```
business-research/
├── index.html                        ← hub landing page
├── CONTRIBUTING.md
│
├── arabic-burqa-pakistan-research/
│   ├── index.html                    ← the research dashboard HTML
│   └── research-data/               ← raw data, CSVs, notes, sources
│
└── your-new-research/               ← new report follows the same pattern
    ├── index.html
    └── research-data/
```

## Steps to add a report

1. **Create the folder**
   ```
   your-research-name/
   ├── index.html
   └── research-data/
   ```
   Folder name: lowercase, hyphenated, descriptive (e.g. `pakistan-solar-energy-market`).

2. **Add the research HTML**
   Copy `arabic-burqa-pakistan-research/index.html` as a starting point.
   It has the dark/gold theme, sticky nav, and card layout already wired up.

3. **Add a card to the hub** — open `index.html` and paste inside `#research-grid`:

   ```html
   <a class="card" href="your-research-name/index.html">
     <span class="card-tag">Industry / Sector</span>
     <h2>Short Report Title</h2>
     <p>One or two sentences describing what this report covers.</p>
     <div class="card-meta">
       <span><span class="dot"></span> Published YYYY</span>
       <span>Geography</span>
     </div>
     <span class="card-arrow">↗</span>
   </a>
   ```

4. **Commit and push**
   ```bash
   git add your-research-name/ index.html
   git commit -m "Add [topic] market research"
   git push
   ```
   GitHub Pages deploys automatically — live in ~1 min.

## Research data files

Drop anything into `research-data/` — CSVs, PDFs, notes, source links.
The folder is tracked by git but not linked from the site, so it stays as a reference archive.

## Live site

`https://umarabdullah23.github.io/business-research/`
