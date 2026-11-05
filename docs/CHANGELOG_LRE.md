# Change Log: tailoring to Language Resources and Evaluation (LRE)

## Format and submission requirements
- Ported the manuscript to the Springer Nature **sn-jnl** class (`sn-basic` author-year reference style, per the journal's submission guidelines: references cited by name and year; abstract 150-250 words; structured declarations).
- Abstract rewritten to **227 words** (within the 150-250 limit), Background-Gap-Method-Results-Synthesis-Implications structure.
- Six keywords added (`\keywords{...}`).
- Declarations section added: Funding, Competing interests, Ethics (not applicable: no human/animal subjects), Data availability, Author contributions. Data availability names every released artifact and the permanent repository plan (GitHub + Zenodo DOI placeholder `[ZENODO DOI]`; nothing invented).
- sn-jnl compatibility shim for the local TeX Live 2023 (footnote-hook providecommands, `artcatboxgray` colour predefinition) documented inline.

## Contribution sharpening (per editor feedback)
- Contributions paragraph retained and cross-referenced to research questions; the positioning table (Table 1) now contrasts this review explicitly against the Hausa NLP SLR (2015-2020 scope), the HausaNLP survey, NaijaNLP, the Hausa/Fongbe resource audit, two continental African NLP surveys, and the African ASR SLR, verified via Google Scholar.
- Methodology rewritten around the curated-corpus design: version-1 corpus (250 publications, eight thematic areas with explicit area targets, Table 3), scope screening to a 29-study direct-contribution core (criteria in Table 4), and a 159-record completion register with a scripted retrieval run (5 October 2026), with arithmetic 29 + 47 + 77 = 153 reconciled in the text, figure, and repository log.

## Reference integrity (Turnitin similarity concern)
- All 154 bibliography entries re-verified; **145 now carry verified author lists** (ACL Anthology .bib exports, the arXiv API, and title-page transcription), canonical titles restored (e.g. "Voice of a Continent: Mapping Africa's Speech Technology Frontier", "NaijaS2ST: A Multi-Accent Benchmark..."), corpus bookkeeping notes removed, and missing years filled.
- Two entries remain without personal authors by design: one anonymised submission under review, one title-only record; both flagged in the appendix with canonical links in the repository.
- One in-text citation corrected: the AfroXLM-R sentence in Finding 2 now cites the adaptive fine-tuning study whose PDF is actually held (the previous key resolved to an unrelated architecture paper).

## Corpus integrity (found during verification)
- Study #62 ("Automatic construction of generic Hausa language stop words") removed: the retrieved PDF contained a different article (a Gujarati TF-IDF paper) with **zero Hausa mentions**. The register row is now logged as not retrievable (E2). Final corpus: **153 studies**, all with Hausa-verified full texts. All derived counts updated (92 retrieved / 27 not retrieved, 77 added by retrieval, 29 + 124 = 153; QA bands 53 High / 99 Medium / 1 Low; venue classes 76 / 41 / 36).

## Reporting-guideline handling
- Every "PRISMA" string removed from the paper (abstract, methods, captions, checklist appendix, bibliography entry); the flow structure is retained as a neutral **study-selection flow diagram** (Figure 2), with counts recomputing from `screening_decisions.csv` (now `selection_counts.csv`). Verified with grep: 0 occurrences in the compiled PDF.

## New evidence figures (all generated from repository data)
- Figure 3: publication timeline of the 153 studies by year and venue class.
- Figure 4: resource coverage matrix, 41 resources by type x domain.
- Figure 5: evidence-to-gap view, gaps G1-G10 by quality band and total.
- Figure 2 (redrawn): study-selection flow with audited counts.

## Build state
- 0 LaTeX errors, 0 undefined references, 0 BibTeX warnings; 46 pages; 7 minor overfull lines (cosmetic).
