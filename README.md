
<!-- README.md is generated from README.Rmd. Please edit that file -->

# gregorian

<!-- badges: start -->

[![CRAN
status](https://www.r-pkg.org/badges/version/gregorian)](https://cran.r-project.org/package=gregorian)
[![Build
Status](https://travis-ci.org/edgararuiz/gregorian.svg?branch=master)](https://travis-ci.org/edgararuiz/gregorian)
[![Coverage
status](https://codecov.io/gh/edgararuiz/gregorian/branch/master/graph/badge.svg)](https://codecov.io/github/edgararuiz/gregorian?branch=master)
<!-- badges: end -->

Provides functions to convert between the gregoriann calendar dates and
Gregorian dates.

## Installation

And the development version from [GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("edgararuiz/gregorian")
```

``` r
as.Date("-99-7-12")
```

    Error in charToDate(x) : 
      character string is not in a standard unambiguous format

``` r
library(gregorian)
as_gregorian("-99-7-12")
#> Friday July 12, 100 BCE
```

``` r
born <- as_gregorian("-99-7-12")

diff_days(born, get_date())
#> [1] 773523
```

``` r
add_days(get_date(), 365)
#> Monday May 11, 2020 CE
```
