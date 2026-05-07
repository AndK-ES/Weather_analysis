# Weather Data Analysis

A data science case study analyzing daily weather observations for Madrid, Spain from 2010 to 2020. The data is sourced from the [Meteostat](https://meteostat.net/) API and covers temperature, precipitation, wind, and pressure metrics.

## Project Overview

The goal is to demonstrate the full data analysis pipeline: acquisition, cleaning, feature engineering, exploratory analysis, and visualization. The analysis includes:

- **Data acquisition** via the Meteostat Python library (`meteostat`)
- **Cleaning and preprocessing**: handling missing values, column renaming, datetime indexing
- **Feature engineering**: extracting year, month, day-of-year, day-of-week; computing daily temperature range and rolling averages (7-day and 30-day windows)
- **Seasonal analysis**: comparing winter vs summer temperature distributions
- **Anomaly detection**: identifying temperature outliers by month using the Interquartile Range (IQR) method
- **Visualization**: line plots, boxplots, histograms, heatmaps, and scatter plots of local extrema

## Project Structure

```
Weather_analysis/
├── data/
│   ├── raw/                    # Raw CSV from Meteostat
│   └── clean/                  # Cleaned and feature-engineered CSV
├── figs/                       # Generated PNG visualizations
├── notebooks/
│   ├── 01_download.ipynb       # Data download from Meteostat
│   ├── 02_clean_explore.ipynb  # Cleaning, feature engineering, statistics
│   └── 03_viz_report.ipynb     # Visualizations and analysis
├── src/
│   ├── download_data.py        # (placeholder)
│   └── utils.py                # (placeholder)
├── .gitignore
├── README.md
└── requirements.txt
```

## Dependencies

- Python 3.11+
- pandas, numpy
- matplotlib, seaborn
- scipy
- meteostat
- jupyterlab

Install: `pip install -r requirements.txt`

## Usage

Run the notebooks in order:

1. **01_download.ipynb** — Fetches daily weather data for Madrid (40.4168, -3.7038) from 2010-01-01 to 2020-12-31 and saves it to `data/raw/`.
2. **02_clean_explore.ipynb** — Loads raw data, drops sparse columns, fills remaining NaNs, creates datetime features and rolling averages, then saves the cleaned dataset to `data/clean/`.
3. **03_viz_report.ipynb** — Produces all charts and analysis: line trends, boxplots, histograms, anomaly detection, correlation heatmaps, and local extreme value identification.

## Generated Figures

All plots are saved to `figs/`:
- `lineal_t-averages.png` / `lineal_t-avg_months.png` — temperature trends
- `boxplot_t-avg_months.png` — monthly temperature distribution
- `z-scores_t-avg.png` / `z-scores_t-winter-summer.png` — anomaly detection
- `histogram_precipitation.png`, `histogram_wind-speed-2015.png`, `histogram_wind-speed_2010-2020.png` — variable distributions
- `histogram_t-avg_winter-summer.png` — seasonal comparison
- `heatmap_corr-matrix.png` / `heatmap_pivot-table.png` — correlation and pivot analysis
- `local_min-max_extremes.png` — local temperature extrema
