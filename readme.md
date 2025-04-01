# Downscaling Precipitation Extremes

This code was developed for the DOE SBIR "UVDAT" (Urban Visualization and Data Analysis Toolkit) with Northeastern University as the subcontractor to Kitware, Inc. This code is publicly available under the MIT license. Written by August Posch, Northeastern University, March 2025.

(IDEEA: intelligent downscaling of precipitation extremes from environments of the atmosphere)

The current version is a work in progress. The current version uses temperature, relative humidity, zonal wind, and meridional wind, each at 925 hPa, 700 hPa, and 500 hPa, over Boston, to predict daily precipitation in the watersheds encompassing Boston's urban rail system. The current version is a toy version using year 1991 for training and year 1992 as validation. Future adds: hyperparameter optimization, more data, more metrics, outputs for visualization.

(The current bottleneck is the CDS API queue for ERA5. Due to their download demand and limited CDS resources, it takes up to 2 hours to download 1 predictor for 1 year, and we will eventually need all 12 predictors for 65 years.)