# Numerical results for the manuscript

Cell-level results for the manuscript. Script paths below are relative to `candidates/c530_complementary_bin_operator_nmf/`.

| File | Manuscript use | Producing script |
|---|---|---|
| `acquisition_factorial_cells.json` | equal-budget origin comparison | `phase_b/run_acquisition_factorial.py` |
| `massbank_cells.json` | semi-synthetic MS/MS comparisons | `phase_b/run_massbank_public.py` |
| `raman_cells.csv` | retrospectively binned Raman comparisons | `phase_b/run_real_raman_oil_validation.py` |
| `operator_loss_paired_cells.csv` | paired Poisson/HALS effects and intervals | `revision_20261007/run_paired_uncertainty_audit.py` |
| `multistart_cases.json` | Appendix A: four representative 50-start cases | `revision_20261007/run_poisson_multistart_audit.py` |
| `full_rank_difficult_cells.csv` | Appendix B: seven full-row-rank regimes | `revision_20261007/run_rho1_failure_study.py` |
| `model_mismatch_cells.csv` | independent-block mismatch comparison | `revision_20261007/run_model_mismatch_stress.py` |
| `raman_baseline_cells.csv` | Raman preprocessing sensitivity | `revision_20261007/run_raman_baseline_correction_sensitivity.py` |

The full-row-rank study used 96 fine channels, noncyclic width-4 training bins at origins 0–3, four blocks of 48 mixtures, and 60 held-out mixtures at width 7, origin 3. It used five seeds (61000–61004) and 20 starts per cell. The seven regimes are named in `full_rank_difficult_cells.csv`.

The mismatch study used four training blocks of 48 rank-4 mixtures on 96 channels and a held-out block of 52. Training used noncyclic width-4 bins at origins 0–3; the held-out operator used width 8, origin 3. Its seven scenarios and four seeds (63000–63003) are recorded in `model_mismatch_cells.csv`. Poisson fits were continued for at most 5000 iterations.

The multistart file records the 420-iteration and extended fits, including objective-gap tolerances of $10^{-4}$ and $10^{-3}$.

