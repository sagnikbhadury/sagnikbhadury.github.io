---
layout: single
permalink: /spatial-methods-workbench/
title: "Spatial Methods Workbench"
seo_title: "Spatial Methods Workbench — Guided Spatial & Biomedical Data Analysis"
author_profile: false
description: "A guided research platform for reproducible spatial, network, predictive, causal, and 3D biomedical data analysis developed by Sagnik Bhadury."
---

<div class="workbench-page">

<section class="workbench-hero">
  <div>
    <p class="section-kicker">Flagship research software · Open source · DOI archived</p>
    <h2>A statistical methods platform for structure in biomedical data.</h2>
    <p class="workbench-hero__lead">The Spatial Methods Workbench transforms specialized methodology into a guided, reproducible analysis environment. Researchers upload a structured dataset, map its scientific variables, choose among compatible pipelines, run the analysis, and receive citation-ready outputs without needing to reconstruct the underlying workflow from separate scripts.</p>
    <div class="workbench-actions">
      <a class="button button--primary" href="https://sagnikbhadury.shinyapps.io/spatial-methods-workbench/">Launch application <span aria-hidden="true">↗</span></a>
      <a class="button button--quiet" href="https://github.com/sagnikbhadury/SpatialMethodsWorkbench">Application source</a>
      <a class="button button--quiet" href="https://github.com/sagnikbhadury/SpatialMethodsWorkbench/releases/tag/v0.2.1">Download v0.2.1</a>
      <a class="button button--quiet" href="https://doi.org/10.5281/zenodo.21764196">Cite the software</a>
      <a class="button button--quiet" href="{{ '/workbench-guide/' | relative_url }}">Installation &amp; usage guide</a>
      <a class="button button--quiet" href="#reproducible-vignettes">Reproducible PDF vignettes</a>
      <a class="button button--quiet" href="https://www.youtube.com/watch?v=Ft9groM2ilI">Watch the complete tutorial <span aria-hidden="true">▶</span></a>
    </div>
  </div>
  <aside class="workbench-release-card">
    <p>Live public application</p>
    <strong>v0.2.1</strong>
    <dl>
      <div><dt>Interface</dt><dd>R Shiny</dd></div>
      <div><dt>Analyses</dt><dd>12 guided paths</dd></div>
      <div><dt>Testing</dt><dd>51 passing tests</dd></div>
      <div><dt>Archive</dt><dd>Zenodo DOI</dd></div>
    </dl>
    <a href="https://sagnikbhadury.shinyapps.io/spatial-methods-workbench/">Open the Workbench ↗</a><br>
    <a href="https://doi.org/10.5281/zenodo.21763606">All-versions DOI ↗</a>
  </aside>
</section>

<section class="workbench-video" aria-labelledby="workbench-video-title">
  <div class="section-heading">
    <div>
      <p class="section-kicker">Complete video tutorial · 20 minutes</p>
      <h2 id="workbench-video-title">See the full research workflow before you run it.</h2>
    </div>
    <p>The narrated walkthrough covers analysis-ready data, all 12 pipelines, the synthetic Moran’s I demonstration, advanced public engines, citation-ready exports, local installation, and the boundary between computation and scientific interpretation.</p>
  </div>
  <div class="workbench-video__frame">
    <iframe
      src="https://www.youtube-nocookie.com/embed/Ft9groM2ilI"
      title="Spatial Methods Workbench complete usage tutorial"
      loading="lazy"
      referrerpolicy="strict-origin-when-cross-origin"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      allowfullscreen>
    </iframe>
  </div>
  <div class="workbench-video__actions">
    <a class="button button--primary" href="https://www.youtube.com/watch?v=Ft9groM2ilI">Watch on YouTube <span aria-hidden="true">↗</span></a>
    <a class="button button--quiet" href="{{ '/workbench-guide/' | relative_url }}">Follow the written guide</a>
    <a class="button button--quiet" href="https://doi.org/10.5281/zenodo.21764196">Cite v0.2.1</a>
  </div>
</section>

<section class="workbench-live" aria-labelledby="live-app-title">
  <div class="section-heading">
    <div>
      <p class="section-kicker">Live application</p>
      <h2 id="live-app-title">Run the Workbench on this page.</h2>
    </div>
    <p>The embedded service may take several seconds to wake after inactivity. Use the full-screen link for large tables, long sessions, or smaller displays.</p>
  </div>
  <div class="workbench-live__frame">
    <iframe
      src="https://sagnikbhadury.shinyapps.io/spatial-methods-workbench/"
      title="Spatial Methods Workbench live Shiny application"
      loading="eager"
      allow="clipboard-write"
      referrerpolicy="strict-origin-when-cross-origin"
      allowfullscreen>
    </iframe>
  </div>
  <p class="workbench-live__fallback"><a class="button button--primary" href="https://sagnikbhadury.shinyapps.io/spatial-methods-workbench/">Open the live application full screen <span aria-hidden="true">↗</span></a></p>
</section>

<section class="workbench-statement">
  <p class="section-kicker">Purpose</p>
  <h2>One disciplined entry point to a broad methods program.</h2>
  <p>Spatial and imaging studies rarely fail because investigators lack another plotting function. The harder problem is choosing an analysis whose assumptions match the available coordinates, regions, identifiers, outcomes, and features—and preserving enough information for the result to be reproduced. The Workbench addresses that gap directly. It evaluates the uploaded data, exposes only compatible analysis paths, and packages the numerical output with the settings, runtime metadata, software object, figure, and required citations.</p>
</section>

<div class="domain-callout">
  <p class="domain-callout__label">Before using real data</p>
  <h2>Read the complete installation, input, restriction, and deployment guide.</h2>
  <p>The guide covers the public Shiny service, controlled local installation, all advanced network engines, Docker, real-data preparation, pipeline contracts, privacy, computational limits, citation, and collaboration. <a href="{{ '/workbench-guide/' | relative_url }}">Open the latest v0.2.1 installation and usage guide →</a></p>
  <p>For exact controls, calls, return objects, failure modes, and citations, read the <a href="https://github.com/sagnikbhadury/SpatialMethodsWorkbench/blob/master/docs/PIPELINE_REFERENCE.md">complete function-by-function pipeline reference ↗</a>.</p>
</div>

<section class="workbench-vignettes" id="reproducible-vignettes" aria-labelledby="vignettes-title">
  <div class="section-heading">
    <div>
      <p class="section-kicker">Executable documentation · Five PDF guides</p>
      <h2 id="vignettes-title">Reproduce the workflows with small simulated data.</h2>
    </div>
    <p>Each vignette was rendered from executable R code with fixed seeds and compact synthetic datasets. Download a PDF for a self-contained worked example, or inspect the matching source file in the public repository.</p>
  </div>

  <div class="vignette-grid">
    <article>
      <span>01 · Start here</span>
      <h3>Application walkthrough</h3>
      <p>Create all four demonstration datasets, validate a mapping, run the app-equivalent spatial workflow, and write a reproducibility bundle.</p>
      <small>72 spatial rows · 48 image subjects · 6 contours · 72 volumetric rows</small>
      <div><a href="{{ '/files/spatial-methods-workbench/vignettes/SpatialMethodsWorkbench-App-Walkthrough.pdf' | relative_url }}">Download PDF ↓</a><a href="https://github.com/sagnikbhadury/SpatialMethodsWorkbench/blob/master/vignettes/app-walkthrough.Rmd">View source ↗</a></div>
    </article>
    <article>
      <span>02 · Spatial structure</span>
      <h3>Spatial diagnostics &amp; networks</h3>
      <p>Reproduce spatial autocorrelation, region-aware conditional networks, and the deployment checks for the exact ISPat and GP–GHS engines.</p>
      <small>72 observations · 5 features · 19 Moran permutations</small>
      <div><a href="{{ '/files/spatial-methods-workbench/vignettes/SpatialMethodsWorkbench-Spatial-Networks.pdf' | relative_url }}">Download PDF ↓</a><a href="https://github.com/sagnikbhadury/SpatialMethodsWorkbench/blob/master/vignettes/spatial-networks.Rmd">View source ↗</a></div>
    </article>
    <article>
      <span>03 · Spatial AI &amp; causal structure</span>
      <h3>Prediction, clustering &amp; mediation</h3>
      <p>Run held-out machine learning, spatial phenotype clustering, shallow-neural prediction, and bootstrap mediation from one compact table.</p>
      <small>72 observations · fixed train/test seed · public workflow citations</small>
      <div><a href="{{ '/files/spatial-methods-workbench/vignettes/SpatialMethodsWorkbench-Prediction-Clustering-Mediation.pdf' | relative_url }}">Download PDF ↓</a><a href="https://github.com/sagnikbhadury/SpatialMethodsWorkbench/blob/master/vignettes/prediction-clustering-mediation.Rmd">View source ↗</a></div>
    </article>
    <article>
      <span>04 · Imaging &amp; morphology</span>
      <h3>Imaging, shape &amp; 3D</h3>
      <p>Exercise scalar-on-image screening, latent image-to-image regression, tumor contour PCA, and the ISPat 3D deployment contract.</p>
      <small>48 image subjects · 8 features · 6 aligned contours · 2 volumes</small>
      <div><a href="{{ '/files/spatial-methods-workbench/vignettes/SpatialMethodsWorkbench-Imaging-Shape-3D.pdf' | relative_url }}">Download PDF ↓</a><a href="https://github.com/sagnikbhadury/SpatialMethodsWorkbench/blob/master/vignettes/imaging-shape-3d.Rmd">View source ↗</a></div>
    </article>
    <article>
      <span>05 · Audit trail</span>
      <h3>Reproducibility bundles</h3>
      <p>Inspect the manifest, write the archive, audit its required artifacts, reopen the R result object, and verify embedded software and method citations.</p>
      <small>60 observations · 19 permutations · manifest, result, figure &amp; citations</small>
      <div><a href="{{ '/files/spatial-methods-workbench/vignettes/SpatialMethodsWorkbench-Reproducibility-Bundles.pdf' | relative_url }}">Download PDF ↓</a><a href="https://github.com/sagnikbhadury/SpatialMethodsWorkbench/blob/master/vignettes/reproducibility-bundles.Rmd">View source ↗</a></div>
    </article>
  </div>

  <div class="vignette-boundary">
    <strong>Scope of these documents</strong>
    <p>The PDFs demonstrate data contracts, function calls, numerical outputs, plots, and reproducibility artifacts. They do not provide biological or scientific interpretation. For study-specific interpretation or collaboration, <a href="mailto:bhadury@umich.edu?subject=Spatial%20Methods%20Workbench%20collaboration">contact Sagnik Bhadury</a>.</p>
  </div>
</section>

<section class="pipeline-architecture" aria-labelledby="architecture-title">
  <div class="section-heading">
    <div>
      <p class="section-kicker">Architecture</p>
      <h2 id="architecture-title">A guided analysis sequence</h2>
    </div>
    <p>Every path begins with the same explicit data contract.</p>
  </div>
  <ol class="pipeline-flow">
    <li><span>01</span><strong>Upload</strong><small>Start with a CSV or synthetic demonstration dataset.</small></li>
    <li><span>02</span><strong>Map</strong><small>Identify coordinates, regions, IDs, outcomes, exposures, mediators, and features.</small></li>
    <li><span>03</span><strong>Validate</strong><small>Check structure and display precisely what each pipeline still requires.</small></li>
    <li><span>04</span><strong>Analyze</strong><small>Configure and run a compatible built-in or advanced public engine.</small></li>
    <li><span>05</span><strong>Export</strong><small>Download results, figures, parameters, R objects, provenance, and citations.</small></li>
  </ol>
</section>

<section class="pipeline-catalog" aria-labelledby="catalog-title">
  <div class="section-heading">
    <div>
      <p class="section-kicker">Pipeline catalog</p>
      <h2 id="catalog-title">Twelve analysis paths, organized by scientific task</h2>
    </div>
  </div>

  <div class="pipeline-tier">
    <div class="pipeline-tier__heading"><span>Spatial structure</span><p>Characterize how measured features and conditional relationships vary across tissue.</p></div>
    <div class="pipeline-cards">
      <article><b>01</b><h3>Spatial exploration &amp; autocorrelation</h3><p>Map a numeric feature and test spatial patterning with permutation-based Moran’s I.</p><small>Input: x/y + feature · Output: map, Moran’s I, permutation p-value</small></article>
      <article><b>02</b><h3>Region-aware conditional networks</h3><p>Estimate ridge-regularized partial-correlation networks overall and within mapped tissue regions.</p><small>Input: 3+ numeric markers, optional region · Output: edge tables + heat maps</small></article>
      <article><b>03</b><h3>ISPat 2D Bayesian network</h3><p>Estimate shared and region-specific conditional-association networks after spatial adjustment.</p><small>Exact public engine · Input: x/y, zone, 3+ markers · Output: networks + full fit</small></article>
      <article><b>04</b><h3>GP–GHS network</h3><p>Estimate spatially varying edges using Gaussian-process structure with group-horseshoe shrinkage.</p><small>Exact public engine · Input: x/y + 3+ features · Output: selected adjacency + full fit</small></article>
    </div>
  </div>

  <div class="pipeline-tier pipeline-tier--3d">
    <div class="pipeline-tier__heading"><span>Volumetric complexity</span><p>Move beyond a single section to serial-section and three-dimensional tumor imaging.</p></div>
    <div class="pipeline-cards pipeline-cards--single">
      <article><b>05</b><h3>ISPat 3D volumetric networks</h3><p>Estimate shared and zone-specific conditional networks across registered volumetric or serial-section imaging data.</p><small>Exact public engine · Input: x/y/z, zone, volume ID, 3+ markers · Output: 3D networks + fits</small></article>
    </div>
  </div>

  <div class="pipeline-tier">
    <div class="pipeline-tier__heading"><span>Spatial AI &amp; machine learning</span><p>Adapt public AI, ML, and deep-learning workflows to spatial biomedical prediction and discovery.</p></div>
    <div class="pipeline-cards pipeline-cards--three">
      <article><b>06</b><h3>Spatial machine-learning prediction</h3><p>Predict a numeric outcome from measured features and optional coordinates with held-out validation.</p><small>Input: outcome + 3+ predictors · Output: predictions, test error, variable importance</small></article>
      <article><b>07</b><h3>Spatial phenotype clustering</h3><p>Discover multivariate phenotypes while explicitly controlling how strongly tissue coordinates influence clusters.</p><small>Input: x/y + 3+ features · Output: assignments, centers, diagnostics, spatial map</small></article>
      <article><b>08</b><h3>Shallow-neural prediction</h3><p>Fit a standardized single-hidden-layer model with weight decay and held-out evaluation.</p><small>Input: outcome + 3+ predictors · Output: held-out predictions + performance metrics</small></article>
    </div>
  </div>

  <div class="pipeline-tier">
    <div class="pipeline-tier__heading"><span>High-dimensional imaging</span><p>Analyze aligned contours, pixel/voxel predictors, and paired predictor–outcome images.</p></div>
    <div class="pipeline-cards pipeline-cards--three">
      <article><b>09</b><h3>Wide-image scalar regression</h3><p>Screen aligned pixel, voxel, or image-derived features against a numeric subject-level outcome.</p><small>Fast ridge screen—not the full SV-NN/ST-CAR posterior · Output: predictions, error, coefficients</small></article>
      <article><b>10</b><h3>Latent image-to-image regression</h3><p>Connect aligned predictor and outcome images through low-dimensional factors and held-out reconstruction.</p><small>Fast latent screen—not the full SBLF posterior · Input: input__* + output__* columns</small></article>
      <article><b>12</b><h3>Tumor contour &amp; shape PCA</h3><p>Resample and align ordered boundaries, then summarize tumor morphology with principal components.</p><small>Input: contour ID + ordered x/y landmarks · Output: aligned shapes, scores, variance</small></article>
    </div>
  </div>

  <div class="pipeline-tier">
    <div class="pipeline-tier__heading"><span>Causal structure</span><p>Estimate a prespecified indirect-effect model while keeping causal requirements explicit.</p></div>
    <div class="pipeline-cards pipeline-cards--single">
      <article><b>11</b><h3>Mediation analysis</h3><p>Estimate model-based direct, indirect, and total effects with bootstrap uncertainty and explicit causal requirements.</p><small>Input: exposure + mediator + outcome · Output: effect estimates + bootstrap intervals</small></article>
    </div>
  </div>
</section>

<section class="workbench-principles public-ecosystem">
  <div>
    <p class="section-kicker">Public workflow ecosystem</p>
    <h2>Broader than a single package—and explicit about attribution.</h2>
  </div>
  <div class="principle-grid">
    <article><h3>AI &amp; ML curricula</h3><p>The <a href="https://github.com/microsoft/AI-For-Beginners">AI for Beginners</a> and <a href="https://github.com/microsoft/ML-For-Beginners">ML for Beginners</a> repositories inform executable spatial clustering and predictive workflows.</p></article>
    <article><h3>Deep-learning foundations</h3><p><a href="https://github.com/mikexcohen/DeepUnderstandingOfDeepLearning">A Deep Understanding of Deep Learning</a> informs the tested shallow-neural extension, adapted to coordinates and biomedical features.</p></article>
    <article><h3>SV-NN direction</h3><p>The image-regression tier cites Wu, Wu &amp; Kang’s <a href="https://jmlr.org/papers/v26/22-0246.html">Bayesian spatially varying neural-network model</a> while labeling the interactive ridge implementation as a screening workflow.</p></article>
    <article><h3>ST-CAR direction</h3><p>Scalar-on-image and image-on-scalar extensions are connected to the <a href="https://openreview.net/forum?id=rnL3OafDdw&noteId=gn2VU2ZeIo">soft-thresholded CAR image-regression publication</a>; full posterior engines remain deployment-gated.</p></article>
    <article><h3>SBLF direction</h3><p>The paired-image workflow follows the latent-factor problem structure established by Guo, Kang &amp; Johnson’s <a href="https://doi.org/10.1111/biom.13420">spatial Bayesian image-on-image model</a>, with exact method identity retained in every label.</p></article>
    <article><h3>Data-isolation boundary</h3><p>Uploaded values and results remain inside the active analysis service and are not sent to a third-party AI interpretation system. The platform does not automate scientific interpretation.</p></article>
  </div>
</section>

<section class="workbench-principles">
  <div>
    <p class="section-kicker">Built for credible research use</p>
    <h2>Compatibility before computation. Provenance after it.</h2>
  </div>
  <div class="principle-grid">
    <article><h3>Explicit compatibility gates</h3><p>The interface tells researchers what is ready, what is missing, and whether an advanced engine exists on the deployment.</p></article>
    <article><h3>Exact engine identity</h3><p>An unavailable Bayesian or 3D method is never replaced by a simpler algorithm under the same name.</p></article>
    <article><h3>Reproducibility bundles</h3><p>Each download preserves results, a figure, parameters, runtime metadata, the R result object, and software citations.</p></article>
    <article><h3>Citation by design</h3><p>Users acknowledge the citation condition before analysis. Citation metadata are embedded in every export and the software has a permanent Zenodo DOI.</p></article>
    <article><h3>Research-data caution</h3><p>The public workflow defaults to synthetic data and explicitly prohibits protected health information on an unsecured deployment.</p></article>
    <article><h3>Tested application behavior</h3><p>Automated analysis, export, citation, and Shiny server tests protect the public workflow as the platform evolves.</p></article>
  </div>
</section>

<section class="interpretation-boundary">
  <div>
    <p class="section-kicker">Scientific interpretation</p>
    <h2>The platform computes results. Scientific conclusions require collaboration.</h2>
  </div>
  <div>
    <p>The Workbench deliberately does not narrate results, assign biological mechanisms, or generate automated explanations. Interpretation depends on study design, tissue context, preprocessing, measurement technology, and the scientific question.</p>
    <p>For study-specific interpretation, methodological consultation, or a research collaboration, contact Sagnik Bhadury directly.</p>
    <a class="button button--light" href="mailto:bhadury@umich.edu?subject=Spatial%20Methods%20Workbench%20collaboration">Discuss a collaboration <span aria-hidden="true">→</span></a>
  </div>
</section>

<section class="workbench-citation">
  <p class="section-kicker">Software record</p>
  <h2>A citable platform, not an ephemeral web demo.</h2>
  <div>
    <p><strong>Version v0.2.1:</strong> Bhadury, S. (2026). <em>SpatialMethodsWorkbench: Spatial Methods Workbench</em> (v0.2.1) [Computer software]. Zenodo.</p>
    <p><a href="https://doi.org/10.5281/zenodo.21764196">doi:10.5281/zenodo.21764196</a></p>
    <p>The all-versions record is <a href="https://doi.org/10.5281/zenodo.21763606">doi:10.5281/zenodo.21763606</a>. Individual statistical engines retain their applicable publication and software citations, which the Workbench adds to the corresponding result bundle.</p>
  </div>
</section>

</div>
