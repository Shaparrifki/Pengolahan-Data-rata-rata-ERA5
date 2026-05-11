# Spatiotemporal Impact of ENSO and IOD on Drought Variability in Central Java 🌦️📉

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Google Earth Engine](https://img.shields.io/badge/Google%20Earth%20Engine-API-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Project Overview
This repository contains the Python and Google Earth Engine (GEE) scripts used for the spatiotemporal analysis of extreme climate forcings (ENSO and IOD) and their impact on drought variability across diverse topographies in Central Java, Indonesia. 

Conducted as part of a research project at the **National Research and Innovation Agency (BRIN)**, this study challenges the traditional paradigm of ENSO dominance by introducing high-resolution temporal and spatial perspectives.

## 🎯 Key Findings & Novelty
Through a hybrid approach utilizing Wavelet Coherence, EOF, and Lead-Lag Correlation, this research reveals:
1. **Acute vs. Chronic Drivers:** Positive IOD acts as an **Acute Driver** with immediate, highly destructive impacts on rainfall (Lag 0). In contrast, ENSO acts as a **Chronic Driver** with a delayed peak impact (Lag 2 months) but longer-lasting drought effects.
2. **The Oceanic Buffering Effect:** Spatial Principal Component Analysis (EOF-1) reveals that the southern coastal area (Cilacap) possesses lower climate sensitivity due to local oceanic moisture buffering. Conversely, the mountainous region (Banjarnegara) and northern coast (Tegal) are significantly more vulnerable to global sea surface temperature anomalies.
3. **Spatiotemporal Convergence:** During extreme climate forcing (Strong El Niño / IOD+), local topographic influences collapse, forcing the entire Central Java region to experience synchronized extreme drought.

## 🗺️ Study Area
- **Cilacap** (South Coast)
- **Banjarnegara** (Mountainous Region)
- **Tegal** (North Coast)

## 📊 Methodologies & Scripts Included
The notebooks in this repository cover the following analytical pipelines:
* **Data Extraction:** Automated fetching of NASA GPM IMERG V07 and ERA5 Copernicus data via GEE Python API.
* **Validation:** Statistical performance evaluation (Pearson *r*, RMSE, MBE) between satellite observations and climate models.
* **Teleconnection Analysis:** Cross-Wavelet Transform (XWT) and Wavelet Coherence (WTC) to detect phase relationships and cyclical periods.
* **Spatiotemporal Clustering:** Empirical Orthogonal Functions (EOF / Spatial PCA) to map climate regimes.
* **Composite Mapping:** Xarray-based anomaly masking for specific extreme years (El Niño vs. Positive IOD) mapped using Cartopy.
* **Lead-Lag Correlation:** Time-shifted Pearson correlation to determine the temporal delay of ocean anomalies reaching the mainland.

## 🛠️ Prerequisites & Libraries
To run the notebooks, ensure you have an active Google Earth Engine account and the following libraries installed:
```bash
pip install earthengine-api pandas numpy matplotlib seaborn cartopy xarray rioxarray geopandas pycwt scikit-learn
