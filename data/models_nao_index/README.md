# NAO Model Index Data

##  Description

This folder contains processed North Atlantic Oscillation (NAO) index data derived from decadal sea level pressure (PSL) modelS outputs.

The NAO index is computed using a box-based method and is intended for use in climate variability analysis and precipitation prediction models.

---

##  Contents

* `XXX_nao_index_results.csv`: Processed dataset containing NAO index values and anomalies for each year and ensemble member.

---

##  Methodology

The NAO index is calculated as the difference between mean sea level pressure in two regions:

* **Azores region**: 36°N–40°N, 332°E–340°E
* **Iceland region**: 63°N–70°N, 335°E–344°E

[
NAO = PSL_{Azores} - PSL_{Iceland}
]

The calculation uses:

* **DJFM months** (December–March)
* **Forecast years 2–9**
* **Initialization years**: 1960–2005
* **Ensemble members**: r1–r10

---

##  Columns

* `Year`: Initialization year
* `Realization`: Ensemble realization number
* `member`: Ensemble member label (r1–r10)
* `NAO Index`: Computed NAO index
* `NAO Anomaly`: Anomaly relative to the member’s mean NAO

---

##  Usage

This dataset is used as an input feature for:

* Climate variability studies
* Decadal prediction models
* Precipitation forecasting

Example usage in Python:

```python
import pandas as pd

df = pd.read_csv("data/models_nao_index/can4_nao_index_results.csv")
print(df.head())
```

---

##  Notes

* Data are preprocessed and ready for analysis
* Anomalies are computed per ensemble member
