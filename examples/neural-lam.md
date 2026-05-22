# AERI Report: neural-lam
**Repository:** https://github.com/mllam/neural-lam
**Date:** 2026-05-22 06:49:11

## Summary
**Total Score: 9/15**
**Classification: Not Agent-Ready**
**Agent-Ready: No**
**AERI Scoring Cost: $0.4713**
**Paper2Agent Cost (if run): $10–30**
**Estimated Savings: $9.53 to $29.53**

## Dimension Scores

**Completeness:** [█░░] 1/3
**Clarity:** [██░] 2/3
**Modularity:** [███] 3/3
**Reproducibility:** [██░] 2/3
**Executability:** [█░░] 1/3

## Detailed Analysis

### Completeness (1/3)
*Critical scanner misalignment - the core neural weather prediction method is in .py files, but scanner will exclude them due to presence of .ipynb files. The notebook is unrelated data preprocessing that doesn't demonstrate the core method, creating a complete miss of the paper's contribution.*

Core files: ['neural_lam/models/step_predictors/graph/graph_lam.py', 'neural_lam/models/step_predictors/graph/hi_lam.py', 'neural_lam/train_model.py']
Scanner finds core: False

### Clarity (2/3)
*Functions have docstrings and type hints, uses proper config system with argparse/yaml, but some documentation gaps exist. No hardcoded paths found in main components.*

### Modularity (3/3)
*Excellent modularity - models are clearly importable independently through proper __init__.py structure, clean separation between models, datastores, and utilities. Well-architected with minimal coupling.*

### Reproducibility (2/3)
*Proper pyproject.toml with dependencies on PyPI, installation should work with effort. CUDA dependencies exist but CPU fallback available. No SSH dependencies or compilation barriers.*

### Executability (1/3)
*No demo exists that demonstrates the core neural weather prediction method. The only notebook is data preprocessing, not a demo of the paper's contribution. Requires external dataset download to run any meaningful examples.*

## Recommendations

- Critical: Remove or move the peripheral data preprocessing notebook to avoid scanner misalignment that completely misses the core method

- Add a proper demo script that runs the neural weather prediction models on included sample data

- Include minimal sample weather data files to enable demo execution without external downloads

- Consider adding a simple example that demonstrates model training and inference workflow

- Add integration tests that verify core functionality works end-to-end

---
*Completed in 147.6s*