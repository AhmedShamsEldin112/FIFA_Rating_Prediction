⚽ FIFA Player Rating Prediction (2015–2021)
📌 Project Overview

This project focuses on predicting FIFA 21 player ratings based on historical player data from FIFA editions 2015–2020.
Using data preprocessing, feature engineering, visualization, and machine learning models (Random Forest), the project analyzes player performance and estimates their future ratings.

The workflow includes:

Data cleaning & transformation

Exploratory data analysis (EDA) with visualizations

Feature engineering (e.g., BMI, potential increase)

Machine Learning models for players and goalkeepers separately

Evaluation using R² Score and RMSE

📂 Dataset

The dataset was sourced from FIFA Player Data (2015–2021) provided on sofifa.com
 (open-source Kaggle datasets).

Files used:

players_15.csv → FIFA 15

players_16.csv → FIFA 16

players_17.csv → FIFA 17

players_18.csv → FIFA 18

players_19.csv → FIFA 19

players_20.csv → FIFA 20

players_21.csv → FIFA 21 (for evaluation)

Main features include:

overall, potential, age, height_cm, weight_kg, pace, shooting, passing, dribbling, defending, physic, gk_diving, gk_reflexes, etc.

⚙️ Data Preprocessing & Feature Engineering

Removed irrelevant/unnecessary columns (URLs, tags, unused positions).

Handled missing values by replacing with 0.

Created new features:

BMI = weight_kg / (height_cm/100)^2

Potential Increase = (potential - overall) / overall * 100

Averaged player stats across FIFA years.

Separated players vs. goalkeepers for more accurate modeling.

📊 Exploratory Data Analysis (EDA)

Some of the key insights & visualizations:

📈 Average overall rating trend (2015 → 2020).

⭐ Progression of Messi & Cristiano Ronaldo ratings.

📦 Distribution of overall ratings per FIFA version.

🏟️ Top 4 clubs (average overall rating trend).

⚖️ Distribution of BMI across positions.

🤖 Machine Learning Models

Algorithm used: Random Forest Regressor (n_estimators=200)

Data split: train_test_split (80% train, 20% test)

Features:

Players → [pace, shooting, passing, dribbling, defending, physic, age]

Goalkeepers → [gk_diving, gk_handling, gk_kicking, gk_reflexes, gk_speed, gk_positioning, age]

✅ Evaluation Metrics:

Players Model:

R² Score ≈ 0.713
RMSE ≈ 3.392

Goalkeepers Model:

R² Score ≈ 0.739
RMSE ≈ 3.439

Overall Model Performance (All Players):

R² Score = 0.9128
RMSE = 1.8780

📌 Results & Insights

The model successfully predicted FIFA 21 ratings using historical stats.

Non-GK and GK models performed differently due to distinct skill sets.

Visualizations show how players/clubs evolved over time.

Potential feature (potential increase) gives insights into underrated/overperforming players.

🚀 How to Run

Clone the repo:

git clone https://github.com/AhmedShamsEldin112/FIFA_Rating_Prediction.git
cd FIFA_Rating_Prediction


Install dependencies:

pip install -r requirements.txt


Run the notebook:

jupyter notebook FIFA_Rating_Prediction.ipynb

📌 Tech Stack

Python 3.9+

Libraries: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn

✨ Future Improvements

Add deep learning models (e.g., Neural Networks, LSTM).

Include transfer value / wages as prediction features.

Extend dataset to FIFA 22–23 for trend continuation.

Build an interactive dashboard (Streamlit/Plotly) for better insights.

👨‍💻 Author

AhmedShamsEldin112
🔗 GitHub Profile
