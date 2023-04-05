# EDA

- no missing values in the main columns
- CO-H2O measurements is likely due to an overlap in measurement spectra or the ability to derive H2O info from CO measurements
    - correlates with humidity and precipitation
    - can be thrown out
- O3 effective temp correlates with O3 concentration
    - can be thrown out
- cloud fraction & aerosol index correlate
- rel. humidity (percentage of possible humidity at a given temp)
- spec. humidity (percentage of water relative to total air weight)
- target min & max columns are likely daily / weekly minima and maxima (or by location)
- cloud values are highly correlated
    - base height, top pressure, base pressure can be thrown out (tell the same as base height)
    - remaining columns: base height, optical depth & fraction
    - lower cloud optical depth & base height --> higher target value (possibly)
- L3_NO2_tropospheric_NO2_column_number_density highly correlated to L3_NO2_NO2_column_number_density
    - drop tropospheric concentration


#### Missingno Info

- CH4 columns have 80% missing values (throw them out)
    - other columns have at least 70% content (decide on individual instances how to deal with them)
    - sometimes there are values of 0 (O3 column number density, L3_CO_CO_column_number_density, L3_NO2_tropopause_pressure, L3_NO2_absorbing_aerosol_index) that need to be imputed specifically to NaNs and then replaced
- depending on the molecule, blocks of data are missing
    - but no overall missing datablocks (dropping rows is out of the question)


### Info for baseline model

- target and humidity/precipitable water are slightly correlated
- lower precip. higher target
- higher rel. humidity, higher target (possibly)
- create magnitude column (windstrength): ws = sqrt(u^2 + v^2)
- So2 absorbing arosol has weird high value (replace? throw out?)
- have to regularize & scale
- baseline model: first with weather variables only?
- second model: 



