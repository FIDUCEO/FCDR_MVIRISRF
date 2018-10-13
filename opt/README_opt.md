# Datasets of optimised forward model parameters

Each file named

    opt_METx_YYYYDDD_YYYYDDD_vvvv-ttttttt_mmmmm_nn.dat
    
contains contains the optimised forward model parameters from the optimisation run for the Meteosat-`x` satellite. The first date `YYYYDDD` of the file name designates the begin of the retrieval period, the second date designates its end.

## File format

The plain text parameter data files contain the optimised parameter values and their uncertainties, the posterior parameter error covariance matrix, and the Hessian matrix of the cost function at its minimum.

Optimised parameters and uncertainties are specified in three-column data columns. The first column designates the parameter index number, while the second and third column designate the optimised values and uncertainties. For example:

        1  0.260377E-003  0.242215E-005
        2  0.234858E+001  0.741508E-001
        3  0.452075E+000  0.455102E-001
        4  0.106871E-001  0.102577E-002
        5 -0.119573E-001  0.732034E-003
        6  0.968870E-002  0.949073E-003
        7  0.100359E-001  0.935150E-003
        8  0.372498E+000  0.167455E-001
        9  0.118287E+001  0.806566E-002
       10  0.678764E+000  0.540245E+000
       11  0.160791E+001  0.242125E+000
       12 -0.179228E-002  0.326212E+000
       13 -0.116949E-002  0.390038E+000
       14  0.133387E+001  0.330975E+000
       15  0.149357E+001  0.277306E+000
       16 -0.107799E-002  0.748840E+000
       17 -0.646605E+000  0.198666E+000
       18  0.481291E-003  0.245661E+000

The posterior parameter error covariance matrix is specified in a similar format. The first column designates the parameter index number, while the remaining columns designate the elements of the matrix. For example:

        1  0.586680E-011 -0.156556E-007 -0.161137E-007 -0.419183E-010 -0.881226E-011  0.854905E-010  0.165812E-010  0.160319E-008  0.100513E-009  0.608859E-007 -0.281826E-007 -0.287160E-010 -0.220725E-010  0.361594E-007 -0.250318E-007 -0.609146E-010 -0.877726E-008 -0.100938E-010
        2 -0.156556E-007  0.549834E-002  0.336271E-002  0.165072E-004  0.297909E-005 -0.185046E-004 -0.174265E-004 -0.284803E-003  0.494895E-005 -0.104741E-001  0.511910E-002  0.218367E-005  0.153067E-005 -0.619085E-002  0.518042E-002  0.430848E-005  0.419399E-002  0.873624E-006
        3 -0.161137E-007  0.336271E-002  0.207118E-002  0.942266E-005  0.192217E-005 -0.109512E-004 -0.102514E-004 -0.164466E-003  0.233515E-005 -0.607485E-002  0.298420E-002  0.139505E-005  0.975265E-006 -0.364307E-002  0.302026E-002  0.273150E-005  0.237888E-002  0.572681E-006
        4 -0.419183E-010  0.165072E-004  0.942266E-005  0.105221E-005  0.128609E-007 -0.137932E-007 -0.523070E-008 -0.540828E-005 -0.279709E-006 -0.205961E-003  0.103444E-003  0.122439E-006  0.879763E-007 -0.163067E-003  0.130075E-003  0.219117E-006  0.494043E-004  0.458993E-007
        5 -0.881226E-011  0.297909E-005  0.192217E-005  0.128609E-007  0.535873E-006  0.326790E-008  0.393218E-008 -0.877231E-006 -0.702956E-007 -0.343668E-004  0.163128E-004  0.210244E-007  0.153641E-007 -0.229857E-004  0.182765E-004  0.366934E-007  0.530968E-005  0.562904E-008
        6  0.854905E-010 -0.185046E-004 -0.109512E-004 -0.137932E-007  0.326790E-008  0.900739E-006  0.835633E-006  0.583968E-005  0.335685E-006  0.223232E-003 -0.111302E-003 -0.130522E-006 -0.945085E-007  0.168865E-003 -0.135919E-003 -0.234495E-006 -0.494809E-004 -0.456801E-007
        7  0.165812E-010 -0.174265E-004 -0.102514E-004 -0.523070E-008  0.393218E-008  0.835633E-006  0.874506E-006  0.561539E-005  0.332856E-006  0.215313E-003 -0.107653E-003 -0.128969E-006 -0.929873E-007  0.164438E-003 -0.131985E-003 -0.230835E-006 -0.463730E-004 -0.464559E-007
        8  0.160319E-008 -0.284803E-003 -0.164466E-003 -0.540828E-005 -0.877231E-006  0.583968E-005  0.561539E-005  0.280411E-003  0.273527E-004  0.896468E-002 -0.395032E-002 -0.561931E-005 -0.434241E-005  0.503554E-002 -0.382860E-002 -0.948588E-005 -0.690465E-003 -0.426666E-007
        9  0.100513E-009  0.494895E-005  0.233515E-005 -0.279709E-006 -0.702956E-007  0.335685E-006  0.332856E-006  0.273527E-004  0.650548E-004  0.106127E-002 -0.492275E-003 -0.888476E-006 -0.886717E-006  0.750219E-003 -0.496758E-003 -0.455931E-005  0.585244E-003 -0.949946E-006
       10  0.608859E-007 -0.104741E-001 -0.607485E-002 -0.205961E-003 -0.343668E-004  0.223232E-003  0.215313E-003  0.896468E-002  0.106127E-002  0.291865E+000 -0.130205E+000 -0.241073E-003 -0.167719E-003  0.166654E+000 -0.125144E+000 -0.331664E-003 -0.198003E-001  0.198937E-005
       11 -0.281826E-007  0.511910E-002  0.298420E-002  0.103444E-003  0.163128E-004 -0.111302E-003 -0.107653E-003 -0.395032E-002 -0.492275E-003 -0.130205E+000  0.586246E-001  0.175638E-003  0.950566E-004 -0.757288E-001  0.565775E-001  0.158782E-003  0.855169E-002 -0.310163E-005
       12 -0.287160E-010  0.218367E-005  0.139505E-005  0.122439E-006  0.210244E-007 -0.130522E-006 -0.128969E-006 -0.561931E-005 -0.888476E-006 -0.241073E-003  0.175638E-003  0.106414E+000  0.280417E-007  0.366726E-004 -0.869454E-005  0.107116E-006 -0.232192E-004 -0.920970E-008
       13 -0.220725E-010  0.153067E-005  0.975265E-006  0.879763E-007  0.153641E-007 -0.945085E-007 -0.929873E-007 -0.434241E-005 -0.886717E-006 -0.167719E-003  0.950566E-004  0.280417E-007  0.152130E+000  0.115686E-003 -0.305543E-004  0.963799E-007 -0.236197E-004 -0.306624E-008
       14  0.361594E-007 -0.619085E-002 -0.364307E-002 -0.163067E-003 -0.229857E-004  0.168865E-003  0.164438E-003  0.503554E-002  0.750219E-003  0.166654E+000 -0.757288E-001  0.366726E-004  0.115686E-003  0.109545E+000 -0.881968E-001 -0.391559E-003 -0.221647E-001  0.888088E-005
       15 -0.250318E-007  0.518042E-002  0.302026E-002  0.130075E-003  0.182765E-004 -0.135919E-003 -0.131985E-003 -0.382860E-002 -0.496758E-003 -0.125144E+000  0.565775E-001 -0.869454E-005 -0.305543E-004 -0.881968E-001  0.768984E-001  0.570919E-003  0.306395E-001 -0.206431E-005
       16 -0.609146E-010  0.430848E-005  0.273150E-005  0.219117E-006  0.366934E-007 -0.234495E-006 -0.230835E-006 -0.948588E-005 -0.455931E-005 -0.331664E-003  0.158782E-003  0.107116E-006  0.963799E-007 -0.391559E-003  0.570919E-003  0.560762E+000 -0.349938E-003 -0.404444E-007
       17 -0.877726E-008  0.419399E-002  0.237888E-002  0.494043E-004  0.530968E-005 -0.494809E-004 -0.463730E-004 -0.690465E-003  0.585244E-003 -0.198003E-001  0.855169E-002 -0.232192E-004 -0.236197E-004 -0.221647E-001  0.306395E-001 -0.349938E-003  0.394683E-001  0.435987E-004
       18 -0.100938E-010  0.873624E-006  0.572681E-006  0.458993E-007  0.562904E-008 -0.456801E-007 -0.464559E-007 -0.426666E-007 -0.949946E-006  0.198937E-005 -0.310163E-005 -0.920970E-008 -0.306624E-008  0.888088E-005 -0.206431E-005 -0.404444E-007  0.435987E-004  0.603491E-001

The Hessian matrix is specified in the same format.

## Mapping of parameters to parameter index numbers

The mapping of parameters to parameter index numbers (and vice versa) for the different Meteosat satellites is defined in the Table below.

| **Parameter**         | **MET7** | **MET6** | **MET5** | **MET4** | **MET3** | **MET2** | **Significance**                            |
|-----------------------|----------|----------|----------|----------|----------|----------|---------------------------------------------|
| *&alpha;*<sub>1</sub> | 1        | 1        | 1        | 1        | 1        | 1        | Temporal degradation rate (d<sup>-1</sup>)  |
| *&alpha;*<sub>2</sub> | 2        | 2        | 2        | 2        | 2        | 2        | Spectral degradation rate (µm<sup>-1</sup>) |
| *&alpha;*<sub>3</sub> | 3        | -        | -        | -        | 3        | -        | Logarithm of asymptotic optical thickness   |
| *a*                   | 8        | 7        | 7        | 7        | 9        | 8        | Lower bound (µm)                            |
| *b*                   | 9        | 8        | 8        | 8        | 10       | 9        | Upper bound (µm)                            |
| *&beta;*<sub>1</sub>  | 10       | 9        | 9        | 9        | 11       | 10       | Square root of Bernstein coefficient        |
| *&beta;*<sub>2</sub>  | 11       | 10       | 10       | 10       | 12       | 11       | Square root of Bernstein coefficient        |
| *&beta;*<sub>3</sub>  | 12       | 11       | 11       | 11       | 13       | 12       | Square root of Bernstein coefficient        |
| *&beta;*<sub>4</sub>  | 13       | 12       | 12       | 12       | 14       | 13       | Square root of Bernstein coefficient        |
| *&beta;*<sub>5</sub>  | 14       | 13       | 13       | 13       | 15       | 14       | Square root of Bernstein coefficient        |
| *&beta;*<sub>6</sub>  | 15       | 14       | 14       | 14       | 16       | 15       | Square root of Bernstein coefficient        |
| *&beta;*<sub>7</sub>  | 16       | 15       | 15       | 15       | 17       | 16       | Square root of Bernstein coefficient        |
| *&beta;*<sub>8</sub>  | 17       | 16       | 16       | 16       | 18       | 17       | Square root of Bernstein coefficient        |
| *&beta;*<sub>9</sub>  | 18       | 17       | 17       | 17       | 19       | 18       | Square root of Bernstein coefficient        |
| *&gamma;*             | -        | -        | -        | -        | 8        | 7        | Gain amplification factor                   |
| *&delta;*<sub>1</sub> | 4        | 3        | 3        | 3        | 4        | 3        | Bias (desert)                               |
| *&delta;*<sub>2</sub> | 5        | 4        | 4        | 4        | 5        | 4        | Bias (ocean)                                |
| *&delta;*<sub>3</sub> | 6        | 5        | 5        | 5        | 6        | 5        | Bias (DCC over ocean)                       |
| *&delta;*<sub>4</sub> | 7        | 6        | 6        | 6        | 7        | 6        | Bias (DCC over land)                        |

The parameter refer to the model and nomenclature defined by Quast et al. (2018, *Climate Data Records from Meteosat First Generation: Retrieval of the in-Flight VIS Spectral Response*, [Remote Sensing Special Issue "Assessment of Quality and Usability of Climate Data Records"](https://www.mdpi.com/journal/remotesensing/special_issues/assessment_cdr)).
