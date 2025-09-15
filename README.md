# EV-StockShare-IT-EU-Analysis

This project analyzes the share of electric vehicles (EV stock share, % of total vehicles) in **Italy** compared to **Europe** between 2015 and 2023, using data from the **IEA Global EV Dataset** (via Kaggle).

## Goal
- Compare Italy and Europe in terms of EV adoption (% of vehicles).
- Explore historical trends (2015–2023).
- Quantify differences in growth (absolute, relative, CAGR).
- Produce a simple, clear example of exploratory data analysis (EDA) in Python.

---

## Repo structure
ev-stock-share-italy-europe/
├─ notebooks/
│ └─ ev-stockshare-it-eu-analysis.ipynb # step-by-step notebook
├─ figures/
│ └─ ev-stock-share_italy-vs-europe_2015-2023.png # final line chart
├─ results/
│ ├─ wide-historical_2015-2023.csv # processed data (wide format)
│ └─ summary-ev-stock-share_2015-2023.csv # summary table with growth metrics
└─ README.md

---

## Method
1. **Filter dataset**: select parameter `EV stock share`, regions = `Italy`, `Europe`, years ≥ 2015.
2. **Clean duplicates**: aggregate multiple entries per (region, year) by mean (since the variable is a percentage).
3. **Transform data**: pivot to wide format (rows = year, cols = region).
4. **Visualize**: plot a line chart comparing Italy vs Europe.
5. **Quantify**: calculate summary metrics (initial, final, absolute change, relative change, CAGR).

---

## Results

### Line chart
![EV stock share](<img width="2060" height="1407" alt="ev-stock-share_italy-vs-europe_2015-2023" src="https://github.com/user-attachments/assets/663367d0-d718-4325-9cd8-a571feb03543" />
)

- In **2015**: Italy ~0.03%, Europe ~0.14%.  
- In **2023**: Italy ~0.98%, Europe ~1.68%.  
- Italy grew almost **28x**, Europe ~11x.  

### Summary table
| Region | 2015 | 2023 | Δ abs. | Δ % | CAGR % |
|--------|------|------|--------|-----|--------|
| Italy  | 0.03 | 0.98 | 0.95   | 2792% | 52.3% |
| Europe | 0.14 | 1.68 | 1.54   | 1064% | 35.9% |

---

## Key findings
- **Italy** is growing faster (higher CAGR), but from a much smaller base.  
- **Europe** maintains higher absolute values: by 2023 it has nearly double Italy’s share (1.68% vs 0.98%).  
- Italy shows a strong catch-up dynamic, yet it still lags behind the EU average.

---

## Data source
- [IEA Global EV Data (Kaggle)](https://www.kaggle.com/datasets/patricklford/global-ev-sales-2010-2024)  
*(dataset not redistributed here; only processed outputs are included in this repo).*

---

## Next steps
- Add **EV sales** (flows) alongside EV stock (stock).
- Extend analysis to **other EU countries** (Germany, France, Spain).
- Integrate **projections to 2030/2035**, clearly distinguishing historical vs forecast data.
- Build interactive visualizations (Plotly/Seaborn).

---

## License
MIT License — free to use, share, and modify with attribution.

---
Author: Mattia Dalla Fontana  
MSc Student in Management & Sustainability, Ca’ Foscari University of Venice
