# Air Quality Index (AQI) Prediction

## 📌 Project Overview
This project focuses on predicting Air Quality Index (AQI) using machine learning regression models. The analysis includes data cleaning, exploratory data analysis (EDA), feature engineering, correlation analysis, and model training.

---

## 📊 Dataset
The dataset contains hourly air quality measurements including:
- NOx
- NO2
- CO
- Benzene (C6H6)
- Sensor readings
- Temperature & Humidity

---

## 🔎 Exploratory Data Analysis
- Correlation heatmap
- Seasonal variation analysis
- Distribution analysis
- Feature relationships

---

## 🤖 Machine Learning Models Used
- Linear Regression
- Random Forest Regressor
- (Add others if used)

---

## 📈 Evaluation Metrics
- RMSE
- R² Score
- MAE

---

## 🛠 Tech Stack
- Python
- Pandas
- NumPy
- Scikit-learn
- Seaborn
- Matplotlib

---

## 🎯 Future Improvements
- Hyperparameter tuning
- Feature selection optimization
- Deploy model using Flask / FastAPI
- 
## ⚙️ Pipeline Steps
1. Data cleaning
2. Missing value handling
3. Feature engineering
4. Train-test split
5. Model training
6. Evaluation


- CONCLUSION

In this project, we developed a machine learning–based approach to predict the Air Quality Index (AQI) using the Italian Air Quality UCI dataset. Starting from raw sensor measurements of pollutants and weather variables, we performed extensive preprocessing, handled missing values, and computed AQI and its health categories using EPA breakpoints. To simulate real-world challenges, we injected artificial noise and outliers into nitrogen dioxide (NO₂) data and applied cleaning methods such as IQR-based detection and rolling average smoothing. This step demonstrated how noisy sensor data can be effectively handled to preserve trends while removing anomalies.

Our exploratory data analysis revealed clear temporal patterns: AQI tended to be worse during winter months and peak traffic hours, while nitrogen dioxide (NO₂) consistently showed the strongest correlation with AQI, supported by carbon monoxide (CO) and ozone (O₃) proxy sensors. These findings aligned with known urban pollution sources, particularly traffic and seasonal heating.

We implemented both regression models (to predict numeric AQI values) and classification models (to predict AQI categories such as Good, Moderate, or Unhealthy). Baseline models (Linear and Logistic Regression) provided reasonable results, but advanced ensemble models performed significantly better. Random Forest achieved the best overall performance, with an almost perfect R² (0.999) for regression and ~99.6% accuracy for classification. XGBoost also performed strongly, though slightly behind Random Forest. These results demonstrate that non-linear ensemble methods are most effective for capturing complex pollutant–AQI relationships.

To complement supervised learning, we applied K-Means clustering as an unsupervised method. This analysis grouped the data into three natural clusters corresponding to cleaner air, moderate pollution, and polluted hours. These clusters closely matched the AQI categories, confirming that the dataset’s structure aligns with health-based thresholds even without labeled targets.

The prediction demo further showed how our trained models can generate reliable AQI predictions for unseen test data and for simulated new inputs. Such a system could be deployed as part of a real-time air monitoring and alert system, enabling citizens to make informed health decisions and policymakers to design better interventions.


