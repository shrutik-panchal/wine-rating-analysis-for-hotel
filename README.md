# Wine Sourcing Analysis for a Luxury Hotel

## Overview
This project analyzes a large collection of global wine reviews to help a five‑star hotel design a wine list that balances **guest satisfaction** (ratings) and **cost efficiency** (price).
Using Python for exploratory data analysis and a star‑schema model for Power BI, the project delivers data‑driven sourcing recommendations across countries and wine varieties.

## Business Problem
A luxury hotel wants to refresh its wine menu using data rather than intuition.
The objective is to identify wines and sourcing countries that provide high quality (ratings) at reasonable prices, so the hotel can delight guests while keeping procurement costs under control.

#### This analysis answers:
- How are wine **ratings and prices** distributed globally?
- Which **varieties** receive the most attention (number of reviews)?
- Which varieties offer **high ratings at budget‑friendly prices** (e.g., rating ≥ 90, price < 20)?
- For each country, what is the **typical variety, average rating, and average price**?
- Which countries provide the **best value for money** and should be prioritized for sourcing?

## Tech Stack
- **Language:** Python
- **Environment:** Jupyter Notebook, VS Code
- **Libraries:** pandas, NumPy, Matplotlib / Seaborn
- **Data Modeling:** Dimensional modeling, star schema (fact + dimension tables)
- **BI & Visualization:** Power BI (importing star schema, building interactive dashboards)
- **Version Control:** Git & GitHub

## Project Structure
```
wine-rating-analysis/
│
├─ notebooks/
│ └─ wine_rating_sourcing_analysis.ipynb # main EDA + analysis + star-schema export
│
├─ data/
│ ├─ raw/
│ │ └─ wine.json # original wine review data
│ └─ model/
│ ├─ FactWine.csv # fact table for Power BI
│ ├─ DimCountry.csv # country dimension
│ ├─ DimVariety.csv # variety dimension
│ └─ DimWinery.csv # winery dimension
│
├─ powerbi/
│ └─ wine_sourcing_star_schema.pbix # Power BI report based on the star schema
│
└─ README.md
```

This layout highlights both the Python analysis and the BI deliverable in a clean, discoverable way.

## Dataset
The dataset contains expert reviews of wines from multiple countries, with attributes such as:
- `country` – producing country  
- `province` / `region` – geographic region (when available)  
- `variety` – grape/wine variety  
- `winery` – producer  
- `points` – expert rating score  
- `price` – listed price (numeric)  
- `description` – free‑text tasting notes (not fully used yet, but available for NLP extensions)

The notebook includes data cleaning steps:
- Converting `price` and `points` to numeric types.
- Handling missing values and dropping invalid rows for price/points.
- Basic quality checks and descriptive statistics.
