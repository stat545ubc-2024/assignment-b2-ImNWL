
<!-- README.md is generated from README.Rmd. Please edit that file -->

# MissingCounter

<!-- badges: start -->
<!-- badges: end -->

The goal of MissingCounter is to provide a straightforward way to
identify and count missing values across columns in a dataset, grouped
by a specified variable. This package can be particularly useful for
exploratory data analysis, as it allows users to quickly assess patterns
of missing data within groups, making data cleaning and preprocessing
more efficient.

## Installation

You can install the development version of MissingCounter using
github_install() from devtools as shown below:

1.  Install devtools:

``` r
install.packages("devtools")
```

2.  Load devtools:

``` r
library(devtools)
```

3.  Install this package from github:

``` r
install_github("stat545ubc-2024/assignment-b2-ImNWL")
```

## Example

This is a basic example which shows you how to solve a common problem:

``` r
library(MissingCounter)

# Count missing values in the airquality dataset by month
result <- count_all_missing_by_group(airquality, Month)
print(result)
#> # A tibble: 5 × 6
#>   Month Ozone Solar.R  Wind  Temp   Day
#>   <int> <int>   <int> <int> <int> <int>
#> 1     5     5       4     0     0     0
#> 2     6    21       0     0     0     0
#> 3     7     5       0     0     0     0
#> 4     8     5       3     0     0     0
#> 5     9     1       0     0     0     0
```
