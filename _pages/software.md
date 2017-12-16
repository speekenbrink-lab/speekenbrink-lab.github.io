---
title: "Speekenbrink lab - Software and code"
layout: default
excerpt: "Speekenbrink lab: Software and code"
sitemap: false
permalink: /software/
---

# Software and code

For statistical/computational modelling, we mainly use <a href="http://www.r-project.org">R</a>. For experiments, we mainly use Python and html/javascript. R packages are hosted on CRAN and R-Forge, but we have recently started to use <a href="https://github.com/speekenbrink-lab">github</a>.


<h2>DepmixS4</h2>
<h4>An R package to estimate mixture and hidden Markov models</h4>
<p>
  DepmixS4 is
  written and maintained by Ingmar Visser and Maarten Speekenbrink and based on Ingmar's earlier depmix package. DepmixS4 has an object-oriented design, providing a flexible interface to fit dependent mixture models with different observation models. Estimation is done by Expectation-Maximisation or numerical optimization of the likelihood using Rsolnp. The current stable release of depmixS4 can be found on <a href="http://cran.r-project.org/web/packages/depmixS4/index.html">CRAN</a>. The latest (beta) version can be found on <a href="http://r-forge.r-project.org/projects/depmix/">R-Forge</a> site.
</p>

<h2>dlrm</h2>
<h4>An R package to estimate dynamic linear regression models</h4>
<p>The Dynamic Lens Model (DLM, Speekenbrink & Shanks, 2010) is used to estimate cue utilization in MCPL tasks. Essentially, the model is a dynamic linear regression model (dlrm). Estimation relies on the Kalman filter/smoother and Expectation-Maximisation. The R package "dlrm" implements this and is hosted on R-Forge. It can be downloaded from this <a href="https://r-forge.r-project.org/R/?group_id=529">link</a>. To install this package directly within R type:</p>
<p><code>install.packages("dlrm", repos="http://R-Forge.R-project.org")</code></p>

<p>At the moment, the documentation is minimal but we hope to correct this in the near future.</p>
