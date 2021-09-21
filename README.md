
# snSMART

The aim of the **snSMART** R package is to consolidate data simulation,
sample size calculation and analysis functions for several snSMART
(small sample sequential, multiple assignment, randomized trial) designs
under one library.

An snSMART is a multi-stage trial design where for a two-stage design,
randomization in the second stage depends on the outcome to first stage
treatment. snSMART designs require that the same outcome is measured at
the end of the first stage and at the end of the second stage.
Additionally, the length of the first stage of the trial must be the
same amount of time as the length for the second stage. snSMARTs are
motivated by obtaining more information from a small sample of
individuals with the primary goal to identify the superior first stage
treatment or dosage level using both stages of data. Data are shared
across the two stages of the snSMART design to more precisely estimate
the effect of the treatments given in the first stage.

## Installation

You can download and install **snSMART** with:

``` r
# Install devtools first if you haven't done so
library(devtools)
# install snSMART
devtools::install_github("sidiwang/snSMART")
library(snSMART)
```

## snSMART designs and functions covered in this package

-   Standard snSMART (3 active treatments, non-responders re-randomized;
    binary outcome)
    -   data simulation function - `data_simulation`
    -   Bayesian Joint Stage Model (BJSM) analysis function -
        `BJSM_binary`
    -   Log Poisson Joint Stage Model (JSRM) analysis function -
        `JSRM_binary`
    -   sample size calculation function - `sample_size`
    -   Group Sequential snSMART simulation function -
        `sim_group_seq_1step` `sim_group_seq_2step` and BJSM analysis
        function - `group_seq`
-   Dose level snSMART (3 dose level: placebo, low, high dose; binary
    outcome)
    -   data simulation function - `data_simulation_dose`
    -   BJSM analysis function - `BJSM_dose_binary`
    -   Log Poisson Joint Stage Model analysis function -
        `JSRM_dose_binary`
-   snSMART with mapping function (3 active treatments, re-randomization
    depends on continuous outcome at stage 1; continuous outcomes)
    -   data simulation function - `c_trialDataGen` `c_trialSim`
    -   BJSM analysis function - `BJSM_c`

## References

Wei, B., Braun, T.M., Tamura, R.N. and Kidwell, K.M., 2018. A Bayesian
analysis of small n sequential multiple assignment randomized trials
(snSMARTs). Statistics in medicine, 37(26), pp.3723-3732.

Chao, Y.C., Braun, T.M., Tamura, R.N. and Kidwell, K.M., 2020. A
Bayesian group sequential small n sequential multiple‐assignment
randomized trial. Journal of the Royal Statistical Society: Series C
(Applied Statistics), 69(3), pp.663-680.

Fang, F., Hochstedler, K.A., Tamura, R.N., Braun, T.M. and Kidwell,
K.M., 2021. Bayesian methods to compare dose levels with placebo in a
small n, sequential, multiple assignment, randomized trial. Statistics
in Medicine, 40(4), pp.963-977.

Hartman, H., Tamura, R.N., Schipper, M.J. and Kidwell, K.M., 2021.
Design and analysis considerations for utilizing a mapping function in a
small sample, sequential, multiple assignment, randomized trials with
continuous outcomes. Statistics in Medicine, 40(2), pp.312-326.
