---
layout: page
title: Projects
---

Since I run simulations and work with large datasets, my code needs to work 
quickly and reliably, and run on a new dataset or specification with very little hassle.

<ul>
<li> <a href="http://github.com/esantorella/tva">teacher value-added</a> implements the value-added algorithm described in Thomas Kane and Doug Staiger's <a href = "http://www.nber.org/papers/w14607">Estimating Teacher Impacts on Student Achievement: An Experimental Evaluation</a>. I incorporate a modification from Chetty, Friedman, and Rockoff's <a href ="http://www.rajchetty.com/chettyfiles/w19424.pdf">Measuring the Impacts of Teachers II: Teacher Value-Added and Student Outcomes in Adulthood</a>: when residualizing outcomes, the coefficients on covariates are estimated using within-teacher variation. 
</li>
<li> <a href="http://github.com/esantorella/hdfe">hdfe</a> runs regressions with 
high-dimensional fixed effects from Python. The "brute force" option uses a sparse least squares solver
and appears to be fastest in test cases. The package also implements the "method of alternating
projections" used in Simen Gaure's R package
<a href ="https://cran.r-project.org/web/packages/lfe/lfe.pdf">lfe</a>
with a C++ back end.
</li>
</ul>
