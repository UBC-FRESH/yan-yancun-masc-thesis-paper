# Literature overlay: HWP half-lives, displacement factors, and comparable modelling studies

Purpose: evidence base for the manuscript's claim (target: *Canadian Journal of Forest Research*) that the emission-minimizing harvest level is not identifiable from current evidence because it flips within empirically reported ranges of HWP half-life and displacement factor (DF). Items marked **[unverified]** were not confirmed against the primary source (paywalls); others were read from the cited source or a named compilation.

## a. Empirically reported HWP half-lives

**IPCC defaults (the field's anchor).** 2019 Refinement Tier 1 (Table 12.3): sawnwood 35 yr, wood-based panels 25 yr, paper/paperboard 2 yr; 2006 Tier 2: solid wood 30, panels 25, paper 2; 2003 GPG background table: saw wood 35, structural panels 30, non-structural panels 20, paper 2 (IPCC 2019 Ch. 12; Spear & Hart 2025, Tables 1-2). IPCC (2003) puts half-life uncertainty at ±50%. Canadian national-scale analyses adopt 35/25/2 as fixed inputs (Smyth et al. 2014, 2020).

**Country/provincial values.** The most detailed Canadian set is BC-HWPv1 (Dymond 2012, compiled in Spear & Hart 2025, Table 10): single-family homes 90 yr, multi-family and commercial buildings 75, furniture/other manufacturing 38, residential upkeep 30, paper 2.5 (full range 2-90; seven pools from US sources, single-family value adapted to Canada). Austria (Braun et al. 2016, in Spear & Hart 2025): construction 31.4 (subcategories 0.75-71), furniture 8.8 (3.5-17), packaging 1.5 (1.0-1.6), all products 14.6. Portugal (Dias et al., in Spear & Hart 2025): construction 21, furniture ~14. Cross-literature ranges (Spear & Hart 2025, Table 6): sawnwood/plywood 27.7-52; panels 0.7-45; paper 0.5-10; furniture 8.7-30; doors/windows 6.9-45.1; packaging/pallets 0.06-6.2.

**Method caveat.** Half-lives are first-order-decay (FOD) artifacts; observed service lives often fit log-normal/Weibull/gamma distributions better, and FOD fits can be pathological (Japanese housing data implied 459 yr; Spear & Hart 2025). Reported commodity-class half-lives span ~0.5-90 yr; the 1-200 yr axis brackets that range but is wider.

## b. Displacement factors

- **Sathre & O'Connor (2010)** — 21-study LCA meta-analysis: mean 2.1 tC/tC; middle estimates 0.4-6.0; most 1-3; full range -2.3 to 15; averages of low/high estimates 0.8/4.6. System boundaries inconsistent across studies (some include forest/soil and post-consumer emissions).
- **Leskinen et al. (2018)** — 51 studies, 433 factors: mean 1.2; 95% range -0.7 to 5.1; structural construction 1.3 (-0.9 to 5.5), non-structural 1.6 (0.2-4.7), textiles 2.8, other 1-1.5. Forest C excluded; most values production-stage only; expressed per kg C in final product (two wood-use conventions acknowledged).
- **Canadian LCA values**: Smyth et al. (2017) sawnwood 0.54, panels 0.45 (general end-use basket weighted by Canadian consumption), building-only 2.1/2.2, bioenergy 0.47-0.89; Smyth et al. (2014) bioenergy -0.08 to 0.79 (domestic), 0.6 (international). Smyth et al. (2020, BC) fix DFs at 0.54/0.45 (low) or 2.1/2.2 (high) and assume no pulp/paper substitution.
- **Recent review**: Myllyviita et al. (2021) — no accepted DF rules; quotes Leskinen's ranges.
- **Critiques / market alternatives**: Leturcq (2020) — DFs are time-dependent; accounting for residue decay lowers the extremum DF by 2-4 tC/tC and broadens negative values. Market-based models (e.g. Daigneault et al. 2022) endogenize prices and leakage and cannot be reduced to a single DF.

Net: central DF estimates cluster ~0.5-1.6 tC/tC; the empirical 95% interval is ~-0.7 to 5.1 (older construction studies to 15). The flip band (0.5-1.2) lies inside these ranges, at the low-to-central end.

## c. Scan of comparable modelling studies

| Study | Design | HWP parameter treatment | Locates a frontier? |
|---|---|---|---|
| Dymond et al. 2025 (FEM) | Empirical 26-yr trial + prescriptive cost-benefit; fixed treatments (clearcut, partial cuts, no harvest) | Wood-product C monitored; carbon price threshold ~CAD65/tCO2e; no half-life/DF axis | No |
| Smyth et al. 2020 (CBM 15:21, BC) | Prescriptive scenario simulation (5 scenarios x 3 levels + longer-lived products) | Fixed IPCC half-lives 35/25/2; DFs fixed at 0.54/0.45 or 2.1/2.2; ranking sensitive to substitution | No (shows DF-dependence) |
| Hennigar et al. 2008 (FEM; New Brunswick) | Optimization (Woodstock/Remsoft); 4 objective functions; 300 yr; 30,000 ha; 4% discount | Tests 3 initial age structures and a range of substitution rates; COT tracks product C through landfill; DOM initialized by CBM-CFS3 spin-up with post-harvest = unmanaged DOM levels (verified full text) | Partial (objective comparison) |
| Neilson et al. 2008 (CJFR) | LP optimization; stand C yield tables + HWP residency periods; 5 scenarios; 428,000 ha | HWP decay emissions included; no DF/half-life sensitivity reported | No |
| Boisvenue et al. 2022 (ERL) | Simulation: WS3 + CBM on open-source platform; capacity + 2 scenarios | Ecosystem C focus; HWP not central | No |
| Boiger et al. 2025 (JEM) | Multi-objective optimization of HWP allocation across value chains | Substitution as marginal changes; harvest limited/fixed | Partial (value-chain only) |
| Daigneault et al. 2022 (GEC) | Global forest-sector economic optimization; 81 SSP/climate scenarios | Endogenous prices/leakage; HWP decay included; no single DF | Yes, but global — not a TSA-scale harvest level |
| Lucey et al. 2024 (USDA GTR) | Synthesis of US/Canadian HWP accounting models | Documents model-specific parameters; notes missing integration with economic/substitution models | N/A (review) |

**Closest precursor:** Yan (2025, UBC MSc; UBC-FRESH repo msc_walter_yan) — open ws3 + libCBM framework generating/validating carbon yield curves for TSA 24, optimizing harvest/HWP scenarios, and looping over half-life and DF. The manuscript's flip analysis is the direct extension.

## d. Prior carbon-yield-curve compilation from CBM, and the initialization question

- Neilson et al. (2008) fed stand-specific C yield tables (Woodstock + forest-development plot age curves + CBM-CFS3) and HWP residency periods into an LP.
- Hennigar et al. (2008) built CBM-CFS3-derived C-storage curves inside a Woodstock/Remsoft optimization, testing three initial age structures. **Verified against the full text (author-provided):** they initialized DOM with CBM-CFS3's spin-up (successive wildfire at a fixed 100-year return interval, which they themselves flag as short for the Acadian forest region) and state: "DOM pools for planted, PCT, and post-selective harvest stands were assumed equal to unmanaged DOM levels until the stand transitioned to its managed state during initialization" (citing Neilson et al., 2007) - i.e., the post-harvest state inherits the spun-up initialization, the exact practice the corrected curve compilation replaces. They did not diagnose or correct the resulting bias; they also excluded the slow to very slow DOM pools from the optimization "due to low confidence in absolute soil C pool estimates".
- Boisvenue et al. (2022) coupled WS3 with CBM to produce management-scale C estimates and reported simulated current C below the landscape C-holding capacity (405.5 vs 477 MtC).
- Yan (2025) explicitly generates, plugs in, and validates CBM-derived carbon yield curves in an open estate model (TSA 24).

No study in this set diagnoses or corrects a post-harvest age-reset/DOM initialization bias in estate-model C yield curves. Hennigar et al. (2008) is now **verified** to *apply* the spun-up post-harvest DOM assumption (quoting Neilson et al., 2007) rather than correct it, and to sidestep slow-DOM uncertainty by excluding those pools from the optimization; Neilson et al. (2007/2008) is the lineage source for that assumption and its full text remains **[unverified]** (paywalled). CBM's spin-up initialization is a documented uncertainty source (Metsaranta et al. 2017). Together this supports the manuscript's gap claim: prior work either assumes spun-up post-harvest DOM states or drops the uncertain pools — neither keeps the full DOM ledger conservation-consistent through harvest.

## e. Red flags for the argument

1. **DF definitions are not comparable** (per final-product C vs harvest input; production-stage vs full LCA; forest C included or not). State the DF convention; 0.5-1.2 is a low-to-central slice of the empirical distribution, not its centre (S&O mean 2.1, Leskinen mean 1.2 sit at/above the band's top).
2. **LCA-based DFs ignore market feedbacks/leakage**; market models imply different effective substitution at scale (Daigneault et al. 2022; Leskinen et al. 2018 caution against policy use of substitution factors alone).
3. **FOD half-life is a contested parameterization**; service-life distributions change HWP trajectories at the same "half-life" (Spear & Hart 2025). The 1-200 yr axis is wider than commodity-class estimates (0.5-90 yr); justify the upper bound.
4. **The "0 or effectively infinite" framing needs care**: instantaneous oxidation and permanent-storage conventions exist, but mainstream studies fix near-default values (2/25/35; DF 0.45-2.2), not 0/infinite.
5. **No scanned study jointly varies half-life and DF over a full grid**; several vary only one axis (Hennigar substitution rates; Smyth low/high DF). This best supports "not identifiable from current evidence".

## f. Software integration and reproducibility (contribution framing, added 2026-10-12)

Two claims to develop for the Introduction/Discussion (user framing; evidence check pending before they reach the manuscript):

**Native estate-model carbon accounting.** Commercial forest-estate modelling systems used for Canadian wood-supply planning (e.g. Remsoft Woodstock, Patchworks/FPS) carry *partial* CBM integrations: analysts export stand and management data into CBM-CFS3 SIT format manually, run CBM-CFS3 in a separate software environment, then merge carbon outputs with wood-supply outputs in ad hoc post-hoc scripts (and CBM-CFS3 itself "does not track the fate of carbon in harvested wood products" - NRCan model documentation; see `partisan_practice_scan.md` for the field-practice evidence). This work instead carries the full ecosystem + HWP carbon ledger *inside* a general, scalable estate-modelling framework (ws3 + libcbm), with automated CBM carbon-yield-curve generation and injection (`fresh_yan`), so carbon is a first-class objective/constraint of the estate optimization rather than a post-hoc merge, without requiring CBM-SIT expertise from the analyst. The optional ws3 embedded agent capabilities (OpenCode-backed) lower the barrier further for large grid-type optimization/simulation hybrid experiments. **To verify:** citable documentation of the Woodstock/Patchworks manual workflows; scan for any prior fully-integrated open system (national systems like Heureka/MELA/SIMO have carbon modules but are jurisdiction-specific and not estate-model-native in the same sense).

**Reproducible model-instance building.** The stack - `femic` (public VRI/VDYP/TIPSY data -> ws3 sections), `freshforge` (workflow-as-code), `ws3` (estate model), `fresh-yan` (carbon experiment pipeline) - makes new open models from public data managed, reproducible, and transparent, for research and production use. Artifacts: five open `femic-tsa<code>-instance` datasets (pinned commits, S3-backed) and this repository's generated records. **To verify:** reproducibility-practice gap statements in the forest-carbon literature; document the stack in software/data-availability terms.
