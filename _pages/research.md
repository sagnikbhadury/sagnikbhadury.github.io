---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
description: "Research in Bayesian graphical models, sparse network estimation, spatial statistics, multiplexed tissue imaging, spatial transcriptomics, computational pathology, and causal inference for cancer."
---

<span style="text-align: justify">My work is organized around four connected themes, rather than a single project. Across them, I develop **Bayesian graphical models, global-local shrinkage methods, spatial statistics, and multimodal learning** for cancer genomics and the tumor microenvironment. See [Publications]({{ "/publications/" | relative_url }}) for full citations and [Data & Projects]({{ "/datasets/" | relative_url }}) for code and model figures.</span>

<div class="domain-callout">
  <p class="domain-callout__label">Research domain guide</p>
  <h2>How the statistical and biomedical vocabulary fits together</h2>
  <p>For a detailed, literature-grounded map of terms such as precision matrices, cellular neighborhoods, spatially variable genes, ligand–receptor communication, pathomics, and radiogenomics, read the <a href="{{ '/research-domains/' | relative_url }}">research domains &amp; methods guide →</a></p>
</div>

---

## 1. Bayesian Graphical Models & Sparse Network Estimation

<span style="text-align: justify">Foundational methods work on **Bayesian Gaussian graphical models**, where a sparse precision matrix encodes conditional-dependence edges between variables. I study scalable covariance selection and neighborhood selection under horseshoe and spike-and-slab priors, joint estimation of related networks through shared shrinkage, and regression with a network-valued predictor.</span>

<div class="term-row" aria-label="Bayesian graphical model topics">
  <span>sparse precision matrices</span><span>global-local shrinkage</span><span>covariance selection</span><span>differential networks</span><span>uncertainty quantification</span>
</div>

* <span style="color:red">Bhadury, S.</span>, Mitra, R., Gaskins, J. <span style="color:blue">[Fast Bayesian High-Dimensional Gaussian Graphical Model Estimation](https://arxiv.org/abs/2308.02713)</span>
* <span style="color:red">Bhadury, S.</span> et al. <span style="color:blue">Bayesian Joint Estimation of Multiple Graphs through Shared Shrinkage</span>

## 2. Spatial Statistics for Multiplexed Tissue Imaging

<span style="text-align: justify">I develop spatially varying graphical models for the **tumor immune microenvironment**, recovering shared and region-specific cell–cell interaction networks from 2D and 3D multiplexed immunofluorescence data. The models connect spatial heterogeneity, cellular neighborhoods, and tissue architecture with Gaussian-process structure and spatially adaptive shrinkage.</span>

<div class="term-row" aria-label="Spatial tissue imaging topics">
  <span>multiplex immunofluorescence</span><span>spatial proteomics</span><span>cellular neighborhoods</span><span>3D tissue imaging</span><span>tumor microenvironment</span>
</div>

* <span style="color:red">Bhadury, S.</span> et al. <span style="color:blue">[ISPAT: Informed Spatially Aware Patterns for Multiplexed Immunofluorescence data](https://www.nature.com/articles/s41598-026-35341-8)</span>, **Nature Scientific Reports**. [Code](https://github.com/sagnikbhadury/ISPAT)
* <span style="color:red">Bhadury, S.</span>, Rao, A. <span style="color:blue">[ISPAT 3D: Spatially Varying Conditional Volumetric Network Estimation for 3D Tumor Imaging](https://doi.org/10.64898/2026.04.16.719017)</span>. [Code](https://github.com/sagnikbhadury/ISPAT-3D)
* <span style="color:red">Bhadury, S.</span>, Gaskins, J., Rao, A. <span style="color:blue">[Spatially Varying Graphical Models for Cell-Cell Interaction Networks in Multiplexed Tissue Imaging](https://doi.org/10.64898/2026.04.01.715977)</span> [Code](https://github.com/sagnikbhadury/GP-GHS)

## 3. Multi-Modal Integration & Imaging Genomics

<span style="text-align: justify">This work fuses histopathology, spatial transcriptomics, radiomics, and molecular features into coherent predictive or inferential models. The scientific targets include spatially variable gene programs, gene regulatory and ligand–receptor interactions, image–transcriptome associations, multimodal survival analysis, and biomarker discovery for precision oncology.</span>

<div class="term-row" aria-label="Multimodal imaging genomics topics">
  <span>spatial multi-omics</span><span>computational pathology</span><span>pathomics</span><span>radiogenomics</span><span>cell–cell communication</span>
</div>

* Tsang, A., Krishnan, S., Kulkarni, R., <span style="color:red">Bhadury, S.</span>, Rao, A., et al. <span style="color:blue">[Encoding functional edges in graphs to model spatially varying relationships in the tumor microenvironment](https://doi.org/10.1038/s44387-026-00075-5)</span>, **npj Artificial Intelligence**
* <span style="color:red">Bhadury, S.</span> et al. <span style="color:blue">Graph-Based Multi-Modal Learning for Integrating Histopathological and Transcriptomic Features in Lung Cancer</span> [Code](https://github.com/sagnikbhadury/GOV)
* <span style="color:red">Bhadury, S.</span> et al. <span style="color:blue">RISM: Radiomic feature Integration with Spike-and-slab for Multimodal survival analysis</span>. [Code](https://github.com/sagnikbhadury/rism)
* **PathMI** &mdash; mutual information estimators (OLS, LASSO, Bayesian horseshoe) linking histopathology embeddings to molecular subtype. [Code](https://github.com/sagnikbhadury/PathMI)

## 4. Causal Inference & Functional Data Analysis

<span style="text-align: justify">I use causal mediation and sensitivity analysis to study spatial cell-type co-occurrence, with explicit attention to the assumptions separating association from causal interpretation. In parallel, functional-depth-based classifiers and interpretable tree-derived rules turn curve-valued histopathology features into robust biomarkers for tumor subtyping.</span>

<div class="term-row" aria-label="Causal and functional data topics">
  <span>causal mediation</span><span>sensitivity analysis</span><span>functional depth</span><span>robust classification</span><span>interpretable biomarkers</span>
</div>

* <span style="color:red">Bhadury, S.</span> et al. <span style="color:blue">Functional Depth biomarkers Distinguish Lung Cancer Subtypes</span>. [Code](https://github.com/sagnikbhadury/Functional-Depth)
* Mediation and sensitivity analyses of spatial cell-type co-occurrence patterns. [Code](https://github.com/sagnikbhadury/Causal-Inference)
* Statistical shape analysis (PCA-based) of MRI-derived tumor contours in lower-grade glioma. [Code](https://github.com/sagnikbhadury/Shape-Analysis-of-LGG)

---
