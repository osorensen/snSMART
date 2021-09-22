
# snSMART

The aim of the **snSMART** R package is to consolidate data simulation,
sample size calculation and analysis functions for several snSMART
(small sample sequential, multiple assignment, randomized trial) designs
under one library.


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

Chao, Y.C., Trachtman, H., Gipson, D.S., Spino, C., Braun, T.M. and
Kidwell, K.M., 2020. Dynamic treatment regimens in small n, sequential,
multiple assignment, randomized trials: An application in focal
segmental glomerulosclerosis. Contemporary clinical trials, 92,
p.105989.

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

Wei, B., Braun, T.M., Tamura, R.N. and Kidwell, K., 2020. Sample size
determination for Bayesian analysis of small n sequential, multiple
assignment, randomized trials (snSMARTs) with three agents. Journal of
Biopharmaceutical Statistics, 30(6), pp.1109-1120.

Wei, B., Braun, T.M., Tamura, R.N. and Kidwell, K.M., 2018. A Bayesian
analysis of small n sequential multiple assignment randomized trials
(snSMARTs). Statistics in medicine, 37(26), pp.3723-3732.
