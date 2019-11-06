
<!-- README.md is generated from README.Rmd. Please edit that file -->

<!-- badges: start -->

[![Travis build
status](https://travis-ci.org/AustralianAntarcticDivision/palr.svg?branch=master)](https://travis-ci.org/AustralianAntarcticDivision/palr)
[![AppVeyor build
status](https://ci.appveyor.com/api/projects/status/github/AustralianAntarcticDivision/palr?branch=master&svg=true)](https://ci.appveyor.com/project/AustralianAntarcticDivision/palr)
[![Codecov test
coverage](https://codecov.io/gh/AustralianAntarcticDivision/palr/branch/master/graph/badge.svg)](https://codecov.io/gh/AustralianAntarcticDivision/palr?branch=master)
[![CRAN
status](https://www.r-pkg.org/badges/version/palr)](https://CRAN.R-project.org/package=palr)
[![CRAN\_Download\_Badge](http://cranlogs.r-pkg.org/badges/silicate)](https://cran.r-project.org/package=silicate)
<!-- badges: end -->

# palr

`palr` provides colour palettes for data, based on some well known
remotely sensed data sets for sea ice concentration, sea surface
temperature and chlorophyll-a. It includes function `image_pal()` to
create the data used by the `image()` function *as colours*.

There are five main ways of working with palr palette functions, which
have names like `ice_pal()`, `chl_pal()` and `sst_pal()` for ice,
chlorophyll-a and sst respectively and `mk_timePal` for creating a
time-mapped palette function.

  - `ice_pal(n)` return n colours from the palette
  - `ice_pal(data)` return the right colour for values in `data`
  - `ice_pal(palette = TRUE)` returns the entire palette, with colours
    `cols` and intervals `breaks`
  - `tfun <- mk_timePal(datetimes, pal); plot(x, tfun(dt))` match
    date-times to a palette, or palette function.
  - `image_pal(data, col = colors, breaks = breaks)` emulates the
    behaviour of `image()` but return colours as data rather than draw a
    plot

There is a vignette illustrating basic usage, this can be read on CRAN
or loaded from within R.

[palr
vignette](https://cran.r-project.org/web/packages/palr/vignettes/palr.html)

Run this code to load the vignette within R:

``` r
library(palr)
vignette("palr")
```

## Installation

Install the current release from CRAN using

``` r
install.packages("palr")
```

The easiest way to install the github version of `palr` is through the
`devtools` package:

``` r
library(devtools)
install_github("AustralianAntarcticDivision/palr")
```

If you don’t have `devtools` installed you should first run

``` r
install.packages('devtools')
```

-----

Please note that the palr project is released with a [Contributor Code
of
Conduct](https://contributor-covenant.org/version/1/0/0/CODE_OF_CONDUCT.html).
By contributing to this project, you agree to abide by its terms.
