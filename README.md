# Seasonal Agriculture Performance Analysis

VOIS AICTE Major Project: This project analyzes a farm-level agricultural dataset to understand how crop yield, profitability, and resource use change across India's three cropping seasons — Kharif, Rabi, and Zaid.

## Problem Statement

Agricultural performance is known to vary across seasons, but raw farm data doesn't make it obvious how much it varies, or why. This project analyzes 4,000 farm records to find real, statistically-checked seasonal patterns rather than just describing the dataset.

## Dataset

`SA_data_raw.csv` — 4,000 rows, 28 columns, covering:
- 8 crops (Rice, Wheat, Maize, Cotton, Sugarcane, Pulses, Groundnut, Chilli)
- 3 seasons (Kharif, Rabi, Zaid)
- 4 irrigation methods (Rainfed, Drip, Sprinkler, Flood)
- Environmental readings (rainfall, temperature, humidity, soil moisture)
- Farm economics (cost, revenue, profit, yield)

## Key Findings

- Kharif outperforms Rabi and Zaid on both yield and profit, for every single one of the 8 crops (confirmed with Kruskal-Wallis tests, p < 0.05 in all cases).
- Loss-making farms rise from 42% in Kharif to 51% in Rabi to 64% in Zaid.
- Zaid is the weakest season on every measure — highest cost, highest water use, lowest yield, and the only season with a negative median profit.
- No single weather variable (rainfall, temperature, soil moisture) strongly predicts yield at the individual farm level — season behaves as a combined effect rather than one driver.
- Flood irrigation is the least water-efficient method in every season; Drip is the best-performing active irrigation method.

Full methodology, statistical tests, and charts are in the notebook.

## Repository Contents

```
├── Seasonal_Agriculture_Performance_Analysis.ipynb   # full analysis, executed
├── seasonal_agriculture_raw.csv                      # raw dataset
├── charts/                                           # exported chart images
└── README.md
```

## Tools Used

Python, Pandas, NumPy, SciPy, Matplotlib, Seaborn, Jupyter Notebook
