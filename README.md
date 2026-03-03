# HLY2202-CTD-O2-Calibration 
-----------------------------------------------------------------------------------------------------------------------
Spline_intp.ipynb: 

This script is used to calibrate CTDO2 from the HLY2202 expedition. This O2 package exhibited hysteresis at depth, so we developed a baseline linear CTD–Winkler calibration, which was applied, and residuals were modeled versus pressure using exponential fits within pressure intervals and combined via spline interpolation to generate a continuous pressure-dependent correction, which was subtracted from CTD oxygen to produce the final calibrated oxygen.

## Features
- Import of CTD .cnv files, parsing, concatenating, and calculation of seawater properties. 
- Import of the Winkler bottle file. Merging Winkler samples within cast using potential density anomaly (sigma0) matching with nearest-neighbor association and tolerance ±0.05 kg m^-3.
- Plots of Winkler O2 vs CTD O2.
- Pressure - dependent correction using an exponential model and plots of residuals.
- Application of correction to full ctd files. 
- Cross-validation with independent measurements from other cruises.
- Conversion of dataset to .ncfile for publication. Plot of the resulting product. 

-------------------------------------------------------------------------------------------------------------------------
CF_sensor1.ipynb:

This script calibrates ctd files from the first sensor during the HLY2202 expedition. 
Follows the same Winkler and CTD O2 matching methods, but uses the traditional calibration factor (Soc) derived from the ratio between Winkler [O₂] versus SBE43 [O₂]. After removal of outliers through IQR, the mean ratio was used as a multiplier factor to correct CTD O2 values of sensor 0-10 and specified in the Spline_intp.ipynb script. 


-------------------------------------------------------------------------------------------------------------------------


## Usage
This script is meant to be used as a Jupyter notebook and not a .py pipeline.

## Documentation
Read Methodology.md dor for information on Data processing. 

## Citation
cff-version: 1.2.0
title: "Hydrographic and Calibrated Dissolved Oxygen Observations from the Canada and Makarov Basins, HLY2202"
authors:
  - Maria Cristina Alvarez Rodriguez, University of Southampton, http://orcid.org/0009-0002-3120-2580
  - Laurie Juranek, Oregon State University, https://orcid.org/0000-0002-4922-8263

    
date-released: 2026-03-03
version: 1.0.0

## Contact
mcar1u25@soton.ac.uk , laurie.juranek@oregonstate.edu

## License
This project is licensed under Apache 2.0 + Commons Clause.

