# Datasets of diagnostic residual data

Each file named

    res_METx_yyyyddd_yyyyddd_vvvv-ttttttt_mmmmm_nn.dat
    
contains residual data from the optimisation run for the Meteosat-`x` satellite. The first date `yyyyddd` of the file name designates the begin of the retrieval period, the second date designates its end.

## File format

The plain text residual data files contain several columns of data separated by blank characters. 

| Column | Description                                                                             | Variable                             |
|--------|-----------------------------------------------------------------------------------------|--------------------------------------|
| 1      | Uncertainty-normalised digital count residual (a zero value indicates a rejected datum) | -                                    |
| 2      | Digital count residual (a zero value indicates a rejected datum)                        | *C*<sub>R</sub>                      |
| 3      | Time of observation (day since launch)                                                  | *t*                                  |
| 4      | Target type `1 = desert`, `2 = ocean`, `4 = DCC over ocean`, `8 = DCC over land`        | *s*                                  |
| 5      | Digital count number resulting from the forward model                                   | *C*<sub>*L*</sub>                     |
| 6      | Digital count number for Earth target                                                   | *C*<sub>E</sub>                      |
| 7      | Digital count number for Space target                                                   | *C*<sub>S</sub>                      |
| 8      | Total uncertainty of residual digital count number                                      | *u*(*C*<sub>R</sub>)                 |
| 9      | Uncertainty of residual digital count number due to Bernstein approximation             | *u*<sub>B</sub>(*C*<sub>R</sub>)     |
| 10     | Uncertainty of digital count number for Earth target                                    | *u*(*C*<sub>E</sub>)                 |
| 11     | Uncertainty of residual digital count number due to errors in the target state vector   | *u*<sub>***x***</sub>(*C*<sub>R</sub>) |
| 12     | Sun zenith angle (degree)                                                               | -                                    |
| 13     | View zenith angle (degree)                                                              | -                                    |
| 14     | Name of matchup data file                                                               | -                                    |

Variable names refer to the nomenclature defined by Quast et al. (2018, *Climate Data Records from Meteosat First Generation: Retrieval of the in-Flight VIS Spectral Response*, [Remote Sensing Special Issue "Assessment of Quality and Usability of Climate Data Records"](https://www.mdpi.com/journal/remotesensing/special_issues/assessment_cdr)).
