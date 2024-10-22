![Meteosat MVIRI spectral response functions](graphicalabstract.png "Meteosat MVIRI spectral response functions")

# Synopsis

How can the in-flight spectral response functions of a series of decades-old broad-band radiometers in Space be retrieved post-flight? This question is the clue to develop Climate Data Records from the Meteosat Visible and Infrared Imager (MVIRI) on board the Meteosat First Generation (MFG) of geostationary satellites, which had been acquiring Earth radiance images in the Visible (VIS) broad-band from 1977 to 2017.

This dataset repository is the result of a new metrological sound method for retrieving the VIS spectral response from matchups of pseudo-invariant calibration site (PICS) pixels with datasets of simulated top-of-atmosphere spectral radiance used as reference. Calibration sites include bright desert, open ocean and deep convective cloud targets. The instrument spectral response function is specified in terms of a decomposition into Bernstein basis polynomials and a degradation function that is based on simple physical considerations and able to represent typical chromatic ageing characteristics. Retrieval uncertainties are specified in terms of an error covariance matrix, which is projected from model parameter space into the spectral response function domain and range (the figure above illustrates an example). The retrieval method considers unknown PICS selection biases and target type-specific errors in the spectral radiance simulation explicitly. It has been validated with well-comprehended observational data from Meteosat Second Generation and has retrieved meaningful results for all MFG satellites except for the prototype Meteosat-1, which was not available for analysis.


# Getting started

The [FIDUCEO in-flight MVIRI VIS spectral response function dataset](https://github.com/FIDUCEO/FCDR_MVIRISRF) is a supplement to the FIDUCEO MVIRI VIS Fundamental Climate Data Record. It includes several folders, which contain spectral response data for different purposes.

| Folder | Description |
|--------|-------------|
| [srf](https://github.com/FIDUCEO/FCDR_MVIRISRF/tree/master/srf) | Contains the retrieved relative in-flight spectral response function and its spectral error covariance matrix for certain days of the year. These data are needed for the processing of Fundamental and derived Thematic Climate Data Records. *Most likely, you will want these data and nothing else from this repository* |
| [opt](https://github.com/FIDUCEO/FCDR_MVIRISRF/tree/master/opt) | Contains the retrieved optimised forward model parameters and their error covariance matrix. These data are needed to compute the absolute or relative spectral response function and the associated spectral error covariance matrix as a function of time since launch, if the retrieved relative spectral response functions are not suitable |
| [dia](https://github.com/FIDUCEO/FCDR_MVIRISRF/tree/master/dia) | Contains data to diagnose a retrieval. These data are needed for diagnostic purposes only |

Each folder contains specific explanations of the contents. All dataset files are named according to the convention

    kkk_METx_yyyyddd_yyyyddd_vvvv-ttttttt_mmmmm_nn

with individual naming components specified in the table below.  

| Filename component | Significance                     |
|--------------------|----------------------------------|
| `kkk`              | Kind of data                     |
| `x`                | Meteosat satellite enumerator    |
| `yyyyddd`          | Year and day (of year) of begin and end of retrieval or validity period |
| `vvvv-ttttttt`     | Software version and version tag |
| `mmmmm`            | Model specifier                  |
| `nn`               | Job enumerator                   |


# Release versions

Release versions are numbered by the year of dataset creation followed by a two-digit enumerator. For example, version 1801 denotes the first release of a dataset created in the year 2018. Release versions have the version tag *Release*.

# Further reading

Govaerts, Y.M.; Rüthrich, F.; John, V.O.; Quast, R. Climate Data Records from Meteosat First Generation Part I: Simulation of Accurate Top-of-Atmosphere Spectral Radiance over Pseudo-Invariant Calibration Sites for the Retrieval of the In-Flight Visible Spectral Response. *Remote Sens.* **2018**, *10*, 1959; <https://doi.org/10.3390/rs10121959)>.

Quast, R.; Giering, R.; Govaerts, Y.; Rüthrich, F.; Roebeling, R. Climate Data Records from Meteosat First Generation Part II: Retrieval of the In-Flight Visible Spectral Response. *Remote Sens.* **2019**, *11*, 480;
<https://doi.org/10.3390/rs11050480>.

Rüthrich, F.; John, V.O.; Roebeling, R.A.; Quast, R.; Govaerts, Y.; Woolliams, E.R.; Schulz, J. Climate Data Records from Meteosat First Generation Part III: Recalibration and Uncertainty Tracing of the Visible Channel on Meteosat-2–7 Using Reconstructed, Spectrally Changing Response Functions. *Remote Sens.* **2019**, *11*, 1165; <https://doi.org/10.3390/rs11101165>.

Quast, R. Easy-peasy: spectrally degrading spectral response functions. [FIDUCEO Blogs 28-01-2019](https://research.reading.ac.uk/fiduceo/easy-peasy-spectrally-degrading-spectral-response-functions/).
