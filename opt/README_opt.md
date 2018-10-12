# Datasets of optimised forward model parameters.

Each file named

    opt_METx_YYYYDDD_YYYYDDD_vvvv-ttttttt_mmmmm_nn.dat
    
contains contains the optimised forward model parameters from the optimisation run for the Meteosat-'x' satellite. The first date `YYYYDDD` of the file name designates the begin of the retrieval period, the second date designates its end.

## File format

The plain text parameter data files contain the optimised parameter values and their uncertainties, the posterior parameter error covariance matrix, and the Hessian matrix of the cost function at its minimum.
