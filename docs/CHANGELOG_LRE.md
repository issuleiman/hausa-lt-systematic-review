# Change Log: tailoring to Language Resources and Evaluation (LRE)

## Format and submission requirements
- Ported the manuscript to the Springer Nature **sn-jnl** class (`sn-basic` author-year reference style, per the journal's submission guidelines: references cited by name and year; abstract 150-250 words; structured declarations).
- Abstract rewritten to **219 words** (strictly within the 150-250 word limit), Background-Gap-Method-Results-Synthesis-Implications structure.
- Six keywords added (`\keywords{...}`).
- Declarations section added: Funding, Competing interests, Ethics (not applicable: no human/animal subjects), Data availability, Author contributions. Data availability links the public GitHub repository (`https://github.com/issuleiman/hausa-lt-systematic-review`) and permanent Zenodo archive (`https://doi.org/10.5281/zenodo.23972015`).
- sn-jnl compatibility shim for TeX Live (footnote-hook providecommands, `artcatboxgray` colour predefinition) documented inline.

## Contribution sharpening & strict 2019-2026 temporal scope
- Contributions paragraph retained and cross-referenced to research questions; the positioning table (Table 1) contrasts this review explicitly against the Hausa NLP SLR (2015-2020 scope), the HausaNLP survey, NaijaNLP, the Hausa/Fongbe resource audit, two continental African NLP surveys, and the African ASR SLR.
- Enforced a strict **2019-2026** inclusion window (Criterion `I2`, removing the three pre-2019 standing exceptions `P-003` [2009], `P-122` [2012], and `P-123` [2012]) so that all **150 included studies** and all **41 catalogued resources** belong to the modern neural and pre-trained model era (2019-2026).
- Methodology structured around the curated-corpus design: version-1 corpus (250 publications, eight thematic areas with explicit area targets, Table 2), scope screening to a 28-study direct-contribution core from 2019-2026 (criteria in Table 3), pre-held working collection outside v1 (63 records -> 61 verified 2019-2026 studies retained + 1 pre-2019 excluded under E1, `P-003` + 1 excluded under E2, `P-062`), and a 159-record completion register with a scripted retrieval run (5 October 2026: 40 E3 already held, 119 sought, 26 E2 publisher-blocked, 93 retrieved, 17 E1 excluded at full text [15 out of scope + 2 pre-2019, `P-122` and `P-123`], 76 eligible 2019-2026 full texts [`P-077`..`P-154` minus `P-122`, `P-123`] of which 15 corroborate v1 core records and 61 are net new), yielding `28 + 61 + 61 = 150` included studies (`74` in `P-001`..`P-076` and `76` in `P-077`..`P-154`), reconciled 1-to-1 in the text, Figure 2, `screening_decisions.csv` (472 rows), and `selection_counts.csv`.

## Full-text PDF & metadata verification audit
- Audited all 150 included 2019-2026 PDFs (`final_version_153`) and all 169 `version_1` PDFs against `study_inventory.csv`, `extraction_sheet.csv`, `resource_catalogue.csv`, `quality_assessment.csv`, `refs.bib`, and `main.tex`.
- Re-downloaded the genuine ACL Anthology / arXiv PDFs for `P-056` (*HausaNLP at SemEval-2023 Task 12*, `2023.semeval-1.6`) and `P-053` (*Multilingual Language Model Adaptive Fine-Tuning: A Study on African Languages*, `arXiv:2204.06487v1`) and synced all 6 re-verified files across `final_version_153` and `version_1`.
- Replaced all 25 `"Authors in paper"` placeholders in `study_inventory.csv` with the verified author lists from the PDFs, corrected author ordering in `refs.bib` (`P-031`, `P-041`, `P-043`, `P-056`), and corrected `P-077`'s dissertation URL.
- Verified and corrected all quantitative claims against the primary PDFs: `P-001` (distinguished 1,130 catalogued Hausa YouTube videos / 20.57 h Whisper transcription at 57.4/100 human quality from the 12.3 h Fongbe MMS-300M fine-tuning reaching 9.48% WER), `P-002` (75.33% Macro-F1 on 2-fold CV and 63.57% character similarity), `P-061` & `R-09` (2,551 Hausa sentence pairs in SemRel), `P-067` (>400,000 noisy-clean pairs), `P-121` (1,158 Hausa sentences / 27,304 tokens in AfriSUD), and `P-044` vs. `P-046`/`P-128`.
- Added in-text citations for all 17 previously uncited corpus studies so that 100% of the 150 included 2019-2026 studies are cited in `main.tex` and appear in the compiled bibliography.
- Recomputed `QA4_hausa_specificity` from the verified full texts (`58 High / 91 Medium / 1 Low`; `74 peer / 43 preprint / 33 other`) and synchronized `study_inventory.csv`, `quality_assessment.csv`, `tables_gen.tex`, `qa_fragments.tex`, `stats_fragments.tex`, and `appendix_inventory.tex`.

## Evidence figures (all generated mechanically from repository CSVs)
- Figure 1 (`fig_timeline.pdf`): publication timeline of the 150 studies (2019-2026) by year and venue class.
- Figure 2 (inline TikZ in `main.tex` and `study_selection.pdf`): study-selection flow diagram with explicit coordinates, unified colour palette, and non-overlapping stage badges.
- Figure 3 (`fig_resources.pdf`): resource coverage matrix, 41 resources (2019-2026) by type x domain.
- Figure 4 (`fig_gaps.pdf`): evidence-to-gap view, gaps G1-G10 by quality band (`58 High / 91 Medium / 1 Low`) and total.
