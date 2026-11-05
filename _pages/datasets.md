---
layout: single
permalink: /datasets/
title: "Data & Projects"
author_profile: true
description: "Research projects, publications and open-source code for gene expression networks, spatial transcriptomics, multiplex immunofluorescence, H&E computational pathology, MRI radiomics, multivariate spatial data, language-model interpretability, and longitudinal clinical and multi-omic data."
redirect_from:
  - /data/
---

Each method below was developed for a particular data type, and the projects are grouped by the data they analyze. The [Research]({{ "/research/" | relative_url }}) page groups the same work by methodological direction. Code and data for each project are released with the corresponding preprint or publication (see [Publications]({{ "/publications/" | relative_url }}) for full citations).

---

## Gene Expression & High-Dimensional Networks

<span style="text-align: justify">Gene expression studies measure thousands of genes on a few hundred patients, and the network of conditional dependence among those genes is high-dimensional and sparse. I estimate such networks through Bayesian regressions fitted at each node, which can run in parallel across genes. This work underlies the spatial and multi-modal graphical models below.</span>

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Mitra, R., Gaskins, J. <span style="color:blue">[Fast Bayesian High-Dimensional Gaussian Graphical Model Estimation](https://arxiv.org/abs/2308.02713)</span>. Horseshoe regression at each node, followed by step-up model selection, with the neighborhoods combined into a graph. [R package](https://github.com/sagnikbhadury/GGMsubho)</span>

  <figure class="align-center" style="max-width: 760px; margin: 0.75rem auto 1.25rem;">
    <img src="{{ '/images/research/subho-pipeline.gif' | relative_url }}" alt="Animated walkthrough of the Graphical-SUBHO pipeline: data matrix, node-wise horseshoe regression, ranking of the predictors, step-up model selection, combining neighbourhoods with the AND rule, and the estimated network, followed by the seven figures of the manuscript" loading="lazy">
    <figcaption>Graphical-SUBHO pipeline and results: node-wise horseshoe regression, ranking of the predictors, step-up model selection and the AND rule, illustrated on simulated data, followed by the simulation comparisons and the METABRIC triple-negative breast cancer gene networks.</figcaption>
  </figure>

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Mitra, R., Gaskins, J. <span style="color:blue">Bayesian Joint Estimation of Multiple Graphs through Shared Shrinkage</span> (in preparation)</span>
* <span style="text-align: justify"> <span style="color:red">Bhadury, Sagnik K.</span> <span style="color:blue"> [Bayesian Methods for Graphical Models with Neighborhood Selection](https://ir.library.louisville.edu/etd/4001/)</span>, PhD Dissertation Thesis Advisors: **Gaskins, Jeremy T. and Mitra, Ritendranath** </span>

## Spatial Transcriptomics

<span style="text-align: justify">Spatial transcriptomics records gene expression together with the tissue coordinates of each measurement, so expression can be studied jointly with tissue architecture. I use these data to model gene–gene and ligand–receptor interactions, to analyze spot-level cell-type proportions as spatial compositional data, and to link tissue morphology to gene expression measured on the same section.</span>

* <span style="text-align: justify">Tsang, A., Krishnan, S., Kulkarni, R., <span style="color:red">Bhadury, S.</span>, Rao, A., et al. <span style="color:blue">[Encoding functional edges in graphs to model spatially varying relationships in the tumor microenvironment](https://doi.org/10.1038/s44387-026-00075-5)</span>, **npj Artificial Intelligence**.</span>
* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Schwob, M., Datta, J. <span style="color:blue">Spatial Active-Set Ray Regression for Compositional Data: Methodology, Validation, and Applications in Spatial Transcriptomics and Community Ecology</span>. Regression for spot-level cell-type proportions that respects the sum-to-one constraint, handles zeros directly, and accounts for spatial dependence. (In preparation)</span>
* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Rao, A. <span style="color:blue">SHIRE: Spatial Horseshoe Image-Basis Regression for Morphology and Gene Expression Associations in Spatial Transcriptomics</span>. Horseshoe-shrunk regression that links H&amp;E morphology to single-cell gene expression. (In preparation)</span>

## 2D & 3D Multiplexed Immunofluorescence (mIF)

<span style="text-align: justify">Multiplexed immunofluorescence records the spatial coordinates and marker intensities of many cell types on a single tissue section (2D) or across registered serial sections (3D). With these data I build spatial graphical models of the cell–cell interaction networks in the tumor microenvironment, test whether the interaction patterns differ by disease state, and separate spatial organization from differences in tissue composition.</span>

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span> et al. <span style="color:blue">[ISPat: Informed Spatially Aware Patterns for Multiplexed Immunofluorescence data](https://www.nature.com/articles/s41598-026-35341-8)</span>, **Nature Scientific Reports**. Bayesian spatial modeling of cell-type intensities that recovers a shared interaction network and one network per tumor-density region. [Code](https://github.com/sagnikbhadury/ISPAT)</span>

  <figure class="align-center" style="max-width: 760px; margin: 0.75rem auto 1.25rem;">
    <img src="{{ '/images/research/ispat-pipeline.gif' | relative_url }}" alt="Animated walkthrough of the ISPat pipeline: stained mIF image, cell point patterns, domain-informed network, tumor sub-regions, spatial intensities, shared and region-specific interaction networks, simulation results and the PDAC versus IPMN comparison" loading="lazy">
    <figcaption>ISPat pipeline and analyses: from the stained multiplexed image to shared and tumor-region-specific interaction networks, simulation checks, and the PDAC versus IPMN comparison across tumor-density areas.</figcaption>
  </figure>


* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Rao, A. <span style="color:blue">[Estimating conditional cell population associations across tumor density trajectory in three dimensional tissue images (ISPat 3D)](https://www.nature.com/articles/s41598-026-73151-0)</span>, **Nature Scientific Reports**. Extends spatial network estimation to volumetric, 3D multiplexed cancer imaging. [Code](https://github.com/sagnikbhadury/ISPAT-3D) | [R package on CRAN](https://cran.r-project.org/web/packages/ISPAT3D/)</span>

  <figure class="align-center" style="max-width: 760px; margin: 0.75rem auto 1.25rem;">
    <img src="{{ '/images/research/ispat3d-pipeline.gif' | relative_url }}" alt="Animated walkthrough of the ISPat 3D pipeline on a registered colorectal cancer CyCIF volume: why 3D, the volumetric neighborhoods, tumor-density trajectory, and the conditional association networks along it" loading="lazy">
    <figcaption>ISPat 3D on a registered colorectal cancer CyCIF volume: single-plane versus volumetric neighborhoods, the tumor-density trajectory, and how conditional cell population associations change along it.</figcaption>
  </figure>


* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Gaskins, J., Rao, A. <span style="color:blue">[Spatially Varying Graphical Models for Cell-Cell Interaction Networks in Multiplexed Tissue Imaging](https://doi.org/10.64898/2026.04.01.715977)</span>. Group horseshoe shrinkage priors combined with Gaussian-process spatial structure (GP-GHS) for interaction network estimation. [Code](https://github.com/sagnikbhadury/GP-GHS)</span>

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Frankel, T.L., Rao, A. <span style="color:blue">[Cellular Proximity and Conditional Coordination in the Colorectal and Pancreatic Tumor Microenvironment: A Patient-Level Analysis of Multiplexed Imaging](https://doi.org/10.64898/2026.10.08.757632)</span></span>
* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Frankel, T., Rao, A. <span style="color:blue">Resolving Compositional Confounding in Spatial Proximity Analysis through Mediation in Tumor Microenvironments</span> (in preparation)</span>
* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Frankel, T., Rao, A. <span style="color:blue">Causal Mediation Decomposes Pancreatic Cancer Spatial Diversity into Compositional and Organizational Pathways</span> (in preparation)</span>
* <span style="text-align: justify">Mediation and sensitivity analyses that test whether cell-type density and spatial co-occurrence patterns mediate the relationship between disease group and tissue-level outcomes. [Code](https://github.com/sagnikbhadury/Causal-Inference)</span>

## H&E Imaging & Computational Pathology

<span style="text-align: justify">Hematoxylin and eosin (H&amp;E) whole-slide images record tissue and cellular morphology. I use them to extract histomorphological features, to relate those features to molecular and spatial data, and to measure the molecular information carried by the embeddings of pathology foundation models.</span>

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Tsang, A., Ray, D., Lagisetty, K., Kundu, S., Rao, A. <span style="color:blue">Graph-on-Vector Association Modeling of Histopathological and Transcriptomic Features in Lung Adenocarcinoma</span>, **npj Artificial Intelligence** (accepted). Graph-on-vector regression of pathway, kinase and transcription-factor activities on participant-specific histomorphological phenotype graphs in TCGA-LUAD, with node-level Bayesian variable selection. [Code](https://github.com/sagnikbhadury/GOV)</span>

  <figure class="align-center" style="max-width: 760px; margin: 0.75rem auto 1.25rem;">
    <img src="{{ '/images/research/gov-pipeline.gif' | relative_url }}" alt="Animated walkthrough of the graph-on-vector pipeline in TCGA lung adenocarcinoma: survival-rank cohort split, H&amp;E morphology, graph construction, molecular activity scores, graph-on-vector regression, and pathway, kinase and transcription-factor results" loading="lazy">
    <figcaption>Graph-on-vector association modeling in TCGA-LUAD: survival-rank cohort split, H&amp;E-derived morphology graphs, molecular activity scores, the graph-on-vector regression, and pathway, kinase and transcription-factor results.</figcaption>
  </figure>

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Kulkarni, R., Rao, A. <span style="color:blue">Quantifying Biological Signal in Pathology Foundation Models through Bayesian Mutual Information Estimation</span>. Compares pathology foundation models by the molecular information their tile embeddings carry, against permutation nulls. (In preparation)</span>

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Tsang, A.P., Ray, D., Lagisetty, K., Rao, A. <span style="color:blue">[Functional Depth Biomarkers Distinguish Lung Squamous Cell Carcinoma from Lung Adenocarcinoma](https://doi.org/10.21203/rs.3.rs-9347794/v1)</span> [Code](https://github.com/sagnikbhadury/Functional-Depth)</span>

## Magnetic Resonance Imaging (MRI)

<span style="text-align: justify">MRI provides tumor shape and radiomic features that characterize tumor phenotype without a biopsy. I combine these features with other modalities in multimodal survival models.</span>

* <span style="text-align: justify">Statistical shape analysis (PCA-based) of MRI-derived tumor contours in lower-grade glioma. [Code](https://github.com/sagnikbhadury/Shape-Analysis-of-LGG)</span>

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span>, Mohammed, S., Kurtek, S., Rao, A. <span style="color:blue">RISM: Radiomic Feature Integration with Spike-and-Slab for Multimodal Survival Analysis</span>. Spike-and-slab variable selection for integrating MRI-derived radiomic features with other modalities in survival models. (In preparation)</span>

## Multivariate Spatial Data

<span style="text-align: justify">Spatial studies often measure several outcomes over the same region at different locations. I build multivariate Gaussian-process models that borrow strength across such misaligned outcomes. Shrinkage priors let the data decide how much borrowing the design supports, and meshed Gaussian processes keep the models tractable for hundreds of thousands of observations.</span>

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span> <span style="color:blue">Design-Adaptive Borrowing Across Misaligned Outcomes in Bayesian Coregionalization Models</span> [Code](https://github.com/sagnikbhadury/meshedghs)</span>

## Language-Model Representations

<span style="text-align: justify">The data are internal activations of large language models and the sparse-autoencoder dictionaries trained on them. I treat interpretability and compression as high-dimensional selection problems: which features carry a behavior, whether a learned feature is used by the model, whether two dictionaries learned the same thing, and which model components can be removed with error control.</span>

* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span> <span style="color:blue">Does the Route Matter? Functional Validation of Shared&ndash;Private Sparse Autoencoders</span></span>
* <span style="text-align: justify"><span style="color:red">Bhadury, S.</span> <span style="color:blue">Comparing Sparse Autoencoder Dictionaries through Decoder Subspaces</span></span>
* <span style="text-align: justify">Ongoing: horseshoe-based selection of sparse-autoencoder features, and Bayesian structured pruning of large language models with false-discovery control.</span>

## Longitudinal Clinical & Multi-Omic Data

<span style="text-align: justify">Clinical cohorts and trials provide repeated biomarker and outcome measurements, together with high-dimensional molecular layers measured on the same patients (CyTOF, proteomics, transcriptomics, and cfDNA methylomics). At Penn Medicine I work on joint models that link biomarker trajectories to time-to-event outcomes, competing-risks frameworks for informative dropout, multi-omic phenotyping, and Bayesian clinical trial design.</span>

## Glioblastoma Biology (Collaborative)

<span style="text-align: justify">Collaborative studies of the glioblastoma microenvironment, tumor cell states and treatment resistance.</span>

* <span style="text-align: justify">Wahl, D., Sravya, P., Altay, L., Do, K., Freeman, J., Gokul, A., ..., <span style="color:red">Bhadury, S.</span>, et al. <span style="color:blue">[Microenvironment-Derived Acetylated Amino Acids Promote Glioblastoma Treatment Resistance](https://doi.org/10.21203/rs.3.rs-10976328/v1)</span></span>
* <span style="text-align: justify"> Palavalasa, S., <span style="color:red">Bhadury, S.</span>, et al.  <span style="color:blue"> Immune-microenvironment-derived acetylated amino acids promote treatment resistance in glioblastoma by facilitating DNA repair through histone acetylation</span>, **Neuro-Oncology 2026** </span>
* <span style="text-align: justify"> Palavalasa, S., Freeman, J., Singer, A., Gokul, A., Baker, E., Scott, A., Wilder-Romans, K., Shankar, S., Ravikumar, V., <span style="color:red">Bhadury, S.</span>, et al.  <span style="color:blue"> [Microglia in the Glioblastoma Microenvironment Secrete Acetylated Amino Acids which Assist in the Repair of Radiation-Induced DNA Damage](https://doi.org/10.1093/neuonc/noae165.1203)</span>, **Neuro-Oncology 2024** </span>
* <span style="text-align: justify"> Sravya, P., Freeman, J. , Gokul, A., <span style="color:red">Bhadury, S.</span>, et al.  <span style="color:blue"> [Microenvironment-derived acetylated amino acids promote glioblastoma DNA repair by rerouting glucose fates and enhancing histone acetylation](https://academic.oup.com/neuro-oncology/article/27/Supplement_5/v464/8319942)</span>, **Neuro-Oncology 2025** </span>
* <span style="text-align: justify"> Shankar, S., Ravikumar, V., Tripathy, A.,  <span style="color:red">Bhadury, S.</span>, et al.  <span style="color:blue"> [Glioblastoma evolution and resistance is mediated by a shift in cell state and tumor microenvironmental interactions](https://aacrjournals.org/cancerres/article/84/5_Supplement_1/B001/734329)</span>, **Cancer Research 2024** </span>
* <span style="text-align: justify"> Tripathi, A., Shankar, S., Ravikumar, V., <span style="color:red">Bhadury, S.</span>, et al.  <span style="color:blue"> [Single Cell Sequencing of Recurrent Glioblastoma Defines Cellular States Associated with Therapy Resistance](https://academic.oup.com/neuro-oncology/article/25/Supplement_5/v292/7406172)</span>, **Neuro-Oncology 2023** </span>
* <span style="text-align: justify"> Sravya, P., Singer, A. , Scott, AJ., <span style="color:red">Bhadury, S.</span>, et al.  <span style="color:blue"> [Microglia in the Glioblastoma Microenvironment Assist Repair of Radiation-Induced DNA Damage in a Contact-Independent Manner](https://academic.oup.com/neuro-oncology/article/25/Supplement_5/v98/7405697)</span>, **Neuro-Oncology 2023** </span>

## Clinical and Health Services Studies (Collaborative)

<span style="text-align: justify">Collaborative studies of access to care, hospital bed capacity, antibiotic use and resistance, and outcomes after radiation therapy.</span>

* <span style="text-align: justify"> Scott, M., Metcalf, C., <span style="color:red">Bhadury, S.</span>, et al., <span style="color:blue"> [Impact of COVID-19 Pandemic Healthcare Restrictions on Utilization and Diagnostic Yield of Outpatient Transthoracic Echocardiograms](https://publications.aap.org/pediatrics/article/149/1/338/185976)</span>, **Pediatrics**</span>
* <span style="text-align: justify"> Wattles, B.A. , Smith, M.J. , Feygin Y. , Jawad K.S. , <span style="color:red">Bhadury, S.</span>, et al., <span style="color:blue">[Recurrent antibiotic use in Kentucky children with 6 years continuous Medicaid enrollment](https://doi.org/10.1093/jpids/piac079)</span>, **Journal of the Pediatric Infectious Diseases Society**</span>
* <span style="text-align: justify"> Scott, M., Metcalf, C., <span style="color:red">Bhadury, S.</span>, et al., <span style="color:blue"> [Impact of COVID-19 Pandemic Healthcare Restrictions on Utilization and Diagnostic Yield of Outpatient Transthoracic Echocardiograms](https://doi.org/10.1017/S1047951122003535)</span>,  **Cardiology in the Young 2022** </span>
* <span style="text-align: justify"> Jackson, C.N., Duncan, S.D., Creel, L.M., Feygin, Y., <span style="color:red">Bhadury, S.</span> et al., <span style="color:blue"> [Using Queuing Theory to Determine Optimal Obstetrical Bed Numbers](https://academyhealth.confex.com/academyhealth/2022arm/meetingapp.cgi/Paper/53422)</span>, Accepted in Conference **Pediatric Academic Societies 2022 & Academy Health Annual Research Meeting 2022** </span>
* <span style="text-align: justify"> Duncan, S.D., Creel, L.M., <span style="color:red">Bhadury, S.</span> et al., <span style="color:blue"> [Using Queuing Theory to Determine Optimal NICU Bed Numbers](https://academyhealth.confex.com/academyhealth/2022arm/meetingapp.cgi/Paper/53170)</span>, Accepted in Conference **Pediatric Academic Societies 2022 & Academy Health Annual Research Meeting 2022** </span>
* <span style="text-align: justify"> Duncan, S.D.,Feygin, Y., <span style="color:red">Bhadury, S.</span> et al.,  <span style="color:blue"> [Declining Access to Obstetrical Beds in Rural Kentucky](https://academyhealth.confex.com/academyhealth/2022arm/meetingapp.cgi/Paper/53463)</span>, Accepted in Conference **Pediatric Academic Societies 2022 & Academy Health Annual Research Meeting 2022** </span>
* <span style="text-align: justify"> Green, J.V., Bryant, K.A., Boland, L.F., Stout, G.G., Junkins, A.D., Stahl, J.A., Feygin, Y., <span style="color:red">Bhadury, S.</span>, Espinosa, C.,  <span style="color:blue"> [Increased NICU mupirocin use drives MRSA mupirocin resistance but not transmission or invasive infection](https://virtual2021.pas-meeting.org/fsPopup.asp?efp=WldIRlFRV1gxNDAzOA&PosterID=365942&rnd=0.5142702&mode=posterinfo)</span>, **Poster at Annual Meeting of Pediatric Academic Societies 2021 - E-PAS2021:4909-HP-QA.478** </span>
* <span style="text-align: justify"> May, M.E. , <span style="color:red">Bhadury, S.</span>, Gaskins, J., Dunlap, N.E. <span style="color:blue"> [Comparison of Outcomes and Pulmonary Toxicity of Motion Management Methods in Stereotactic Body Radiation Therapy for the Treatment of Early Stage Non-Small Cell Lung Cancer](https://www.sciencedirect.com/science/article/pii/S0360301619321960)</span>, **Proceedings of the 61st Annual Meeting of the American Society for Radiation Oncology 2019** </span>
* <span style="text-align: justify">  May, M.E. , <span style="color:red">Bhadury, S.</span>, Gaskins, J., Dunlap, N.E. <span style="color:blue"> [Assessing the Relationship of Background Lung Density on Outcome and Toxicity after Stereotactic Body Radiation Therapy](https://www.sciencedirect.com/science/article/pii/S0360301619300768)</span>, **Proceedings of the 61st Annual Meeting of the American Society for Radiation Oncology 2019** </span>

## Software

* <span style="text-align: justify"><span style="color:blue">[GGMsubho](https://github.com/sagnikbhadury/GGMsubho)</span> (v0.1.0). R package for sparse Gaussian graphical model estimation with step-up Bayesian horseshoe selection.</span>
* <span style="text-align: justify"><span style="color:blue">[Spatial Methods Workbench]({{ "/spatial-methods-workbench/" | relative_url }})</span> (v0.4.0). A browser application that runs exploratory through advanced spatial network analyses on uploaded data, calling the CRAN ISPAT3D and GPGHS engines. [Application](https://sagnikbhadury.shinyapps.io/spatial-methods-workbench/) | [Zenodo](https://doi.org/10.5281/zenodo.23627817) | [GitHub](https://github.com/sagnikbhadury/SpatialMethodsWorkbench)</span>
* <span style="text-align: justify"><span style="color:blue">[ISPAT3D](https://cran.r-project.org/web/packages/ISPAT3D/)</span> (v0.3.1). R package on CRAN for spatial conditional association networks in registered tumor volumes. [GitHub](https://github.com/sagnikbhadury/ISPAT-3D)</span>

---

<span style="text-align: justify; font-size: 0.85em; color: #7a8288;">The animated figures walk through each method's pipeline and the analyses in the corresponding paper. The pipeline panels of the SUBHO animation use simulated data.</span>
