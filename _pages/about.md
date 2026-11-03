---
layout: home
title: "Sagnik Bhadury"
seo_title: "Sagnik Bhadury: Bayesian Biostatistics and Clinical Trial Methods"
permalink: /
author_profile: false
description: "Research Associate at Penn Medicine developing Bayesian methods for clinical trials, biomedical phenotyping, graphical models, and spatial data."
schema_type: ProfilePage
redirect_from:
  - /about.html
---

<section class="home-hero">
  <div class="home-hero__copy">
    <p class="eyebrow"><span></span> Research Associate · Penn Medicine</p>
    <h1>Bayesian methods for complex biomedical data and <em>clinical trials</em>.</h1>
    <p class="home-hero__lead">I develop Bayesian statistical methods, machine-learning models, and bioinformatic pipelines for clinical trials, biomedical phenotyping, molecular cohorts, and high-dimensional spatial data.</p>
    <div class="home-actions">
      <a class="button button--primary" href="https://sagnikbhadury.shinyapps.io/spatial-methods-workbench/">Launch the Workbench <span aria-hidden="true">↗</span></a>
      <a class="button button--quiet" href="{{ '/research/' | relative_url }}">Explore my research <span aria-hidden="true">→</span></a>
      <a class="button button--quiet" href="{{ '/publications/' | relative_url }}">View publications</a>
    </div>
    <ul class="home-meta" aria-label="Current role and location">
      <li><i class="fa fa-building-o" aria-hidden="true"></i> University of Pennsylvania</li>
      <li><i class="fa fa-map-marker" aria-hidden="true"></i> Philadelphia, Pennsylvania</li>
    </ul>
  </div>

  <div class="home-hero__portrait">
    <div class="portrait-frame">
      <img src="{{ '/images/PORTRAIT.jpg' | relative_url }}" alt="Portrait of Sagnik Bhadury">
      <div class="portrait-card">
        <span class="status-dot" aria-hidden="true"></span>
        <p><strong>Current focus</strong><br>Bayesian trial design &amp; biomedical phenotyping</p>
      </div>
    </div>
  </div>
</section>

<section class="home-intro" aria-labelledby="intro-title">
  <div>
    <p class="section-kicker">What I do</p>
    <h2 id="intro-title">Statistical methods for questions that arise in clinical and biomedical studies.</h2>
  </div>
  <div class="home-intro__body">
    <p>I am a Research Associate in the <a href="https://dbei.med.upenn.edu/">Department of Biostatistics, Epidemiology and Informatics</a> at Penn Medicine and the University of Pennsylvania. I work with <a href="https://dbei.med.upenn.edu/staff/michael-harhay-phd-mph/">Michael Harhay, PhD</a>, and colleagues in the <a href="https://dbei.med.upenn.edu/center-of-excellence/center-for-clinical-trials-innovation-ccti/">Center for Clinical Trials Innovation</a> and the <a href="https://pair.upenn.edu/">Palliative and Advanced Illness Research (PAIR) Center</a>.</p>
    <p>My current work covers ARDS, pneumonia, and sepsis phenotyping, molecular cohort studies, and Bayesian early-phase trial design. These problems draw on my earlier work in Bayesian variable selection, graphical models, and spatial methods for high-dimensional biomedical data.</p>
    <p>Previously, I was a Postdoctoral Research Fellow at the University of Michigan, where I worked with <a href="https://sibl.lab.medicine.umich.edu/">Arvind Rao, PhD</a>. I earned my PhD in Biostatistics from the University of Louisville in 2022 under Jeremy Gaskins, PhD, and the late Riten Mitra, PhD.</p>
  </div>
</section>

<section class="workbench-spotlight" aria-labelledby="workbench-spotlight-title">
  <div class="workbench-spotlight__lead">
    <p class="section-kicker">Flagship research software · Open source · DOI archived</p>
    <h2 id="workbench-spotlight-title">The Spatial Methods Workbench turns an uploaded dataset into a reproducible, citation-ready analysis.</h2>
    <p>The Workbench collects the methods from this research program in one guided analysis platform. Twelve executable paths cover 2D and 3D cell-interaction networks, spatial machine learning, high-dimensional image regression, prediction, mediation, and tumor shape. The current release, v0.4.0, runs the ISPat 2D, ISPat 3D, and GP–GHS paths through the CRAN package ISPAT3D 0.3.1 and GPGHS 1.0.1, and it is archived on Zenodo with a citable DOI. Each path checks the uploaded data for compatibility before it runs and exports a complete provenance bundle (results, settings, software objects, figure, and citations). A twenty-minute narrated tutorial walks through the full workflow.</p>
    <div class="home-actions">
      <a class="button button--light" href="https://sagnikbhadury.shinyapps.io/spatial-methods-workbench/">Launch application <span aria-hidden="true">↗</span></a>
      <a class="button button--outline-light" href="{{ '/spatial-methods-workbench/' | relative_url }}">Explore all pipelines <span aria-hidden="true">→</span></a>
      <a class="button button--outline-light" href="https://www.youtube.com/watch?v=Ft9groM2ilI">Watch the tutorial <span aria-hidden="true">▶</span></a>
      <a class="button button--outline-light" href="https://doi.org/10.5281/zenodo.23627817">Cite the software</a>
      <a class="button button--outline-light" href="https://github.com/sagnikbhadury/SpatialMethodsWorkbench">Source ↗</a>
    </div>
  </div>
  <div class="workbench-spotlight__map" aria-label="Workbench pipeline overview">
    <div><span>01</span><strong>Upload and map</strong><small>Coordinates, regions, identifiers, outcomes, and features</small></div>
    <div><span>02</span><strong>Compatibility check</strong><small>Only the pipelines that fit the data become available</small></div>
    <div><span>03</span><strong>Run the analysis</strong><small>From exploratory summaries to the Bayesian ISPAT3D and GPGHS engines</small></div>
    <div><span>04</span><strong>Export provenance</strong><small>Results, settings, software objects, figures, and citations</small></div>
  </div>
</section>

<section class="home-intro" aria-labelledby="workbench-funding-title">
  <div>
    <p class="section-kicker">Funding acknowledgement</p>
    <h2 id="workbench-funding-title">Support for the Spatial Methods Workbench.</h2>
  </div>
  <p>Research reported in this software was supported by the National Cancer Institute of the National Institutes of Health under Award Number <strong>R37CA214955-01A1</strong>. The content is solely the responsibility of the author and does not necessarily represent the official views of the National Institutes of Health.</p>
</section>

<section class="home-section" aria-labelledby="themes-title">
  <div class="section-heading">
    <div>
      <p class="section-kicker">Research themes</p>
      <h2 id="themes-title">Eight connected research directions</h2>
    </div>
    <a class="text-link" href="{{ '/research/' | relative_url }}">See the full research program <span aria-hidden="true">→</span></a>
  </div>

  <div class="theme-grid">
    <a class="theme-card" href="{{ '/research/#1-bayesian-graphical-models--sparse-network-estimation' | relative_url }}">
      <span class="theme-card__number">01</span>
      <h3>Graphical models</h3>
      <p>High-dimensional network estimation with horseshoe and spike-and-slab priors.</p>
      <span class="theme-card__arrow" aria-hidden="true">↗</span>
    </a>
    <a class="theme-card" href="{{ '/research/#2-spatial-statistics-for-multiplexed-tissue-imaging' | relative_url }}">
      <span class="theme-card__number">02</span>
      <h3>Spatial statistics</h3>
      <p>Cell–cell interaction networks in 2D and 3D multiplexed tissue imaging.</p>
      <span class="theme-card__arrow" aria-hidden="true">↗</span>
    </a>
    <a class="theme-card" href="{{ '/research/#3-gaussian-processes--spatial-point-patterns' | relative_url }}">
      <span class="theme-card__number">03</span>
      <h3>Gaussian processes</h3>
      <p>Borrowing strength across misaligned spatial outcomes and point patterns.</p>
      <span class="theme-card__arrow" aria-hidden="true">↗</span>
    </a>
    <a class="theme-card" href="{{ '/research/#4-spatial-transcriptomics--compositional-data' | relative_url }}">
      <span class="theme-card__number">04</span>
      <h3>Compositional data</h3>
      <p>Regression for spatial cell-type proportions and morphology–expression links.</p>
      <span class="theme-card__arrow" aria-hidden="true">↗</span>
    </a>
    <a class="theme-card" href="{{ '/research/#5-multi-modal-integration--imaging-genomics' | relative_url }}">
      <span class="theme-card__number">05</span>
      <h3>Multi-modal integration</h3>
      <p>Histopathology, transcriptomics, and radiomics combined in one model.</p>
      <span class="theme-card__arrow" aria-hidden="true">↗</span>
    </a>
    <a class="theme-card" href="{{ '/research/#6-causal-inference--functional-data-analysis' | relative_url }}">
      <span class="theme-card__number">06</span>
      <h3>Causal &amp; functional data</h3>
      <p>Mediation, sensitivity analysis, and interpretable functional biomarkers.</p>
      <span class="theme-card__arrow" aria-hidden="true">↗</span>
    </a>
    <a class="theme-card" href="{{ '/research/#7-bayesian-methods-for-ai--interpretability' | relative_url }}">
      <span class="theme-card__number">07</span>
      <h3>Bayesian methods for AI</h3>
      <p>Shrinkage and error control for interpretability and pruning of language models.</p>
      <span class="theme-card__arrow" aria-hidden="true">↗</span>
    </a>
    <a class="theme-card" href="{{ '/research/#8-clinical-trials--longitudinal-biomedical-data' | relative_url }}">
      <span class="theme-card__number">08</span>
      <h3>Clinical trials &amp; longitudinal data</h3>
      <p>Bayesian trial design, joint models, and multi-omic phenotyping.</p>
      <span class="theme-card__arrow" aria-hidden="true">↗</span>
    </a>
  </div>
</section>

<section class="home-section home-featured" aria-labelledby="featured-title">
  <div class="section-heading">
    <div>
      <p class="section-kicker">Selected work</p>
      <h2 id="featured-title">From statistical idea to research tool</h2>
    </div>
    <a class="text-link" href="{{ '/datasets/' | relative_url }}">Browse data &amp; projects <span aria-hidden="true">→</span></a>
  </div>

  <div class="featured-grid">
    <article class="featured-card featured-card--visual">
      <div class="featured-card__image">
        <img src="{{ '/images/research/ispat-schematic.svg' | relative_url }}" alt="Diagram of the ISPat spatial graphical model">
      </div>
      <div class="featured-card__body">
        <p class="card-label">Published · Scientific Reports · Workbench path</p>
        <h3>ISPat</h3>
        <p>ISPat (Informed Spatially Aware Patterns) is a Bayesian spatial graphical model for multiplexed immunofluorescence images. It recovers the cell-cell interaction network shared across tumor-density areas and the part specific to each area, and it admits prior biological knowledge about which interactions to expect. In pancreatic tissue the model separates PDAC from IPMN by interactions that differ only in the intermediate-density areas. The 2D fit runs through the CRAN package ISPAT3D and is one of the Spatial Methods Workbench paths.</p>
        <div class="card-links">
          <a href="https://www.nature.com/articles/s41598-026-35341-8">Read paper ↗</a>
          <a href="https://github.com/sagnikbhadury/ISPAT">View code ↗</a>
          <a href="https://cran.r-project.org/web/packages/ISPAT3D/">ISPAT3D on CRAN ↗</a>
        </div>
      </div>
    </article>

    <div class="featured-list">
      <article>
        <p class="card-label">Published · Scientific Reports · R package on CRAN</p>
        <h3>ISPat 3D</h3>
        <p>ISPat 3D extends ISPat to registered three-dimensional tissue volumes. It estimates how conditional cell population associations change along the tumor density trajectory, with volumetric neighborhoods in place of single-plane ones. The method is implemented in the R package ISPAT3D (v0.3.1 on CRAN), which also powers the ISPat 2D and 3D paths of the Spatial Methods Workbench.</p>
        <a class="text-link" href="https://www.nature.com/articles/s41598-026-73151-0">Read article <span aria-hidden="true">↗</span></a>
        <a class="text-link" href="https://cran.r-project.org/web/packages/ISPAT3D/">ISPAT3D on CRAN <span aria-hidden="true">↗</span></a>
        <a class="text-link" href="https://github.com/sagnikbhadury/ISPAT-3D">View code <span aria-hidden="true">↗</span></a>
      </article>
      <article>
        <p class="card-label">Open-source methods · R, C++ and Python</p>
        <h3>Ten research repositories</h3>
        <p>Each published method has a public implementation. The repositories cover spatial interaction networks in 2D and 3D tissue images (ISPAT, ISPAT-3D, GP-GHS), adaptive borrowing across misaligned outcomes in meshed Gaussian process models (meshedghs), patient-level analysis of multiplex imaging (spatialMIFtools), graph-on-vector regression of molecular activity on histology graphs (GOV), causal mediation, functional depth, and tumor shape analysis. The Spatial Methods Workbench wraps the spatial paths in one guided interface.</p>
        <a class="text-link" href="https://github.com/sagnikbhadury">Explore GitHub <span aria-hidden="true">↗</span></a>
        <a class="text-link" href="https://github.com/sagnikbhadury/SpatialMethodsWorkbench">Workbench source <span aria-hidden="true">↗</span></a>
      </article>
    </div>
  </div>
</section>

<section class="modality-band" aria-labelledby="modalities-title">
  <div>
    <p class="section-kicker">Data modalities</p>
    <h2 id="modalities-title">One set of statistical tools, applied across biomedical data types.</h2>
  </div>
  <ul>
    <li>Critical-care phenotyping</li>
    <li>Early-phase clinical trials</li>
    <li>Molecular cohorts &amp; spatial omics</li>
    <li>Tissue imaging &amp; radiomics</li>
  </ul>
  <a class="modality-band__link" href="{{ '/research-domains/' | relative_url }}">Read the research domain guide <span aria-hidden="true">→</span></a>
</section>

<section class="contact-band">
  <div>
    <p class="section-kicker">Contact</p>
    <h2>Interested in a statistical or biomedical collaboration?</h2>
  </div>
  <div class="contact-band__actions">
    <a class="button button--light" href="{{ '/work-with-me/' | relative_url }}">Ways to work together <span aria-hidden="true">→</span></a>
    <a class="contact-email" href="mailto:bhadury@upenn.edu">bhadury@upenn.edu</a>
    <div class="contact-social">
      <a href="https://github.com/sagnikbhadury" aria-label="GitHub"><i class="fa fa-github" aria-hidden="true"></i></a>
      <a href="https://www.linkedin.com/in/sagnik-k-bhadury" aria-label="LinkedIn"><i class="fa fa-linkedin" aria-hidden="true"></i></a>
      <a href="https://www.researchgate.net/profile/Sagnik-Bhadury" aria-label="ResearchGate"><i class="ai ai-researchgate" aria-hidden="true"></i></a>
    </div>
  </div>
</section>
