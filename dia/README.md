# Datasets of diagnostic data

Each file named

    res_METx_YYYYDDD_YYYYDDD_vvvv-ttttttt_mmmmm_nn
    
contains diagnostic residual data from the optimisation run for the Meteosat-'x' satellite. The first date `YYYYDDD` of the folder name designates the begin of the retrieval period, the second date designates its end.

## File format

The plain text residual data files contain several columns of data separated by blank characters. 

**Column 1**
:  Uncertainty-normalised digital count residual

**Column 2**
:  Digital count residual

**Column 3**
:  Time of observation (day since launch)

**Column 4**
:  Target type `1 = desert`, `2 = ocean`, `4 = DCC over ocean`, `8 = DCC over land`

**Column 5**
:  Digital count number resulting from the forward model

**Column 6**
:  Digital count number taken by the satellite (for the Earth view)

**Column 7**
:  Digital count number taken by the satellite (for the Space view)

**Column 8**
:  Total uncertainty of residual digital count number

**Column 9**
:  Uncertainty of residual digital count number due to Bernstein approximation

**Column 10**
:  Uncertainty of residual digital count number due to errors in pixel extraction process

**Column 11**
:  Uncertainty of residual digital count number due to errors in radiativr transfer modelling

**Column 12**
:  Sun zenith angle (degree)

**Column 13**
:  View zenith angle (degree)

**Column 14**
:  Name of matchup data file 
