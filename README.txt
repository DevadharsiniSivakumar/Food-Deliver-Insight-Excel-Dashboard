# Food Delivery Insight
### Understand Delivery Time • Find Bottlenecks • Improve Service

## Project Overview

Food Delivery Insight is a data analysis and machine learning project designed to identify the factors contributing to longer food delivery times and poor delivery performance.

The project analyzes order details, rider experience, delivery routes, traffic conditions, weather, and restaurant pickup times. It uses Python for data preprocessing, exploratory data analysis (EDA), and machine learning, along with WPS Spreadsheet for data visualization and dashboard preparation.

> **Note:** This project uses a synthetic dataset created for the QuickBite Delivery Services use case. The findings are for educational and demonstration purposes and do not represent actual company performance.

## Objectives

- Identify zones with longer delivery times.
- Analyze the impact of traffic and weather on delivery performance.
- Identify restaurants with longer pickup durations.
- Understand the relationship between delivery distance and time.
- Identify peak periods based on order volume.
- Build a machine learning model to predict total delivery time.
- Present insights through charts, PivotTables, and a summary dashboard.

## Dataset Description

The project uses five CSV files:

| File | Description |
|---|---|
| `orders.csv` | Order time, restaurant, customer zone, and order value |
| `riders.csv` | Rider details, experience, and shift |
| `routes.csv` | Route distance, traffic level, and zone |
| `weather.csv` | Rainfall, temperature, and visibility |
| `delivery.csv` | Pickup time, delivery time, and delivery status |

The datasets are linked using common identifiers such as `order_id`, `rider_id`, and `weather_id`.

## Technologies Used

- **Python** – Data analysis and preprocessing
- **Pandas and NumPy** – Data cleaning and feature engineering
- **Matplotlib and Seaborn** – Data visualization
- **Scikit-learn** – Machine learning and model evaluation
- **Jupyter Notebook / Google Colab** – Development environment
- **WPS Spreadsheet** – PivotTables, charts, and dashboard creation

## Project Workflow

1. **Data Loading:** Load the five CSV files into Python.
2. **Data Cleaning:** Handle duplicate records, missing values, inconsistent zone names, and invalid durations.
3. **Data Integration:** Combine the datasets using common identifiers.
4. **Feature Engineering:** Create features such as pickup duration, total delivery time, order hour, and time period.
5. **Exploratory Data Analysis:** Analyze delivery time by zone, traffic, weather, restaurant, distance, and time period.
6. **Machine Learning:** Use Random Forest Regression to predict total delivery time.
7. **Model Evaluation:** Evaluate predictions using MAE, RMSE, and R² score.
8. **Visualization:** Create charts, PivotTables, and a summary dashboard in WPS Spreadsheet.

## Machine Learning Model

**Algorithm:** Random Forest Regression

**Target variable:** `total_delivery_min`

**Input features:** Delivery distance, order value, rider experience, rainfall, temperature, visibility, order hour, traffic level, weather condition, customer zone, and time period.

Random Forest Regression was selected because it can learn complex relationships between multiple input features and a continuous numerical target such as delivery time.

Model performance is evaluated using:

- **MAE:** Mean Absolute Error
- **RMSE:** Root Mean Squared Error
- **R² Score:** Coefficient of Determination

Actual performance values should be reported after running the notebook.

## Visualizations

The project includes the following analyses:

- Average delivery time by customer zone
- Delivery time by traffic level
- Delivery time by weather condition
- Average pickup time by restaurant
- Delivery time versus distance
- Order count by time period
- Summary dashboard with key performance indicators

## Expected Insights

The analysis aims to identify patterns associated with delivery delays, such as high traffic, adverse weather, restaurant pickup bottlenecks, and peak order periods.

These findings can help inform operational recommendations, including better rider allocation, route optimization, and improved preparation for adverse weather.

## How to Run

1. Clone or download this repository.
2. Open the Jupyter Notebook in Google Colab or a local Jupyter environment.
3. Upload the five CSV files to your working folder or Google Drive.
4. Update the dataset path in the notebook.
5. Run the notebook cells in order.
6. Review the EDA charts and machine learning evaluation metrics.
7. Open the cleaned dataset in WPS Spreadsheet to create PivotTables and charts.

Install the required Python packages if needed:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

## Suggested Repository Structure

```text
Food-Delivery-Insight/
├── data/
│   ├── orders.csv
│   ├── riders.csv
│   ├── routes.csv
│   ├── weather.csv
│   ├── delivery.csv
│   └── cleaned_food_delivery.csv
├── notebooks/
│   └── Food_Delivery_Insight_Round2_Simple.ipynb
├── dashboard/
│   └── food_delivery_dashboard.xlsx
└── README.md
```

*Adjust the folder names and filenames to match the files you actually upload.*

## Future Enhancements

- Use real-world food delivery data for validation.
- Compare Random Forest with Linear Regression and other regression models.
- Improve outlier detection and data quality checks.
- Develop an interactive dashboard.
- Integrate real-time traffic and weather information for more practical delivery-time predictions.

## Conclusion

Food Delivery Insight demonstrates how data preprocessing, exploratory analysis, visualization, and machine learning can be combined to study food delivery performance. The project provides a foundation for identifying potential bottlenecks and supporting data-driven operational decisions.

## Disclaimer

This project is intended for academic and educational purposes. The dataset is synthetic, and the findings and model performance should not be interpreted as real-world business results.
