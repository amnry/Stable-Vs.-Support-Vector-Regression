# Stable vs. Support Vector Regression

This repository explores the mathematical equivalence between Nu-Support Vector Regression (NuSVR) and Conditional Value at Risk (CVaR) regression methods. Through empirical analysis on various datasets, we demonstrate that these seemingly different approaches produce remarkably similar results under equivalent parameter settings.

## Overview

The project investigates the relationship between:
- **Nu-Support Vector Regression (NuSVR)**: A variant of SVR that uses the nu parameter to control the number of support vectors
- **Conditional Value at Risk (CVaR) Regression**: A stable regression method based on risk measures from financial mathematics

Our analysis shows that these methods are mathematically equivalent under certain conditions, with the nu parameter in NuSVR corresponding to (1-alpha) in CVaR regression.

## Repository Contents

- **Abalone_Model.ipynb**: Application of both regression methods to the Abalone dataset, including stability analysis across 1000 train-test splits
- **Regression_Testing.ipynb**: Demonstration of equivalence on a simple synthetic linear dataset with visualization
- **Multivariate_Model.ipynb**: Extension to multivariate regression with 4 features

## Key Findings

1. **Coefficient Similarity**: Both methods produce nearly identical coefficients and intercepts across all tested datasets
2. **Parameter Correspondence**: The nu parameter in NuSVR corresponds to (1-alpha) in CVaR regression
3. **Regularization Handling**: Both methods handle regularization similarly, with the C parameter controlling the strength
4. **Stability**: Both methods show similar stability properties when tested across multiple data splits

## Requirements

- Python 3.x
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- PSG Python (for CVaR regression implementation)

## Usage

Each notebook is self-contained and can be run independently. The PSG solver is required for the CVaR regression implementation.


## Theoretical Background

The equivalence between NuSVR and CVaR regression provides insights into the theoretical foundations of both methods:

- NuSVR is typically understood through the lens of structural risk minimization and margin maximization
- CVaR regression is derived from risk measures in financial mathematics
- Their equivalence suggests a deeper connection between these seemingly different theoretical frameworks

## Future Work

- Exploration of non-linear kernels in both frameworks
- Analysis of computational efficiency differences
- Investigation of cases where the equivalence might break down
- Applications to other domains and datasets

## References

- Schölkopf, B., et al. (2000). New support vector algorithms.
- Rockafellar, R. T., & Uryasev, S. (2000). Optimization of conditional value-at-risk.
- Takeda, A., & Sugiyama, M. (2008). ν-Support vector machine as conditional value-at-risk minimization.
EOL

# Verify the file was created
ls -la README.md

# Add the file to git
git add README.md

# Commit the file
git commit -m "Add README.md with project description"

# Push the changes to GitHub
git push origin main