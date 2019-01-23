<img alt="METEOSAT MVIRI spectral response functions"
        src="https://github.com/FIDUCEO/FCDR_MVIRISRF/blob/master/graphicalabstract.png"
        style="display:block; margin:auto"
        title="METEOSAT MVIRI spectral response functions"> 
        
# Synopsis

How can the in-flight spectral response functions of a series of decades-old broad-band radiometers in Space be retrieved post-flight? This question is the clue to develop Climate Data Records from the Meteosat Visible and Infrared Imager (MVIRI) on board the Meteosat First Generation (MFG) of geostationary satellites, which had been acquiring Earth radiance images in the Visible (VIS) broad-band from 1977 to 2017.

This dataset repository is the result of a new metrological sound method for retrieving the VIS spectral response from matchups of pseudo-invariant calibration site (PICS) pixels with datasets of simulated top-of-atmosphere spectral radiance used as reference. Calibration sites include bright desert, open ocean and deep convective cloud targets. The instrument spectral response function is specified in terms of a decomposition into Bernstein basis polynomials and a degradation function that is based on simple physical considerations and able to represent typical chromatic ageing characteristics. Retrieval uncertainties are specified in terms of an error covariance matrix, which is projected from model parameter space into the spectral response function domain and range (the figure above illustrates an example). The retrieval method considers unknown PICS selection biases and target type-specific errors in the spectral radiance simulation explicitly. It has been validated with well-comprehended observational data from Meteosat Second Generation and has retrieved meaningful results for all MFG satellites except for the prototype Meteosat-1, which was not archived.


# Getting started

The [FIDUCEO in-flight MVIRI VIS spectral response function dataset](https://github.com/FIDUCEO/FCDR_MVIRISRF) dataset is a supplement to the FIDUCEO MVIRI VIS Fundamental Climate Data Record. It includes several folders, which contain spectral response data for different purposes.

| Folder | Description |
|--------|-------------|
| [srf](https://github.com/FIDUCEO/FCDR_MVIRISRF/tree/master/srf) | Contains the retrieved relative in-flight spectral response function and its spectral error covariance matrix for certain days of the year. These data are needed for the processing of Fundamental and derived Thematic Climate Data Records. *Most likely, you will want these data and nothing else from this repository* |
| [opt](https://github.com/FIDUCEO/FCDR_MVIRISRF/tree/master/opt) | Contains the retrieved optimised forward model parameters and their error covariance matrix. These data are needed to compute the absolute or relative spectral response function and the associated spectral error covariance matrix as a function of time since launch, if the retrieved relative spectral response functions are not suitable |
| [dia](https://github.com/FIDUCEO/FCDR_MVIRISRF/tree/master/dia) | Contains data to diagnose a retrieval. These data are needed for diagnostic purposes only |

Each folder contains specific explanations of the contents. All dataset files are named according to the convention

    kkk_METx_yyyyddd_yyyyddd_vvvv-ttttttt_mmmmm_nn

with individual naming components specified in the table below.  

| **Filename component** | **Significance**                 |
|------------------------|----------------------------------|
| `kkk`                  | Kind of data                     |
| `x`                    | Meteosat satellite enumerator    |
| `yyyyddd`              | Year and day (of year) of begin and end of retrieval or validity period |
| `vvvv-ttttttt`         | Software version and version tag |
| `mmmmm`                | Model specifier                  |
| `nn`                   | Job enumerator                   |


# Release versions

Release versions are numbered by the year of the release followed by a two-digit number that enumerates the release within the release year. For example, version 1801 denotes the first release of the year 2018. Release versions have the version tag *Release*.


# Further reading

Ralf Quast, Ralf Giering, Yves Govaerts, Frank Rüthrich, Rob Roebeling (2018). *Climate Data Records from Meteosat First Generation: Retrieval of the in-Flight VIS Spectral Response*. [Remote Sensing Special Issue "Assessment of Quality and Usability of Climate Data Records"](https://www.mdpi.com/journal/remotesensing/special_issues/assessment_cdr).

Frank Rüthrich, Ralf Quast, Yves Govaerts, Viju O. John, Rob Roebeling, Emma Wooliams and Jörg Schulz (2018). *A Fundamental Climate Data Record for the Meteosat Visible and Infrared Imager (MVIRI)*. [Remote Sensing Special Issue "Assessment of Quality and Usability of Climate Data Records"](https://www.mdpi.com/journal/remotesensing/special_issues/assessment_cdr).
