# Weather Data Analysis

This project is a small Data Science case study focused on **weather analysis** using Python.  
It was created as a practice project after completing the *Python Data Analysis* course on Coursera.  

---

## 📊 Project Description
The goal of this project is to analyze daily weather data (temperature, etc.) over the period **2010–2020**, and demonstrate different data analysis techniques:

- Data preprocessing (handling missing values, adding features like year/month, moving averages)  
- Exploratory Data Analysis (EDA): line plots, boxplots, histograms, heatmaps  
- Seasonal analysis (summer vs winter temperatures)  
- Anomaly detection using the **IQR method**  
- Detecting local extrema (maxima and minima)  
- Visualization of results  

---

## 📂 Project Structure

```
weather-analysis/
  ├─ data/
  │   ├─ raw/      
  │   └─ clean/    
  ├─ notebooks/
  │   ├─ 01_download.ipynb
  │   ├─ 02_clean_explore.ipynb
  │   └─ 03_viz_report.ipynb
  ├─ src/
  │   ├─ download_data.py
  │   └─ utils.py
  ├─ figs/                  # plots PNG
  └─ requirements.txt
```

## ⚙️ Installation
Clone the repository and install dependencies:

```bash
git clone https://github.com/AndK-ES/Weather_analysis
cd weather-analysis
pip install -r requirements.txt