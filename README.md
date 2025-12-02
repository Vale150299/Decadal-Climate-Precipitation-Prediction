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
- Scripts for data preprocessing, drift correction, and diagnostics  
- Jupyter notebooks for generating the main plots used in the thesis  

decadal-precipitation-prediction/
│
├── data/ # raw and processed climate data (not uploaded)
├── scripts/ # python scripts for processing and analysis
├── notebooks/ # jupyter notebooks for exploration
├── models/ # CNN weights and hybrid model outputs
├── plots/ # figures and visualizations
├── thesis/ # thesis PDF and related material
├── docs/ # method descriptions and documentation
├── environment.yml
├── LICENSE
└── README.md



---

## 🔧 Environment Setup

A Python environment file will be added to support:
- xarray, netCDF4  
- numpy, pandas, scipy  
- scikit-learn  
- tensorflow (for CNN pattern model)  
- matplotlib, cartopy  
- jupyterlab  

---

## 👤 Author

**Valerio Ippoliti**  
Master’s Thesis — University of Bologna  

