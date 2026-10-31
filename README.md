# Fuel Inventory Variance Analysis

Simulated 90-day fuel depot dataset (3 tanks: Diesel, Gasoline, Kerosene) used to practice detecting stock loss/gain, similar to oil control monitoring work.

## Tools
Excel logic (expected vs. actual closing), SQL (SQLite), Python (pandas, matplotlib), Google Colab

## Method
1. Generated sample daily tank data (opening, received, issued, closing).
2. Computed variance = actual closing - expected closing.
3. Flagged days with variance beyond ±200 liters as CHECK.
4. Summarized variance per tank and per month with SQL.
5. Charted daily variance to spot outliers.
6. Fixed the first version of the data, which had negative stock, by adding deliveries when stock fell low.

## Findings
- 11 of 270 tank-days were flagged CHECK (T1: 6, T2: 5, T3: 0).
- T1 Diesel had the largest total loss (-3,491 L), followed by T2 Gasoline (-2,393 L) and T3 Kerosene (-738 L).
- Largest single-day losses were on 2026-07-07 (T1) and 2026-08-31 (T1).
- Recommendation: inspect T1 first.

## Note
All data is simulated. No real company records were used.

