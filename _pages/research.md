---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
description: "Research in Bayesian graphical models, spatial statistics, Gaussian processes, spatial transcriptomics, multimodal imaging genomics, causal inference, Bayesian methods for AI interpretability, and clinical trials and longitudinal biomedical data."
---

<span style="text-align: justify">My work is organized around eight connected research directions rather than a single project. Across them, I develop **Bayesian graphical models, global-local shrinkage methods, spatial and Gaussian-process models, causal inference, and multimodal learning**, and apply them to cancer biology, the tumor microenvironment, clinical studies, and the internal representations of modern AI models. See [Publications]({{ "/publications/" | relative_url }}) for full citations and [Data & Projects]({{ "/datasets/" | relative_url }}) for code and model figures.</span>

<div class="domain-callout">
  <p class="domain-callout__label">Research domain guide</p>
  <h2>How the statistical and biomedical vocabulary fits together</h2>
  <p>For a detailed, literature-grounded map of terms such as precision matrices, cellular neighborhoods, spatially variable genes, ligand–receptor communication, pathomics, and radiogenomics, read the <a href="{{ '/research-domains/' | relative_url }}">research domains &amp; methods guide →</a></p>
</div>

---

## 1. Bayesian Graphical Models & Sparse Network Estimation

<span style="text-align: justify">Foundational methods work on **Bayesian Gaussian graphical models**, where a sparse precision matrix encodes conditional-dependence edges between variables. I study scalable covariance selection and neighborhood selection under horseshoe and spike-and-slab priors, joint estimation of related networks through shared shrinkage, and regression with a network-valued predictor ([GOV](https://github.com/sagnikbhadury/GOV)).</span>

<div class="term-row" aria-label="Bayesian graphical model topics">
  <span>sparse precision matrices</span><span>global-local shrinkage</span><span>covariance selection</span><span>differential networks</span><span>uncertainty quantification</span>
</div>

* <span style="color:red">Bhadury, S.</span>, Mitra, R., Gaskins, J. <span style="color:blue">[Fast Bayesian High-Dimensional Gaussian Graphical Model Estimation](https://arxiv.org/abs/2308.02713)</span>
* <span style="color:red">Bhadury, S.</span>, Mitra, R., Gaskins, J. <span style="color:blue">Bayesian Joint Estimation of Multiple Graphs through Shared Shrinkage</span> (in preparation)

## 2. Spatial Statistics for Multiplexed Tissue Imaging

<span style="text-align: justify">I develop spatially varying graphical models for the **tumor immune microenvironment**, recovering shared and region-specific cell–cell interaction networks from 2D and 3D multiplexed immunofluorescence data. The models connect spatial heterogeneity, cellular neighborhoods, and tissue architecture with Gaussian-process structure and spatially adaptive shrinkage.</span>

<div class="term-row" aria-label="Spatial tissue imaging topics">
  <span>multiplex immunofluorescence</span><span>spatial proteomics</span><span>cellular neighborhoods</span><span>3D tissue imaging</span><span>tumor microenvironment</span>
</div>

* <span style="color:red">Bhadury, S.</span> et al. <span style="color:blue">[ISPat: Informed Spatially Aware Patterns for Multiplexed Immunofluorescence data](https://www.nature.com/articles/s41598-026-35341-8)</span>, **Nature Scientific Reports**. [Code](https://github.com/sagnikbhadury/ISPAT)
* <span style="color:red">Bhadury, S.</span>, Rao, A. <span style="color:blue">[Estimating conditional cell population associations across tumor density trajectory in three dimensional tissue images (ISPat 3D)](https://www.nature.com/articles/s41598-026-73151-0)</span>, **Nature Scientific Reports**. [Code](https://github.com/sagnikbhadury/ISPAT-3D) | [R package on CRAN](https://cran.r-project.org/web/packages/ISPAT3D/)
* <span style="color:red">Bhadury, S.</span>, Gaskins, J., Rao, A. <span style="color:blue">[Spatially Varying Graphical Models for Cell-Cell Interaction Networks in Multiplexed Tissue Imaging](https://doi.org/10.64898/2026.04.01.715977)</span> [Code](https://github.com/sagnikbhadury/GP-GHS)

## 3. Gaussian Processes & Spatial Point Patterns

<span style="text-align: justify">Spatial studies rarely measure every outcome at every location. I build **multivariate Gaussian-process models** that borrow strength across outcomes observed at misaligned locations, with shrinkage priors deciding how much to borrow, and **Bayesian models for spatial point patterns** that treat cell locations themselves as the data.</span>

<div class="term-row" aria-label="Gaussian process topics">
  <span>multivariate Gaussian processes</span><span>coregionalization</span><span>misaligned outcomes</span><span>meshed GPs</span><span>point processes</span>
</div>

* <span style="color:red">Bhadury, S.</span> <span style="color:blue">Design-Adaptive Borrowing Across Misaligned Outcomes in Bayesian Coregionalization Models</span>. [Code](https://github.com/sagnikbhadury/meshedghs)
* Bayesian inference for point patterns in space (presented at JSM 2024 and IISA 2024).

## 4. Spatial Transcriptomics & Compositional Data

<span style="text-align: justify">Spot-level spatial transcriptomics measures mixtures of cells, so cell-type proportions are **compositional**: they sum to one, contain zeros, and are spatially dependent. I am developing regression models for spatial compositional data, and shrinkage-based image-basis regression models that link tissue morphology to gene expression.</span>

<div class="term-row" aria-label="Spatial transcriptomics topics">
  <span>compositional regression</span><span>cell-type proportions</span><span>zeros in compositions</span><span>morphology–expression association</span><span>spatially variable genes</span>
</div>

* <span style="color:red">Bhadury, S.</span>, Schwob, M., Datta, J. <span style="color:blue">Spatial Active-Set Ray Regression for Compositional Data: Methodology, Validation, and Applications in Spatial Transcriptomics and Community Ecology</span> (in preparation)
* <span style="color:red">Bhadury, S.</span>, Rao, A. <span style="color:blue">SHIRE: Spatial Horseshoe Image-Basis Regression for Morphology and Gene Expression Associations in Spatial Transcriptomics</span> (in preparation)

## 5. Multi-Modal Integration & Imaging Genomics

<span style="text-align: justify">This work fuses histopathology, spatial transcriptomics, radiomics, and molecular features into coherent predictive or inferential models. The scientific targets include gene regulatory and ligand–receptor interactions, image–transcriptome associations, multimodal survival analysis, and how much molecular information pathology foundation models actually carry.</span>

<div class="term-row" aria-label="Multimodal imaging genomics topics">
  <span>spatial multi-omics</span><span>computational pathology</span><span>pathology foundation models</span><span>radiogenomics</span><span>cell–cell communication</span>
</div>

* Tsang, A., Krishnan, S., Kulkarni, R., <span style="color:red">Bhadury, S.</span>, Rao, A., et al. <span style="color:blue">[Encoding functional edges in graphs to model spatially varying relationships in the tumor microenvironment](https://doi.org/10.1038/s44387-026-00075-5)</span>, **npj Artificial Intelligence**
* <span style="color:red">Bhadury, S.</span>, Tsang, A., Ray, D., Lagisetty, K., Kundu, S., Rao, A. <span style="color:blue">Graph-Based Multi-Modal Learning for Integrating Histopathological and Transcriptomic Features in Lung Adenocarcinoma</span>
* <span style="color:red">Bhadury, S.</span>, Kulkarni, R., Rao, A. <span style="color:blue">Quantifying Biological Signal in Pathology Foundation Models through Bayesian Mutual Information Estimation</span> (in preparation)
* <span style="color:red">Bhadury, S.</span>, Mohammed, S., Kurtek, S., Rao, A. <span style="color:blue">RISM: Radiomic Feature Integration with Spike-and-Slab for Multimodal Survival Analysis</span> (in preparation)

## 6. Causal Inference & Functional Data Analysis

<span style="text-align: justify">I use causal mediation and sensitivity analysis to separate what spatial cell-type co-occurrence reflects: differences in **tissue composition** versus genuine **spatial organization**, with explicit attention to the assumptions that separate association from causal interpretation. In parallel, functional-depth-based classifiers turn curve-valued histopathology features into robust biomarkers for tumor subtyping.</span>

<div class="term-row" aria-label="Causal and functional data topics">
  <span>causal mediation</span><span>sensitivity analysis</span><span>compositional confounding</span><span>functional depth</span><span>interpretable biomarkers</span>
</div>

* <span style="color:red">Bhadury, S.</span>, Frankel, T.L., Rao, A. <span style="color:blue">[Cellular Proximity and Conditional Coordination in the Colorectal and Pancreatic Tumor Microenvironment: A Patient-Level Analysis of Multiplexed Imaging](https://doi.org/10.64898/2026.10.08.757632)</span>
* <span style="color:red">Bhadury, S.</span>, Frankel, T., Rao, A. <span style="color:blue">Resolving Compositional Confounding in Spatial Proximity Analysis through Mediation in Tumor Microenvironments</span> (in preparation)
* <span style="color:red">Bhadury, S.</span>, Frankel, T., Rao, A. <span style="color:blue">Causal Mediation Decomposes Pancreatic Cancer Spatial Diversity into Compositional and Organizational Pathways</span> (in preparation)
* <span style="color:red">Bhadury, S.</span>, Tsang, A.P., Ray, D., Lagisetty, K., Rao, A. <span style="color:blue">[Functional Depth Biomarkers Distinguish Lung Squamous Cell Carcinoma from Lung Adenocarcinoma](https://doi.org/10.21203/rs.3.rs-9347794/v1)</span>. [Code](https://github.com/sagnikbhadury/Functional-Depth)
* Mediation and sensitivity analyses of spatial cell-type co-occurrence patterns. [Code](https://github.com/sagnikbhadury/Causal-Inference)
* Statistical shape analysis (PCA-based) of MRI-derived tumor contours in lower-grade glioma. [Code](https://github.com/sagnikbhadury/Shape-Analysis-of-LGG)

## 7. Bayesian Methods for AI & Interpretability

<span style="text-align: justify">Many questions about large neural networks are, at heart, **high-dimensional variable selection** problems: which learned features carry a behavior, which components can be removed, and whether two models have learned the same thing. I bring global-local shrinkage, Bayesian uncertainty quantification, and error-rate control to the **interpretability and compression of language models**: selecting sparse-autoencoder features with calibrated uncertainty, testing whether the features a dictionary learns are actually used by the model, comparing dictionaries learned by different models, and deciding which components of a large language model can be pruned with statistical guarantees.</span>

<div class="term-row" aria-label="AI and interpretability topics">
  <span>sparse autoencoders</span><span>mechanistic interpretability</span><span>feature selection</span><span>model diffing</span><span>LLM pruning</span><span>error-rate control</span>
</div>

* <span style="color:red">Bhadury, S.</span> <span style="color:blue">Does the Route Matter? Functional Validation of Shared&ndash;Private Sparse Autoencoders</span>
* <span style="color:red">Bhadury, S.</span> <span style="color:blue">Comparing Sparse Autoencoder Dictionaries through Decoder Subspaces</span>
* Ongoing: horseshoe-based selection of sparse-autoencoder features, and Bayesian structured pruning of large language models with false-discovery control.

## 8. Clinical Trials & Longitudinal Biomedical Data

<span style="text-align: justify">At Penn Medicine, I work on **Bayesian clinical trial design** and on longitudinal modeling of repeated biomarker and outcome data: joint models linking biomarker trajectories to time-to-event outcomes, mixed-effects models for serial plasma and omics measurements, and competing-risks frameworks for informative missingness due to death or dropout. This includes high-dimensional multi-omic integration across CyTOF, proteomics, transcriptomics, and cfDNA methylomics for biomedical phenotyping.</span>

<div class="term-row" aria-label="Clinical trials and longitudinal data topics">
  <span>Bayesian trial design</span><span>joint models</span><span>competing risks</span><span>informative missingness</span><span>multi-omic phenotyping</span>
</div>

---
