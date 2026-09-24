# City Bike Trip Analysis

This project analyzes NYC Citi Bike trips together with station and weather data.

## Project Goals

- Clean and combine Citi Bike trip files.
- Add station information and hourly weather data.
- Explore trip duration, distance, time, rider type, and weather effects.
- Build a linear regression model to predict trip duration.

## Project Structure

```text
data/
	raw/          Original Citi Bike trip files
	external/     Station and weather data
	processed/    Cleaned and merged CSV files
notebooks/
	01_data_collection.ipynb
	02_data_cleaning.ipynb
	03_eda.ipynb
	04_linear_regression.ipynb
src/            Reusable Python scripts
reports/        Analysis reports
```

## Workflow

1. Load the raw trip, station, and weather data.
2. Convert timestamps and calculate trip duration and distance.
3. Remove duplicate trips and handle missing values.
4. Merge station and weather information with trip records.
5. Create time features such as hour, day of week, and weekend status.
6. Perform exploratory data analysis.
7. Train and evaluate a linear regression model.

## Main Outputs

Processed data is saved in `data/processed/`, including:

- `citibike_cleaned.csv`
- `citibike_trips_with_stations.csv`
- `citibike_all_data.csv`
- `citibike_final_cleaned.csv`

## Model Evaluation

The regression model is evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R-squared (R2)

The latest model uses all usable trip, station, time, and weather features. Its latest test results are approximately:

- MAE: 5.36 minutes
- RMSE: 17.52 minutes
- R2: 0.21

## Requirements

Install the main Python packages with:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

Open the notebooks in order, starting with `01_data_collection.ipynb` and ending with `04_linear_regression.ipynb`.
