# Dataset of relative MVIRI VIS spectral response functions

Each folder named

    srf_METx_yyyyddd_yyyyddd_vvvv-ttttttt_mmmmm_nn
    
contains the retrieved *relative* in-flight MVIRI VIS spectral response function of the Meteosat-`x` satellite. The first date `yyyyddd` of the folder name designates the begin of the retrieval period, the second date designates its end. Each file

    srf_METx_yyyyddd_yyyyddd_vvvv-ttttttt_mmmmm_nn.dat

included with such a folder provides the relative MVIRI VIS spectral response function for a certain day of a year. The first date `yyyyddd` of the file name designates the begin of the validity period, the second date designates its end. A spectral response data file is provided every 45 days.

## File format

The plain text format of the spectral response files has been defined by EUMETSAT and FastOpt GmbH. The files starts with a header that provides basic information on the retrieval. For example: 

    &HEADER
      CAL_COEFFICIENT             =  0.181811E+001 ! W m-2 sr-1 µm-1
      CAL_COEFFICIENT_UNCERTAINTY =  0.109265E-001 ! W m-2 sr-1 µm-1
      GAIN                        =  0.550021E+000 ! W-1 m2 sr µm
      GAIN_UNCERTAINTY            =  0.330551E-002 ! W-1 m2 sr µm
      BIAS_DESERT                 =  0.106871E-001
      BIAS_DESERT_UNCERTAINTY     =  0.102577E-002
        GAIN_DESERT                          =  0.555899E+000 ! W-1 m2 sr µm
        GAIN_DESERT_UNCERTAINTY              =  0.338814E-002 ! W-1 m2 sr µm
        CAL_COEFFICIENT_DESERT               =  0.179889E+001 ! W m-2 sr-1 µm-1
        CAL_COEFFICIENT_DESERT_UNCERTAINTY   =  0.109640E-001 ! W m-2 sr-1 µm-1
      BIAS_SEA                    = -0.119573E-001
      BIAS_SEA_UNCERTAINTY        =  0.732034E-003
        GAIN_SEA                             =  0.543445E+000 ! W-1 m2 sr µm
        GAIN_SEA_UNCERTAINTY                 =  0.329071E-002 ! W-1 m2 sr µm
        CAL_COEFFICIENT_SEA                  =  0.184011E+001 ! W m-2 sr-1 µm-1
        CAL_COEFFICIENT_SEA_UNCERTAINTY      =  0.111424E-001 ! W m-2 sr-1 µm-1
      BIAS_DCC                    =  0.968870E-002
      BIAS_DCC_UNCERTAINTY        =  0.949073E-003
        GAIN_DCC                             =  0.555350E+000 ! W-1 m2 sr µm
        GAIN_DCC_UNCERTAINTY                 =  0.337811E-002 ! W-1 m2 sr µm
        CAL_COEFFICIENT_DCC                  =  0.180067E+001 ! W m-2 sr-1 µm-1
        CAL_COEFFICIENT_DCC_UNCERTAINTY      =  0.109532E-001 ! W m-2 sr-1 µm-1
      BIAS_DCC_LAND               =  0.100359E-001
      BIAS_DCC_LAND_UNCERTAINTY   =  0.935150E-003
        GAIN_DCC_LAND                        =  0.555541E+000 ! W-1 m2 sr µm
        GAIN_DCC_LAND_UNCERTAINTY            =  0.337807E-002 ! W-1 m2 sr µm
        CAL_COEFFICIENT_DCC_LAND             =  0.180005E+001 ! W m-2 sr-1 µm-1
        CAL_COEFFICIENT_DCC_LAND_UNCERTAINTY =  0.109455E-001 ! W m-2 sr-1 µm-1
      BERNSTEIN_DEGREE            = 10
      INVERSION_COST              =  0.950549E+004
      INVERSION_COST_DATA         =  0.949111E+004
      INVERSION_COST_PRIM         =  0.143731E+002
      PERIOD_START                = 19970916T000000Z
      PERIOD_CENTER               = 19970916T120000Z
      PERIOD_END                  = 19970917T000000Z
      RESPONSE_ABSOLUTE_MAX             =  0.104254E+001 ! W-1 m2 sr
      RESPONSE_ABSOLUTE_MAX_UNCERTAINTY =  0.388283E-001 ! W-1 m2 sr
      RESPONSE_BOUND_MIN          =  0.372498E+000 ! µm
      RESPONSE_BOUND_MAX          =  0.118287E+001 ! µm
      SAT                         = MET7      
      SAT_GAIN_SETTING            = 0
      TARGET_COUNT_DESERT         = 10413
      TARGET_COUNT_SEA            = 21626
      TARGET_COUNT_DCC            = 16367
      TARGET_COUNT_TOTAL          = 48406
      VERSION_SIMULATION_DESERT   = V035
      VERSION_SIMULATION_SEA      = V000
      VERSION_SIMULATION_DCC      = V007
      VERSION_INVERSION           = 1801-Release
      JOB_ID                      = 10
      JOB_ID_LONG                 = job-met07-all-10.nml
    /

The first line after the header specifies a UUID which identifies the optimisation run. For example:

    486DB2AF-C741-41DC-BF60-06DD4A217FB2

The second line after the header specifies the number of spectral wavelength samples `N` and the increment `R` between consecutive samples. For example, the line

    1011   0.100000E-002

states that there are `N = 1011` samples and the increment is `R = 0.001 µm`. The third line after the header is the first line of the spectral response function data block. The data block consists of several columns:

| Column                | Description                                              |
|-----------------------|----------------------------------------------------------|
| 1                     | Spectral wavelength (µm)                                 |
| 2                     | Relative spectral response                               |
| 3                     | Uncertainty of the relative spectral response            |
| Remaining `N` columns | Columns of the relative spectral error covariance matrix |

The difference between the spectral wavelengths associated with successive columns of the spectral error covariance matrix is `R`, too.
