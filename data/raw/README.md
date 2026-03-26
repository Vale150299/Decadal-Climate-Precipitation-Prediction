# Raw Climate Data (ESGF Download)

##  Description

This folder contains raw climate model data (NetCDF format) downloaded from the ESGF (Earth System Grid Federation).

The data are used as input for computing the NAO (North Atlantic Oscillation) index.

---

##  Data Source

Data are obtained from ESGF:

 https://esgf-metagrid.cloud.dkrz.de/search

Typical dataset:

* Model: **CanCM4**
* Variable: **psl** (sea level pressure)
* Frequency: **Amon (monthly)**

---

##  Download Method (Wget Script)

Data are downloaded using an ESGF-generated Wget script.

### Run the script:

```bash
bash wget_script_XXXX.sh -H 2>&1 | tee download.log
```

This command:

* downloads all files in the DataCart
* logs output to `download.log`
* allows monitoring and debugging

---

##  Authentication

During execution, you will be prompted:

```text
Enter your openid : your_email
Enter password :
```

* ESGF uses OpenID authentication
* A temporary certificate is generated and stored in:

```text
~/.esg/
```

These certificates are required to access data and typically expire after a few days ([esgf.github.io][1])

---

##  Example Terminal Output

```text
Retrieving Federation Certificates...
done!

psl_Amon_CanCM4_decadal1960_r1_196101-197012.nc ...Downloading
psl_Amon_CanCM4_decadal1960_r2_196101-197012.nc ...Already downloaded and verified
```

### Meaning:

* **Downloading** → file is being downloaded
* **Already downloaded and verified** → file exists and checksum is correct
* **Resuming** → partial download continues

 ESGF wget scripts automatically:

* skip existing files
* resume interrupted downloads
* verify file integrity ([esgf.github.io][1])

---

##  File Naming Convention

Files follow this structure:

```text
psl_Amon_CanCM4_decadal{year}_{member}_{start}-{end}.nc
```

Example:

```text
psl_Amon_CanCM4_decadal1960_r1_196101-197012.nc
```

Where:

* `year` = initialization year
* `member` = ensemble member (`r1`–`r10`)
* `{start}-{end}` = forecast period

---

##  Folder Structure

Recommended organization:

```text
data/raw/psl/
```

Example:

```text
data/raw/psl/
├── psl_Amon_CanCM4_decadal1960_r1_196101-197012.nc
├── psl_Amon_CanCM4_decadal1960_r2_196101-197012.nc
```

---

##  Integration with Workflow

These raw files are used by:

* [`01_load_and_prepare_model_data_NAO.ipynb`](../../notebooks/NAO_processing/01_load_and_prepare_model_data_NAO.ipynb)
* [`02_compute_NAO_model_index.ipynb`](../../notebooks/NAO_processing/02_compute_NAO_model_index.ipynb)

Processed outputs are stored in:

```text
../models_nao_index/
```

---

##  Notes

* Files can be large (GB scale)
* The script can be safely re-run multiple times
* Certificates may expire → rerun script to refresh
* Logs (`download.log`) help debug failures

---

##  Summary

Workflow:

ESGF → Wget script → NetCDF files → preprocessing → NAO index → results

[1]: https://esgf.github.io/esgf-user-support/user_guide.html?utm_source=chatgpt.com "User Tutorials — ESGF User Support 0.0.0 documentation"

