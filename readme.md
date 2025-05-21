# Downscaling Precipitation Extremes

This code was developed for the DOE SBIR "UVDAT" (Urban Visualization and Data Analysis Toolkit) with Northeastern University as the subcontractor to Kitware, Inc. This code is publicly available under the MIT license. Written by August Posch, Northeastern University, March-May 2025.

(IDEEA: intelligent downscaling of extremes from environments of the atmosphere)

The current version uses temperature, relative humidity, zonal wind, and meridional wind, each at 925 hPa, 700 hPa, and 500 hPa, over Boston, to predict daily precipitation in the watersheds encompassing Boston's urban rail system. The current version is trained on 1975-1994 and validated on 1995-2014. Information about hyperparameters, metrics, trained model files, and visuals is provided within the notebook machine_learning.ipynb. Coming soon: predictions on 2031-2050 future climate.

Datasets: The datasets are ERA5 reanalysis as training and validation predictors, and Livneh-unsplit gridded observations as labels. Both of these have been processed into machine learning format; the processing will be shared along with the CESM2 validation and future predictors.