# Downscaling Precipitation Extremes

This code was developed for the DOE SBIR "UVDAT" (Urban Visualization and Data Analysis Toolkit) with Northeastern University as the subcontractor to Kitware, Inc. This code is publicly available under the MIT license. Written by August Posch, Northeastern University, March-June 2025.

(IDEEA: intelligent downscaling of extremes from environments of the atmosphere)

The current version uses temperature, relative humidity, zonal wind, and meridional wind, each at 925 hPa, 700 hPa, and 500 hPa, over Boston, to predict daily precipitation in the watersheds encompassing Boston's urban rail system. The current version is trained on 1975-1994 and validated on 1995-2014 using ERA5 reanalysis as predictors, which represents historical weather conditions. Then, climate-level validation is performed on 1995-2014 and future predictions are obtained for 2031-2050, using the CESM2 climate model outputs which represent simulated weather. Information about hyperparameters, metrics, trained model files, and visuals is provided within the notebook machine_learning.ipynb.

Datasets: The datasets are ERA5 reanalysis as training and validation predictors, Livneh-unsplit gridded observations as labels, and CESM2 climate model outputs as extra validation and future-period predictors. All of these have been processed into machine learning format.

Known faults as of 6/24: the model needs to focus more on the extremes; exact location of CESM2 gridcell that ERA5 must match; relative humidity calculation should account for solid/liquid phase; slightly different pressure levels CESM2 vs ERA5 (936/691/525 vs 925/700/500). As shown in the notebook, the current model is unable to predict extremes beyond about 73 mm.