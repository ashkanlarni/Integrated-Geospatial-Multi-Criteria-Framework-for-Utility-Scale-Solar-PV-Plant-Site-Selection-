# Integrated Geospatial Multi-Criteria Framework for Utility-Scale Solar PV Plant Site Selection

Python code for the research paper *Integrated Geospatial Multi-Criteria Framework for Utility-Scale Solar PV Plant Site Selection with Techno-Economic and Environmental Impact Assessments: A Case Study of Nevada, United States* (Nazaripour et al.).

## Setup

Use Python 3.10+ (recommended). From the repository root:

```bash
pip install -r requirements.txt
```

Or, inside `main.ipynb`, uncomment the first code cell and run `%pip install -r requirements.txt`.

## Notebook (`main.ipynb`)

`main.ipynb` runs **fuzzy Analytic Hierarchy Process (AHP)** for twelve solar site-selection criteria (e.g. GHI, slope, proximity to grid and roads, climate variables). The workflow is:

1. **Fuzzy pairwise matrix** — triangular fuzzy numbers `(L, M, U)` per comparison (the values in the notebook match the paper’s consensus matrix after reciprocals and fuzzification).
2. **Fuzzy AHP** — `pyDecision`’s `fuzzy_ahp_method` for fuzzy, defuzzified, and normalized weights plus the consistency ratio (RC).
3. **Results** — printed weights and a pie chart of normalized weights.
4. **One-at-a-time (OAT) sensitivity** — perturbs crisp midpoints of the fuzzy comparisons on the Saaty scale, then re-runs reciprocal fill, fuzzification, and fuzzy AHP for each scenario.

### Outputs (when you run the sensitivity section)

| Location | Contents |
|----------|----------|
| `sensitivity_weights_oat/` | Normalized weights per scenario as `.txt` (TSV after a short header), plus a matching **pie chart `.png`** for each file (including `baseline.txt` / `baseline.png`). |
| `results_summary/` | Excel summaries of the OAT runs (`oat_step1_summary.xlsx`, `oat_step2_summary.xlsx`). |

Open the notebook with Jupyter Lab, Jupyter Notebook, or VS Code/Cursor after installing the dependencies.
