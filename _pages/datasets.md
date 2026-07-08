---
layout: single
permalink: /datasets/
title: "Data & Projects"
author_profile: true
redirect_from:
  - /data/
---

My methods work is developed hand-in-hand with the complex biomedical data types below. Code and data associated with each project are released alongside the corresponding preprint or publication; see the [Publications]({{ "/publications/" | relative_url }}) page for full citations.

---

## Spatial Transcriptomics

<span style="text-align: justify">Spatially resolved gene expression profiles that preserve the tissue coordinates of each measurement, allowing transcriptomic activity to be studied jointly with tissue architecture. I use these data to model gene-gene and ligand-receptor interactions and to integrate transcriptomic regulatory signal with histomorphological features of the tumor microenvironment.</span>

![Spot-level gene expression graph](/images/research/spatial-transcriptomics-schematic.svg "Model schematic: functional edges over a spatial spot grid encode spatially varying gene relationships")
{: .align-center}

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span> et al. <span style="color:blue">Graph-Based Multi-Modal Learning for Integrating Histopathological and Transcriptomic Features in Lung Cancer</span> — graph-based fusion of transcriptomic and histopathological features in non-small cell lung cancer (LUAD-LUSC) to identify gene interactions and ligand-receptor interactions.</span>

![H&E and transcriptomic graph fusion](/images/research/he-fusion-schematic.svg "Model schematic: dual-branch graph fusion of H&E morphology and transcriptomic features")
{: .align-center}

* <span style="text-align: justify">Tsang, A., Krishnan, S., Kulkarni, R., <span style="color:red">Bhadury, S.</span>, Rao, A., et al. <span style="color:blue">[Encoding functional edges in graphs to model spatially varying relationships in the tumor microenvironment](https://doi.org/10.1038/s44387-026-00075-5)</span>, **npj Artificial Intelligence**.</span>

## 2D & 3D Multiplexed Immunofluorescence (mIF)

<span style="text-align: justify">High-plex single-cell imaging that records the spatial coordinates and marker intensities of many cell types on a single tissue section (2D) or across serial sections and volumes (3D). These data let me build spatial graphical models of the cell-cell interaction networks that make up the tumor microenvironment, and to test whether those interaction patterns differ by disease state.</span>

![ISPAT spatial graphical model](/images/research/ispat-schematic.svg "Model schematic: spatial graphical model over multiplexed immunofluorescence cell-type intensities")
{: .align-center}

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span> et al. <span style="color:blue">[ISPAT: Informed Spatially Aware Patterns for Multiplexed Immunofluorescence data](https://www.nature.com/articles/s41598-026-35341-8)</span>, **Nature Scientific Reports** — Bayesian spatial mixed-effects modeling (Poisson & Gaussian) of cell-type intensities across tissue slides. [Code](https://github.com/sagnikbhadury/ISPAT)</span>

![ISPAT-3D volumetric network](/images/research/ispat3d-schematic.svg "Model schematic: volumetric spatial network estimation across serial tissue sections")
{: .align-center}

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Rao, A. <span style="color:blue">[ISPAT 3D: Spatially Varying Conditional Volumetric Network Estimation for 3D Tumor Imaging](https://doi.org/10.64898/2026.04.16.719017)</span> — extends spatial network estimation to volumetric, 3D multiplexed cancer imaging. [Code](https://github.com/sagnikbhadury/ISPAT-3D)</span>
* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Gaskins, J., Rao, A. <span style="color:blue">[Spatially Varying Graphical Models for Cell-Cell Interaction Networks in Multiplexed Tissue Imaging](https://doi.org/10.64898/2026.04.01.715977)</span></span>

![GP-GHS spatially varying shrinkage](/images/research/gp-ghs-schematic.svg "Model schematic: Gaussian Process group horseshoe shrinkage of interaction strength across space")
{: .align-center}

* <span style="text-align: justify"><span style="color:blue">GP-GHS: Gaussian Process Group Horseshoe for spatial Cell-Cell Interactions in Tissue Images</span> — group horseshoe shrinkage priors combined with Gaussian Process spatial structure for interaction network estimation. [Code](https://github.com/sagnikbhadury/GP-GHS)</span>

![Spatial mediation diagram](/images/research/mediation-schematic.svg "Model schematic: mediation analysis of spatial cell-type co-occurrence between disease group and tissue outcome")
{: .align-center}

* <span style="text-align: justify">Mediation and sensitivity analyses testing whether cell-type density and spatial co-occurrence patterns mediate the relationship between disease group and tissue-level outcomes. [Code](https://github.com/sagnikbhadury/Causal-Inference)</span>

## Magnetic Resonance Imaging (MRI)

<span style="text-align: justify">Volumetric radiologic imaging used to derive tumor shape and radiomic features for non-invasive characterization of tumor phenotype, which I combine with other modalities for multimodal survival modeling.</span>

![MRI tumor shape PCA](/images/research/lgg-shape-schematic.svg "Model schematic: statistical shape analysis of MRI-derived tumor contours in lower-grade glioma")
{: .align-center}

* <span style="text-align: justify">Statistical shape analysis (PCA-based) of MRI-derived tumor contours in lower-grade glioma. [Code](https://github.com/sagnikbhadury/Shape-Analysis-of-LGG)</span>

![RISM multimodal spike-and-slab survival model](/images/research/rism-schematic.svg "Model schematic: spike-and-slab selection over radiomic and other modality features for survival prediction")
{: .align-center}

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span> et al. <span style="color:blue">RISM: Radiomic feature Integration with Spike-and-slab for Multimodal survival analysis</span> — spike-and-slab variable selection for integrating MRI-derived radiomic features with other modalities in survival models. [Code](https://github.com/sagnikbhadury/rism)</span>

## H&E Imaging

<span style="text-align: justify">Hematoxylin and eosin stained whole-slide images capturing tissue and cellular morphology. I use these images to extract histomorphological features and integrate them with molecular and spatial data for a more complete picture of the tumor microenvironment.</span>

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span> et al. <span style="color:blue">Graph-Based Multi-Modal Learning for Integrating Histopathological and Transcriptomic Features in Lung Cancer</span> — see the graph fusion figure above.</span>

![Functional depth biomarkers](/images/research/functional-depth-schematic.svg "Model schematic: functional depth bands distinguishing lung cancer subtypes from H&E-derived functional curves")
{: .align-center}

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span> et al. <span style="color:blue">Functional Depth biomarkers Distinguish Lung Cancer Subtypes</span></span>

---

<span style="text-align: justify; font-size: 0.85em; color: #7a8288;">Figures above are original schematic illustrations I created to summarize each project's modeling approach; they are conceptual diagrams, not reproductions of figures from the papers.</span>

