# Weather Temperature Prediction using Random Forest

This project implements a supervised machine learning regression model to predict global average temperatures. By leveraging a **RandomForestRegressor** and a structured Scikit-Learn pipeline, the model identifies non-linear climatic patterns with high precision.

## Project Overview
* **Dataset:** Kaggle Weather Data (3,192 samples, 9 features)
* **Problem Type:** Nonlinear Regression
* **Target Variable:** `LandAndOceanAverageTemperature`
* **Implementation:** Jupyter Notebook (`.ipynb`)

*The objective was to implement a complete end-to-end regression workflow, focusing on preprocessing, ensemble learning, and evaluation fundamentals.*

---

## Machine Learning Workflow
The project utilizes a Scikit-Learn **Pipeline** to ensure consistent preprocessing and prevent data leakage:

1.  **Data Cleaning:** Handled missing values and removed uncertainty columns.
2.  **Feature Engineering:** Extracted `month` and `year` from datetime objects to capture seasonality.
3.  **Feature Selection (`SelectKBest`):** Identified the most impactful predictors.
4.  **Scaling (`StandardScaler`):** Normalized features for stable model training.
5.  **Modeling:** Used `RandomForestRegressor` for its ability to handle complex, non-linear relationships.



---

## Performance Evaluation
The model was evaluated using a **75/25 Train-Test split**. The high $R^2$ scores and low error metrics indicate excellent generalization to unseen data.

### Key Metrics
| Metric | Training Set | Test Set |
| :--- | :--- | :--- |
| **MAE** | 0.00462 | 0.02949 |
| **MSE** | 0.00462 | 0.02949 |
| **RMSE** | 0.06796 | 0.17174 |
| **$R^2$ Score** | 0.99718 | 0.98137 |

### Visual Insights
* **Actual vs. Predicted:** Data points cluster tightly around the "Perfect Prediction" line, indicating a strong fit.
* **Residual Analysis:** Residuals are small and randomly scattered around zero, confirming the absence of systematic bias or heteroscedasticity.
* **Feature Importance:** The Random Forest model allowed for the interpretation of which weather variables (Min vs. Max temperatures) contributed most to the prediction.



---

## Tools and Libraries
* **Python:** Core programming language.
* **Pandas & NumPy:** Data manipulation and numerical analysis.
* **Matplotlib & Seaborn:** Data visualization (Heatmaps, Pair plots, Residual plots).
* **Scikit-Learn:** Machine learning pipeline, scaling, and regression.

---

## Repository Structure
```text
weather-prediction-ml/
├── model.ipynb         # Full Jupyter Notebook implementation
├── weather_data.csv    # Dataset used for training
├── requirements.txt    # List of dependencies
└── README.md           # Project documentation
