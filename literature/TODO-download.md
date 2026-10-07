# Paper acquisition - COMPLETE (14 / 14)

Nothing outstanding. All 14 papers are in `literature/papers/`, each verified by
text-extracting the PDF and confirming title and authors against `matrix.csv`.

Kept as a provenance record, because **which version of a paper you hold affects
how you cite it** - see the note at the bottom.

## Source and version of each PDF

| # | Citekey | Source | Version held |
|---|---|---|---|
| 1 | `xue2016survey` | IEEE Xplore (CC-BY) | **published** - IEEE typeset, pp. 606-626 |
| 2 | `guyon2003introduction` | JMLR, free | published |
| 3 | `mei2023explainable` | Victoria Univ. of Wellington figshare (CC BY-NC-ND) | accepted manuscript |
| 4 | `zhou2025roadmap` | IEEE Xplore | **published** - IEEE typeset, pp. 2213-2228 |
| 5 | `rodrigues2024slug` | Springer (CC-BY) | published |
| 6 | `mweshi2019feature` | Zambia ICT Journal (gold OA) | published |
| 7 | `chen2017feature` | Victoria Univ. of Wellington figshare (CC BY-NC-ND) | accepted manuscript |
| 8 | `muni2006genetic` | IEEE Xplore via U.Porto access | published |
| 9 | `liu2022feature` | Taylor & Francis (gold, CC-BY) | published |
| 10 | `lundberg2017unified` | NeurIPS 2017 proceedings, free | published |
| 11 | `ribeiro2016why` | arXiv:1602.04938**v3** | camera-ready content, no ACM typesetting |
| 12 | `marcilio2020explanations` | IEEE Xplore via U.Porto access | published |
| 13 | `verhaeghe2023powershap` | Springer (CC-BY) | published |
| 14 | `wang2025improving` | Springer (CC-BY) | published |

Only #8 and #12 needed institutional access. Everything else was legal open
access - publisher OA, arXiv, or an institutional repository. No shadow libraries
were used.

## Version notes (2 files, down from 5)

**#3 Mei and #7 Chen are author accepted manuscripts**, not the IEEE typeset
version. The text is the peer-reviewed text, but it is pre-copyedit, so it can
differ from the published article in wording as well as pagination. A concrete
example in this very folder: the Chen accepted manuscript is titled
*"...Improve **Generalisation** of Genetic Programming..."*, while the published
IEEE article uses *"**Generalization**"*. `references.bib` and `matrix.csv`
carry the **published** title and page numbers - quote from those, not from the
PDF's own header.

**#11 Ribeiro is arXiv v3**, which is the camera-ready content: same 10 pages as
the KDD version (pp. 1135-1144) and the same text. It is fine to quote from
directly. The only thing missing is ACM's typesetting and running page numbers,
so take the page range for a citation from `references.bib`.

Everything else in the table is the publisher's own file, so no caveat applies.

## If you add more papers later

1. Drop the PDF in the right theme folder as `Year_FirstAuthor_ShortTitle.pdf`.
2. Add a row to `literature/matrix.csv` (next `id`, `read_status=to-read`).
3. Add the BibTeX entry to `literature/references.bib` with a
   `firstauthorYEARkeyword` citekey.
4. Create `literature/notes/<citekey>.md` using any existing note as a template.
