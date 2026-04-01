# Integrated Geospatial Multi-Criteria Framework for Utility-Scale Solar PV Plant Site Selection

Python code for the research paper *Integrated Geospatial Multi-Criteria Framework for Utility-Scale Solar PV Plant Site Selection with Techno-Economic and Environmental Impact Assessments: A Case Study of Nevada, United States* (Nazaripour et al.).

## Setup

Use Python 3.10+ (recommended). From the repository root:

```bash
pip install -r requirements.txt
```

Or, inside `main.ipynb`, uncomment the first code cell and run `%pip install -r requirements.txt`.

## Notebook (`main.ipynb`)

`main.ipynb` implements **fuzzy Analytic Hierarchy Process (AHP)** for twelve solar site-selection criteria (e.g. GHI, slope, proximity to grid and roads, climate variables). It builds a consensus pairwise comparison matrix from expert judgments, converts it to triangular fuzzy numbers, runs `pyDecision`’s fuzzy AHP to obtain criterion weights and consistency checks, and includes **one-at-a-time sensitivity** on weights (outputs under `sensitivity_weights_oat/` and `results_summary/` when those sections are executed).

Open the notebook with Jupyter Lab, Jupyter Notebook, or VS Code/Cursor after installing the dependencies.
