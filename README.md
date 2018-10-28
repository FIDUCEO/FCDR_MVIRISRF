<img alt="Error covariance matrix of a relative spectral response function"
        src="https://github.com/FIDUCEO/FCDR_MVIRISRF/wiki/resources/7-rcov.jpg"
        style="display:block; margin:auto"
        title="Example of an error covariance matrix of a relative spectral response function"> 
        
# Synopsis

How can the in-flight spectral response functions of a series of decades-old broad-band radiometers in Space be retrieved post-flight? This question is the clue to develop Climate Data Records from the Meteosat Visible and Infrared Imager (MVIRI) on board the Meteosat First Generation (MFG) of geostationary satellites, which had been acquiring Earth radiance images in the Visible (VIS) broad-band from 1977 to 2017.

This dataset repository is the result of a new metrological sound method for retrieving the VIS spectral response from matchups of pseudo-invariant calibration site (PICS) pixels with datasets of simulated top-of-atmosphere spectral radiance used as reference. Calibration sites include bright desert, open ocean and deep convective cloud targets. The instrument spectral response function is specified in terms of a decomposition into Bernstein basis polynomials and a degradation function that is based on simple physical considerations and able to represent typical chromatic ageing characteristics. Retrieval uncertainties are specified in terms of an error covariance matrix, which is projected from model parameter space into the spectral response function domain and range (the figure above illustrates an example). The retrieval method considers unknown PICS selection biases and target type-specific errors in the spectral radiance simulation explicitly. It has been validated with well-comprehended observational data from Meteosat Second Generation and has retrieved meaningful results for all MFG satellites except for the prototype Meteosat-1, which was not archived.


# Getting started

The [FCDR_MVIRISRF](https://github.com/FIDUCEO/FCDR_MVIRISRF) dataset includes several folders, which contain data for different purposes.

| Folder | Description |
|--------|-------------|
| srf | Contains the retrieved relative in-flight spectral response function and its spectral error covariance matrix for certain days of the year. These data are needed for the processing of Fundamental and derived Thematic Climate Data Records. *Most likely, you will want these data and nothing else from this repository* |
| opt | Contains the retrieved optimised forward model parameters and their error covariance matrix. These data are needed to compute the absolute or relative spectral response function and the associated spectral error covariance matrix as a function of time since launch, if the retrieved relative spectral response functions are not suitable |
| dia | Contains data to diagnose a retrieval. These data are needed for diagnostic purposes only |

Each folder contains specific explanations of the contents. You may want to consult the [FCDR_MVIRISRF wiki](https://github.com/FIDUCEO/FCDR_MVIRISRF/wiki) for additional information.


# Release versions

Release versions are numbered by the year of the release followed by a two-digit number that enumerates the release within the release year. For example, version 1801 denotes the first release of the year 2018. Release versions have the version tag *Release*.


# Further reading

Ralf Quast, Ralf Giering, Yves Govaerts, Frank Rüthrich, Rob Roebeling (2018). *Climate Data Records from Meteosat First Generation: Retrieval of the in-Flight VIS Spectral Response*. [Remote Sensing Special Issue "Assessment of Quality and Usability of Climate Data Records"](https://www.mdpi.com/journal/remotesensing/special_issues/assessment_cdr).

Frank Rüthrich, Ralf Quast, Yves Govaerts, Viju O. John, Rob Roebeling, Emma Wooliams and Jörg Schulz (2018). *A Fundamental Climate Data Record for the Meteosat Visible and Infrared Imager (MVIRI)*. [Remote Sensing Special Issue "Assessment of Quality and Usability of Climate Data Records"](https://www.mdpi.com/journal/remotesensing/special_issues/assessment_cdr).
