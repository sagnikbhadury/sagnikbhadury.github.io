---
layout: archive
title: "Research Domains & Methods"
permalink: /research-domains/
author_profile: true
description: "A guide to Bayesian graphical models, spatial tumor microenvironment analysis, Gaussian processes, spatial transcriptomics and compositional data, computational pathology, causal mediation, Bayesian methods for AI interpretability, and clinical trials and longitudinal data."
---

This guide places my research in its broader statistical and biomedical context. It follows the eight directions on the [Research]({{ '/research/' | relative_url }}) page and explains the domain language behind each, along with the connections among **Bayesian network science, spatial statistics, imaging genomics, AI interpretability, and clinical research**. The terms below describe the questions and methodological neighborhoods in which I work; they do not imply that every project addresses every concept.

<nav class="domain-index" aria-label="Research domain index">
  <a href="#bayesian-graphical-models-and-sparse-network-inference"><span>01</span> Bayesian graphical models</a>
  <a href="#spatial-statistics-for-the-tumor-microenvironment"><span>02</span> Spatial tumor microenvironment</a>
  <a href="#gaussian-processes-and-spatial-point-patterns"><span>03</span> Gaussian processes &amp; point patterns</a>
  <a href="#spatial-transcriptomics-and-compositional-data"><span>04</span> Spatial transcriptomics &amp; compositional data</a>
  <a href="#computational-pathology-and-multimodal-precision-oncology"><span>05</span> Multimodal precision oncology</a>
  <a href="#causal-inference-and-functional-biomarkers"><span>06</span> Causal &amp; functional methods</a>
  <a href="#bayesian-methods-for-ai-and-interpretability"><span>07</span> Bayesian methods for AI</a>
  <a href="#clinical-trials-and-longitudinal-biomedical-data"><span>08</span> Clinical trials &amp; longitudinal data</a>
  <a href="#disease-and-application-contexts"><span>09</span> Disease &amp; application contexts</a>
</nav>

## Bayesian graphical models and sparse network inference

A **Gaussian graphical model (GGM)** represents multivariate dependence as a network. Variables form the nodes; a nonzero off-diagonal entry in the inverse covariance, or **precision matrix**, represents a conditional association after accounting for the remaining variables. In genomic applications, the resulting graph can summarize gene–gene, protein–protein, or cell-type dependence patterns that marginal correlations alone cannot distinguish.

The central challenge is high dimensionality: molecular studies often have many more candidate variables than independent samples. A scientifically plausible network is usually sparse, but deciding which edges are signal is difficult. My work approaches this through **Bayesian covariance selection**, **neighborhood regression**, and sparsity-inducing priors. The **horseshoe prior** is a global–local shrinkage prior: a global parameter regularizes the network overall while local parameters allow a small number of strong edges to escape shrinkage. **Spike-and-slab priors** instead mix concentrated and diffuse components, providing a direct probabilistic language for edge inclusion.

This domain also includes **joint graphical models** and **differential network analysis**. When several cancer subtypes, tissue regions, or patient groups are related, their networks can be estimated together: shared shrinkage borrows strength for common edges while retaining group-specific structure. A complementary direction is **graph-on-vector regression**, in which a network is the predictor: a latent-space model places each node in a low-dimensional space, and a Gaussian-process regression with spike-and-slab selection identifies which nodes drive a scalar response.

My work includes [fast Bayesian high-dimensional GGM estimation](https://arxiv.org/abs/2308.02713), Bayesian joint estimation of multiple graphs, and the [GOV graph-on-vector regression package](https://github.com/sagnikbhadury/GOV).

<div class="term-panel">
  <strong>Domain terminology</strong>
  <span>Bayesian Gaussian graphical model</span><span>precision matrix estimation</span><span>inverse covariance</span><span>conditional dependence</span><span>covariance selection</span><span>neighborhood selection</span><span>high-dimensional statistics</span><span>sparse network inference</span><span>graphical horseshoe</span><span>spike-and-slab prior</span><span>global–local shrinkage</span><span>joint graphical model</span><span>differential network</span><span>network-valued predictors</span><span>posterior uncertainty</span>
</div>

## Spatial statistics for the tumor microenvironment

A solid tumor is an organized ecosystem, not a well-mixed collection of cells. Cancer cells, immune cells, fibroblasts, endothelial cells, and extracellular structures form a spatially heterogeneous **tumor microenvironment (TME)**. Their locations create **cellular neighborhoods**, immune niches, invasive fronts, tumor–stroma interfaces, and patterns of immune exclusion. Spatial organization can therefore carry biological information beyond cell abundance alone.

**Multiplex immunofluorescence (mIF)**, imaging mass cytometry, and related **spatial proteomics** platforms measure many protein markers while preserving the position of each cell. These data support questions about cell-type co-occurrence, preferential proximity or avoidance, spatial gradients, and region-specific conditional dependence. The statistical complications include irregular sampling, multiple spatial scales, between-slide heterogeneity, edge effects, and the distinction between direct interactions and associations induced by shared tissue structure.

My research develops **spatially varying graphical models** in which network edges can change across tissue. Gaussian processes provide a flexible model for smooth spatial variation, while group horseshoe priors favor parsimonious interaction maps. The move from a two-dimensional tissue section to **3D multiplexed tissue imaging** matters because serial sections and reconstructed volumes can reveal interactions that a single plane misses.

Related projects include [ISPat](https://github.com/sagnikbhadury/ISPAT), [ISPat 3D](https://github.com/sagnikbhadury/ISPAT-3D) (R package [ISPAT3D on CRAN](https://cran.r-project.org/web/packages/ISPAT3D/)), and [GP-GHS](https://github.com/sagnikbhadury/GP-GHS).

<div class="term-panel">
  <strong>Domain terminology</strong>
  <span>tumor immune microenvironment</span><span>intratumoral heterogeneity</span><span>multiplex immunofluorescence</span><span>spatial proteomics</span><span>cellular neighborhoods</span><span>cell–cell interactions</span><span>spatial co-occurrence</span><span>immune niches</span><span>tumor–stroma interface</span><span>spatially varying coefficients</span><span>Gaussian process</span><span>3D tissue imaging</span><span>marked spatial data</span>
</div>

## Gaussian processes and spatial point patterns

A **Gaussian process (GP)** is a prior over functions: it says how similar the values at two locations should be as a function of the distance between them. GPs are the standard tool for smooth spatial surfaces, but they scale poorly with the number of locations. **Nearest-neighbor and meshed GPs** restore scalability by letting each location depend only on a small, structured set of neighbors.

Many spatial studies measure several outcomes, and rarely at the same places. In a **linear model of coregionalization (LMC)**, several outcome surfaces are built from a shared set of latent GPs, so an outcome measured densely can inform one measured sparsely. With **misaligned outcomes** the key question becomes how much to borrow: too little wastes shared structure, too much transfers signal that is not there. My work places grouped horseshoe priors on the coregionalization weights so that the data decide, outcome by outcome, how much borrowing the design supports.

A second line treats the cell locations themselves as the data. A **spatial point pattern** records where events occur; **point-process models** describe their intensity and interaction, such as clustering, regularity, or attraction between cell types. Bayesian inference for point patterns gives uncertainty-aware estimates of these spatial relationships.

Related projects include the [meshedghs package](https://github.com/sagnikbhadury/meshedghs) for design-adaptive borrowing across misaligned outcomes.

<div class="term-panel">
  <strong>Domain terminology</strong>
  <span>Gaussian process regression</span><span>nearest-neighbor GP</span><span>meshed GP</span><span>linear model of coregionalization</span><span>multivariate spatial models</span><span>misaligned data</span><span>borrowing strength</span><span>grouped horseshoe</span><span>spatial point patterns</span><span>point-process intensity</span><span>spatial interaction</span>
</div>

## Spatial transcriptomics and compositional data

**Spatial transcriptomics** measures gene expression while retaining tissue coordinates. Depending on the platform, observations may represent multicellular spots, near-single-cell measurements, or subcellular transcript locations. Compared with dissociated single-cell RNA sequencing, the retained spatial context supports the localization of cell states and gene programs within histopathological structure.

Core computational tasks include identifying **spatially variable genes**, segmenting **spatial domains** or tissue niches, mapping or deconvolving cell types, and discovering **gene regulatory networks**. A second major goal is **cell–cell communication (CCC)** analysis, which relates ligand expression in a sender cell or region to receptor expression in a spatially proximate receiver. Spatial proximity does not by itself establish biochemical signaling, but it can reduce biologically implausible candidates and sharpen hypotheses about ligand–receptor interactions.

Spot-level data raise a specific statistical problem. Cell-type proportions estimated at each spot are **compositional**: they are non-negative, sum to one, often contain exact zeros, and are spatially dependent. Standard log-ratio methods break down at zeros, and ignoring the sum-to-one constraint distorts every association. My work develops **regression models for spatial compositional data** that respect the simplex, handle zeros directly, and account for spatial dependence. A related project uses horseshoe-shrunk **image-basis regression** to link H&amp;E tissue morphology to gene expression measured on the same section.

Collaborative work in this area includes [functional edges in spatially varying tumor-microenvironment graphs](https://doi.org/10.1038/s44387-026-00075-5).

<div class="term-panel">
  <strong>Domain terminology</strong>
  <span>spatially resolved transcriptomics</span><span>spatially variable genes</span><span>spatial domains</span><span>cell-type deconvolution</span><span>compositional data</span><span>simplex regression</span><span>zeros in compositions</span><span>ligand–receptor interactions</span><span>cell–cell communication</span><span>gene regulatory networks</span><span>functional edges</span><span>morphology–expression association</span>
</div>

## Computational pathology and multimodal precision oncology

**Computational pathology** extracts quantitative information from digitized tissue. In H&amp;E **whole-slide images (WSIs)**, models may characterize nuclei, glands, tissue topology, morphology, and learned image embeddings. The term **pathomics** is often used for high-throughput quantitative features derived from pathology images. These representations can be associated with molecular subtype, gene expression, treatment response, or outcome.

**Pathology foundation models** are large networks pretrained on millions of tissue tiles, whose embeddings are reused for many downstream tasks. A natural question is how much molecular information those embeddings actually carry. **Mutual information** answers it on an interpretable scale; my work estimates it with Bayesian shrinkage and calibrates it against permutation nulls, so that different foundation models and molecular targets can be compared on the same footing.

Other scales contribute different views. **Radiomics** derives quantitative shape, intensity, and texture features from modalities such as MRI. **Radiogenomics**, also called imaging genomics in this context, connects radiologic phenotype with genomic or transcriptomic variation. Molecular assays describe pathways and cell states at a finer scale, while clinical variables and survival outcomes provide patient-level context.

**Multimodal data integration** aims to learn from these complementary views. Early fusion combines features before modeling; intermediate fusion learns a joint latent representation; late fusion combines modality-specific predictions. Graph-based representations are natural here, because cells, genes, and tissue regions can be represented as different node or edge types. Statistical issues include unmatched scales, missing modalities, batch and site effects, high dimensionality, limited sample size, and the need for calibrated uncertainty. My work emphasizes structured sparsity and interpretable association alongside prediction, including graph-based integration of histopathology and transcriptomics in lung adenocarcinoma, **multimodal survival analysis** with spike-and-slab selection of radiomic features, and biomarker selection.

<div class="term-panel">
  <strong>Domain terminology</strong>
  <span>computational pathology</span><span>digital pathology</span><span>whole-slide imaging</span><span>H&amp;E histology</span><span>pathomics</span><span>pathology foundation models</span><span>mutual information</span><span>radiomics</span><span>radiogenomics</span><span>imaging genomics</span><span>multimodal fusion</span><span>heterogeneous graphs</span><span>survival analysis</span><span>precision oncology</span>
</div>

## Causal inference and functional biomarkers

Spatial and multimodal associations are not automatically causal. A **causal mediation analysis** asks whether part of an exposure–outcome relationship operates through an intermediate process. In spatial oncology, a recurring example is **compositional confounding**: two cell types can look spatially close simply because a tissue contains more of both, not because they are organized together. Mediation separates the part of a spatial association explained by tissue composition from the part that reflects genuine spatial organization. Interpretation requires assumptions about confounding, temporal ordering, measurement, and model specification; **sensitivity analysis** evaluates how conclusions change when key assumptions are relaxed.

My functional-data work addresses a different structure: each observation may be a curve rather than a scalar. **Functional data analysis (FDA)** retains this shape information. **Statistical depth** ranks observations from central to peripheral, offering robust summaries, outlier detection, and depth-based classification. For H&amp;E-derived functional curves, depth bands and interpretable tree rules can expose which curve regions distinguish lung cancer subtypes, turning complex trajectories into candidate **functional biomarkers**.

I also study MRI-derived tumor contours through **statistical shape analysis**, using principal components to represent dominant modes of geometric variation in lower-grade glioma.

Related projects include spatial mediation analyses in the [Causal-Inference repository](https://github.com/sagnikbhadury/Causal-Inference), [Functional-Depth](https://github.com/sagnikbhadury/Functional-Depth), and [Shape-Analysis-of-LGG](https://github.com/sagnikbhadury/Shape-Analysis-of-LGG).

<div class="term-panel">
  <strong>Domain terminology</strong>
  <span>causal mediation analysis</span><span>direct and indirect effects</span><span>compositional confounding</span><span>sensitivity analysis</span><span>spatial confounding</span><span>functional data analysis</span><span>functional depth</span><span>robust classification</span><span>functional biomarkers</span><span>statistical shape analysis</span><span>interpretable machine learning</span>
</div>

## Bayesian methods for AI and interpretability

Large language models compute with internal representations that are hard to read directly. **Mechanistic interpretability** tries to decompose those representations into human-meaningful pieces. A **sparse autoencoder (SAE)** learns a large dictionary of directions, often called features, so that each internal activation is approximated by a sparse combination of them. The open statistical questions are familiar ones in new clothing: which of thousands of features actually drive a behavior, whether a feature the dictionary learned is one the model uses, and whether two dictionaries, or two models, have learned the same thing.

These are **high-dimensional variable selection** and **model comparison** problems. My work brings global–local shrinkage priors, posterior uncertainty, and error-rate control to them. Horseshoe priors select the small set of SAE features associated with a behavior while reporting how certain each selection is. **Shared–private dictionaries** separate features common to two models from features specific to one, and functional tests ask whether intervening on a feature changes the model's output as predicted. **Decoder subspaces** compare dictionaries at the level of the spaces they span rather than feature by feature, since individual features need not match one-to-one across training runs.

The same tools apply to **model compression**. Deciding which attention heads, neurons, or blocks of a large language model can be removed is a selection problem with a cost for false discoveries: removing a component that mattered degrades the model. Bayesian structured pruning frames it that way, with **false-discovery control** over the components selected for removal.

<div class="term-panel">
  <strong>Domain terminology</strong>
  <span>mechanistic interpretability</span><span>sparse autoencoders</span><span>dictionary learning</span><span>feature selection</span><span>causal interventions</span><span>model diffing</span><span>decoder subspaces</span><span>LLM pruning</span><span>structured sparsity</span><span>false-discovery control</span><span>global–local shrinkage</span><span>posterior uncertainty</span>
</div>

## Clinical trials and longitudinal biomedical data

Clinical studies follow patients over time, so their data are **longitudinal**: repeated biomarker measurements, intermittent clinical assessments, and outcomes that arrive as events. Observations within a patient are correlated, visits are irregular, and follow-up often ends for reasons related to the outcome itself.

**Mixed-effects models** describe how each patient's biomarker trajectory departs from the population trend. **Joint models** link those trajectories to **time-to-event outcomes**, so that the biomarker and the event are analyzed together rather than one being treated as a fixed covariate. When death or dropout cuts follow-up short, the missingness is **informative**, and **competing-risks** frameworks are needed to avoid estimating trajectories in patients who could no longer have been measured.

Modern studies add high-dimensional molecular layers measured on the same patients: CyTOF, proteomics, transcriptomics, and cfDNA methylomics. Integrating them calls for **penalized regression**, **unsupervised clustering**, and **multi-omic feature selection** to identify biologically coherent patient subgroups, a task often called **biomedical phenotyping**. **Bayesian clinical trial design** uses prior information and accumulating data to choose sample sizes, decision rules, and adaptations with known operating characteristics.

<div class="term-panel">
  <strong>Domain terminology</strong>
  <span>Bayesian trial design</span><span>operating characteristics</span><span>longitudinal data</span><span>mixed-effects models</span><span>joint models</span><span>time-to-event outcomes</span><span>competing risks</span><span>informative missingness</span><span>multi-omic integration</span><span>penalized regression</span><span>biomedical phenotyping</span>
</div>

## Disease and application contexts

My methods are motivated by problems across several solid tumors, clinical cohorts, and modern AI systems rather than a single application:

| Context | Domain questions represented in my work |
| --- | --- |
| Pancreatic cancer, including IPMN–PDAC progression | spatial cell organization, multiplexed imaging, compositional confounding, tumor–stroma interactions |
| Colorectal cancer | spatial proximity and coordination, compositional data, perineural niche |
| Non-small-cell lung cancer, including LUAD and LUSC | H&amp;E–transcriptome integration, subtype biomarkers, functional depth |
| Breast cancer, including triple-negative breast cancer | high-dimensional gene networks and Bayesian graphical models |
| Lower-grade glioma and glioblastoma | MRI tumor shape, radiomics, imaging genomics, microenvironmental interactions |
| Prostate and hepatocellular cancers | spatial heterogeneity, cell–cell interaction networks, molecular signal in pathology foundation models |
| Clinical and molecular cohorts | Bayesian trial design, longitudinal biomarkers, joint models, multi-omic phenotyping |
| Large language models | sparse-autoencoder interpretability, model comparison, structured pruning |

Across these contexts, the unifying aim is to turn complex dependence and structure into **interpretable, uncertainty-aware statistical evidence**.
