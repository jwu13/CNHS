
<!-- README.md is generated from README.Rmd. Please edit that file -->

# CHNS

<!-- badges: start -->

[![Lifecycle:
experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://lifecycle.r-lib.org/articles/stages.html#experimental)
[![CRAN
status](https://www.r-pkg.org/badges/version/surveyjanitor)](https://CRAN.R-project.org/package=surveyjanitor)
[![R-CMD-check](https://github.com/Bettyjpu/chns/actions/workflows/R-CMD-check.yaml/badge.svg)](https://github.com/Bettyjpu/chns/actions/workflows/R-CMD-check.yaml)
<!-- badges: end -->

## Purpose

We wanted to create a package that helps researchers explore China
Health and Nutrition Survey (CHNS) with just a basic R understanding.
The package `surveyjanitor` allows easy access to a wide variety of
information regarding effects of the health, nutrition, and family
planning policies on the health and nutritional status of its
population. CHNS data has both inconsistencies in variable units and
ways of recording N/A values, as well as general inconvenience caused by
panel data. This package aims to provide a clearer and more efficient
way of exploring CHNS Data.

## Target audience

This package can be used by researchers and students who are interested
in using data from China Health and Nutrition Survey (CHNS).
Additionally, anyone who’s interested in using CHNS data and wish to
simplify the data cleaning process are welcomed to use this package as a
data cleaning aid tool.

## Installation

You can install the development version of surveyjanitor like so:

``` r
devtools::install_github("Bettyjpu/chns")
```

## Load

You can load it by:

``` r
library(chns)
```

## Example: Get Real Income with selected base year.

This is a basic example for `real_income()` that returns a tibble with
income weighted over inflation for the selected base year.

``` r
real_income(base_year=1989) 
#> # A tibble: 88,166 × 5
#>           IDind  wave indwage annual_wage_CPI  base
#>           <dbl> <dbl>   <dbl>           <dbl> <dbl>
#>  1 211103001001  1989   1140.           1140.  1989
#>  2 211103001002  1989    940.            940.  1989
#>  3 211103002001  1989   1590.           1590.  1989
#>  4 211103002002  1989    229.            229.  1989
#>  5 211103003003  1989    784.            784.  1989
#>  6 211103003004  1989    784.            784.  1989
#>  7 211103004003  1989    940.            940.  1989
#>  8 211103004004  1989    784.            784.  1989
#>  9 211103005001  1989   1140.           1140.  1989
#> 10 211103005002  1989    784.            784.  1989
#> # … with 88,156 more rows
```

## Project Proposal

We would like to build an R package that makes importing data, tidying
data and data analysis more user friendly for social science data sets,
specifically, we’ll be creating the following functions for The China
Health and Nutrition Survey (CHNS) data. CHNS contains panel data over
two decades and we would like to reduce repetitive data-tidying work for
researchers.

We will be creating the following functions for this project, serving
both data wrangling and data visualization purposes on CHNS data.

### Data Wrangling:

1)  `real_income(base_year)`: This function calculates the
    deflated/inflated real income based on the selected survey year.

2)  `num_of_children(base_year)`: This function returns the number of
    children a woman had up to an inputted year.

### Data Visualization:

3)  `map_china(year)`: This function would potentially map the
    population density by province on the map for the selected year.

For Project Phase 3, we would like to import more data sets from CHNS
and more variables. We plan to create similar data wrangling functions
for the newly imported variables so that that would make data analysis
in R more convenient.

For Data Visualization, we plan to finish mapping by the survey province
and visualize more useful information.

## Group Members

-   Junru Wu
-   Betty Pu
