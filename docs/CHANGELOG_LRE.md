# Change Log: tailoring to Language Resources and Evaluation (LRE)

## Format and submission requirements
- Ported the manuscript to the Springer Nature **sn-jnl** class (`sn-basic` author-year reference style, per the journal's submission guidelines: references cited by name and year; abstract 150-250 words; structured declarations).
- Abstract written to **205 words** (strictly within the 150-250 word limit), Background-Gap-Method-Results-Synthesis-Implications structure.
- Six keywords added (`\keywords{...}`).
- Declarations section added: Funding, Competing interests, Ethics (not applicable: no human/animal subjects), Data availability, Author contributions. Data availability links the public GitHub repository (`https://github.com/issuleiman/hausa-lt-systematic-review`) and permanent Zenodo archive (`https://doi.org/10.5281/zenodo.23972015`).
- sn-jnl compatibility shim for TeX Live (footnote-hook providecommands, `artcatboxgray` colour predefinition) documented inline.

## Methodology & strict 2019-2026 temporal scope
- Contributions paragraph cross-referenced to research questions; the positioning table (Table 1) contrasts this review against the Hausa NLP SLR (2015-2020 scope), the HausaNLP survey, NaijaNLP, the Hausa/Fongbe resource audit, two continental African NLP surveys, and the African ASR SLR.
- Structured the methodology directly around the actual downloaded collection (`version_1`, 169 candidate papers `V1-001`..`V1-169`):
  1. **Full-text topical and document verification (`169 -> 153`)**: every downloaded PDF was inspected in full; 15 multi-language papers lacking direct Hausa-specific content were excluded under E1, and 1 Hausa stopwords paper (`V1-062`, `P-062`) whose hosted PDF contained a different article was excluded under E2, leaving 153 verified Hausa studies (`P-001`..`P-154` minus `P-062`).
  2. **Temporal eligibility filter (`153 -> 150`, Criterion `I2`: `2019-2026`)**: excluded the 3 pre-2019 studies (`V1-003` / `P-003` [2009], `V1-133` / `P-122` [2012], and `V1-134` / `P-123` [2012]) under E1/I2 so that all **150 included studies** (`final_version_150`) and all **41 catalogued resources** (`R-01`..`R-41`) belong to the modern neural and pre-trained model era (2019-2026).
- Reconciled every count 1-to-1 across `main.tex`, Figure 2, `screening_decisions.csv` (169 rows), and `selection_counts.csv`.

## Full-text PDF & metadata verification audit
- Audited all 169 `version_1` PDFs and all 150 included 2019-2026 PDFs (`final_version_150`) against `study_inventory.csv`, `extraction_sheet.csv`, `resource_catalogue.csv`, `quality_assessment.csv`, `refs.bib`, and `main.tex`.
- Re-downloaded the genuine ACL Anthology / arXiv PDFs for `P-056` (*HausaNLP at SemEval-2023 Task 12*, `2023.semeval-1.6`) and `P-053` (*Multilingual Language Model Adaptive Fine-Tuning: A Study on African Languages*, `arXiv:2204.06487v1`) and synced all 6 re-verified files across `final_version_150` and `version_1`.
- Replaced all 25 `"Authors in paper"` placeholders in `study_inventory.csv` with the verified author lists from the PDFs, corrected author ordering in `refs.bib` (`P-031`, `P-041`, `P-043`, `P-056`), and corrected `P-077`'s dissertation URL.
- Verified and corrected all quantitative claims against the primary PDFs: `P-001` (distinguished 1,130 catalogued Hausa YouTube videos / 20.57 h Whisper transcription at 57.4/100 human quality from the 12.3 h Fongbe MMS-300M fine-tuning reaching 9.48% WER), `P-002` (75.33% Macro-F1 on 2-fold CV and 63.57% character similarity), `P-061` & `R-09` (2,551 Hausa sentence pairs in SemRel), `P-067` (>400,000 noisy-clean pairs), `P-121` (1,158 Hausa sentences / 27,304 tokens in AfriSUD), and `P-044` vs. `P-046`/`P-128`.
- Added in-text citations for all 17 previously uncited corpus studies so that 100% of the 150 included 2019-2026 studies are cited in `main.tex` and appear in the compiled bibliography.
- Recomputed `QA4_hausa_specificity` from the verified full texts (`58 High / 91 Medium / 1 Low`; `74 peer / 43 preprint / 33 other`) and synchronized `study_inventory.csv`, `quality_assessment.csv`, `tables_gen.tex`, `qa_fragments.tex`, `stats_fragments.tex`, and `appendix_inventory.tex`.

## Evidence figures (all generated mechanically from repository CSVs)
- Figure 1 (`fig_timeline.pdf`): publication timeline of the 150 studies (2019-2026) by year and venue class.
- Figure 2 (inline TikZ in `main.tex` and `study_selection.pdf`): study-selection flow diagram (`169 -> 153 -> 150`) with unified colour palette and non-overlapping stage badges.
- Figure 3 (`fig_resources.pdf`): resource coverage matrix, 41 resources (2019-2026) by type x domain.
- Figure 4 (`fig_gaps.pdf`): evidence-to-gap view, gaps G1-G10 by quality band (`58 High / 91 Medium / 1 Low`) and total.
