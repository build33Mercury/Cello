# Cello 3.2 Sensitivity & Uncertainty

## Local sensitivity

Cello evaluates selected model inputs at low and high values around the active experiment. It reports a finite-difference derivative and normalized elasticity where both the baseline factor and baseline response are non-zero.

Local sensitivity is neighborhood-specific and should not be interpreted as a universal parameter ranking.

## Uncertainty propagation

Cello uses reproducible Latin-hypercube sampling over independent uniform ranges explicitly supplied by the user.

The response is summarized with mean, standard deviation, median, 5th/95th percentiles, minimum and maximum. Standardized regression coefficients and Pearson correlations are provided as screening diagnostics.

## Scientific boundary

Input ranges are assumptions unless justified by data. Computational samples are not biological replicates, and screening metrics do not establish causality.
