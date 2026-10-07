# Feature Selection Optimization through Genetic Programming in Machine Learning Models

M.EIC dissertation - FEUP (Faculdade de Engenharia da Universidade do Porto).

## Structure

```
.
├── README.md                     this file
├── admin/                        administrative documents
│   └── thesis-theme.pdf          approved thesis theme
├── slides/                       PDIS class slides (course material)
├── meetings/                     one file per supervisor meeting, YYYY-MM-DD.md
│   ├── 2025-09-26.md             cleaned notes + action items
│   └── 2025-09-26-raw-notes.txt  original notes as typed in the meeting
├── literature/
│   ├── papers/                   PDFs, grouped by theme
│   │   ├── 01-surveys-background/        surveys, foundations
│   │   ├── 02-gp-ga-feature-selection/   GP and GA for feature selection
│   │   ├── 03-xai-shap-lime/             SHAP, LIME, explanation-driven selection
│   │   └── 04-gp-with-xai/               GP combined with XAI
│   ├── notes/                    one <citekey>.md per paper, reading notes
│   ├── matrix.csv                the comparison table (one row per paper)
│   ├── references.bib            BibTeX for all papers
│   ├── tools.md                  existing tools to evaluate
│   └── TODO-download.md          provenance of each PDF + citation caveats
└── deliverables/
    ├── d1-manifest/              deliverable 1
    └── d2-literature-review/     deliverable 2
```

## Conventions

- **PDF filenames:** `Year_FirstAuthor_ShortTitle.pdf` (e.g. `2024_Rodrigues_SLUG.pdf`).
  The year is the *official publication* year, which can differ from the
  online-first year (see `note` fields in `references.bib`).
- **Citekeys:** `firstauthorYEARkeyword` (e.g. `rodrigues2024slug`). The same key
  identifies the paper in `references.bib`, in `matrix.csv`, and as the filename
  in `literature/notes/`.
- **Meeting files:** `meetings/YYYY-MM-DD.md`, one per meeting.

## Working with the literature

`literature/matrix.csv` is the single source of truth for the comparison table the
supervisor asked for. Bibliographic columns are filled; the analysis columns
(`task_type`, `datasets_scenario`, `application_domain`, `method_summary`,
`advantages`, `limitations`, `does_not_solve`, `future_work`,
`relevance_to_thesis`) are intentionally **empty** - fill them while reading.

Each paper also has `literature/notes/<citekey>.md` with those same fields as
headings, plus *Key quotes / figures to cite* and *Ideas for my thesis*.
**Keep the CSV row and the note file in sync.**

`quartile_or_rank` is filled for all 14 rows: SJR/JCR quartiles for journals and
CORE ranks for conferences.

Two PDFs (Mei 2023, Chen 2017) are author accepted manuscripts rather than the
publisher's typeset version, so their wording and pagination can differ from the
published article - always quote the title and page numbers from
`references.bib`. See `literature/TODO-download.md`.

## Status

| | |
|---|---|
| Papers selected | 14 (supervisor asked for 10-15) |
| PDFs collected | 14 / 14 |
| Papers read | 0 / 14 |
| Venue rankings | filled (SJR/JCR + CORE) |
