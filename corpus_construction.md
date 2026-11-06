# Corpus construction and screening record

This document records the collection, full-text screening, and temporal eligibility filtering of the review corpus, matching `data/screening_decisions.csv` (169 rows) and `data/selection_counts.csv`.

## 1. Initial downloaded collection (version 1: n = 169)

To assemble the candidate literature on Hausa language technology, we compiled an initial collection (version 1) of **169 downloaded papers** (`V1-001` to `V1-169`, archived in the `version_1/` folder). Candidate works were collected from the primary venues and repositories where African and Hausa language technology research is published: the ACL Anthology (including main conferences and the AfricaNLP, WMT, LoResMT, and SemEval workshops), arXiv, IEEE Xplore, Springer, ACM, regional Nigerian and African university journals, and open-access repositories. Alongside the candidate papers, we compiled a parallel catalogue of **41 computational resources** (`R-01` to `R-41`) covering text corpora, speech corpora, lexicons, pre-trained models, and evaluation benchmarks for Hausa.

## 2. Full-text topical and document verification (169 -> 153)

Every one of the 169 downloaded papers in version 1 was read at full text and assessed against the review's scope criteria (paper Table 2). At this full-text screening stage, **16 records were excluded**:

| Decision | n | Details |
|---|---|---|
| Excluded at full text: no Hausa-specific content (E1) | 15 | Multi-language African or low-resource studies whose full texts do not evaluate, build, or analyse a Hausa dataset or system (`V1-080`, `V1-081`, `V1-082`, `V1-087`, `V1-095`, `V1-096`, `V1-097`, `V1-098`, `V1-100`, `V1-116`, `V1-124`, `V1-142`, `V1-154`, `V1-168`, `V1-169`). |
| Excluded: failed PDF content verification (E2) | 1 | `V1-062` (originally assigned `P-062`, a Hausa stopwords study): the hosted PDF file contained a different journal article from the same issue, and an authentic publisher copy could not be obtained. |
| **Retained after full-text screening** | **153** | Verified Hausa language technology studies (`P-001` to `P-154` minus `P-062`). |

## 3. Temporal eligibility filter: 2019-2026 review window (153 -> 150)

Because the review focuses strictly on the modern neural and pre-trained model era from **2019 to 2026** (Criterion I2), we applied a temporal eligibility filter to the 153 verified Hausa studies and the 41 catalogued resources:

- **3 pre-2019 studies excluded under E1/I2:**
  - `V1-003` (formerly `P-003`, 2009): *Tone and Length in an LKB-grammar of Hausa*.
  - `V1-133` (formerly `P-122`, 2012): *HaG: A Computational Grammar of Hausa*.
  - `V1-134` (formerly `P-123`, 2012): *Hausa Large Vocabulary Continuous Speech Recognition*.
- **150 studies retained in the final 2019-2026 review corpus:** `P-001` to `P-154` minus `P-003`, `P-062`, `P-122`, and `P-123` (archived in `final_version_150/`).
- **41 computational resources retained in full:** all 41 resources (`R-01` to `R-41`) were verified to have been released between 2019 and 2026 (`data/resource_catalogue.csv`).

## 4. Final corpus summary (2019-2026)

- **150 included studies** (`2019: 3, 2020: 4, 2021: 8, 2022: 18, 2023: 15, 2024: 20, 2025: 39, 2026: 43`; `74` peer-reviewed venue/workshop, `43` preprint/repository copy, `33` other venue; `58 High, 91 Medium, 1 Low` on the 0-6 quality rubric).
- **41 catalogued resources** (`R-01` to `R-41`, all 2019-2026).
- Every per-record screening decision and reason is logged in `data/screening_decisions.csv` (169 rows), and the stage counts are recorded in `data/selection_counts.csv`.
