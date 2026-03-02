# Alberta Separation: Economic Consequences Formal Model

**Asymmetric Adjustment Costs in Subnational Separation: Evidence from Fiscal Federalism and Commodity Trade**

A formal economic model and analysis examining the distributional welfare consequences of Alberta separating from Canada, developed by Zach Esses Johnson (University of Virginia).

---

## Table of Contents

1. [Overview](#overview)
2. [Model Summary](#model-summary)
3. [Repository Structure](#repository-structure)
4. [Requirements](#requirements)
5. [Setup](#setup)
6. [Usage](#usage)
7. [Reproducibility](#reproducibility)
8. [Citation](#citation)
9. [License](#license)
10. [Contributing](#contributing)
11. [Contact](#contact)

---

## Overview

Standard trade theory predicts that smaller economies bear disproportionate adjustment costs when exiting larger unions — a pattern confirmed by Brexit, where the UK experienced GDP losses roughly ten times larger than the EU‑27. This project examines whether that prediction holds for the Alberta–Canada case.

When a departing region simultaneously (i) makes substantial net fiscal contributions, (ii) specialises in commodities with globally elastic demand, and (iii) faces systematic monetary policy misalignment, the conventional small-country penalty may not apply. This repository contains the working paper and supporting materials that develop three analytical frameworks to investigate these conditions:

- A **modified gravity model** distinguishing commodity exports from differentiated manufactures.
- A **fiscal federalism model** calibrated to Canadian equalization transfers.
- An **Optimal Currency Area (OCA) analysis** applying Mundell–Bayoumi–Eichengreen criteria.

Historical precedents — the 1993 Czechoslovak dissolution and Brexit — are used to identify empirical analogues and bound the parameter space.

---

## Model Summary

### 1. Trade Framework (Modified Gravity)

Extends Anderson–van Wincoop (2003) to disaggregate exports into energy commodities (high world demand elasticity σ_E) and differentiated manufactures (σ_M). Derives a *welfare cost reversal condition*: when the remaining federation's dependence on the departing region's commodity exports (weighted by import substitution difficulty) exceeds the departing region's dependence on the federation's goods, the standard small-country asymmetry reverses.

### 2. Fiscal Federalism Framework

Models Canadian equalization following Boadway (2006). Calibrated to Alberta's net fiscal contribution of **$14.2 billion/year** (2022) and cumulative contributions of **$244.6 billion** (2007–2022). Derives *Theorem 1 (Fiscal Transfer Asymmetry)*: for a net fiscal contributor, post-separation welfare changes have opposite signs for the departing region and the remaining federation.

### 3. Optimal Currency Area Analysis

Applies Mundell (1961) criteria and the Bayoumi–Eichengreen (1997) OCA index. Finds Alberta is the only Canadian province for which common monetary policy imposes significant welfare costs (Chaban and Voss, 2016), partly due to the CAD's "petrocurrency" behaviour relative to oil prices.

### Quantitative Assessment

Conservative baseline estimates (Table 1 in the paper):

| Party | Net Welfare Effect |
|---|---|
| Alberta | Near zero (fiscal gains ~3 % GDP offset trade losses of 2–4 % GDP) |
| Remaining Canada | Negative 1.5–2.5 % of GDP |

Estimates carry substantial uncertainty and are sensitive to negotiation outcomes, trade agreement succession, and general equilibrium behavioural responses.

---

## Repository Structure

```
Alberta-Separation/
├── Alberta_Separation (1).pdf   # Working paper (LaTeX-compiled, pdfTeX)
├── LICENSE                      # Apache-2.0
└── README.md                    # This file
```

> **Note:** Additional source files (LaTeX `.tex`, data scripts, or notebooks) are not yet present in this repository. If you have access to the source materials, see [Contributing](#contributing) or [Contact](#contact).

---

## Requirements

The current repository contains only the compiled PDF. To **read the paper**, you need:

- A PDF viewer (e.g., Adobe Acrobat, Preview, Evince, or any modern web browser).

If source code (LaTeX, R, Python, Julia, etc.) is added in a future update, requirements will be listed here. Typical dependencies for this kind of economic modelling work include:

| Tool | Purpose |
|---|---|
| LaTeX / pdfTeX (TeX Live ≥ 2024) | Typesetting the working paper |
| R or Python ≥ 3.10 | Data wrangling and calibration scripts *(placeholder)* |
| Standard econometrics packages | Gravity estimation, OCA index *(placeholder)* |

---

## Setup

> **Placeholder:** No executable source code is currently included. Update this section when scripts or notebooks are added.

1. **Clone the repository**

   ```bash
   git clone https://github.com/zachessesjohnson/Alberta-Separation.git
   cd Alberta-Separation
   ```

2. **Install dependencies** *(once source files are available)*

   ```bash
   # Example for R
   Rscript -e "install.packages(c('gravity', 'fixest', 'tidyverse'))"

   # Example for Python
   pip install -r requirements.txt
   ```

3. **Compile the paper** *(once `.tex` sources are available)*

   ```bash
   pdflatex "Alberta_Separation.tex"
   bibtex Alberta_Separation
   pdflatex "Alberta_Separation.tex"
   pdflatex "Alberta_Separation.tex"
   ```

---

## Usage

> **Placeholder:** Replace this section with concrete instructions once runnable scripts are added to the repository.

To read the compiled paper directly:

```
Alberta_Separation (1).pdf
```

When analysis scripts are available, the expected workflow will be:

```
# Step 1 – Download / prepare data
# [placeholder: describe data sources and download steps]

# Step 2 – Run calibration
# [placeholder: e.g., Rscript analysis/calibrate_gravity.R]

# Step 3 – Generate tables and figures
# [placeholder: e.g., Rscript analysis/welfare_decomposition.R]

# Step 4 – Compile paper
# [placeholder: pdflatex Alberta_Separation.tex]
```

Key data sources used in the paper (publicly available):

| Dataset | Source | URL |
|---|---|---|
| Provincial GDP & per-capita income | Statistics Canada, Tables 36-10-0222-01 and 36-10-0221-01 | https://www150.statcan.gc.ca |
| Federal equalization transfers | Finance Canada | https://www.canada.ca/en/department-finance.html |
| Alberta oil production share | Canada Energy Regulator | https://www.cer-rec.gc.ca |
| Net fiscal contributions | Fraser Institute (2025) | https://www.fraserinstitute.org |
| Federal employment by province | Treasury Board of Canada Secretariat (2024) | https://www.canada.ca/en/treasury-board-secretariat.html |

---

## Reproducibility

The paper was compiled with **pdfTeX, Version 3.141592653-2.6-1.40.27 (TeX Live 2025)**. All quantitative results in the paper are calibration exercises rather than computationally intensive simulations; the key parameter values are fully reported in Table 1 of the paper, making hand-replication straightforward.

When additional source files are deposited:

- A `CHANGELOG.md` or release notes will document any updates to the calibration.
- Version tags will correspond to specific paper drafts.
- If data cleaning scripts are added, a `data/raw/` vs. `data/processed/` directory convention will be followed.

---

## Citation

If you use or build on this work, please cite:

```bibtex
@unpublished{johnson2026asymmetric,
  author  = {Johnson, Zach Esses},
  title   = {Asymmetric Adjustment Costs in Subnational Separation:
             Evidence from Fiscal Federalism and Commodity Trade},
  year    = {2026},
  month   = {February},
  note    = {Working paper, University of Virginia},
  url     = {https://github.com/zachessesjohnson/Alberta-Separation}
}
```

---

## License

This project is licensed under the **Apache License, Version 2.0**. See [`LICENSE`](LICENSE) for the full text.

You are free to use, reproduce, and distribute the materials in this repository (including derivative works) under the terms of the Apache 2.0 License.

---

## Contributing

Contributions — including corrections, additional empirical evidence, or code that replicates the paper's results — are welcome.

1. **Fork** the repository and create a feature branch:
   ```bash
   git checkout -b feature/my-contribution
   ```
2. **Make your changes** and commit with a clear message.
3. **Open a Pull Request** against `main`, describing what you changed and why.

For substantive methodological suggestions, please open an **Issue** first to discuss the proposed change.

---

## Contact

**Zach Esses Johnson**
University of Virginia

- GitHub: [@zachessesjohnson](https://github.com/zachessesjohnson)
- For questions about the paper or repository, please open an [Issue](https://github.com/zachessesjohnson/Alberta-Separation/issues).
