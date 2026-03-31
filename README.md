# Toronto Rental Affordability Index

## Overview
This project analyzes rental affordability across Toronto neighbourhoods by combining 
rental listing data with Statistics Canada median income figures. Each neighbourhood 
is assigned an affordability ratio (monthly rent / monthly income) and benchmarked 
against the standard 30% affordability threshold.

## Key Findings
- **93.6% of Toronto neighbourhoods are unaffordable** for a median-income household
- The average renter spends **38% of gross income** on rent — 8 points above the threshold
- **Most expensive:** Trinity-Bellwoods ($4,177/mo avg | ratio: 0.60)
- **Most affordable:** Greenwood-Coxwell ($1,440/mo avg | ratio: 0.21)
- Only **7 of 109 neighbourhoods** meet the 30% affordability standard

## Methodology
- Affordability ratio = average monthly rent / median monthly income
- Median household income: $84,000/yr (~$7,000/mo) — Statistics Canada 2021 Census
- Affordability threshold: 30% of gross monthly income (industry standard)
- Neighbourhoods with fewer than 3 listings excluded (insufficient sample size)

## Data Sources
- Rental listings: RentFaster.ca dataset via Kaggle (25,000+ Canadian listings, June 2024)
- Neighbourhood boundaries: City of Toronto Open Data Portal (GeoJSON)
- Income data: Statistics Canada 2021 Census (median household income)

## Limitations
- 49 of 158 Toronto neighbourhoods had insufficient listing data (<3 listings)
- Dataset represents a single point in time (June 2024) — no longitudinal comparison
- Income figure is a single citywide median — neighbourhood-level income variation not captured

## Tech Stack
Python, pandas, GeoPandas, Folium, matplotlib, seaborn, Shapely, Jupyter

## Visuals
- `visuals/affordability_map.png` — static choropleth map
- `visuals/affordability_map.html` — interactive map with hover tooltips
- `visuals/affordability_barchart.png` — top 15 most/least affordable neighbourhoods
