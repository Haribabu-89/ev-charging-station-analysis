# EV Charging Station & Grid Optimization Analysis

Exploratory data analysis of 8,354 electric-vehicle charging sessions across 20 stations
(Jan–Mar 2025, 27 columns) using Python.

## Tools
Python · Pandas · NumPy · Matplotlib · Seaborn · SciPy · Jupyter Notebook

## What this project does
- **Cleaning:** missing-value checks, duplicate removal, datetime conversion for 4 time columns, removal of a non-analytical ID column.
- **Feature engineering:** `charging_efficiency` (kWh/min), `charging_cost`, `battery_gain`, and a `peak_hour` flag.
- **Analysis:** station rankings by efficiency and optimization reward, revenue by day of week, demand by weather and time slot, duration by vehicle type.
- **Statistics:** min-max normalisation, covariance between charging power and optimization reward, Z-score outlier detection on charging duration.
- **Visualisation:** 7 charts — bar, pie, histogram, scatter, box plot, line, and correlation heatmap.

## Key findings
- Differences between groups are small. Average charging demand varies by about 1% across weather conditions, and average charging duration varies by about 1% across vehicle types — inside normal variation, not real effects.
- Most numeric variables are weakly correlated. The strongest relationship (energy consumed vs charging cost) exists by construction.
- Optimization reward is negative at every station with a narrow spread, so rankings on that metric are not meaningful.

## Limitations
The dataset appears to be synthetic. Variables that would be strongly linked in real
operations show almost no relationship, so this project is best read as a demonstration
of EDA method rather than a source of operational conclusions. A production version would
need observed station data and significance testing before any group difference is acted on.

## How to run
```bash
pip install pandas numpy matplotlib seaborn scipy jupyter
```
1. Place `charging_ev_and_grid_optimization_dataset.csv` in a `data/` folder next to the notebook.
2. Open `Electric_Vehicle_Charging_Station.ipynb` and run all cells.

## Repository structure
```
├── Electric_Vehicle_Charging_Station.ipynb
├── data/
│   └── charging_ev_and_grid_optimization_dataset.csv
└── README.md
```
