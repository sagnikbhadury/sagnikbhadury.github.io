---
layout: single
permalink: /datasets/
title: "Data & Projects"
author_profile: true
description: "Research projects and open-source code for spatial transcriptomics, multiplex immunofluorescence, H&E computational pathology, MRI radiomics, multivariate spatial data, language-model interpretability, and longitudinal clinical and multi-omic data."
redirect_from:
  - /data/
---

My methods work is developed hand-in-hand with the complex data types below. Projects are grouped by the data they analyze; the [Research]({{ "/research/" | relative_url }}) page groups the same work by methodological direction. Code and data associated with each project are released alongside the corresponding preprint or publication; see the [Publications]({{ "/publications/" | relative_url }}) page for full citations.

---

## Spatial Transcriptomics

<span style="text-align: justify">Spatially resolved gene expression profiles that preserve the tissue coordinates of each measurement, allowing transcriptomic activity to be studied jointly with tissue architecture. I use these data to model gene–gene and ligand–receptor interactions, to analyze spot-level cell-type proportions as spatial compositional data, and to link tissue morphology to gene expression measured on the same section.</span>

![Spot-level gene expression graph](/images/research/spatial-transcriptomics-schematic.svg "Model schematic: functional edges over a spatial spot grid encode spatially varying gene relationships")
{: .align-center}

* <span style="text-align: justify">Tsang, A., Krishnan, S., Kulkarni, R., <span style="color:red">Bhadury, S.</span>, Rao, A., et al. <span style="color:blue">[Encoding functional edges in graphs to model spatially varying relationships in the tumor microenvironment](https://doi.org/10.1038/s44387-026-00075-5)</span>, **npj Artificial Intelligence**.</span>
* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Schwob, M., Datta, J. <span style="color:blue">Spatial Active-Set Ray Regression for Compositional Data: Methodology, Validation, and Applications in Spatial Transcriptomics and Community Ecology</span> — regression for spot-level cell-type proportions that respects the sum-to-one constraint, handles zeros directly, and accounts for spatial dependence. (In preparation)</span>
* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Rao, A. <span style="color:blue">SHIRE: Spatial Horseshoe Image-Basis Regression for Morphology and Gene Expression Associations in Spatial Transcriptomics</span> — horseshoe-shrunk regression linking H&amp;E morphology to single-cell gene expression. (In preparation)</span>

## 2D & 3D Multiplexed Immunofluorescence (mIF)

<span style="text-align: justify">High-plex single-cell imaging that records the spatial coordinates and marker intensities of many cell types on a single tissue section (2D) or across serial sections and volumes (3D). These data let me build spatial graphical models of the cell–cell interaction networks that make up the tumor microenvironment, test whether those interaction patterns differ by disease state, and separate spatial organization from differences in tissue composition.</span>

![ISPat spatial graphical model](/images/research/ispat-schematic.svg "Model schematic: spatial graphical model over multiplexed immunofluorescence cell-type intensities")
{: .align-center}

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span> et al. <span style="color:blue">[ISPat: Informed Spatially Aware Patterns for Multiplexed Immunofluorescence data](https://www.nature.com/articles/s41598-026-35341-8)</span>, **Nature Scientific Reports** — Bayesian spatial mixed-effects modeling (Poisson & Gaussian) of cell-type intensities across tissue slides. [Code](https://github.com/sagnikbhadury/ISPAT)</span>

![ISPat 3D volumetric network](/images/research/ispat3d-schematic.svg "Model schematic: volumetric spatial network estimation across serial tissue sections")
{: .align-center}

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Rao, A. <span style="color:blue">[Estimating conditional cell population associations across tumor density trajectory in three dimensional tissue images (ISPat 3D)](https://www.nature.com/articles/s41598-026-73151-0)</span>, **Nature Scientific Reports** — extends spatial network estimation to volumetric, 3D multiplexed cancer imaging. [Code](https://github.com/sagnikbhadury/ISPAT-3D) | [R package on CRAN](https://cran.r-project.org/web/packages/ISPAT3D/)</span>

![GP-GHS spatially varying shrinkage](/images/research/gp-ghs-schematic.svg "Model schematic: Gaussian Process group horseshoe shrinkage of interaction strength across space")
{: .align-center}

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Gaskins, J., Rao, A. <span style="color:blue">[Spatially Varying Graphical Models for Cell-Cell Interaction Networks in Multiplexed Tissue Imaging](https://doi.org/10.64898/2026.04.01.715977)</span> — group horseshoe shrinkage priors combined with Gaussian Process spatial structure (GP-GHS) for interaction network estimation. [Code](https://github.com/sagnikbhadury/GP-GHS)</span>

![Spatial mediation diagram](/images/research/mediation-schematic.svg "Model schematic: mediation analysis of spatial cell-type co-occurrence between disease group and tissue outcome")
{: .align-center}

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Frankel, T.L., Rao, A. <span style="color:blue">[Cellular Proximity and Conditional Coordination in the Colorectal and Pancreatic Tumor Microenvironment: A Patient-Level Analysis of Multiplexed Imaging](https://doi.org/10.64898/2026.10.08.757632)</span></span>
* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Frankel, T., Rao, A. <span style="color:blue">Resolving Compositional Confounding in Spatial Proximity Analysis through Mediation in Tumor Microenvironments</span> (in preparation)</span>
* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Frankel, T., Rao, A. <span style="color:blue">Causal Mediation Decomposes Pancreatic Cancer Spatial Diversity into Compositional and Organizational Pathways</span> (in preparation)</span>
* <span style="text-align: justify">Mediation and sensitivity analyses testing whether cell-type density and spatial co-occurrence patterns mediate the relationship between disease group and tissue-level outcomes. [Code](https://github.com/sagnikbhadury/Causal-Inference)</span>

## H&E Imaging & Computational Pathology

<span style="text-align: justify">Hematoxylin and eosin stained whole-slide images capturing tissue and cellular morphology. I use these images to extract histomorphological features, integrate them with molecular and spatial data, and measure how much molecular information the embeddings of pathology foundation models actually carry.</span>

<!--
![H&E and transcriptomic graph fusion](/images/research/he-fusion-schematic.svg "Model schematic: dual-branch graph fusion of H&E morphology and transcriptomic features")
{: .align-center}
-->

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Tsang, A., Ray, D., Lagisetty, K., Kundu, S., Rao, A. <span style="color:blue">Graph-Based Multi-Modal Learning for Integrating Histopathological and Transcriptomic Features in Lung Adenocarcinoma</span> — graph-based fusion of transcriptomic and histopathological features to identify gene interactions and ligand–receptor interactions.</span>
* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Kulkarni, R., Rao, A. <span style="color:blue">Quantifying Biological Signal in Pathology Foundation Models through Bayesian Mutual Information Estimation</span> — compares pathology foundation models by the molecular information their tile embeddings carry, against permutation nulls. (In preparation)</span>

![Functional depth biomarkers](/images/research/functional-depth-schematic.svg "Model schematic: functional depth bands distinguishing lung cancer subtypes from H&E-derived functional curves")
{: .align-center}

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Tsang, A.P., Ray, D., Lagisetty, K., Rao, A. <span style="color:blue">[Functional Depth Biomarkers Distinguish Lung Squamous Cell Carcinoma from Lung Adenocarcinoma](https://doi.org/10.21203/rs.3.rs-9347794/v1)</span> [Code](https://github.com/sagnikbhadury/Functional-Depth)</span>

## Magnetic Resonance Imaging (MRI)

<span style="text-align: justify">Volumetric radiologic imaging used to derive tumor shape and radiomic features for non-invasive characterization of tumor phenotype, which I combine with other modalities for multimodal survival modeling.</span>

![MRI tumor shape PCA](/images/research/lgg-shape-schematic.svg "Model schematic: statistical shape analysis of MRI-derived tumor contours in lower-grade glioma")
{: .align-center}

* <span style="text-align: justify">Statistical shape analysis (PCA-based) of MRI-derived tumor contours in lower-grade glioma. [Code](https://github.com/sagnikbhadury/Shape-Analysis-of-LGG)</span>

![RISM multimodal spike-and-slab survival model](/images/research/rism-schematic.svg "Model schematic: spike-and-slab selection over radiomic and other modality features for survival prediction")
{: .align-center}

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Mohammed, S., Kurtek, S., Rao, A. <span style="color:blue">RISM: Radiomic Feature Integration with Spike-and-Slab for Multimodal Survival Analysis</span> — spike-and-slab variable selection for integrating MRI-derived radiomic features with other modalities in survival models. (In preparation)</span>

## Multivariate Spatial Data

<span style="text-align: justify">Several outcomes measured over the same region, but often at different locations. I build multivariate Gaussian-process models that borrow strength across such misaligned outcomes, with shrinkage priors letting the data decide how much borrowing the design supports, and scalable meshed Gaussian processes for hundreds of thousands of observations.</span>

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span> <span style="color:blue">Design-Adaptive Borrowing Across Misaligned Outcomes in Bayesian Coregionalization Models</span> [Code](https://github.com/sagnikbhadury/meshedghs)</span>

## Language-Model Representations

<span style="text-align: justify">Internal activations of large language models and the sparse-autoencoder dictionaries trained on them. I treat interpretability and compression as high-dimensional selection problems: which features carry a behavior, whether a learned feature is used by the model, whether two dictionaries learned the same thing, and which model components can be removed with error control.</span>

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span> <span style="color:blue">Does the Route Matter? Functional Validation of Shared&ndash;Private Sparse Autoencoders</span></span>
* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span> <span style="color:blue">Comparing Sparse Autoencoder Dictionaries through Decoder Subspaces</span></span>
* <span style="text-align: justify">Ongoing: horseshoe-based selection of sparse-autoencoder features, and Bayesian structured pruning of large language models with false-discovery control.</span>

## Longitudinal Clinical & Multi-Omic Data

<span style="text-align: justify">Repeated biomarker and outcome measurements from clinical cohorts and trials, together with high-dimensional molecular layers measured on the same patients, including CyTOF, proteomics, transcriptomics, and cfDNA methylomics. At Penn Medicine I work on joint models linking biomarker trajectories to time-to-event outcomes, competing-risks frameworks for informative dropout, multi-omic phenotyping, and Bayesian clinical trial design.</span>

## Software

* <span style="text-align: justify"><span style="color:blue">[Spatial Methods Workbench]({{ "/spatial-methods-workbench/" | relative_url }})</span> (v0.3.0) — a browser application that runs exploratory through advanced Bayesian spatial analyses on uploaded data. [Application](https://sagnikbhadury.shinyapps.io/spatial-methods-workbench/) | [Zenodo](https://doi.org/10.5281/zenodo.21777139) | [GitHub](https://github.com/sagnikbhadury/SpatialMethodsWorkbench)</span>
* <span style="text-align: justify"><span style="color:blue">[ISPAT3D](https://cran.r-project.org/web/packages/ISPAT3D/)</span> (v0.3.1) — R package on CRAN for spatial conditional association networks in registered tumor volumes. [GitHub](https://github.com/sagnikbhadury/ISPAT-3D)</span>

---

<span style="text-align: justify; font-size: 0.85em; color: #7a8288;">Figures above are original schematic illustrations I created to summarize each project's modeling approach; they are conceptual diagrams, not reproductions of figures from the papers.</span>
