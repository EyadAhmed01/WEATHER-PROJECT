# Global Weather Trend Forecasting

A data-science assessment project built around the **Global Weather Repository** on Kaggle. The work lives in a single Jupyter notebook: end-to-end **cleaning**, **exploratory analysis**, **time-series forecasting** (using `last_updated`), **model comparison and a simple ensemble**, plus **advanced topics** (anomalies, air quality vs weather, climate zones, spatial and country-level patterns).

---

### PM Accelerator mission 
**Our Mission:** By making industry-leading tools and education available to individuals from all 
backgrounds, we level the playing field for future PM leaders. This is the PM Accelerator motto: we 
grant aspiring and experienced PMs what they need most — **Access**. We introduce you to industry 
leaders, surround you with the right PM ecosystem, and discover the new world of **AI product 
management** skills.

## What’s in the notebook

- **Preprocessing:** valid timestamps, numeric coercion, median imputation, IQR-based caps on temperature and precipitation  
- **EDA:** correlations, temperature/precipitation distributions, global mean temperature over time  
- **Forecasting:** per-city daily series from `last_updated`; naive baseline, `ARIMA(2,1,2)`, Random Forest on lag features, ensemble (ARIMA + RF); MAE, RMSE, MAPE  
- **Advanced:** IsolationForest anomalies, Spearman air-quality vs weather, latitude-based climate zones, monthly aggregates, lat/lon maps (matplotlib), country summaries  

**Stack:** Python · pandas · NumPy · matplotlib · seaborn · scikit-learn · statsmodels · [KaggleHub](https://github.com/Kaggle/kagglehub)

---

## Prerequisites

- **Python 3.10+** recommended  
- Internet access on first run if you use KaggleHub to download the dataset  

---

## Installation

```bash
git clone <your-repo-url>
cd <repo-folder>

python -m venv .venv
# Windows:
.venv\Scripts\activate
# macOS / Linux:
# source .venv/bin/activate

pip install -r requirements.txt
```

---

## Data setup

The notebook resolves the CSV in this order:

1. Environment variable **`WEATHER_CSV_PATH`** pointing to `GlobalWeatherRepository.csv`  
2. **`data/GlobalWeatherRepository.csv`** next to the notebook or in the parent directory  
3. **KaggleHub** — downloads [`nelgiriyewithana/global-weather-repository`](https://www.kaggle.com/datasets/nelgiriyewithana/global-weather-repository) if nothing local is found  

---

## Running the analysis

```bash
jupyter notebook Weather_Trend_Forecast_Assessment.ipynb
```

Use **Run → Run All Cells**. To share a static report, export the notebook as **HTML** or **PDF** from Jupyter (*File → Save and Export Notebook As…*).

---

## PM Accelerator (assessment)

This project was prepared for the **PM Accelerator** technical assessment.
**Website:** [pmaccelerator.io](https://www.pmaccelerator.io/)

---
