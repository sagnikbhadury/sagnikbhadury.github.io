---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

<span style="text-align: justify">My work is organized around four connected themes, rather than a single project &mdash; each theme applies Bayesian graphical modeling and sparsity-inducing priors to a different data modality in cancer genomics. See [Publications]({{ "/publications/" | relative_url }}) for full citations and [Data & Projects]({{ "/datasets/" | relative_url }}) for code and model figures.</span>

---

## 1. Bayesian Graphical Models & Sparse Network Estimation

<span style="text-align: justify">Foundational methods work on estimating high-dimensional graphical models under horseshoe and spike-and-slab priors, and on regressing a scalar outcome on a network-valued predictor.</span>

* <span style="color:red">Bhadury, S.</span>, Mitra, R., Gaskins, J. <span style="color:blue">[Fast Bayesian High-Dimensional Gaussian Graphical Model Estimation](https://arxiv.org/abs/2308.02713)</span>
* <span style="color:red">Bhadury, S.</span> et al. <span style="color:blue">Bayesian Joint Estimation of Multiple Graphs through Shared Shrinkage</span>

## 2. Spatial Statistics for Multiplexed Tissue Imaging

<span style="text-align: justify">Spatially varying graphical models that recover shared and region-specific cell-cell interaction networks from 2D and 3D multiplexed immunofluorescence data, extended with Gaussian-process-based spatial shrinkage.</span>

* <span style="color:red">Bhadury, S.</span> et al. <span style="color:blue">[ISPAT: Informed Spatially Aware Patterns for Multiplexed Immunofluorescence data](https://www.nature.com/articles/s41598-026-35341-8)</span>, **Nature Scientific Reports**. [Code](https://github.com/sagnikbhadury/ISPAT)
* <span style="color:red">Bhadury, S.</span>, Rao, A. <span style="color:blue">[ISPAT 3D: Spatially Varying Conditional Volumetric Network Estimation for 3D Tumor Imaging](https://doi.org/10.64898/2026.04.16.719017)</span>. [Code](https://github.com/sagnikbhadury/ISPAT-3D)
* <span style="color:red">Bhadury, S.</span>, Gaskins, J., Rao, A. <span style="color:blue">[Spatially Varying Graphical Models for Cell-Cell Interaction Networks in Multiplexed Tissue Imaging](https://doi.org/10.64898/2026.04.01.715977)</span> [Code](https://github.com/sagnikbhadury/GP-GHS)

## 3. Multi-Modal Integration & Imaging Genomics

<span style="text-align: justify">Fusing histopathology, transcriptomics, and radiomic features into a single predictive or inferential model &mdash; identifying gene and ligand-receptor interactions, and integrating features for survival analysis and biomarker discovery.</span>

* Tsang, A., Krishnan, S., Kulkarni, R., <span style="color:red">Bhadury, S.</span>, Rao, A., et al. <span style="color:blue">[Encoding functional edges in graphs to model spatially varying relationships in the tumor microenvironment](https://doi.org/10.1038/s44387-026-00075-5)</span>, **npj Artificial Intelligence**
* <span style="color:red">Bhadury, S.</span> et al. <span style="color:blue">Graph-Based Multi-Modal Learning for Integrating Histopathological and Transcriptomic Features in Lung Cancer</span> [Code](https://github.com/sagnikbhadury/GOV)
* <span style="color:red">Bhadury, S.</span> et al. <span style="color:blue">RISM: Radiomic feature Integration with Spike-and-slab for Multimodal survival analysis</span>. [Code](https://github.com/sagnikbhadury/rism)
* **PathMI** &mdash; mutual information estimators (OLS, LASSO, Bayesian horseshoe) linking histopathology embeddings to molecular subtype. [Code](https://github.com/sagnikbhadury/PathMI)

## 4. Causal Inference & Functional Data Analysis

<span style="text-align: justify">Mediation analysis for spatial cell-type co-occurrence, and functional-depth-based classifiers with interpretable, tree-derived decision rules for distinguishing tumor subtypes.</span>

* <span style="color:red">Bhadury, S.</span> et al. <span style="color:blue">Functional Depth biomarkers Distinguish Lung Cancer Subtypes</span>. [Code](https://github.com/sagnikbhadury/Functional-Depth)
* Mediation and sensitivity analyses of spatial cell-type co-occurrence patterns. [Code](https://github.com/sagnikbhadury/Causal-Inference)
* Statistical shape analysis (PCA-based) of MRI-derived tumor contours in lower-grade glioma. [Code](https://github.com/sagnikbhadury/Shape-Analysis-of-LGG)

---
