# Corpus construction and provenance record

The review follows a curated-corpus methodology in two versions; this record states
where the evidence came from, what was done to it, and when, to the level the logged
artifacts show.

## Version 1: breadth-first mapping (n = 250)

Finalised on 1 October 2026 (internal archive timestamps). 250 publications,
2011-2026, each recorded with title, authors, year, thematic area, task, a working
insight, access status, and link. Built against explicit area targets:

| Thematic area | target = achieved |
|---|---|
| Hausa speech and NLP | 35 = 35 |
| Other African-language speech and NLP | 35 = 35 |
| Low-resource and multilingual speech | 50 = 50 |
| Self-supervised and foundation speech models | 45 = 45 |
| Cross-lingual transfer, adaptation, fine-tuning | 25 = 25 |
| Evaluation, benchmarks, fairness, robustness | 25 = 25 |
| Adjacent methods | 20 = 20 |
| Surveys and tutorials | 15 = 15 |

Year bands: 193 records 2019-2026, 44 records 2012-2018, 13 pre-2012.
Access: 218 open, 32 closed. The Distribution Check sheet of `corpus_v1.xlsx`
verifies these targets against the achieved counts.

## Scope screening (250 -> 29)

Every record was assessed against the scope criteria (paper Table 4) for direct
contribution to the review's goal. Outcome, logged per record in
`data/screening_decisions.csv` (rows V1-001 to V1-250):

| Decision | n |
|---|---|
| Included as the direct-contribution core | 29 |
| Set aside: outside direct scope (E1) | 203 |
| Set aside: Hausa-area records superseded in the completion pass | 16 |
| Set aside: overlapping entries (E3) | 2 |

Per-area discard counts come from each record's recorded area field.

## Completion pass and retrieval (29 -> 153)

A structured completion register of 159 candidate records (same metadata fields as
v1) was compiled from systematic monitoring of the venues and communities where
Hausa work appears. Platform distribution: 101/159 (63.5%) resolve to the ACL
Anthology (68) and arXiv (33); the remainder spread across ~30 further platforms
(ResearchGate 8, OpenReview 6, IEEE Xplore 3, Research Square 3, MIT Press/TACL 3,
Academia.edu 2, AJOL 2, PLOS 2, and regional African journals among others).

- 40 of 159 candidates described works already held with verified full texts (E3).
- The remaining 119 were pursued in a single scripted retrieval run on
  **5 October 2026 (UTC)** with strict PDF validation (file signature and minimum
  size), publisher-specific fallbacks, and open-access metadata lookups.
- Outcome: 92 full texts retrieved; 27 candidates not retrieved or failing verification and excluded
  under E2 (publisher blocks: ResearchGate, OpenReview, IEEE Xplore, MIT Press,
  ScienceDirect, AJOL, Academia.edu, Cell Press, JMIR, Preprints.org, and others).
- Of the 92 retrieved, 15 fell outside the direct scope at the eligibility check (E1),
  leaving 77 studies added by retrieval.
- Together with 47 studies already held and verified outside v1, the completion
  pass contributed 124 studies.

## Final corpus (version 2)

29 (v1 core) + 125 (completion) = **153 studies**, plus a parallel catalogue of
**41 resources** (R-01 to R-41). Every per-record decision, with reason, route, and
the study identifier it became, is in `data/screening_decisions.csv` (409 rows);
the counts recompute mechanically from that log and are summarised in
`data/selection_counts.csv`.

## Registration

The review had no prospective registration. Scope criteria and extraction fields
were fixed before screening began; this record is reconstructed from the logged
artifacts (per-record decision logs and retrieval timestamps).
