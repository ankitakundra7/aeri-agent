# AERI Report: scanpy
**Repository:** https://github.com/scverse/scanpy
**Date:** 2026-05-22 14:12:18

## Summary
**Total Score: 15/15**
**Classification: Agent-Ready**
**Agent-Ready: Yes**
**AERI Scoring Cost: $0.4706**
**Paper2Agent Cost (if run): $10–30**

## Dimension Scores

**Completeness:** [███] 3/3
**Clarity:** [███] 3/3
**Modularity:** [███] 3/3
**Reproducibility:** [███] 3/3
**Executability:** [███] 3/3

## Detailed Analysis

### Completeness (3/3)
*Core method (single-cell analysis pipeline) is demonstrated in relevant notebooks that import and use scanpy extensively. Built-in dataset functions provide readily available data. Clear README and well-organized structure.*

Core files: ['src/scanpy/preprocessing/', 'src/scanpy/tools/', 'src/scanpy/plotting/']
Scanner finds core: True

### Clarity (3/3)
*Comprehensive docstrings throughout codebase, well-documented functions, clear README, minimal hardcoded paths, extensive documentation website*

### Modularity (3/3)
*Library is designed for import as 'import scanpy as sc', clean module structure with preprocessing, tools, and plotting submodules. No top-level side effects.*

### Reproducibility (3/3)
*Single-command pip install works, all dependencies on PyPI, no SSH URLs, comprehensive pyproject.toml*

### Executability (3/3)
*Comprehensive demos exist showing full single-cell analysis workflow from data loading to clustering and visualization. Built-in dataset functions provide readily available data. Runs on CPU in reasonable time.*
Demo: notebooks/pbmc3k.ipynb

## Recommendations

- Repository is already well-structured for agent conversion

- Notebooks effectively demonstrate core single-cell analysis capabilities

- Built-in dataset functions eliminate external data dependencies

---
*Completed in 209.4s*