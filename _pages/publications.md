---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
description: "Publications and preprints by Sagnik Bhadury in Bayesian graphical models, spatial statistics, cancer genomics, multiplexed tissue imaging, and multimodal learning."
redirect_from: 
- /publications.html
---

--- 

Peer-reviewed publications, preprints, and collaborative contributions are listed below. For questions about current manuscripts or ongoing work, please [email me](mailto:bhadury@upenn.edu).

# Selected Publications

* <span style="text-align: justify"><span style ="color:red">Bhadury, S.</span> et al. <span style ="color:blue"> [ISPat: Informed Spatially Aware Patterns for Multiplexed Immunofluorescence data](https://www.nature.com/articles/s41598-026-35341-8)</span>, **Nature Scientific Reports**. A Bayesian spatial graphical model that recovers shared and region-specific cell-cell interaction networks from mIF imaging.</span>

  <figure class="align-center" style="max-width: 760px; margin: 0.75rem auto 1.25rem;">
    <img src="{{ '/images/research/ispat-pipeline.gif' | relative_url }}" alt="Animated walkthrough of the ISPat pipeline: stained mIF image, cell point patterns, domain-informed network, tumor sub-regions, spatial intensities, shared and region-specific interaction networks, simulation results and the PDAC versus IPMN comparison" loading="lazy">
    <figcaption>ISPat pipeline and analyses: from the stained multiplexed image to shared and tumor-region-specific interaction networks, simulation checks, and the PDAC versus IPMN comparison across tumor-density areas.</figcaption>
  </figure>
* <span style="text-align: justify">Tsang, A., Krishnan, S., Kulkarni, R., <span style ="color:red">Bhadury, S.</span>, Rao, A., et al. <span style ="color:blue"> [Encoding functional edges in graphs to model spatially varying relationships in the tumor microenvironment](https://doi.org/10.1038/s44387-026-00075-5)</span>, **npj Artificial Intelligence**.</span>
* <span style="text-align: justify"><span style ="color:red">Bhadury, S.</span>, Rao, A. <span style ="color:blue"> [Estimating conditional cell population associations across tumor density trajectory in three dimensional tissue images (ISPat 3D)](https://www.nature.com/articles/s41598-026-73151-0)</span>, **Nature Scientific Reports**. The method extends ISPat to three-dimensional tissue images and estimates how conditional cell population associations change along tumor density trajectories. The R package [ISPAT3D](https://cran.r-project.org/web/packages/ISPAT3D/) is available on CRAN.</span>

  <figure class="align-center" style="max-width: 760px; margin: 0.75rem auto 1.25rem;">
    <img src="{{ '/images/research/ispat3d-pipeline.gif' | relative_url }}" alt="Animated walkthrough of the ISPat 3D pipeline on a registered colorectal cancer CyCIF volume: why 3D, the volumetric neighborhoods, tumor-density trajectory, and the conditional association networks along it" loading="lazy">
    <figcaption>ISPat 3D on a registered colorectal cancer CyCIF volume: single-plane versus volumetric neighborhoods, the tumor-density trajectory, and how conditional cell population associations change along it.</figcaption>
  </figure>
* <span style="text-align: justify"><span style ="color:red">Bhadury, S.</span>, Tsang, A., Ray, D., Lagisetty, K., Kundu, S., Rao, A. <span style ="color:blue">Graph-on-Vector Association Modeling of Histopathological and Transcriptomic Features in Lung Adenocarcinoma</span>, **npj Artificial Intelligence** (accepted). Graph-on-vector regression of pathway, kinase and transcription-factor activities on participant-specific histomorphological phenotype graphs in TCGA-LUAD, with node-level Bayesian variable selection.</span>

  <figure class="align-center" style="max-width: 760px; margin: 0.75rem auto 1.25rem;">
    <img src="{{ '/images/research/gov-pipeline.gif' | relative_url }}" alt="Animated walkthrough of the graph-on-vector pipeline in TCGA lung adenocarcinoma: survival-rank cohort split, H&amp;E morphology, graph construction, molecular activity scores, graph-on-vector regression, and pathway, kinase and transcription-factor results" loading="lazy">
    <figcaption>Graph-on-vector association modeling in TCGA-LUAD: survival-rank cohort split, H&amp;E-derived morphology graphs, molecular activity scores, the graph-on-vector regression, and pathway, kinase and transcription-factor results.</figcaption>
  </figure>
* <span style="text-align: justify"><span style ="color:red">Bhadury, S.</span>, Mitra, R., Gaskins, J. <span style ="color:blue"> [Fast Bayesian High-Dimensional Gaussian Graphical Model Estimation](https://arxiv.org/abs/2308.02713)</span>. This methods paper underlies the spatial and multi-modal graphical models above. The R package [GGMsubho](https://github.com/sagnikbhadury/GGMsubho) is available on GitHub.</span>

  <figure class="align-center" style="max-width: 760px; margin: 0.75rem auto 1.25rem;">
    <img src="{{ '/images/research/subho-pipeline.gif' | relative_url }}" alt="Animated walkthrough of the Graphical-SUBHO pipeline: data matrix, node-wise horseshoe regression, ranking of the predictors, step-up model selection, combining neighbourhoods with the AND rule, and the estimated network, followed by the seven figures of the manuscript" loading="lazy">
    <figcaption>Graphical-SUBHO pipeline and results: node-wise horseshoe regression, ranking of the predictors, step-up model selection and the AND rule, illustrated on simulated data, followed by the simulation comparisons and the METABRIC triple-negative breast cancer gene networks.</figcaption>
  </figure>

See [Research]({{ "/research/" | relative_url }}) for how these fit into the broader research program, organized by theme.

# Manuscripts and Preprints

* <span style="text-align: justify"><span style ="color:red">Bhadury, S.</span>, Mitra, R., Gaskins, J. <span style ="color:blue">[Fast Bayesian High-Dimensional Gaussian Graphical Model Estimation](https://arxiv.org/abs/2308.02713)</span>. R package: [GGMsubho](https://github.com/sagnikbhadury/GGMsubho).</span>
* <span style="text-align: justify"><span style ="color:red">Bhadury, S.</span>, Gaskins, J., Rao, A. <span style ="color:blue">[Spatially Varying Graphical Models for Cell-Cell Interaction Networks in Multiplexed Tissue Imaging](https://doi.org/10.64898/2026.04.01.715977)</span></span>
* <span style="text-align: justify"><span style ="color:red">Bhadury, S.</span>, Tsang, A.P., Ray, D., Lagisetty, K., Rao, A. <span style ="color:blue">[Functional Depth Biomarkers Distinguish Lung Squamous Cell Carcinoma from Lung Adenocarcinoma](https://doi.org/10.21203/rs.3.rs-9347794/v1)</span></span>
* <span style="text-align: justify"><span style ="color:red">Bhadury, S.</span>, Frankel, T.L., Rao, A. <span style ="color:blue">[Cellular Proximity and Conditional Coordination in the Colorectal and Pancreatic Tumor Microenvironment: A Patient-Level Analysis of Multiplexed Imaging](https://doi.org/10.64898/2026.10.08.757632)</span></span>
* <span style="text-align: justify"><span style ="color:red">Bhadury, S.</span> <span style ="color:blue">Design-Adaptive Borrowing Across Misaligned Outcomes in Bayesian Coregionalization Models</span></span>
* <span style="text-align: justify"><span style ="color:red">Bhadury, S.</span> <span style ="color:blue">Does the Route Matter? Functional Validation of Shared&ndash;Private Sparse Autoencoders</span></span>
* <span style="text-align: justify"><span style ="color:red">Bhadury, S.</span> <span style ="color:blue">Comparing Sparse Autoencoder Dictionaries through Decoder Subspaces</span></span>
* <span style="text-align: justify">Wahl, D., Sravya, P., Altay, L., Do, K., Freeman, J., Gokul, A., ..., <span style ="color:red">Bhadury, S.</span>, et al. <span style ="color:blue">[Microenvironment-Derived Acetylated Amino Acids Promote Glioblastoma Treatment Resistance](https://doi.org/10.21203/rs.3.rs-10976328/v1)</span></span>

# Manuscripts in Preparation

* <span style="text-align: justify"><span style ="color:red">Bhadury, S.</span>, Schwob, M., Datta, J. <span style ="color:blue">Spatial Active-Set Ray Regression for Compositional Data: Methodology, Validation, and Applications in Spatial Transcriptomics and Community Ecology</span></span>
* <span style="text-align: justify"><span style ="color:red">Bhadury, S.</span>, Frankel, T., Rao, A. <span style ="color:blue">Resolving Compositional Confounding in Spatial Proximity Analysis through Mediation in Tumor Microenvironments</span></span>
* <span style="text-align: justify"><span style ="color:red">Bhadury, S.</span>, Frankel, T., Rao, A. <span style ="color:blue">Causal Mediation Decomposes Pancreatic Cancer Spatial Diversity into Compositional and Organizational Pathways</span></span>
* <span style="text-align: justify"><span style ="color:red">Bhadury, S.</span>, Mohammed, S., Kurtek, S., Rao, A. <span style ="color:blue">RISM: Radiomic Feature Integration with Spike-and-Slab for Multimodal Survival Analysis</span></span>
* <span style="text-align: justify"><span style ="color:red">Bhadury, S.</span>, Mitra, R., Gaskins, J. <span style ="color:blue">Bayesian Joint Estimation of Multiple Graphs through Shared Shrinkage</span></span>
* <span style="text-align: justify"><span style ="color:red">Bhadury, S.</span>, Kulkarni, R., Rao, A. <span style ="color:blue">Quantifying Biological Signal in Pathology Foundation Models through Bayesian Mutual Information Estimation</span></span>
* <span style="text-align: justify"><span style ="color:red">Bhadury, S.</span>, Rao, A. <span style ="color:blue">SHIRE: Spatial Horseshoe Image-Basis Regression for Morphology and Gene Expression Associations in Spatial Transcriptomics</span></span>

# Software

* <span style="text-align: justify"><span style ="color:red">Bhadury, S.</span> <span style ="color:blue">[ISPAT3D: Spatial Conditional Association Networks in Registered Tumor Volumes](https://cran.r-project.org/web/packages/ISPAT3D/)</span>, R package on **CRAN** (v0.3.1). [GitHub](https://github.com/sagnikbhadury/ISPAT-3D)</span>
* <span style="text-align: justify"><span style ="color:red">Bhadury, S.</span> <span style ="color:blue">[Spatial Methods Workbench]({{ "/spatial-methods-workbench/" | relative_url }})</span> (v0.4.0). [Zenodo](https://doi.org/10.5281/zenodo.23627817) | [GitHub](https://github.com/sagnikbhadury/SpatialMethodsWorkbench)</span>

# Published
* Pediatrics: <span style="text-align: justify"> Scott, M., Metcalf, C., <span style ="color:red">Bhadury, S.</span>, et al., <span style ="color:blue"> [Impact of COVID-19 Pandemic Healthcare Restrictions on Utilization and Diagnostic Yield of Outpatient Transthoracic Echocardiograms](https://publications.aap.org/pediatrics/article/149/1/338/185976)</span> </span>
* Journal of the Pediatric Infectious Diseases Society: <span style="text-align: justify"> Wattles, B.A. , Smith, M.J. , Feygin Y. , Jawad K.S. , <span style ="color:red">Bhadury, S.</span>, et al., <span style ="color:blue">[Recurrent antibiotic use in Kentucky children with 6 years continuous Medicaid enrollment](https://doi.org/10.1093/jpids/piac079)</span> </span>
* Nature Scientific Reports: <span style="text-align: justify"> <span style ="color:red">Bhadury, S.</span> et al. <span style ="color:blue"> [ISPat: Informed Spatially Aware Patterns for Multiplexed Immunofluorescence data](https://www.nature.com/articles/s41598-026-35341-8)  </span>
* npj Artificial Intelligence: Tsang, A., Krishnan, S., Kulkarni, R., <span style="text-align: justify"> <span style ="color:red">Bhadury, S.</span> Rao, A., et al. <span style ="color:blue"> [Encoding functional edges in graphs to model spatially varying relationships in the tumor microenvironment.](https://doi.org/10.1038/s44387-026-00075-5)  </span>
* Nature Scientific Reports: <span style="text-align: justify"> <span style ="color:red">Bhadury, S.</span>, Rao, A. <span style ="color:blue"> [Estimating conditional cell population associations across tumor density trajectory in three dimensional tissue images (ISPat 3D)](https://www.nature.com/articles/s41598-026-73151-0)  </span>
* npj Artificial Intelligence: <span style="text-align: justify"> <span style ="color:red">Bhadury, S.</span>, Tsang, A., Ray, D., Lagisetty, K., Kundu, S., Rao, A. <span style ="color:blue"> Graph-on-Vector Association Modeling of Histopathological and Transcriptomic Features in Lung Adenocarcinoma (accepted)</span>  </span>


# Others 


* <span style="text-align: justify"> Palavalasa, S., <span style ="color:red">Bhadury, S.</span>, et al.  <span style ="color:blue"> Immune-microenvironment-derived acetylated amino acids promote treatment resistance in glioblastoma by facilitating DNA repair through histone acetylation</span>, **Neuro-Oncology 2026** </span>

* <span style="text-align: justify"> Palavalasa, S., Freeman, J., Singer, A., Gokul, A., Baker, E., Scott, A., Wilder-Romans, K., Shankar, S., Ravikumar, V., <span style ="color:red">Bhadury, S.</span>, et al.  <span style ="color:blue"> [Microglia in the Glioblastoma Microenvironment Secrete Acetylated Amino Acids which Assist in the Repair of Radiation-Induced DNA Damage](https://doi.org/10.1093/neuonc/noae165.1203)</span>, **Neuro-Oncology 2024** </span>

* <span style="text-align: justify"> Sravya, P., Freeman, J. , Gokul, A., <span style ="color:red">Bhadury, S.</span>, et al.  <span style ="color:blue"> [Microenvironment-derived acetylated amino acids promote glioblastoma DNA repair by rerouting glucose fates and enhancing histone acetylation](https://academic.oup.com/neuro-oncology/article/27/Supplement_5/v464/8319942)</span>, **Neuro-Oncology 2025** </span>

* <span style="text-align: justify"> Shankar, S., Ravikumar, V., Tripathy, A.,  <span style ="color:red">Bhadury, S.</span>, et al.  <span style ="color:blue"> [Glioblastoma evolution and resistance is mediated by a shift in cell state and tumor microenvironmental interactions](https://aacrjournals.org/cancerres/article/84/5_Supplement_1/B001/734329)</span>, **Cancer Research 2024** </span>

* <span style="text-align: justify"> Tripathi, A., Shankar, S., Ravikumar, V., <span style ="color:red">Bhadury, S.</span>, et al.  <span style ="color:blue"> [Single Cell Sequencing of Recurrent Glioblastoma Defines Cellular States Associated with Therapy Resistance](https://academic.oup.com/neuro-oncology/article/25/Supplement_5/v292/7406172)</span>, **Neuro-Oncology 2023** </span>

* <span style="text-align: justify"> Sravya, P., Singer, A. , Scott, AJ., <span style ="color:red">Bhadury, S.</span>, et al.  <span style ="color:blue"> [Microglia in the Glioblastoma Microenvironment Assist Repair of Radiation-Induced DNA Damage in a Contact-Independent Manner](https://academic.oup.com/neuro-oncology/article/25/Supplement_5/v98/7405697)</span>, **Neuro-Oncology 2023** </span>

* <span style="text-align: justify"> Scott, M., Metcalf, C., <span style ="color:red">Bhadury, S.</span>, et al., <span style ="color:blue"> [Impact of COVID-19 Pandemic Healthcare Restrictions on Utilization and Diagnostic Yield of Outpatient Transthoracic Echocardiograms](https://doi.org/10.1017/S1047951122003535)</span>,  **Cardiology in the Young 2022** </span>


* <span style="text-align: justify"> Jackson, C.N., Duncan, S.D., Creel, L.M., Feygin, Y., <span style ="color:red">Bhadury, S.</span> et al., <span style ="color:blue"> [Using Queuing Theory to Determine Optimal Obstetrical Bed Numbers](https://academyhealth.confex.com/academyhealth/2022arm/meetingapp.cgi/Paper/53422)</span>, Accepted in Conference **Pediatric Academic Societies 2022 & Academy Health Annual Research Meeting 2022** </span>

*  <span style="text-align: justify"> Duncan, S.D., Creel, L.M., <span style ="color:red">Bhadury, S.</span> et al., <span style ="color:blue"> [Using Queuing Theory to Determine Optimal NICU Bed Numbers](https://academyhealth.confex.com/academyhealth/2022arm/meetingapp.cgi/Paper/53170)</span>, Accepted in Conference **Pediatric Academic Societies 2022 & Academy Health Annual Research Meeting 2022** </span>
  
* <span style="text-align: justify"> Duncan, S.D.,Feygin, Y., <span style ="color:red">Bhadury, S.</span> et al.,  <span style ="color:blue"> [Declining Access to Obstetrical Beds in Rural Kentucky](https://academyhealth.confex.com/academyhealth/2022arm/meetingapp.cgi/Paper/53463)</span>, Accepted in Conference **Pediatric Academic Societies 2022 & Academy Health Annual Research Meeting 2022** </span>

*  <span style="text-align: justify"> Green, J.V., Bryant, K.A., Boland, L.F., Stout, G.G., Junkins, A.D., Stahl, J.A., Feygin, Y., <span style ="color:red">Bhadury, S.</span>, Espinosa, C.,  <span style ="color:blue"> [Increased NICU mupirocin use drives MRSA mupirocin resistance but not transmission or invasive infection](https://virtual2021.pas-meeting.org/fsPopup.asp?efp=WldIRlFRV1gxNDAzOA&PosterID=365942&rnd=0.5142702&mode=posterinfo)</span>, **Poster at Annual Meeting of Pediatric Academic Societies 2021 - E-PAS2021:4909-HP-QA.478** </span>

* <span style="text-align: justify"> May, M.E. , <span style ="color:red">Bhadury, S.</span>, Gaskins, J., Dunlap, N.E. <span style ="color:blue"> [Comparison of Outcomes and Pulmonary Toxicity of Motion Management Methods in Stereotactic Body Radiation Therapy for the Treatment of Early Stage Non-Small Cell Lung Cancer](https://www.sciencedirect.com/science/article/pii/S0360301619321960)</span>, **Proceedings of the 61st Annual Meeting of the American Society for Radiation Oncology 2019** </span>

* <span style="text-align: justify">  May, M.E. , <span style ="color:red">Bhadury, S.</span>, Gaskins, J., Dunlap, N.E. <span style ="color:blue"> [Assessing the Relationship of Background Lung Density on Outcome and Toxicity after Stereotactic Body Radiation Therapy](https://www.sciencedirect.com/science/article/pii/S0360301619300768)</span>, **Proceedings of the 61st Annual Meeting of the American Society for Radiation Oncology 2019** </span>



<!---# Thesis

* <span style="text-align: justify"> <span style ="color:red">Bhadury, Sagnik K.</span> <span style ="color:blue"> [Bayesian Methods for Graphical Models with Neighborhood Selection](https://ir.library.louisville.edu/etd/4001/)</span>, PhD Dissertation Thesis Advisors: **Gaskins, Jeremy T. and Mitra, Ritendranath** </span>
--->

---







