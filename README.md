# E. coli FBA Analysis — Part 1

Computational lab for flux balance analysis (FBA) of *E. coli* central metabolism,
using [COBRApy](https://cobrapy.readthedocs.io) and [Escher](https://escher.github.io).
This is the programmatic equivalent of the EcoCyc Pathway Tools lab exercise.

## Open in Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kouroshSA/E.Coli_FBA1/blob/main/FBA_Part1_EcoColi.ipynb)

> Click the badge above — no local Python installation required.

## What students will do

| Lab Step | Notebook Section |
|----------|-----------------|
| Load the *E. coli* glucose/oxygen model | Section 1 |
| Run FBA and record biomass flux (2a) | Section 2 |
| Identify highest-flux reaction (2b) | Section 2 |
| Visualise fluxes on metabolic map (2c) | Section 2 |
| View energy/cofactor dashboard (2d) | Section 2 |
| Knock out an assigned reaction (3a) | Section 3 |
| Compare WT vs KO results (Q1, Q2) | Section 4 |
| *(Bonus)* Genome-wide essentiality screen | Section 5 |

## Model

The **E. coli core metabolic model** (`e_coli_core`) from [BiGG Models](http://bigg.ucsd.edu/models/e_coli_core):

- 72 metabolites · 95 reactions · 137 genes
- Covers glycolysis, pentose phosphate pathway, TCA cycle, and oxidative phosphorylation
- Default condition: aerobic minimal medium with glucose as sole carbon source

## Software

| Package | Purpose |
|---------|---------|
| [COBRApy](https://cobrapy.readthedocs.io) | FBA solver and model I/O |
| [Escher](https://escher.github.io) | Interactive metabolic pathway maps |
| pandas / matplotlib | Data tables and dashboard plots |

All packages install automatically inside the notebook — students need only a browser and a Google account.

## Repository structure

```
FBA_Part1_EcoColi.ipynb   ← main notebook (open in Colab)
README.md
```

## Instructor notes

- Each student should be assigned a different reaction to knock out (see the table in Section 3).
  The notebook provides a drop-down selector for the 12 curated options, but students can also
  type any valid BiGG reaction ID.
- The bonus essentiality screen (Section 5) takes ~30 s and is suitable for students who finish early.
- Generated figures (`.png`) and Escher maps (`.html`) can be downloaded from the Colab file browser
  for inclusion in lab reports.
