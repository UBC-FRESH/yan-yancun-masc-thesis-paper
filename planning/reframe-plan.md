# Reframe plan — CJFR manuscript (started 2026-10-13)

Spine (adversarial review, §5): *the climate-optimal harvest level is not identifiable
from current HWP evidence; it flips inside empirically reported parameter ranges,
varies across landscapes, and could be pinned down by negotiated product standards.*
Kill the alternative-silviculture claim; state the telescoping property explicitly;
honest novelty; five-landscape generality + unit-dependence; structural robustness;
uncertainty overlay; validation under harvest.

## Pass 1 — done in this change set
- Title rewritten to the threshold-under-uncertainty claim (five-landscape test).
- Abstract rewritten (<=200 words): five-TSA flip result, unit-vs-half-life
  sensitivity, the cessation region, the contract/standards implication.
- Intro: "first to optimize" claim retired (hedged, decision-focused replacement);
  aims rewritten around the decision question; roadmap corrected.
- Orphaned duplicate draft paragraphs removed (broken fragment + redundant
  climate-history paragraph).

## Pass 2 — methods reconciliation (next)
1. One experiment design only: half-lives 1-200 yr x displacement factors 0-2.4 tC/tC,
   5,000 emission-minimizing scenarios per management unit, five units (remove the
   superseded hl 30-60 / df 0-1.5 description).
2. Five-unit case study: TSA 08/16/24/40/41 (Boisvenue et al. 2022 AOI); model
   instances built with the open femic pipeline from 2025 VRI + VDYP/TIPSY (cite the
   instance datasets); THLB-filtered (thlb_raw >= 50).
3. The correction narrative: simulated-clearcut managed curves (no post-reset DOM
   spike); rotation-cycle residual bounds; curve simplification tolerance 1.4%;
   state the telescoping property of the objective (maximize terminal system stock +
   cumulative substitution) as the structural caveat.
4. Harvested-landscape validation (max-harvest spot checks) - pending; either rerun
   the corrected records or scope the claim to the no-harvest + LP-identity audits.

## Pass 3 — results
1. Single-landscape (TSA 24): corrected surfaces (replace the legacy Fig. 12),
   reference cells, the base-scenario comparison.
2. Cross-landscape section (new): flip mid-thresholds 0.95-1.61 at hl=100; df10 range
   0.17-0.87; grid maxima 0.57-0.78 of base; tsa16 full-cessation region; the
   "unit shifts the threshold about as much as the whole half-life axis" statement;
   relate to unit attributes (area, initial carbon, age structure, species).
   Records: `results/cross-tsa/` in fresh-yan (`40d115d`).
3. Structural robustness (legacy spot-checks, label them as TSA 24): even-flow
   0/5/15%, allocation 50/50 vs 100% solid, horizon 15/20/25 (planning/robustness-
   checks.md); add per-TSA spot checks if cheap.

## Pass 4 — discussion + synthesis
1. Comparators: Boiger et al. 2025, Hu et al. 2025, Daigneault et al. 2022, Dymond
   et al. 2025, Smyth et al. 2020, Hennigar et al. 2008, Neilson et al. 2008
   (overlay `planning/literature_overlay.md` + partisan scan).
2. Policy/epistemic point: stop proving harvesting is good/bad with hidden implicit
   parameters; negotiate/monitor product lifetimes and substitution via contracts and
   product standards.
3. Limitations: fixed 120-yr rotation, clearcut-only prescription set, 200-yr horizon
   (telescoping), LP vertex solutions, curve simplification, parameter ranges.
4. Uncertainty overlay figure: literature df/hl ranges against the threshold surface.

## Pass 5 — figures + submission checklist
- Figure plan: framework (keep), five-unit map (new), curve method + reset residual
  (revise), single-TSA surface (corrected), cross-TSA thresholds (new, from
  `results/cross-tsa/cross_tsa_thresholds.pdf`), robustness panel, overlay (new).
- Checklist: abstract <=200 words (done, verify), main text <=6000 words, refs <=50
  (currently ~43; add the femic/ws3/libcbm software refs + new comparators, drop
  dead weight), Dryad deposit (data + records pointer), AI-assistance disclosure,
  CRediT (author confirmation pending), funding line (pending authors).

## Status (2026-10-13, later)
- Passes 1-4 complete and pushed: 666589c (title/abstract/intro), b96546d + 1c1df7d
  (methods), 7e34599 + dc5aa6b + a0aa2aa (results + validation), 5482209 (discussion,
  limitations, conclusion).
- Pass 5: no-harvest figures refreshed from the femic TSA 24 records; build clean
  (38 pp); abstract 195 words; references 43; main text ~5,700 words.
- Pass 5b: five-unit map, age-structure and species-mix figures generated from the
  instances (`scripts/five_tsa_figures.py` in fresh-yan) and wired into the
  manuscript; the data-availability statement now uses the GitHub-release + Zenodo
  DOI route (author account; per author preference over Dryad); an AI-assistance
  declaration was added. Build clean at 34 pp.
- Remaining: typo and formatting pass; author items (funding line, CRediT
  confirmation); tag the release to mint the Zenodo DOI.

## Artifact pointers
- fresh-yan records: curves (`curves/femic-tsa<code>/`), base scenarios, grids
  (`results/femic-tsa<code>/tradeoff_grid/`), cross-TSA analysis
  (`results/cross-tsa/`); commits `4eb3e71`, `40d115d`, `2fe3bd0`.
- Femic instances: pins `9032dc9` / `1d7f5f8` / `8b29bb9` / `7de7927` / `efa2c0d`.
