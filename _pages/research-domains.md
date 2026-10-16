---
layout: archive
title: "Research Domains & Methods"
permalink: /research-domains/
author_profile: true
description: "A guide to Bayesian graphical models, spatial tumor microenvironment analysis, spatial transcriptomics, computational pathology, radiogenomics, causal mediation, and functional data analysis."
---

This guide places my research in its broader statistical and biomedical context. It explains the domain language behind my projects and the connections among **Bayesian network science, spatial oncology, imaging genomics, and precision medicine**. The terms below describe the questions and methodological neighborhoods in which I work; they do not imply that every project addresses every concept.

<nav class="domain-index" aria-label="Research domain index">
  <a href="#bayesian-graphical-models-and-sparse-network-inference"><span>01</span> Bayesian graphical models</a>
  <a href="#spatial-statistics-for-the-tumor-microenvironment"><span>02</span> Spatial tumor microenvironment</a>
  <a href="#spatial-transcriptomics-and-cellcell-communication"><span>03</span> Spatial transcriptomics</a>
  <a href="#computational-pathology-and-multimodal-precision-oncology"><span>04</span> Multimodal precision oncology</a>
  <a href="#causal-inference-and-functional-biomarkers"><span>05</span> Causal &amp; functional methods</a>
  <a href="#cancer-disease-contexts"><span>06</span> Disease contexts</a>
</nav>

## Bayesian graphical models and sparse network inference

A **Gaussian graphical model (GGM)** represents multivariate dependence as a network. Variables form the nodes; a nonzero off-diagonal entry in the inverse covariance, or **precision matrix**, represents a conditional association after accounting for the remaining variables. In genomic applications, the resulting graph can summarize gene–gene, protein–protein, or cell-type dependence patterns that marginal correlations alone cannot distinguish.

The central challenge is high dimensionality: molecular studies often have many more candidate variables than independent samples. A scientifically plausible network is usually sparse, but deciding which edges are signal is difficult. My work approaches this through **Bayesian covariance selection**, **neighborhood regression**, and sparsity-inducing priors. The **horseshoe prior** is a global–local shrinkage prior: a global parameter regularizes the network overall while local parameters allow a small number of strong edges to escape shrinkage. **Spike-and-slab priors** instead mix concentrated and diffuse components, providing a direct probabilistic language for edge inclusion.

This domain also includes **joint graphical models** and **differential network analysis**. When several cancer subtypes, tissue regions, or patient groups are related, their networks can be estimated together: shared shrinkage borrows strength for common edges while retaining group-specific structure. A complementary direction is **graph-on-vector regression**, in which the response is itself a network and covariates explain how connectivity changes across subjects.

My work includes [fast Bayesian high-dimensional GGM estimation](https://arxiv.org/abs/2308.02713), Bayesian joint estimation of multiple graphs, and the [GOV graph-on-vector regression project](https://github.com/sagnikbhadury/GOV).

<div class="term-panel">
  <strong>Domain terminology</strong>
  <span>Bayesian Gaussian graphical model</span><span>precision matrix estimation</span><span>inverse covariance</span><span>conditional dependence</span><span>covariance selection</span><span>neighborhood selection</span><span>high-dimensional statistics</span><span>sparse network inference</span><span>graphical horseshoe</span><span>spike-and-slab prior</span><span>global–local shrinkage</span><span>joint graphical model</span><span>differential network</span><span>posterior uncertainty</span>
</div>

## Spatial statistics for the tumor microenvironment

A solid tumor is an organized ecosystem, not a well-mixed collection of cells. Cancer cells, immune cells, fibroblasts, endothelial cells, and extracellular structures form a spatially heterogeneous **tumor microenvironment (TME)**. Their locations create **cellular neighborhoods**, immune niches, invasive fronts, tumor–stroma interfaces, and patterns of immune exclusion. Spatial organization can therefore carry biological information beyond cell abundance alone.

**Multiplex immunofluorescence (mIF)**, imaging mass cytometry, and related **spatial proteomics** platforms measure many protein markers while preserving the position of each cell. These data support questions about cell-type co-occurrence, preferential proximity or avoidance, spatial gradients, and region-specific conditional dependence. The statistical complications include irregular sampling, multiple spatial scales, between-slide heterogeneity, edge effects, and the distinction between direct interactions and associations induced by shared tissue structure.

My research develops **spatially varying graphical models** in which network edges can change across tissue. Gaussian processes provide a flexible model for smooth spatial variation, while group horseshoe priors favor parsimonious interaction maps. The move from a two-dimensional tissue section to **3D multiplexed tissue imaging** matters because serial sections and reconstructed volumes can reveal interactions that a single plane misses.

Related projects include [ISPat](https://github.com/sagnikbhadury/ISPAT), [ISPat 3D](https://github.com/sagnikbhadury/ISPAT-3D), [GP-GHS](https://github.com/sagnikbhadury/GP-GHS), and spatial mediation analyses in the [Causal-Inference repository](https://github.com/sagnikbhadury/Causal-Inference).

<div class="term-panel">
  <strong>Domain terminology</strong>
  <span>tumor immune microenvironment</span><span>intratumoral heterogeneity</span><span>multiplex immunofluorescence</span><span>spatial proteomics</span><span>cellular neighborhoods</span><span>cell–cell interactions</span><span>spatial co-occurrence</span><span>immune niches</span><span>tumor–stroma interface</span><span>spatially varying coefficients</span><span>Gaussian process</span><span>3D tissue imaging</span><span>marked spatial data</span>
</div>

## Spatial transcriptomics and cell–cell communication

**Spatial transcriptomics** measures gene expression while retaining tissue coordinates. Depending on the platform, observations may represent multicellular spots, near-single-cell measurements, or subcellular transcript locations. Compared with dissociated single-cell RNA sequencing, the retained spatial context supports the localization of cell states and gene programs within histopathological structure.

Core computational tasks include identifying **spatially variable genes**, segmenting **spatial domains** or tissue niches, mapping or deconvolving cell types, and discovering **gene regulatory networks**. A second major goal is **cell–cell communication (CCC)** analysis. Here, ligand expression in a sender cell or region is related to receptor expression in a spatially proximate receiver. Spatial proximity does not by itself establish biochemical signaling, but it can reduce biologically implausible candidates and sharpen hypotheses about ligand–receptor interactions.

Modern spatial analyses increasingly combine gene expression, coordinates, H&amp;E morphology, protein measurements, and prior biological networks. Graph-based representations are natural because spots, cells, genes, and tissue regions can be represented as different node or edge types. In this context, terms such as **heterogeneous graph learning**, **functional edges**, **spatial multi-omics**, and **image–transcriptome integration** describe complementary ways to model biological relations rather than treating each modality as an isolated feature table.

My work in this area includes graph-based multimodal learning for lung cancer and collaborative work on [functional edges in spatially varying tumor-microenvironment graphs](https://doi.org/10.1038/s44387-026-00075-5).

<div class="term-panel">
  <strong>Domain terminology</strong>
  <span>spatially resolved transcriptomics</span><span>spatially variable genes</span><span>spatial domains</span><span>cell-type deconvolution</span><span>ligand–receptor interactions</span><span>cell–cell communication</span><span>gene regulatory networks</span><span>heterogeneous graphs</span><span>functional edges</span><span>spatial multi-omics</span><span>tissue architecture</span><span>image–transcriptome integration</span>
</div>

## Computational pathology and multimodal precision oncology

**Computational pathology** extracts quantitative information from digitized tissue. In H&amp;E **whole-slide images (WSIs)**, models may characterize nuclei, glands, tissue topology, morphology, and learned image embeddings. The term **pathomics** is often used for high-throughput quantitative features derived from pathology images. These representations can be associated with molecular subtype, gene expression, treatment response, or outcome.

Other scales contribute different views. **Radiomics** derives quantitative shape, intensity, and texture features from modalities such as MRI. **Radiogenomics**, also called imaging genomics in this context, connects radiologic phenotype with genomic or transcriptomic variation. Molecular assays describe pathways and cell states at a finer scale, while clinical variables and survival outcomes provide patient-level context.

**Multimodal data integration** aims to learn from these complementary views. Early fusion combines features before modeling; intermediate fusion learns a joint latent representation; late fusion combines modality-specific predictions. Statistical issues include unmatched scales, missing modalities, batch and site effects, high dimensionality, limited sample size, and the need for calibrated uncertainty. My work emphasizes structured sparsity and interpretable association alongside prediction, including **multimodal survival analysis**, mutual-information-based image–molecular association, and biomarker selection.

Related projects include [PathMI](https://github.com/sagnikbhadury/PathMI), which links histopathology embeddings with molecular subtype, and [RISM](https://github.com/sagnikbhadury/rism), which uses spike-and-slab selection to integrate radiomic and other features in survival models.

<div class="term-panel">
  <strong>Domain terminology</strong>
  <span>computational pathology</span><span>digital pathology</span><span>whole-slide imaging</span><span>H&amp;E histology</span><span>pathomics</span><span>radiomics</span><span>radiogenomics</span><span>imaging genomics</span><span>multimodal fusion</span><span>representation learning</span><span>survival analysis</span><span>multimodal biomarkers</span><span>precision oncology</span>
</div>

## Causal inference and functional biomarkers

Spatial and multimodal associations are not automatically causal. A **causal mediation analysis** asks whether part of an exposure–outcome relationship operates through an intermediate process. In spatial oncology, that mediator might summarize cell density, cell-type co-occurrence, or a tissue-neighborhood feature. Interpretation requires assumptions about confounding, temporal ordering, measurement, and model specification; **sensitivity analysis** evaluates how conclusions change when key assumptions are relaxed.

My functional-data work addresses a different structure: each observation may be a curve rather than a scalar. **Functional data analysis (FDA)** retains this shape information. **Statistical depth** ranks observations from central to peripheral, offering robust summaries, outlier detection, and depth-based classification. For H&amp;E-derived functional curves, depth bands and interpretable tree rules can expose which curve regions distinguish lung cancer subtypes, turning complex trajectories into candidate **functional biomarkers**.

I also study MRI-derived tumor contours through **statistical shape analysis**, using principal components to represent dominant modes of geometric variation in lower-grade glioma.

<div class="term-panel">
  <strong>Domain terminology</strong>
  <span>causal mediation analysis</span><span>direct and indirect effects</span><span>sensitivity analysis</span><span>spatial confounding</span><span>functional data analysis</span><span>functional depth</span><span>robust classification</span><span>functional biomarkers</span><span>statistical shape analysis</span><span>interpretable machine learning</span>
</div>

## Cancer disease contexts

My methods are motivated by problems across several solid tumors rather than a single organ site:

| Disease context | Domain questions represented in my work |
| --- | --- |
| Pancreatic cancer, including IPMN–PDAC progression | spatial cell organization, multiplexed imaging, tumor–stroma interactions |
| Non-small-cell lung cancer, including LUAD and LUSC | H&amp;E–transcriptome integration, subtype biomarkers, functional depth |
| Breast cancer, including triple-negative breast cancer | high-dimensional gene networks and Bayesian graphical models |
| Lower-grade glioma and glioblastoma | MRI tumor shape, radiomics, imaging genomics, microenvironmental interactions |
| Colorectal, prostate, and hepatocellular cancers | spatial heterogeneity, cell–cell interaction networks, multimodal biomarkers |

Across these diseases, the unifying aim is to turn complex dependence and spatial organization into **interpretable, uncertainty-aware statistical evidence**.
