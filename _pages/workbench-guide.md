---
layout: single
permalink: /workbench-guide/
title: "Spatial Methods Workbench: Installation & Usage Guide"
author_profile: false
description: "Complete guide to launching, installing, configuring, and responsibly using the Spatial Methods Workbench with real spatial and biomedical data."
---

<div class="domain-callout">
  <p class="domain-callout__label">Live public application</p>
  <h2>Use the Workbench in your browser</h2>
  <p><a class="button button--primary" href="https://sagnikbhadury.shinyapps.io/spatial-methods-workbench/">Launch the application ↗</a> <a class="button button--quiet" href="{{ '/spatial-methods-workbench/' | relative_url }}">Review all pipelines</a></p>
</div>

The **Spatial Methods Workbench** is a guided research platform for spatial diagnostics, conditional networks, Bayesian 2D and 3D network estimation, spatial AI and machine learning, image regression, mediation, and tumor-shape analysis. It validates an uploaded table, exposes compatible pipelines, runs the selected workflow, and exports numerical results with parameters, software objects, provenance, and citations.

## Function-by-function reference

The [complete pipeline reference](https://github.com/sagnikbhadury/SpatialMethodsWorkbench/blob/master/docs/PIPELINE_REFERENCE.md) documents every public executable function and all 12 workflows: purpose, input contract, interface controls, programmatic call, returned object, exported files, assumptions, common failures, and required method citations. The same 669-line manual is available in the live application under **Pipeline reference**. Read it before applying a workflow to real data.

The accompanying [usage, restrictions, and local installation manual](https://github.com/sagnikbhadury/SpatialMethodsWorkbench/blob/master/docs/USER_GUIDE.md) is the authoritative operational guide distributed with the toolkit.

> **Interpretation boundary:** the Workbench computes outputs but does not explain results, assign biological mechanisms, or make scientific or clinical conclusions. For study-specific interpretation or collaboration, contact [bhadury@umich.edu](mailto:bhadury@umich.edu?subject=Spatial%20Methods%20Workbench%20collaboration).

## Restrictions before use

1. **Research use only.** The suite is not a medical device and must not guide diagnosis, treatment, patient management, or clinical decisions.
2. **Do not upload protected health information to the public application.** Remove direct identifiers, detailed dates, rare identifiers, free text, raw DICOM headers, and other re-identification risks. Follow institutional, IRB, data-use, and security requirements.
3. **Use a controlled local deployment for sensitive data.** The application does not intentionally persist uploads, but a public host has infrastructure and operational logs outside the R source code.
4. **Preprocessing remains the user's responsibility.** Registration, segmentation, normalization, batch correction, coordinate definitions, zone labels, feature identity, missingness, and quality control must be finalized before upload.
5. **Readiness is not scientific approval.** A green compatibility status confirms the minimum technical input contract, not that the design, estimand, assumptions, sample size, or method are appropriate.
6. **Network edges are not automatically causal or mechanistic.** They do not alone demonstrate physical contact, signaling, intervention effects, or biological mechanisms.
7. **Predictive validation must respect the sampling hierarchy.** Use patient-, slide-, site-, time-, or spatially blocked validation when random row splitting would leak information.
8. **Aligned-image workflows require identical masks and feature order.** All subjects must share registration, coordinate space, resolution, preprocessing version, and pixel/voxel correspondence.
9. **Mediation estimates are model-based.** Temporal ordering, positivity, consistency, specification, and confounding assumptions must be defended independently.
10. **Advanced engines can exceed public-host resources.** Run large ISPat, GP–GHS, and ISPat 3D analyses locally, on institutional HPC, Posit Connect, or a dedicated container host.
11. **Review convergence, uncertainty, multiplicity, and robustness.** The application does not replace statistical or domain review.
12. **Citation is required.** Users acknowledge this before execution. Result bundles include the Workbench DOI and method-specific references.

## Using the public Shiny application

1. [Launch the public Workbench](https://sagnikbhadury.shinyapps.io/spatial-methods-workbench/).
2. Start with the synthetic demonstration to learn the column map and readiness system.
3. Upload a `.csv` containing one row per unit required by the chosen pipeline.
4. Map x/y/z coordinates, region/zone, sample or volume ID, outcome, exposure, mediator, and numeric features. Leave unused roles unselected.
5. Inspect **Readiness**. Every blocked path names the missing input or server engine.
6. Select only prespecified scientific features; exclude identifiers, leakage variables, and post-outcome measurements.
7. Set the method controls, acknowledge citation, and run.
8. Review the figure and numerical table. The application deliberately provides no automated result narrative.
9. Download the reproducibility bundle and preserve it with the frozen analysis dataset and protocol.
10. Contact Sagnik Bhadury for interpretation, deployment planning, or collaboration.

The free public host may sleep when inactive and has active-hour, memory, runtime, and concurrency limits. A cold start can take several seconds. A browser session is not a durable job queue; do not rely on it for a long production analysis.

## Input formats

### Cell-, spot-, or location-level spatial data

Use one row per cell, spot, spatial location, or field-level observation. Include consistent numeric x/y coordinates, optional z/section/depth, a region or density zone, a sample/patient/field/volume ID, and numeric marker or expression features. Repeated measurements and nested sampling must be identified and addressed in the analysis design.

### Tumor contours

Use one row per ordered boundary point with contour ID and numeric x/y coordinates. Each contour needs at least six ordered points, and at least five contours are required. The app does not repair unordered or self-intersecting boundaries.

### Scalar-on-image wide data

Use one row per subject, map a numeric scalar outcome, and select aligned pixel, voxel, or image-derived numeric columns. The interactive ridge screen accepts up to 5,000 selected image features. It is explicitly not the full Bayesian SV-NN or ST-CAR posterior algorithm.

### Image-to-image wide data

Use one row per subject. Name aligned predictor-image columns `input__*` and outcome-image columns `output__*`, then select both groups. At least three columns per group and 30 complete subjects are required. The interactive path is a low-rank screen related to—not mislabeled as—the full Bayesian SBLF engine.

### Three-dimensional ISPat data

Use one row per volumetric cell/location with x/y/z coordinates, zone, volume/spot ID, and multiple numeric markers. Serial sections must already be registered to a common 3D coordinate system. Validate orientation, section spacing, missing sections, masks, and zone consistency.

## Pipeline input matrix

| Pipeline | Minimum input | Important boundary |
|---|---|---|
| Spatial maps and Moran's I | x, y, numeric feature | Descriptive under the selected neighbor graph |
| Conditional networks | three or more numeric features; optional zone | Exploratory ridge network |
| ISPat 2D | x, y, zone, markers, installed `ISPAT` | Intensive Bayesian/variational engine |
| GP–GHS | x, y, markers, installed `GPGHS` | MCMC and shrinkage settings require review |
| ISPat 3D | x, y, z, zone, ID, markers, installed `ISPAT3D` | Registered 3D data and substantial compute |
| Spatial ML prediction | outcome plus three or more features | Random split is exploratory |
| Spatial phenotype clustering | x, y, three or more features | Coordinate influence and cluster count are chosen |
| Shallow-neural prediction | outcome plus three or more features | Numeric or binary outcome; max 250 predictors |
| Wide-image scalar screen | numeric outcome plus five or more image features | Max 5,000 aligned features |
| Latent image-to-image screen | three or more `input__*` and `output__*` features | Registered paired images |
| Mediation | numeric exposure, mediator, outcome | Not automatically causal |
| Shape PCA | ID and ordered x/y landmarks | Five or more valid contours |

## Prepare real-life data

Create a frozen analysis dataset and data dictionary before opening the app:

- define the unit of analysis and nested/repeated-measure structure;
- remove direct and indirect identifiers;
- preserve a read-only raw-data copy separately;
- document assay, segmentation, registration, transformation, normalization, and filtering versions;
- verify axes, units, origins, orientation, and section spacing;
- harmonize feature names and identities across samples;
- assess missingness, zero variance, extremes, sparsity, and class imbalance;
- prespecify train/test grouping and prevent patient/slide/spatial leakage;
- prespecify zones, outcomes, exposures, mediators, primary contrasts, and tuning choices where possible;
- maintain exclusions, checksums, software versions, and a provenance log.

## Install the complete suite locally

Local installation is recommended for real data, sensitive information, long Bayesian jobs, and reproducible production studies.

### 1. Prerequisites

- Git
- R 4.5.x or a compatible current R release
- RStudio (optional)
- Rtools matching the installed R version on Windows when compilation is required
- sufficient memory/CPU; real Bayesian and 3D analyses may require a workstation or cluster

### 2. Clone the application

```text
git clone https://github.com/sagnikbhadury/SpatialMethodsWorkbench.git
cd SpatialMethodsWorkbench
```

### 3. Install interface and built-in dependencies

Run in R:

```r
install.packages(c(
  "shiny", "bslib", "DT", "ggplot2", "jsonlite",
  "markdown", "zip", "testthat", "nnet", "remotes"
))
```

### 4. Install all public advanced engines

Run in R:

```r
remotes::install_github("sagnikbhadury/GP-GHS", upgrade = "never")
remotes::install_github("sagnikbhadury/ISPAT-3D", upgrade = "never")
remotes::install_github("sagnikbhadury/ISPAT", upgrade = "never")
```

This installs the `GPGHS`, `ISPAT3D`, and `ISPAT` packages and their declared dependencies. ISPAT uses Stan; first installation and model compilation may take substantial time. Freeze package/compiler versions for formal analyses.

### 5. Verify the installation

From the repository directory:

```text
Rscript tests/testthat.R
```

In R:

```r
stopifnot(
  requireNamespace("ISPAT", quietly = TRUE),
  requireNamespace("ISPAT3D", quietly = TRUE),
  requireNamespace("GPGHS", quietly = TRUE)
)
```

### 6. Run only on the local machine

```r
shiny::runApp(".", host = "127.0.0.1", port = 3838)
```

Open `http://127.0.0.1:3838`. The `127.0.0.1` binding prevents access from other machines. Do not expose the port publicly without authentication, TLS, firewall controls, upload limits, monitoring, and a reviewed retention policy.

## Docker installation

Built-in workflows:

```text
docker compose up --build
```

Image with public advanced engines:

```text
docker build --build-arg INSTALL_ADVANCED_ENGINES=true -t spatial-methods-workbench:advanced .
docker run --rm -p 127.0.0.1:3838:3838 spatial-methods-workbench:advanced
```

Pin the image and dependency revisions for production. Do not mount sensitive directories read-write unless explicitly required.

## Choosing a deployment

- **shinyapps.io:** public demonstrations and moderate exploratory workloads; no PHI.
- **Local workstation:** sensitive or moderate real-data work under local controls.
- **Institutional HPC:** long Bayesian, MCMC, high-dimensional imaging, and 3D workloads; run through an approved batch workflow.
- **Posit Connect:** authenticated organizational access, process controls, managed content, and audit-oriented deployment.
- **Dedicated container host:** maximum control over CPU, memory, queues, authentication, logs, and retention.

## Reproducibility bundle

The download includes a results table, figure when applicable, `manifest.json`, R result object, `CITATION.txt`, and `COLLABORATION.txt`. It contains no automated interpretation and no LLM prompt. The original input should be preserved separately under the study's governance plan; it is not duplicated into the bundle.

## Citation

Current release:

> Bhadury, S. (2026). *SpatialMethodsWorkbench: Spatial Methods Workbench* (v0.2.1) [Computer software]. Zenodo. [https://doi.org/10.5281/zenodo.21764196](https://doi.org/10.5281/zenodo.21764196)

The all-versions DOI is [10.5281/zenodo.21763606](https://doi.org/10.5281/zenodo.21763606). Also cite every method-specific publication included in the downloaded citation file.

## Support and collaboration

For method selection, study-specific interpretation, deployment architecture, or collaboration, email [bhadury@umich.edu](mailto:bhadury@umich.edu?subject=Spatial%20Methods%20Workbench%20collaboration). Include only a non-sensitive study summary in the initial message; do not email protected data.
