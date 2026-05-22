# AERI Report: Semi-DETR
**Repository:** https://github.com/JCZ404/Semi-DETR
**Date:** 2026-05-22 06:38:19

## Summary
**Total Score: 5/15**
**Classification: Not Agent-Ready**
**Agent-Ready: No**
**AERI Scoring Cost: $0.6732**
**Paper2Agent Cost (if run): $10–30**
**Estimated Savings: $9.33 to $29.33**

## Dimension Scores

**Completeness:** [█░░] 1/3
**Clarity:** [█░░] 1/3
**Modularity:** [█░░] 1/3
**Reproducibility:** [█░░] 1/3
**Executability:** [█░░] 1/3

## Detailed Analysis

### Completeness (1/3)
*This is a 'misaligned notebooks' pattern. The core Semi-DETR method is in .py files, but .ipynb files exist that are unrelated peripheral content (generic MMDetection tutorials). The scanner will exclude all .py files and select only the notebooks, completely missing the core Semi-DETR method. This is a critical content gap.*

Core files: ['detr_od/models/dino_detr.py', 'detr_od/models/dense_heads/dino_detr_head.py', 'detr_ssod/']
Scanner finds core: False

### Clarity (1/3)
*Minimal documentation with inconsistent docstrings. Config system exists but has relative path dependencies. No comprehensive documentation or clear entry points for understanding the core method.*

### Modularity (1/3)
*Tightly coupled architecture with multiple interdependent custom packages (detr_od, detr_ssod). Complex dependency on customized mmdetection. Not easily importable as standalone module due to extensive coupling.*

### Reproducibility (1/3)
*Environment installation likely fails due to complex multi-step process requiring CUDA compilation, custom mmdetection installation, and custom CUDA ops. Dependencies not on PyPI and require specific environment setup.*

### Executability (1/3)
*Demo exists but requires external model checkpoint downloads and cannot run without extensive setup. Requires multi-GPU setup as indicated in issues. No CPU-only capability for demonstrating core method.*
Demo: demo/image_demo.py

## Recommendations

- Remove or relocate the peripheral MMDetection notebooks that cause scanner misselection

- Include sample datasets or provide built-in dataset download functionality

- Simplify installation to single pip install command without CUDA compilation

- Provide pre-trained model weights that can be downloaded automatically

- Add CPU-only inference capability for demos

- Improve documentation with comprehensive API docs and usage examples

- Reduce coupling between custom packages to enable standalone usage

---
*Completed in 217.0s*