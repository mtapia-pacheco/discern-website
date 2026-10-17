# PI feedback review

Source: [DISCERN public manuscript, arXiv:2609.33357v1](https://arxiv.org/html/2609.33357v1), reviewed October 17, 2026. Scientific content was checked against Sections 2, 4.2–4.3, Figure 2, and Appendix E; authors and affiliations against the public manuscript header. No deployment or GitHub push is part of this update.

## Website structure

Hero / Introduction (with authors) → About DISCERN → Benchmark Coverage → Framework and Evaluation Levels (with task composition, evaluation coverage, and Figure 2) → Results / Leaderboard → Key Findings → Resources.

The Results section is now a direct child of the page's main element. Its nine tabs, chart rendering, model colors, sorting, model details, cost-efficiency zoom, scoring definitions, and data are preserved. Figure assets and enlargement controls are preserved. The redundant Framework footnote was removed; other framework explanations remain.

## Verified scientific coverage

Section 2 names five domains. Figure 2B uses shorter or alternate labels for two of them; the website uses the Section 2 names and Figure 2B grouping.

| Domain | Tracks | Figure 2 label, where different |
| --- | --- | --- |
| Genetics | Genome-wide association studies (GWAS); clinical variant interpretation (ClinVar / ACMG) | — |
| Transcriptomics | Bulk RNA-seq; single-cell RNA-seq | — |
| Regulatory genomics | CRISPR perturbation screening; enhancer activity | Functional genomics |
| Epigenomics | Chromatin regulation (histone / gene expression) | — |
| Protein biophysics | Protein stability and structure | Biophysics |

Sources: [Section 2 and Figure 2](https://arxiv.org/html/2609.33357v1#S2.F2), [Appendix E inventory](https://arxiv.org/html/2609.33357v1#A5). The physics extension is separate from the life-science core.

## Task composition and clarified PI request

Verified counts: **79 L1 tasks + 102 L2 tasks + 22 L3 scientific worlds = 203 tasks**. Section 2 and Appendix E confirm the totals. The paper also identifies 24 L2 analysis families. Figure 2C breaks down the existing tasks:

- L1: 8 clean controls + 71 challenges = 79.
- L2: 24 clean controls + 8 statistical traps + 34 tool/procedure traps + 36 data confounds = 102.
- L3: 8 real-data worlds + 6 native counterfactuals + 8 injected counterfactuals = 22.

The clarified request calls for two complementary summaries before Figure 2:

1. **Benchmark composition:** 79 + 102 + 22 = 203 distinct benchmark tasks. The three-level count summary retains the existing descriptions and stacks into compact rows on mobile.
2. **Evaluation coverage:** 8 models × 8 life-science tracks × 3 levels = 192 aggregated model–track–level scores. [Appendix D, Figure 11](https://arxiv.org/html/2609.33357v1#A4.F11) explicitly reports these 192 scores. This is a matrix of aggregated evaluations, not 192 distinct tasks, a score-normalization multiplier, or a single sequential pipeline.

The summaries have separate titles and units. The evaluation matrix is a compact equation below the task inventory and uses the existing typography and colors. The earlier ambiguity is resolved by the distinction between task inventory and aggregated evaluation scores.

Figure 2 now follows the existing level descriptions within Framework, as requested in the clarification. Its artwork, caption, source, and enlargement controls remain intact. The five-domain coverage section stays before Framework. The earlier multiplication ambiguity is resolved; no further PI clarification is needed for this item.

## Figure headings

| Figure | Before | After |
| --- | --- | --- |
| 3 | Aggregate scores hide variation across tasks. | GLM-5.3 scores 100 in protein data integrity but 3.5 in CRISPR analysis verification. |
| 4 | Caution, commitment, and novelty differ. | Opus proposes hypotheses more often than Sol, yet their submitted hypotheses have similar average novelty. |

Figure 3: Section 4.2 identifies GLM-5.3's protein L1 score of 100 and CRISPR L2 score of 3.5; these are track-level scores on the 0–100 rubric, not individual-task success rates. [Source](https://arxiv.org/html/2609.33357v1#S4.F3).

Figure 4: Section 4.3 reports hypothesis participation of 81.0% for Opus versus 18.2% for Sol, and mean novelty of 41.2 versus 41.7 among submitted eligible hypotheses. The heading and caption retain that conditional population. The caption still notes Astra's single-hypothesis mean and the four ineligible outcomes excluded from panel C. [Source](https://arxiv.org/html/2609.33357v1#S4.F4).

## Authors

Public manuscript order: Nan Huang; Mario Tapia-Pacheco; Kun Zhou; Yiming Huang; Kevin José Barrientos Díaz; Tiffany Amariuta; Jingbo Shang.

All are affiliated with the University of California San Diego except Kevin José Barrientos Díaz, listed as Independent Researcher. Tiffany Amariuta and Jingbo Shang are co-corresponding authors. Superscripts in the hero connect names to these affiliations. Separate anonymous submission materials and promotional videos were not modified.

## Validation completed

- Checked the seven-section order, independent Results section, Figure 2 placement, unique IDs, and all internal anchor targets.
- Verified all nine leaderboard tabs, eight models, default rankings, reverse sorting, table-header/tab synchronization, keyboard navigation, model details, cost-efficiency zoom, and the Fable dropdown.
- Checked 1440, 1024, 768, 390, and 320 px viewport widths with no page overflow. Inspected desktop and mobile screenshots of the hero and coverage, plus the desktop leaderboard. Existing desktop vertical and mobile horizontal chart behavior was retained.
- Opened all five figures at desktop and mobile widths; checked image loading, enlargement, zoom, closing, and focus restoration.
- Checked framework tabs, mobile navigation/anchor placement, and Back to top.
- Confirmed the no-JavaScript leaderboard still contains all eight models and all nine metrics.
- Compared the leaderboard markup and data with the original: only its section wrapper and Results heading level changed. `script.js` and all five figure assets are unchanged. JavaScript syntax and `git diff --check` passed.

Changed files: `index.html` (content, order, navigation, authors), `styles.css` (minimal responsive styles and anchor offsets), and this review note. No new dependencies were introduced.
