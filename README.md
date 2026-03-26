# Decadal Prediction of African Precipitation Variability
Decadal Climate Predictions • Hybrid Statistical–Dynamical Forecasting • Mode Matching • NAO Matching Post-processing • ENSO-based subsampling • CNN Teleconnection Diagnostics


This repository will contain the code, data structure, and analysis workflow for my thesis:

**"Hybrid Statistical–Dynamical Methods for Decadal Prediction of African Precipitation Variability."**

The project explores and provides two Mode Matching methodologies:
- To improve decadal precipitation skill across the domain 
- To better understand the impact of the teleconnections involved

- Boreal Winter (DJFM): NAO matching; selecting members based on their ability to reproduce NAO
- Boreal Summer (JJAS): ENSO Based Subsampling; selecting members based on their ability to reproduce ENSO
- ENSO teleconnection analysis using a CNN-based model
- Jupyter for data preprocessing, drift correction, and diagnostics  
- Jupyter notebooks for generating the main plots used in the thesis
   
##  Data
- Models NAO Index
   8-yr boreal winter (December to March) means representing years 2–9 from each    start date
---

##  Project Goals

- Improve DJFM decadal predictability via NAO signal correction  
- Evaluate RPC/RPS and create lagged larger-ensembles  
- Apply ensemble selection based on dynamical–statistical criteria  
- Use CNN-CD to diagnose ENSO zonal patterns  
- Improve JJAS West African Monsoon forecasts using hybrid models  




---

##  Environment Setup

A Python environment file will be added to support:
- xarray, netCDF4  
- numpy, pandas, scipy  
- scikit-learn  
- tensorflow (for CNN pattern model)  
- matplotlib, cartopy  
- jupyterlab

---

##  Author

**Valerio Ippoliti**  
Master’s Thesis in Science of Climate

University of Bologna

2024-2025

---
##  License

This project is released under the MIT License (see LICENSE file).
--- 

