---
layout: page
title: Projects
---

Since I run simulations and work with large datasets, my code needs to work quickly and reliably, and run on a new dataset or specification with very little hassle.

<ul>
<li> <a href="http://github.com/esantorella/tva">teacher value-added</a> implements the value-added algorithm described in Thomas Kane and Doug Staiger's <a href = "http://www.nber.org/papers/w14607">Estimating Teacher Impacts on Student Achievement: An Experimental Evaluation</a>. I incorporate a modification from Chetty, Friedman, and Rockoff's <a href ="http://www.rajchetty.com/chettyfiles/w19424.pdf">Measuring the Impacts of Teachers II: Teacher Value-Added and Student Outcomes in Adulthood</a>: when residualizing outcomes, the coefficients on covariates are estimated using within-teacher variation. 
</li>
<li> <a href="http://github.com/esantorella/hdfe">hdfe</a> runs regressions with high-dimensional fixed effects. At this point, it's not faster than creating a lot of dummies and solving x \ y by brute force. I probably shouldn't even have it on here, but I didn't want to have to call this page "Project."
</li>
</ul>
