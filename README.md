# Unemployment Analysis in India 

## Project Overview

This repository contains exploratory data analysis (EDA) on the "Unemployment in India" dataset using Python. The analysis is implemented in `Task2.ipynb` and performs data cleaning, summary statistics, and visualizations to investigate unemployment rates across regions and through time.

## Files

- `Task2.ipynb` - Jupyter notebook with the full analysis and visualizations.
- `Unemployment in India.csv` - Dataset used for the analysis.
- `graph 1.png`, `graph 2.png`, `result.png` - Generated plots / outputs from the notebook.
- `README.md` - This file.

## Requirements

Recommended Python packages:

- Python 3.8+
- pandas
- numpy
- matplotlib
- seaborn
- jupyterlab or notebook

Quick install:

```bash
pip install pandas numpy matplotlib seaborn jupyterlab
```

(Optional) Create a virtual environment before installing packages:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt  # if you create one
```

## How to run

1. Open `Task2.ipynb` in Jupyter Lab / Notebook or upload the notebook to Google Colab.
2. Make sure `Unemployment in India.csv` is in the same folder as the notebook (or change the path in the notebook).
   - If running locally, change the read line to:
     ```python
     df = pd.read_csv("Unemployment in India.csv")
     ```
3. Run cells top-to-bottom. The notebook includes:
   - Data import and initial inspection (`df.head()`, `df.info()`)
   - Missing value check and cleanup (`df.dropna()`)
   - Column normalization
   - Summary statistics and distribution plot of unemployment rate
   - State/Region bar plot of unemployment rate
   - Correlation heatmap between numeric fields
   - Time series plot of unemployment rate (if `Date` is present)

## Key Findings (from the notebook)

- The dataset requires minor cleaning (whitespace in column names and some null values).
- The unemployment rate shows a distribution that can be inspected with the histogram plot.
- There is notable variation in unemployment rate across different regions (see `graph 1.png`).
- Numeric fields such as unemployment rate, employed counts, and labor participation show measurable correlations (see correlation heatmap).
- If a `Date` column is present, the notebook will visualize unemployment trends over time.

> Tip: The notebook was originally written to run in Google Colab (path uses `/content`). If running locally, update the CSV path to the local filename.

## Extending the analysis

- Add trend decomposition or seasonal analysis on time series data.
- Build predictive models to forecast unemployment rate (ARIMA, Prophet, or supervised ML methods).
- Integrate additional socio-economic datasets for richer insights (education, GDP, sectoral employment).

## Result
![Input Form](https://github.com/Arshad-5068/AML-Task-2-/blob/main/result.png?raw=true)
