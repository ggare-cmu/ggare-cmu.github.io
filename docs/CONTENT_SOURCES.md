# Content Sources — where the same info lives

Purpose: this site repeats the same facts (papers, patents, experience, positioning) across
the website **and** the PDF resume. When you change one, update every location listed here so
they stay consistent. This file is in `docs/` which is excluded from the Jekyll build
(`_config.yml` → `exclude`), so it is never published.

## The two-source rule (read first)

There are **two independent renderers** for the same CV content — editing one does NOT update the other:

| What the visitor sees | Rendered from | Notes |
| --- | --- | --- |
| `/cv/` web page | `_data/cv.yml` (via the `al_folio_cv` gem) | Entries must use `bullet:`/`label:` for custom sections, or they render blank. |
| Downloadable **resume PDF** (`assets/pdf/Gautam_Gare_Resume.pdf`) | `resume_tex/cv_new.tex` (LaTeX) | Hand-maintained; NOT generated from `cv.yml`. See "Regenerate the resume". |
| `/publications/` page + "selected" list on home | `_bibliography/papers.bib` | The resume's Selected Publications is a **separate hand-copied list** in `cv_new.tex`. |

RenderCV (`assets/rendercv/`, `render-cv.yml` workflow) is **not** the live path — the PDF is LaTeX.
Ignore the `assets/rendercv/rendercv_output/*Einstein*` sample.

## Regenerate the resume PDF

```bash
cd resume_tex
export PATH="$HOME/Library/TinyTeX/bin/universal-darwin:$PATH"
pdflatex -interaction=nonstopmode cv_new.tex && pdflatex -interaction=nonstopmode cv_new.tex
cp cv_new.pdf ../assets/pdf/Gautam_Gare_Resume.pdf
rm -f cv_new.aux cv_new.log cv_new.out
```
Source: `resume_tex/cv_new.tex` (+ `altacv.cls`). Everything else in `resume_tex/` is unused and
git-ignored: `cv_new_v1.tex`, `main.tex`, `template.tex`, `papers.bib`, `references.bib`,
`photo.jpg`, `sections/`, `cv_new.pdf`. Do **not** rely on those — `cv_new.tex` hardcodes its content.

## Master map — update these together

### Positioning / summary / tagline ("inference-time adaptation of frozen VLMs")
- `_pages/about.md` — intro line, the Adapt/Understand/Deploy threads, subtitle, "My focus:" line
- `_data/cv.yml` — `cv.summary`, and Education `Focus:` highlight
- `resume_tex/cv_new.tex` — `\tagline{...}`, the Research Summary tcolorbox, Education `Focus:` item
- `_config.yml` — `description:` and `keywords:`

### Publications (title, authors, venue, links, abstract)
- `_bibliography/papers.bib` — **canonical**. Drives `/publications/` and the home "selected" list (`selected: true`).
- `resume_tex/cv_new.tex` — "Selected Publications" section (independent hand-copied list + author initials)
- `_projects/1..5_*.md` — papers referenced inside project narratives (+ their inline links)
- `_news/*.md` — acceptance/coverage announcements (+ their links)
- `_data/coauthors.yml` — co-author name → profile URL (controls author-name links on `/publications/`)
- A paper's **title/link change** => update it in ALL of the above that mention it.

### Author lists (e.g., adding a co-author like Krystal Kirby)
- `_bibliography/papers.bib` (full names)
- `resume_tex/cv_new.tex` (initials form, e.g. `K. Kirby`)

### Patents (numbers, titles, and the COUNT)
- `_pages/patents.md` — **canonical** full list: **5 U.S. + 2 Indian = 7** (links to Google Patents/WIPO)
- `_data/cv.yml` → `Patents:` — mirrors all 7 on `/cv/`
- `resume_tex/cv_new.tex` — "Selected Patents": the **4 CMU/medical** US patents only (no Sling, no Indian)
- `_projects/5_patents.md` — the same **4** CMU/medical patents; says "Four U.S. patents"
- Count phrasing that must agree:
  - "four U.S. patents" (medical scope = 4 CMU patents): `_pages/about.md`, `_data/cv.yml` summary, `resume_tex/cv_new.tex` summary box, `_projects/5_patents.md`
  - "5 U.S. and 2 Indian" / "7 patents" (all patents): `_pages/patents.md` description, `_pages/publications.md`
- `_news/2024-06-01-patents.md` says "Three U.S. patent applications published" — **historical, leave as-is** (accurate for June 2024; the 4th was granted later, the 5th/Sling is non-medical).

### Research & Professional Experience
- `_data/cv.yml` → `Research Experience:` / `Professional Experience:` (`/cv/`)
- `resume_tex/cv_new.tex` → Research Experience, Professional Experience sections
- `_pages/about.md` — Sling/DawnLight/Bosch prose mentions
- `_news/*.md` — 2021-08 PhD start, 2021-06 DawnLight, 2026-05 Bosch, 2026-07 candidacy

### Education
- `_data/cv.yml` → `Education:`  •  `resume_tex/cv_new.tex` → Education  •  `_pages/about.md` (M.S./B.E. prose)

### Fellowships & Awards
- `_data/cv.yml`  •  `resume_tex/cv_new.tex`  •  `_projects/5_patents.md` (grants)  •  `_pages/about.md` (Liang Zhao, CMLH)  •  `_news/*` (fellowship announcements)

### Teaching & Service
- `_pages/teaching.md` — **canonical** (Teaching / Reviewing / Talks / Mentorship)
- `_data/cv.yml` → `Teaching and Service:`  •  `resume_tex/cv_new.tex` → Teaching & Service

### Media Coverage
- `_data/cv.yml` → `Media Coverage:`  •  `resume_tex/cv_new.tex` → Media Coverage  •  `_news/*` (LINK Magazine 2022, New Zhiyuan 2024)

### Projects (thematic research pages)
- `_projects/1_vlm_prompt_optimization.md` — Inference-Time Adaptation of VLMs (DetPO, Attribute Selection, ARM, Soft-prompt)
- `_projects/2_causal_feature_selection.md` — When Can Models Trust Their Training Data? (LCA, Natural Experiments, Ask Twice)
- `_projects/3_lus_biomarkers.md` — Interpretable Lung Ultrasound Biomarkers
- `_projects/4_label_structure.md` — Learning with Label Structure and Uncertainty
- `_projects/5_patents.md` — Patents & Translational Work
- Credit lives on `/publications/`; project pages intentionally have **no** `Collaborators:` lists.

### Contact / socials / identity
- `_data/socials.yml` (a hash-valued social needs `title:`+`logo:` or the build errors)
- `_pages/about.md` profile block  •  `_config.yml` (`first_name`, `email`, `og_image`, etc.)

### Wildlife gallery
- `_pages/wildlife_pics.md` — curated `photos:` list (deduped, one per subject, `data-zoomable` for zoom)
- `assets/wildlife_clicks/` — only files in the `photos:` list are git-tracked; unused/`exclude_*` are git-ignored

### Resume PDF link
- File: `assets/pdf/Gautam_Gare_Resume.pdf` (tracked)  •  Linked from `_pages/cv.md` (`cv_pdf:`) and `_pages/about.md`

## Gotchas
- **Patent counts have two valid scopes**: "four" = CMU/medical US patents (about, cv summary, resume, project 5); "5 US + 2 Indian = 7" = everything (patents tab, publications). Keep each in its lane.
- **`cv.yml` custom sections only render on `/cv/` if entries use `bullet:` or `label:`** — `title:`/`company:`/`name:` render blank there (gem limitation).
- **Kramdown treats a bare `|` as a table cell** — escape as `\|` inside `bullet:` strings.
- After editing `_config.yml`, **restart** `jekyll serve` (config is not hot-reloaded).

## Customizations & gem overrides (re-check on `bundle update`)

These local files shadow or extend `al_folio_core` gem files. On a gem upgrade, run
`bundle exec al-folio upgrade overrides audit` — if it reports drift, re-apply the change on
top of the new upstream file. Acknowledged overrides are recorded in `.al-folio-overrides.yml` (commit it).

| Local file | What it does | Tracked? |
| --- | --- | --- |
| `assets/js/theme.js` | Default theme = **light/day**: one line, `determineThemeSetting()` fallback `"system"` → `"light"`. Toggle (light→dark→system) unchanged. | Yes — `.al-folio-overrides.yml` |
| `_sass/_publications.scss` | Pre-existing style override of the publications page. | Not yet acknowledged (`overrides accept` to record) |
| `_includes/zoom_original_fix.liquid` | Local include (used by `about.md`) that points medium-zoom's `data-zoom-src` at the full-res image. | Local include, not a gem shadow |
| `_data/socials.yml` → `cmu_cs_homepage` | Custom hash-valued social needs `title:`+`logo:` (else the `jekyll-socials` build errors). | Data file |

Related knobs in `_config.yml`: `enable_darkmode: true` (toggle on; set `false` to remove dark mode entirely), `max_width: 1200px` (content width), `enable_medium_zoom: true` (click-to-zoom, used by the wildlife gallery via `data-zoomable`).
