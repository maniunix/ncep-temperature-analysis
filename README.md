# NCEP Temperature Analysis (1981–2000)

## 📌 Overview
This project performs an end-to-end analysis of NCEP Reanalysis temperature data from 1981 to 2000 using Python. The workflow includes data acquisition, preprocessing, spatial-temporal aggregation, and visualization.

The objective is to analyze temperature patterns both spatially (global maps) and temporally (time series at a specific location).

---

## 📂 Dataset
- **Source**: NOAA NCEP Reanalysis Daily Averages  
- **Variable**: Air temperature at sigma level 995 (`air.sig995`)  
- **Time Period**: 1981–2000  
- **Format**: NetCDF (.nc)

---

## ⚙️ Methodology

### 1. Data Acquisition
- Retrieved NetCDF files from NOAA PSL server using `requests` and `BeautifulSoup`
- Automated download and avoided re-downloading existing files

### 2. Data Processing
- Loaded multi-year NetCDF files using `xarray`
- Converted longitude from **0–360° to -180–180°**
- Converted temperature from **Kelvin to Celsius**
- Updated metadata (`units`, `actual_range`) for consistency

### 3. Aggregation
- Monthly mean temperature (time series: 1981–2000)
- Annual mean temperature (per year)
- Summer seasonal mean (June–August)

### 4. Visualization
- Global temperature map for **December 1992**
- Time series analysis at:
  - Latitude: 37.98  
  - Longitude: -78.15  
- Included:
  - 12-month rolling mean  
  - Standard deviation shading  

---

## 📊 Results

- The spatial map highlights expected global temperature gradients, with colder regions at higher latitudes.
- The time series shows clear seasonal variability with a smoothed long-term trend using a rolling mean.
- Variability in temperature is captured using standard deviation shading.

---

## 🛠️ Tools & Libraries
- Python
- Xarray
- Pandas
- NumPy
- Matplotlib
- Requests
- BeautifulSoup
- NetCDF4

---

## 📁 Project Structure
# ncep-temperature-analysis
