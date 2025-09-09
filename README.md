🚍 Transport Demand Prediction Using Regression Models
📌 Project Overview

This project predicts seat demand for Mobiticket rides using machine learning.
The goal is to forecast the number of seats sold for each ride (based on route, date, and time) so that fleet allocation and pricing can be optimized.

🎯 Problem Statement

Passenger demand varies across routes and times, making it difficult for Mobiticket to plan resources effectively.
Accurate prediction of seats sold per ride helps reduce empty seats, avoid overbooking, and improve customer satisfaction.

🗂️ Dataset

Records: 51,645 bookings

Features:

ride_id, seat_number, payment_method, travel_date, travel_time, travel_from, travel_to, car_type, max_capacity

Target Variable: seats_sold (aggregated per ride)

⚙️ Steps Followed

Data Cleaning & Aggregation

Grouped bookings per ride → computed seats_sold

Extracted features: day of week, month, travel hour

Encoded categorical variables

Exploratory Data Analysis (EDA)

Distribution of seats sold

Seats sold vs max capacity

Effect of day of week and routes on demand

Model Building

Random Forest Regressor

XGBoost Regressor

Evaluation Metrics

RMSE (Root Mean Squared Error)

MAE (Mean Absolute Error)

R² (Coefficient of Determination)

📊 Results
Model	RMSE	MAE	R²
Random Forest	~5.1	~3.4	0.89
XGBoost	~5.0	~3.4	0.90

✅ Both models performed well, with XGBoost slightly outperforming Random Forest.

🔑 Key Insights

Day of week and route are the strongest predictors of demand.

Max capacity and travel hour also influence seat sales.

Models can capture around 90% of demand variation.

🚀 Future Scope

Add holiday, event, and weather data to improve predictions.

Use time-series models (ARIMA, LSTM) for seasonality.

Deploy the model as a real-time prediction API for Mobiticket.

📂 Repository Structure
├── data/                   # Dataset (train_revised.csv)
├── notebooks/              # Jupyter notebooks with EDA & modeling
├── src/                    # Python scripts for preprocessing & models
├── reports/                # Final report & presentation
├── requirements.txt        # Dependencies
└── README.md               # Project description

🛠️ Technologies Used

Python (Pandas, NumPy, Matplotlib, Seaborn)

Scikit-learn (Random Forest, preprocessing, evaluation)

XGBoost (gradient boosting model)

Jupyter Notebook

👤 Author

Manoj Choudhary
Supervised by: Meghana Gowda
