# Hausa Language Technologies in the Age of Artificial Intelligence
## Systematic Review: Corpus, Protocol, and Extraction Records (2019–2026)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23972015.svg)](https://doi.org/10.5281/zenodo.23972015)

This repository contains every machine-readable artifact of the systematic review
"Hausa Language Technologies in the Age of Artificial Intelligence: A Systematic
Review of Resources, Applications, Challenges, and Research Gaps", covering the
2019–2026 neural and pre-trained model era.

## Authors

- **Ismail Suleiman** - Woxsen University, Hyderabad, India - iismail.suleiman_phd.2026@woxsen.edu.in
- **Dr. Monday Jubrin Abdullahi** (supervisor) - Woxsen University, Hyderabad, India - abdullahi.monday@woxsen.edu.in

## How to cite

Cite the archived dataset via its Zenodo DOI
([10.5281/zenodo.23972015](https://doi.org/10.5281/zenodo.23972015)) and/or the
review paper. Citation metadata is in `CITATION.cff`.

## Structure

```
data/
  selection_counts.csv         counts for every stage of the study-selection flow
                               (169 downloaded -> 153 verified Hausa -> 150 in 2019-2026)
  screening_decisions.csv      one row per candidate paper in the version-1 collection
                               (V1-001 to V1-169: filename, title, year, link, decision,
                               reason, and final corpus ID; 169 rows)
  study_inventory.csv          the 150 included studies (2019-2026) with metadata,
                               thematic block, per-study insight, paper section, and QA scores
  quality_assessment.csv       the five-item bibliographic rubric, scored per study
  extraction_sheet.csv         fixed extraction form: task, dataset, size, method, result
  resource_catalogue.csv       the 41 resources (R-01..R-41, all 2019-2026) with year,
                               type, domain, size, access, insight, and paper section
  evidence_gap_matrix.csv      each gap G1-G10 mapped to cited studies, with quality-band
                               breakdown
  claim_audit_log.csv          audit of claims and how each was verified against the PDFs
docs/
  CHANGELOG_LRE.md             detailed change log for the LRE submission
corpus_construction.md         collection and screening record: version 1 (169 downloaded
                               papers), full-text screening (169 -> 153), and 2019-2026
                               temporal filter (153 -> 150)
latex/                         full LaTeX source of the review (main.tex, refs.bib,
                               figures, appendix, and Springer Nature class files)
.zenodo.json                   Zenodo deposit metadata
CITATION.cff                   citation metadata for this repository
LICENSE                        CC BY 4.0
```

## Study IDs

`P-001` ... `P-154` (minus pre-2019 records `P-003`, `P-122`, `P-123` and unverified `P-062`, 150 studies total from 2019–2026) are stable identifiers for the included studies. Resource records are `R-01` ... `R-41` (all 2019–2026).

## Quality assessment

The rubric (paper Table 4) scores five objectively verifiable items: venue class (0/0.5/1), data statement (0/0.5/1), quantitative result (0/1), Hausa specificity (0/1/2), and artifact link (0/1), for a maximum of 6 points. Bands: High >= 4.5, Medium 2.5-4.4, Low < 2.5. The scoring is mechanical and can be recomputed from `extraction_sheet.csv`; it measures documentation transparency and Hausa specificity, not methodological rigour.

## Reproducibility statement

Every one of the 169 candidate papers in the version-1 collection (`V1-001` to `V1-169`) was inspected at full text, and every screening decision is logged with its reason in `data/screening_decisions.csv`. Full-text screening excluded 15 papers lacking direct Hausa content (E1) and 1 paper whose PDF failed verification (`V1-062`, E2), leaving 153 verified Hausa studies; applying the 2019–2026 temporal eligibility criterion (I2) then excluded 3 pre-2019 studies (`P-003` [2009], `P-122` [2012], `P-123` [2012]), yielding the final corpus of 150 studies alongside 41 computational resources from 2019–2026 (see `corpus_construction.md`).

## License

CC BY 4.0. The full-text PDFs (`version_1/` with 169 files and `final_version_150/` with 150 files) are distributed separately on request, respecting the access conditions of their publishers.
