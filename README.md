# Emily Strickland

My M.S. Data Science portfolio, built with [Quarto](https://quarto.org) and
published at **[emvstrick.github.io](https://emvstrick.github.io)**.

M.S. Data Science, Willamette University, 2026. Two summers at NASA's Jet
Propulsion Laboratory working with aerosol and remote sensing data. Currently
focused on data engineering and geospatial work.

## What's here

| Page | What it covers |
|------|----------------|
| [Home](https://emvstrick.github.io) | Short introduction and current focus |
| [Capstone](https://emvstrick.github.io/capstone.html) | Reading the Data: an analysis of Willamette University Library's e-resource usage |
| [Projects](https://emvstrick.github.io/projects.html) | Course and side projects, including a Prague metro data warehouse and pipeline |
| [Resume](https://emvstrick.github.io/resume.html) | Web summary plus downloadable PDF |
| [About](https://emvstrick.github.io/about.html) | The longer version |

### Featured work

**Reading the Data: An Analysis of WU Library's E-Resource Usage** (M.S. capstone,
with Sophia Rabbanian and Tiffany Truong). Seven COUNTER usage reports across five
publisher platforms joined to three years of university enrollment data, so
librarians can see which e-resources each department actually uses before deciding
what to renew or retire. Code lives at
[sophiarabb/data510-libraries](https://github.com/sophiarabb/data510-libraries).

**Prague Metro Ridership: Warehouse, Pipeline, and Dashboards** (Advanced Data
Engineering). A PostgreSQL star-schema warehouse on a containerized Linux VM,
Airflow pipelines landing Parquet in an S3-compatible lake, dbt transformations,
and Grafana dashboards over roughly 443,000 rides.

## How this site is built

Quarto renders the `.qmd` files into a static site. Every push to `main` triggers
[`.github/workflows/publish.yml`](.github/workflows/publish.yml), which renders and
deploys to GitHub Pages. Build output is never committed.

Computational output is frozen (`execute: freeze: auto` in `_quarto.yml`), so CI
installs only Quarto and does not need R or Python. If I add a code chunk, I
render locally first and commit `_freeze/`.

### Running it locally

```bash
git clone https://github.com/emvstrick/emvstrick.github.io.git
cd emvstrick.github.io
quarto preview
```

`quarto preview` watches for changes and reloads on save.

## Repository layout

```
.
├── _quarto.yml                    # site config, navbar, theme
├── index.qmd                      # home
├── capstone.qmd                   # featured capstone
├── projects.qmd                   # listing page for other projects
├── projects/
│   ├── capstone/                  # capstone figures
│   └── prague-metro-warehouse/    # data engineering project
├── resume.qmd                     # resume page
├── about.qmd
├── assets/                        # resume PDF
├── images/                        # headshot
├── styles.scss                    # theme tweaks
└── .github/workflows/publish.yml  # deploy
```

## Contact

- Email: [emvstrick@icloud.com](mailto:emvstrick@icloud.com)
- LinkedIn: [emilyvstrickland](https://linkedin.com/in/emilyvstrickland)

---

Built for DATA 510: Data Science Capstone, Willamette University, from the course
Quarto portfolio template.