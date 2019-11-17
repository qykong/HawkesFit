HawkesFit: simulation, fitting of Hawkes processes
================

## Introduction

This package is designed for simulating and fitting the Hawkes processes
and the HawkesN processes with several options of kernel functions.
Currently, it assumes univariate processes without background event
rates. Prior knowledge about the models is assumed in the following
tutorial and please refer to \[1\] and \[2\] for details about the
models.

``` r
library(HawkesFit)
```

## Installation and dependencies

Several dependencies are required for running this package:

  - poweRlaw (r package, will be installed while installing the
    HawkesFit package)
  - AMPL (download the demo version from
    <https://ampl.com/try-ampl/download-a-free-demo/>)
  - Ipopt (compile from the source code here
    <https://www.coin-or.org/Ipopt/documentation/> so that the linear
    solver ma57 will be available)

Install the package by executing

``` r
if (!require('devtools')) install.packages('devtools')
devtools::install_github('qykong/HawkesFit')
```

## Available models

TODO: show a table of models here with
equations?

## Simulating cascades

Let’s

``` r
lapply(seq(2), function(i) generate_Hawkes_event_series(c(K = 0.8, theta = 1), model_type = 'EXP'))
```

    ## [[1]]
    ##   magnitude time
    ## 1     10000    0
    ## 
    ## [[2]]
    ##   magnitude time
    ## 1     10000    0

## Fitting a model on data

## Acknowledgement

The development of this package is supported by the Green Policy grant
from the National Security College, Crawford School, ANU.

## Reference

\[1\] Rizoiu, Marian-Andrei, et al. “Hawkes processes for events in
social media.” Frontiers of Multimedia Research. Association for
Computing Machinery and Morgan & Claypool, 2017.

\[2\] Rizoiu, Marian-Andrei, et al. “SIR-Hawkes: Linking epidemic models
and Hawkes processes to model diffusions in finite populations.”
Proceedings of the 2018 World Wide Web Conference. International World
Wide Web Conferences Steering Committee, 2018. You can also embed plots,
for example:
