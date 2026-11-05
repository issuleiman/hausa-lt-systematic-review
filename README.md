# Hausa Language Technologies in the Age of Artificial Intelligence
## Systematic Review: Corpus, Protocol, and Extraction Records (2019–2026)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23972015.svg)](https://doi.org/10.5281/zenodo.23972015)

This repository contains every machine-readable artifact of the systematic review
"Hausa Language Technologies in the Age of Artificial Intelligence: A Systematic
Review of Resources, Applications, Challenges, and Research Gaps", reported in
line with the study-selection 2020 statement and covering the 2019–2026 neural and
pre-trained model era.

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
  corpus_v1.xlsx               version-1 corpus (250 quota-structured publications)
  selection_counts.csv         counts for every stage of the study-selection flow
  screening_decisions.csv      one row per record: stream, decision, reason, retrieval
                               route, and study ID (472 rows)
  study_inventory.csv          the 150 included studies (2019-2026) with metadata,
                               thematic block, per-study insight, paper section, and QA scores
  quality_assessment.csv       the five-item bibliographic rubric, scored per study
  extraction_sheet.csv         fixed extraction form: task, dataset, size, method, result
  resource_catalogue.csv       the 41 resources (R-01..R-41, all 2019-2026) with type,
                               domain, size, access, insight, and paper section
  evidence_gap_matrix.csv      each gap G1-G10 mapped to cited studies, with quality-band
                               breakdown
  claim_audit_log.csv          audit of categorical claims and how each was substantiated
docs/
  CHANGELOG_LRE.md             detailed change log for the LRE submission
corpus_construction.md         provenance record: corpus v1 (250), scope screening
                               (250 -> 28), completion pass (63 working collection + 159 register -> 122 net studies), and timestamps
latex/                         full LaTeX source of the review (main.tex, refs.bib,
                               figures, appendix, and Springer Nature class files)
.zenodo.json                   Zenodo deposit metadata
CITATION.cff                   citation metadata for this repository
LICENSE                        CC BY 4.0
```

## Study IDs

`P-001` ... `P-154` (minus pre-2019 records `P-003`, `P-122`, `P-123` and unverified `P-062`, 150 studies total from 2019–2026) are stable identifiers for the included studies, assigned in the
final synthesis order. Resource records are `R-01` ... `R-41` (all 2019–2026).

## Quality assessment

The rubric (paper, Table on quality assessment) scores five objectively verifiable
items: venue class (0/0.5/1), data statement (0/0.5/1), quantitative result (0/1),
Hausa specificity (0/1/2), and artifact link (0/1), for a maximum of 6 points.
Bands: High >= 4.5, Medium 2.5-4.4, Low < 2.5. The scoring is mechanical and can be
recomputed from `extraction_sheet.csv`; it measures documentation transparency and
Hausa specificity, not methodological rigour.

## Reproducibility statement

Retrieval was scripted (validated PDF signatures, publisher-specific fallbacks,
open-access metadata lookups) and every screening decision is logged with its reason.
This is a curated-corpus review: the evidence base is version 1 of the corpus
(250 quota-structured publications, `data/corpus_v1.xlsx`), reduced by scope
screening to a 28-study core (2019–2026), then completed to 150 studies through a
63-record working collection outside v1 and a 159-record register with a scripted
retrieval run (see `corpus_construction.md`). Note the limitations recorded in the
paper: scope-screening bias, single-reviewer screening, no prospective registration,
and 26 records that could not be retrieved because their publishers block automated access.

## License

CC BY 4.0. The 150 full-text PDFs are distributed separately on request, respecting
the access conditions of their publishers.
