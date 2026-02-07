# **Weather Prediction using Random Forest Regression**
## Project Overview
This project implements a supervised machine learning regression model for weather prediction using a Kaggle dataset.
- **Dataset size:** 3,192 samples
- **Number of features:** 9
- **Problem type:** Nonlinear regression
- Implementation format: Jupyter Notebook <br>
<br>

*The objective was to implement a complete end-to-end regression workflow and understand preprocessing, ensemble learning, and evaluation fundamentals.*

## Machine Learning Workflow
The modelling process includes:
- Data preprocessing using Pandas and NumPy
- Feature selection using SelectKBest
- Feature scaling using StandardScaler
- Model training using RandomForestRegressor
- Performance evaluation using Mean Absolute Error (MAE)
- Train–Test-Split analysis to study generalisation behaviour
### Pipeline structure:
SelectKBest → StandardScaler → RandomForestRegressor <br>
The use of scikit-learn’s Pipeline ensures consistent preprocessing and avoids data leakage.
## Model Evaluation
The model was evaluated using:
- 70–30 Train–Test-Split
- Mean Absolute Error (MAE)
### Example results:

- Train MAE: 0.004618812976506039
- Test MAE:  0.029493678800803644

The comparison between training and testing MAE was used to inspect potential overfitting and understand bias–variance behaviour.
## Feature Importance
Random Forest provides feature importance scores, enabling interpretability of model behaviour.
The analysis helps identify which weather variables contribute most significantly to prediction performance.
## Tools and Libraries
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn
Repository Structure
Copy code

weather-prediction-ml/
<br>
├── model.ipynb <br>
├── weather.csv <br>
└── README.md <br>

## Learning Outcomes
Through this project, I strengthened understanding of:
- End-to-end ML workflow implementation
- Regression modelling
- Ensemble learning principles
- Train–test evaluation methodology
- Bias–variance trade-off
- Feature importance interpretation
