# Datasets of diagnostic spectral response data

Each file named

    dia_METx_yyyyddd_yyyyddd_vvvv-ttttttt_mmmmm_nn.dat.zyyyy
    
contains spectral response data from the optimisation run for the Meteosat-`x` satellite. The first date `yyyyddd` of the file name designates the begin of the retrieval period, the second date designates its end.

## File format

After being unzipped, the plain text spectral response data files contain the instrument gain factor (i.e. the area of the absolute instrument spectral response) and the absolute instrument spectral response function for each day of the retrieval period. Each file starts with a header that provides some basic information on the retrieval. For example:

    &HEADER
      JOB_ID              = 10        
      JOB_ID_LONG         = job-met03-all-10.nml                                                            
      INVERSION_COST      =  0.109269E+004
      INVERSION_COST_DATA =  0.107385E+004
      INVERSION_COST_PRIM =  0.188428E+002
      TARGET_COUNT_DESERT = 451
      TARGET_COUNT_SEA    = 2399
      TARGET_COUNT_DCC    = 287
      TARGET_COUNT_TOTAL  = 3137
      VERSION_INVERSION   = 1801-RC00004
      NUM_DAYS            = 927
      MIN_DAY             =  159.5
      MAX_DAY             = 1085.5
    /

The two lines following the file header specify the number of days `D` and the number of spectral wavelength samples `N`. For example

     0927
     1011

specifies that the retrieval period comprises `D = 927` days and that the spectral response function is sampled at `N = 1011` different spectral wavelengths.

The next `D` lines exhibit two columns, where the first column designates the instrument gain factor and the second column designates its uncertainty. For example

      0.579864E+000  0.643021E-002
      0.579815E+000  0.642128E-002
      0.579766E+000  0.641240E-002
      0.579717E+000  0.640357E-002
      0.579667E+000  0.639478E-002
      0.579618E+000  0.638604E-002
      0.579569E+000  0.637734E-002
      ...

specifies the instrument gain factor for the first seven days of the retrieval period. After the data block of instrument gain factors, which exhibits two columns, follows a data block of `D * N` lines that exhibits three columns and includes the absolute instrument spectral response function for each day of the retrieval period. The first column designates the spectral wavelength (µm), while the second and thirs column designate the absolute instrument spectral response (W-1 m2 sr) and its uncertainty. For example

      ...
      0.500500E+000  0.624834E+000  0.391316E-001
      0.501500E+000  0.628938E+000  0.388697E-001
      0.502500E+000  0.633027E+000  0.386254E-001
      0.503500E+000  0.637101E+000  0.383995E-001
      0.504500E+000  0.641159E+000  0.381927E-001
      0.505500E+000  0.645201E+000  0.380057E-001
      0.506500E+000  0.649228E+000  0.378393E-001
      ...

Note that the individual data blocks of `N` lines, each specifying the absolute spectral response for a single day of the retrieval period, are *not* separated by a blank line, i.e. the spectral response data are written continously.
