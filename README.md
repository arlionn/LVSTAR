<!-- README.md is generated from README.Rmd. Please edit that file -->
LVSTAR version 1.0.0 (RED STAR)
===============================

The PSTR package implements the Logistic Vector Smooth Transition AutoRegression (LVSTAR) modelling.

The modelling procedure consists of three stages: Specification, Estimation and Evaluation. The package offers tools helping the users to conduct model specification tests, to do LVSTAR model estimation, and to do model evaluation.

The heteroskedasticity-consistent tests are implemented in the package. The wild bootstrap tests are also implemented.

Parallel computation (as an option) is implemented in some functions, especially the bootstrap tests. Therefore, the package suits tasks running many cores on super-computation servers.

How to install
--------------

You can install the package by running

``` r
if(!require(devtools)) install.packages("devtools")
devtools::install_github("yukai-yang/LVSTAR")
```

After installing the package, you need to load (attach better say) it by running the code

``` r
library("LVSTAR")
```

You can first check the information and the current version number by running

``` r
version()
#> LVSTAR version 1.0.0 (RED STAR) from GitHub
```

Then you can take a look at all the available functions and data in the package

``` r
ls( grep("LVSTAR", search()) ) 
#> [1] "NewLVSTAR" "sunspot"   "version"
```

The sunspot example
===================

In the package, a data set called "sunspot" is offered to give prompt example. For details of the data set, you can run

``` r
?sunspot
```

Initialization
--------------

You can create a new object of the class PSTR by doing

``` r
star = NewLVSTAR(sunspot,freq=1,start=c(1700,1))
```
