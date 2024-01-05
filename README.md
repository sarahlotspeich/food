# Combining straight-line and map-based distances to investigate the connection between proximity to healthy foods and disease

This repository contains R code and simulation data to reproduce results from the manuscript by Lotspeich, Mullan, D'Agostino McGowan, and Hepler (2023+). These simulations rely on the `possum` package, which implements the multiple imputation approach for covariate measurement error in Poisson regression from the paper. The package can be found in its own repo [here](https://github.com/sarahlotspeich/possum), and installed in `R` as follows:

``` r
# Run once
# install.packages("devtools")
devtools::install_github("sarahlotspeich/possum", ref = "main")
```

## Tables 

**Table 1.** Simulation results under increasing severity of errors in straight-line proximity to healthy foods, as controlled by the error standard deviation $\sigma_U$.

  - [Script (Run Simulations Locally)](sims-scripts/sims_vary_sigmaU.R)
  - [Script (Run Simulations on a Cluster)](sims-scripts/sims_vary_sigmaU_cluster.R)
  - [Script (Make Table)](table-scripts/table1_vary_sigmaU.R)
  - [Data (Simulation Results)](sims-data/vary_sigmaU_sims_combined.csv)

**Table 2.** Simulation results under increasing proportion of neighborhoods queried to obtain map-based proximity to healthy foods, as controlled by $p_V$.

  - [Script (Run Simulations Locally)](sims-scripts/sims_vary_pV.R)
  - [Script (Run Simulations on a Cluster)](sims-scripts/sims_vary_pV_cluster.R)
  - [Script (Make Table)](table-scripts/table2_vary_pV.R)
  - [Data (Simulation Results)](sims-data/vary_pV_sims_combined.csv)

**Table 3.** Simulation results under higher disease prevalence and prevalence ratios for map-based proximity to healthy foods, as controlled by the coefficients $\beta_0$ (**Prev.** $=\exp(\beta_0)$) and $\beta_1$ (**PR** $=\exp(\beta_1)$), respectively.

  - [Script (Run Simulations Locally)](sims-scripts/sims_vary_prev.R)
  - [Script (Run Simulations on a Cluster)](sims-scripts/sims_vary_prev_cluster.R)
  - [Script (Make Table)](table-scripts/table3_vary_prev.R)
  - [Data (Simulation Results)](sims-data/vary_prev_sims_combined.csv)

**Table 4.** Simulation results under increasingly severe multiplicative errors in straight-line proximity to healthy foods, as controlled by the max of the error distribution $\tau_W$. 

  - [Script (Run Simulations Locally)](sims-scripts/sims_mult_error.R)
  - [Script (Run Simulations on a Cluster)](sims-scripts/sims_vary_mult_error_cluster.R)
  - [Script (Make Table)](table-scripts/table4_mult_error.R)
  - [Data (Simulation Results)](sims-data/mult_error_sims_combined.csv)

**Table S1.** Simulation results under increasing severity of errors in straight-line proximity to healthy foods, as controlled by the error mean $\mu_U$.

  - [Script (Run Simulations Locally)](sims-scripts/sims_vary_muU.R)
  - [Script (Run Simulations on a Cluster)](sims-scripts/sims_vary_muU_cluster.R)
  - [Script (Make Table)](table-scripts/tableS1_vary_muU.R)
  - [Data (Simulation Results)](sims-data/vary_muU_sims_combined.csv)  

## Figures 

**Figure 1.** Straight-line and map-based distances from Reynolda House (square symbol) to a nearby Food Lion grocery store (triangle symbol) in Winston-Salem, North Carolina.

  - [Figure](figures/fig1_map_comparing_distances.png)
  - [Script (Make Figure)](figure-scripts/fig1_map_comparing_distances.R)

**Figure S1.** Estimated log prevalence ratios for food access $X$ on health. The five possible ways to include the analysis model outcome in the imputation model for $X$ were considered. 

## Data 

**Grocery Stores (from the [USDA SNAP Retail Locator](https://www.fns.usda.gov/snap/retailer-locator) 

  - [Script (Run Simulations Locally)](sims-scripts/sims_incl_outcome.R)
