
<!-- README.md is generated from README.Rmd. Please edit that file -->

# ggsegTracula

<!-- badges: start -->

[![Travis build
status](https://travis-ci.com/LCBC-UiO/ggsegTracula.svg?branch=master)](https://travis-ci.com/LCBC-UiO/ggsegTracula)
[![AppVeyor build
status](https://ci.appveyor.com/api/projects/status/github/LCBC-UiO/ggsegTracula?branch=master&svg=true)](https://ci.appveyor.com/project/LCBC-UiO/ggsegTracula)
[![Codecov test
coverage](https://codecov.io/gh/LCBC-UiO/ggsegTracula/branch/master/graph/badge.svg)](https://codecov.io/gh/LCBC-UiO/ggsegTracula?branch=master)
[![R build
status](https://github.com/LCBC-UiO/ggsegTracula/workflows/R-CMD-check/badge.svg)](https://github.com/LCBC-UiO/ggsegTracula/actions)
<!-- badges: end -->

This package contains dataset for plotting the Tracula white matter
tracts with ggseg and ggseg3d.

Yendiki et al. (2011) *Automated probabilistic reconstruction of
white-matter pathways in health and disease using an atlas of the
underlying anatomy*. Front. Neuroinform. 5:23.
[doi: 10.3389/fninf.2011.00023](https://www.ncbi.nlm.nih.gov/pubmed/22016733)

## Installation

You can install the released version of ggsegTracula from
[GitHub](https://github.com/) with:

``` r
# install.packages("remotes")
remotes::install_github("LCBC-UiO/ggsegTracula")
```

``` r
library(ggseg)
#> Loading required package: ggplot2
library(ggseg3d)
library(ggsegTracula)
library(dplyr)
#> 
#> Attaching package: 'dplyr'
#> The following objects are masked from 'package:stats':
#> 
#>     filter, lag
#> The following objects are masked from 'package:base':
#> 
#>     intersect, setdiff, setequal, union

plot(tracula) +
  theme(legend.position = "bottom", 
        legend.text = element_text(size = 9)) +
  guides(fill = guide_legend(ncol = 3))
```

<img src="man/figures/README-unnamed-chunk-2-1.png" width="100%" />

``` r
ggseg3d(atlas = tracula_3d) %>% 
  add_glassbrain() %>% 
  pan_camera("right lateral")
```

<img src="man/figures/README-3d-plot.png" width="100%" />

Please note that the ‘ggsegTracula’ project is released with a
[Contributor Code of Conduct](CODE_OF_CONDUCT.md). By contributing to
this project, you agree to abide by its terms.
