# Formula 1 Lap Time Predictor

Classical Machine Learning / Regression project for predicting Formula 1 lap times.

## Race
**2019 British Grand Prix**

Eight drivers who completed at least 90% of the winner's race distance are selected.

## Dataset
Formula 1 World Championship (1950–2020) dataset by Rohan Rao on Kaggle:

https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020

Required files:
- `lap_times.csv`
- `pit_stops.csv`
- `results.csv`
- `races.csv`

Download the dataset and put these files inside the `data/` folder.

## Methodology
- Remove pit-stop laps.
- Remove the lap immediately after each pit stop.
- Remove laps slower than 1.5 × the driver's median lap time.
- Engineer `tire_age`.
- Use earlier stints for training and each driver's final stint for testing.
- Avoid a random split to reduce leakage.
- Compare Linear Regression and Random Forest Regression.
- Evaluate using RMSE and MAE.
- Plot predicted vs actual lap times for one complete final stint.

## Features

**Baseline:** `grid`, `lap`

**Enhanced:** `grid`, `lap`, `tire_age`

## Technologies
Python, Pandas, NumPy, Matplotlib, Scikit-learn, Jupyter Notebook.

## Run the project

```bash
pip install -r requirements.txt
jupyter notebook
```

Open `F1_Lap_Time_Predictor.ipynb` and run the cells from top to bottom.

## Project structure

```text
F1-Lap-Time-Predictor/
├── F1_Lap_Time_Predictor.ipynb
├── README.md
├── requirements.txt
├── data/
│   ├── lap_times.csv
│   ├── pit_stops.csv
│   ├── results.csv
│   └── races.csv
└── images/
    └── predicted_vs_actual.png
```
